# Podcast Community

School-project with the goal of creating a community based around podcasts

- [Podcast Community](#podcast-community)
  - [Intended fetures:](#intended-fetures)
  - [Main parts of the app](#main-parts-of-the-app)
  - [Project setup](#project-setup)
    - [Useful commands](#useful-commands)
  - [Deployment](#deployment)
    - [Build](#build)
    - [Pipline](#pipline)
    - [Server](#server)
    - [Sites](#sites)
  - [Related repositories](#related-repositories)
  - [Documentation](#documentation)

## Intended fetures:

* follow podcasts
* listen to podcasts
* download episodes
* recomend episodes/shows to friends (both in the app and outside the app)
* outhenticate with facebook/google/twitter
* import/email friends from the platform you registered thrue
* get notificaitons when new episode are relesed/recomended to you
* rate episodes and programs


## Main parts of the app

API for podcasts: https://market.mashape.com/listennotes/listennotes

frontend: React with redux and TypeScript

backend: node

database: mongoDB


## Project setup

* run `./bin/init` in this repo to clone the clinte and api code into your repo
* run `cp .env.example .env` and then set the .env variables
* make sure that the instructinons for setup has been follow both for the [client](https://github.com/SebastianGerS/podcast-community-client) and [api](https://github.com/SebastianGerS/podcast-community-api) repository
* run `docker-compose -f docker-compose-dev.yml --build up` this process will start the continers and let you follow any changes if you which to run the process in the background just add the `-d` flag


### Useful commands

* `docker-compose -f docker-compose-dev.yml up` starts all containers defined in the docker file
* `docker-compose -f docker-compose-dev.yml down` stops all the containers defined in the docker file

[All docker-compose commands](https://docs.docker.com/compose/reference/overview/)


## Deployment


### Build

the docker-compose.yml file is used when building for production also the client repo is using Dockerfile_Prod instead of the regular docker file settings for the nginx container that servs the client are also found in the client repo (default.conf.example)

### Pipline

Pipline setup at https://app.buddy.works/portfoliosgs/podcast-community/pipelines/pipeline/175262/
I have chosen to set it to require manual trigger

### Server

The apps are served on from a [digitalocean](https://www.digitalocean.com/) droplet that I have configured and uses nginx and and certbot.

### Sites

* [client](https://thru.the.ether.sebastiangerstelsollerman.me/)
* [client-dev](https://dev.thru.the.ether.sebastiangerstelsollerman.me/)
* [api](https://thru.the.ether-api.sebastiangerstelsollerman.me/) (slash redirects to docks)
* [api-dev](https://dev.thru.the.ether-api.sebastiangerstelsollerman.me/) (slash redirect to docks)

## Related repositories

* https://github.com/SebastianGerS/podcast-community-client
* https://github.com/SebastianGerS/podcast-community-api

## Documentation

* Preproject survey:
  * [survay-data](user-survay-data.pdf)

* Userpersonas and userstories:
  * https://docs.google.com/document/d/1G0pdUc-anVnASBaJzLOzyOTGzSDQHntw4nZ_Wlm49bI/edit?usp=sharing

* Sitemap:
  * [sitemap-current](sitemap-current.png)
  * [sitemap-model-v1](sitemap-model.png)
  * [sitemap-model-v2](sitemap-model-v2.png)
  * [sitemap-model-v3](sitemap-model-v3.png)
  * https://docs.google.com/document/d/1kVqCablrY-5T7b5RESdLV-_wVF0_D2ZHxkCfBsciGNc/edit?usp=sharing

* Requirement Specification:
  * https://docs.google.com/document/d/1xzZjNwXzCyOgcMQHjV7NhzTBWHdAfpQHxZ2fiZsOBnY/edit?usp=sharing

* Sketches (note that thees are wery preliminery sketches of the intended design, and I do apologise for my lack if skill when it comes to drawing)
  * [Views](Sketches/Views/)
  * [Modals](Sketches/Modals/)

* Wireframes/Mockups (toggle between mockup and wireframes by pressing ⌘ Y (Mac) or CtrlShift ⇧  3 (PC)) note that all wireframes are for mobile, slight adjustments will be made for laptop

  * https://www.figma.com/file/GfVE8P1nduYgw6nWMkJMh5Sa/Thru-the-Ether?node-id=0%3A1

* Prototype
	* https://www.figma.com/proto/GfVE8P1nduYgw6nWMkJMh5Sa/Thru-the-Ether?node-id=0%3A1&scaling=scale-down

* Database structure
	* https://docs.google.com/document/d/1HFzVH5swF5VcTHSc7vrW2rzpyvXFkNnvjCjOF3By-us/edit?usp=sharing

* [logbook enteries](logbook/)
