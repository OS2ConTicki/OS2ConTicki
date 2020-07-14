# OS2ConTicki

A complete conference management system

This is the main repository with documentation and specifications (e.g. requirements for API endpoints and data formats).

## Implementations

Two parts are needed: “admin” for managing conferences and “app” for displaying data from admin. 

### Drupal

* https://github.com/OS2ConTicki/drupal-admin
* https://github.com/OS2ConTicki/drupal-app

### Symfony

* https://github.com/OS2ConTicki/symfony-admin
* https://github.com/OS2ConTicki/symfony-app

### Phrasebook

Conference (conference)
A conference consists of a series of events.

Events (arrangementer)
An event is a time and date limited incident that takes places in one location, with one or more speakers. An event can have multiple tags and but only one theme.

Tags (emner)
Tags are subjects related to different events. Tags are used as a way of inspiring users to explore different themes.

Themes (temaer)
Events are categorized in terms of different themes. A theme can only be related to one event.

Location (sted)
Where the event takes place. An event can only have one location.

Organizer (arrangør)
A conference can have one organizer where as an event can have one or more organizers.

Speakers (oplægsholdere)
A speaker can be associated with one or a number of events.

Sponsors (sponsorer)
A conference (not an event) can have one or multiple sponsors.
