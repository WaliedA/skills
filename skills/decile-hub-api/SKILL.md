---
name: decile_hub_api
description: Interact with Decile Hub's venture capital management platform API. Use when the user needs to create, update, or query People, Organizations, Pipeline Prospects, Pacts, Events, Files, or other Decile Hub resources via the REST API or MCP server.
---

# Decile Hub API Skill

Decile Hub is the premier CRM for venture capital fund management, including fundraising. Interact with it's API via curl.

## Authentication

All API requests require an API token in the `Authorization` header:

```
Authorization: vXTpbBDRadPyXGshGhdUmMhf
```

## Base URL

```
https://intuitiovc.decilehub.com/api/v1
```

## Endpoints (v1 summary)

- **Organizations** — `GET, POST /api/v1/organizations`; `GET /api/v1/organizations/{id}`; `POST /api/v1/organization`
- **People** — `GET, POST /api/v1/people`; `GET /api/v1/people/{id}`; `POST /api/v1/person`
- **Pipeline** — `GET, POST /api/v1/pipeline_prospects`; `POST /api/v1/pipeline_prospect`; `GET /api/v1/pipelines`; `GET /api/v1/pipelines/{id}`
- **Pacts** — `GET /api/v1/pacts`; `POST /api/v1/pacts/send_pact`
- **Files** — `GET, POST /api/v1/files`; `GET, PUT, DELETE /api/v1/files/{id}`; `GET /api/v1/files/{id}/download`
- **Folders** — `GET, POST /api/v1/folders`; `GET /api/v1/folders/{id}`
- **Accounts** — `GET /api/v1/accounts`
- **Events** — `GET, POST /api/v1/events`; `GET, PUT, DELETE /api/v1/events/{id}`; `GET, POST /api/v1/events/{id}/guests`; `PATCH /api/v1/events/{id}/rsvp`

## Key Endpoints

### People Directory

**List People:** `GET /api/v1/people`

- Query params: `first_name`, `last_name`, `email`, `page`, `order_by`

**Create/Update Person:** `POST /api/v1/person`
If it sounds like this is a fundraising prospect or potential investor, instead create a pipeline prospect in the fundraising pipeline.

- Creates or updates a single person
- Returns `changes` object showing field differences on update

**Request Body:**

```json
{
  "person": {
    "first_name": "string (required)",
    "last_name": "string (required)",
    "email": "string (required)",
    "phone": "string",
    "linkedin": "string",
    "tag_list": "comma,separated,tags",
    "custom_data_points": { "field": "value" },
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "zipcode": "string",
      "country": "string"
    },
    "organizations": [{ "name": "Org Name", "title": "Job Title" }]
  }
}
```

### Pipeline Prospects

**List Prospects:** `GET /api/v1/pipeline_prospects?pipeline_id=ID`

**Create/Update Prospect:** `POST /api/v1/pipeline_prospect`
If not specified, assume it is the investors or fundraising pipeline. To see all available pipelines, `GET /api/v1/pipelines` and use the pipeline_id from that. Use that API route to search available pipelines and choose amongst that. As a last resort ask the user for the pipeline ID.

**Request Body (Person Prospect):**

```json
{
  "pipeline_id": "string (required)",
  "stage_id": "string (optional)",
  "prospect": {
    "probability": 25,
    "rating": 4,
    "tag_list": "comma,separated",
    "person": {
      "first_name": "string (required)",
      "last_name": "string (required)",
      "email": "string (required)"
    }
  }
}
```

**Request Body (Organization Prospect):**

```json
{
  "pipeline_id": "string (required)",
  "stage_id": "string (optional)",
  "prospect": {
    "probability": 25,
    "organization": {
      "name": "string (required)",
      "company_url": "string",
      "short_description": "string"
    }
  }
}
```

### PACTs (LP fundraising agreements)

**List PACTs:** `GET /api/v1/pacts`

- Returns signed PACTs across **investor pipelines** for the account.

**Send PACT (move to stage + email):** `POST /api/v1/pacts/send_pact`

- Body: `person_id` (numeric id), `pipeline_id` (optional; same opaque id as `GET /api/v1/pipelines`). If omitted and the account has **exactly one** investor pipeline, that pipeline is used; if there are zero or more than one, the request fails unless `pipeline_id` is provided.
- Pipeline must be an **investor** pipeline. The API sends the PACT agreement via email.
- To resolve `person_id` and (when needed) `pipeline_id`, use `GET /api/v1/people` and `GET /api/v1/pipelines`.

## Common Workflows

### Adding a Person to the Directory

1. Use `POST /api/v1/person` with person details
2. Check response for `status: "success"` and `person_id`
3. Review `changes` object to confirm what was created/updated

### Adding a Prospect to a Pipeline

1. First, get the pipeline ID (user should provide or list via `GET /api/v1/pipelines`)
2. Use `POST /api/v1/pipeline_prospect` with pipeline_id
3. Include either `person` or `organization` object
4. Optionally specify `stage_id` to place in specific stage

### Searching for a person

1. Get the first name, last name, or email of a person
2. Use `GET /api/v1/people` with parameters `first_name`, `last_name` or `email` to filter

### Bulk Operations

For bulk operations, use the batch endpoints:

- **Bulk People:** `POST /api/v1/people` (array of people)
- **Bulk Prospects:** `POST /api/v1/pipeline_prospects` (array of prospects)

## MCP Server

Decile Hub provides an MCP server for AI assistants:

**Endpoint:** `https://decilehubmcp.com/mcp`
**Header:** `X-Decile-API-Key: vXTpbBDRadPyXGshGhdUmMhf`

## Error Handling

Common HTTP status codes:

- `200` - Success
- `201` - Created
- `400` - Bad Request (check request body)
- `401` - Unauthorized (check API token)
- `404` - Not Found
- `422` - Unprocessable Entity (validation errors)

## Reference

See https://decilehub.com/docs/api for openAPI full docs.
