# Website

This is the public website for the Jump.doctor project.

## Development

To work on this project, it is necessary to:

* Install docker
* Run `docker-compose up`
* Navigate to `http://localhost:4567`
* Make changes and refresh

When making changes to the Gemfile:

* Stop the `docker-compose` process
* Run `docker-compose run web bundle` to (un-)install gems and update the `Gemfile.lock`
* Re-start the server with `docker-compose up`

To clean up this project from your local machine, run `docker-compose down`, which will delete all containers, networks, images and volumes associated with this project.

## Deployment

TBD