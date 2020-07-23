# API

The API implements the [JSON:API specification](https://jsonapi.org/).

## Links

A Conference must have the following [links](https://jsonapi.org/format/#document-links):

| Name        | Description                                                                   |
|-------------|-------------------------------------------------------------------------------|
| `event`     | Url for getting all events in the conference                                  |
| `location`  | Url for getting all locations in the conference                               |
| `organizer` | Url for getting all organizers in the conference                              |
| `speaker`   | Url for getting all speakers in the conference                                |
| `sponsor`   | Url for getting all sponsors in the conference                                |
| `tag`       | Url for getting all tags in the conference                                    |
| `theme`     | Url for getting all themes in the conference                                  |
| `all`       | Url for getting all events in the conference including *all* related entities |
| `self`      | Url for getting all events in the conference                                  |

To get all data for a Conference, requests must be sent for all links apart from
`self` and `all`, or by getting everything in one go using the `all` link.
