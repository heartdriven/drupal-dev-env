# drupal-dev-env for macOS

## Installation:

* Install docker for mac
* Execute pre-commands on first time using docker + docker-sync
* In docker-compose.yml, rename *docker-sync-unison-dev* to *docker-sync-unison-appname* on all occurences
* In docker-sync.yml, make sure the name above is also matched here
* Run `docker-sync start`
* Run `docker-compose up -d`
* Run `docker exec -i container_name mysql -udrupal -pdrupal --database=drupal < ~/path/to/dump_file.sql` to insert dump into the database container
  (Use `docker ps` to figure the name of the container)

Happy coding!

References:
* http://docs.docker4drupal.org/en/latest/macos/
