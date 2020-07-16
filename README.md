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

## Definition list

<dl>
  <dt>Conference (conference)</dt>
  <dd>A conference consists of a series of events.</dd>
</dl>

<dl>
  <dt>Events (arrangementer)</dt>
  <dd>An event is a time and date limited incident that takes places in one location, with one or more speakers. An event can have multiple tags and but only one theme.</dd>
</dl>

<dl>
  <dt>Tags (emner)</dt>
  <dd>Tags are subjects related to different events. Tags are used as a way of inspiring users to explore different themes.</dd>
</dl>

<dl>
  <dt>Themes (temaer)</dt>
  <dd>Events are categorized in terms of different themes. A theme can only be related to one event.</dd>
</dl>

<dl>
  <dt>Location (sted)</dt>
  <dd>Where the event takes place. An event can only have one location.</dd>
</dl>

<dl>
  <dt>Organizer (arrangør)</dt>
  <dd>A conference can have one organizer where as an event can have one or more organizers.</dd>
</dl>

<dl>
  <dt>Speakers (oplægsholdere)</dt>
  <dd>A speaker can be associated with one or a number of events.</dd>
</dl>

<dl>
  <dt>Sponsors (sponsorer)</dt>
  <dd>A conference (not an event) can have one or multiple sponsors.</dd>
</dl>

![image](https://user-images.githubusercontent.com/31030948/87430713-e5189e80-c5e5-11ea-85f0-ac6cb6aca444.png)
