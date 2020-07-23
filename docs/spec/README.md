# Entities

This document describes the entities and their attributes.

See [Definition list](../../README.md#definition_list) for detailed descriptions
on of the entities.

For reference, we list the entity names here as well:

| Entity       |
|--------------|
| `conference` |
| `event`      |
| `location`   |
| `organizer`  |
| `speaker`    |
| `sponsor`    |
| `tag`        |
| `theme`      |

## Attributes

https://jsonapi.org/format/#document-resource-object-attributes

### Shared attributes

Apart from `tag` and `theme`, all entities have the following attributes

| Attribute        | Type    | Description                    |
|------------------|---------|--------------------------------|
| `title`          | string  | The title                      |
| `promote`        | boolean |                                |
| `image`          | object  |                                |
| `image.url`      | string  | Image url                      |
| `image.meta.alt` | string  | Alternative text for the image |
| `description`    | string  | Full description of the entity |
| `summary`        | string  | Summary of the description     |

`tag` and `theme` have only the `title` attribute.

### `conference` attributes

| Attribute     | Type                       | Description                         |
|---------------|----------------------------|-------------------------------------|
| `start_time`  | datetime (ISO 8601 string) | The start time                      |
| `end_time`    | datetime (ISO 8601 string) | The end time                        |
| `ticket`      | object                     |                                     |
| `ticket.url`  | string                     | Url to ticket system                |
| `ticket.text` | string (nullable)          | Text to show on “Buy ticket” button |

### `event` attributes

| Attribute     | Type                       | Description                         |
|---------------|----------------------------|-------------------------------------|
| `start_time`  | datetime (ISO 8601 string) | The start time                      |
| `end_time`    | datetime (ISO 8601 string) | The end time                        |
| `ticket`      | object                     |                                     |
| `ticket.url`  | string                     | Url to ticket system                |
| `ticket.text` | string (nullable)          | Text to show on “Buy ticket” button |

## Relationships

https://jsonapi.org/format/#document-resource-object-relationships

### Shared relationships

Apart from `conference`, all entities have the following relationships

| Relationship | Description                        |
|--------------|------------------------------------|
| `conference` | A relationship with the conference |

### `conference` relationships

| Relationship | Description                              |
|--------------|------------------------------------------|
| `organizers` | List of `organizer`s of the `conference` |

### `event` relationships

| Relationship | Description |
|--------------|-------------|
| `organizers` |             |
| `location`   |             |
| `speakers`   |             |
| `tags`       |             |
| `themes`     |             |
