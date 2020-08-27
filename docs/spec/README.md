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

| Attribute           | Type                       | Description                                                                                          |
|---------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| `language`          | string (ISO 639-1 Code)    | The language for the conference                                                                      |
| `start_time`        | datetime (ISO 8601 string) | The start time                                                                                       |
| `end_time`          | datetime (ISO 8601 string) | The end time                                                                                         |
| `ticket`            | object                     |                                                                                                      |
| `ticket.url`        | string                     | Url to ticket system                                                                                 |
| `ticket.text`       | string (nullable)          | Text to show on “Buy ticket” button                                                                  |
| `app`               | object                     | App metadata                                                                                         |
| `app.logo`          | string                     | App logo url (should be 512x512 pixels)                                                              |
| `app.logo_svg`      | string (optional)          | App SVG logo url                                                                                     |
| `app.icons`         | object                     | App icons urls indexed by `«width»x«height»`, e.g. `{"196x196":	"https://lorempixel.com/196/196/"}` |
| `app.primary_color` | color (css color string)   | Primary app color                                                                                    |

### `event` attributes

| Attribute     | Type                       | Description                         |
|---------------|----------------------------|-------------------------------------|
| `language`    | string (ISO 639-1 Code)    | The language for the event          |
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

| Relationship | Description                     |
|--------------|---------------------------------|
| `organizers` | List of organizers of the event |
| `location`   | The location of the event       |
| `speakers`   | List of speakers at the event   |
| `tags`       | List of tags for the event      |
| `themes`     | List of themes for the event    |
