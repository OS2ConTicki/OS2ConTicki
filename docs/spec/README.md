# Entities

This document describes the entities and their properties.

See [Definition list](../../README.md#definition_list) for a list of all
entities.

## Properties

### Shared properties

Apart from Tag and Theme, all entities have the following attributes

| Attribute        | Type    | Description                    |
|------------------|---------|--------------------------------|
| `title`          | string  | The title                      |
| `promote`        | boolean |                                |
| `image`          | object  |                                |
| `image.url`      | string  |                                |
| `image.meta.alt` | string  | Alternative text for the image |
| `summary`        | string  |                                |
| `description`    | string  |                                |

Tag and Theme have only the `title` attribute.

### Conference properties

| Attribute    | Type                       | Description    |
|--------------|----------------------------|----------------|
| `start_time` | datetime (ISO 8601 string) | The start time |
| `end_time`   | datetime (ISO 8601 string) | The end time   |

### Event properties

| Attribute    | Type                       | Description    |
|--------------|----------------------------|----------------|
| `start_time` | datetime (ISO 8601 string) | The start time |
| `end_time`   | datetime (ISO 8601 string) | The end time   |

## Relationships

### Shared relationships

Apaert from Conference, all entities have the following relationships

| Relationship | Description                        |
|--------------|------------------------------------|
| `conference` | A relationship with the conference |

### Conference relationships

| Relationship | Description |
|--------------|-------------|
| `organizers` |             |

### Event relationships

| Relationship | Description |
|--------------|-------------|
| `organizers` |             |
| `location`   |             |
| `speakers`   |             |
| `tags`       |             |
| `themes`     |             |
