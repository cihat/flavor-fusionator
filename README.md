# Flavor Fusionator

## Unleash your culinary creativity with "Flavor Fusionator." Discover delightful recipes using ingredients you already have at home and elevate your cooking game effortlessly.


Basic Mind Map:
![Mind Map](./architecture-planning/mind-map.png)

Class Diagram:
![Class Diagram](https://raw.githubusercontent.com/cihat/flavor-fusionator/master/architecture-planning/Class-Diagram.png?token=GHSAT0AAAAAACBNP3Y2QXKAAQR37RL7FSC4ZEDWEJA)



### To-Dos

- [ ] Backend
  - [ ] Design UML Diagram
  - [ ] ...
- [ ] Frontend
  - [ ] Create UI 
    - [ ] Landing Page
    - [ ] Input ingredients and get recipes
    - [ ] Recipe Page
    - [ ] User Profile Page
    - [ ] ...




# Technical Overview

A starter repository for MongoDB, Node.js, and Vue.js, with a local environment based on Docker.

# Installation

## Running the stack

```sh
$ docker-compose up
```

## Accessing the stack from a browser

The starter stack works with a load balancer that binds to ports 80 and 443. It currently serves the domain http://stack.localhost. In order to reach the frontend through the stack, you need to edit your `hosts` file (usually under `/etc/hosts` in UNIX environments and `C:\Windows\System32\Drivers\etc\hosts` in Windows) and add the following line:

```
127.0.0.1 stack.localhost
```

Now if you visit http://stack.localhost, you will be greeted with the frontend starter project.

## Changing the local domain

If you wish to use a domain name other than http://stack.localhost, simply set the environment variable `DOMAIN` to any domain you want.

```sh
$ DOMAIN=another-domain.localhost docker-compose up
```

You then also need to update your `hosts` file accordingly.

## Debugging

You can debug the backend while it's running in VSCode. Instead of running `docker-compose up`, run the following command:

```sh
$ docker-compose -f docker-compose.yml -f docker-compose.debug.yml up
```

This starts the backend service in the debug mode, so you can use the built-in debug task `Attach to backend` to debug your backend service.

# Running tests

## Running backend tests

```sh
$ cd backend
$ npm i
$ npm test
```

## Running frontend tests

```sh
$ cd frontend
$ npm i
$ npm test:unit
$ npm test:e2e
```

# Linting

Run `npm install` on the root folder and it will set up a pre-commit hook to lint the staged files. You will also have two lint commands, `npm run lint` and `npm run lint-staged` that you can run on the root folder.

These commands run the individual `lint` and `lint-staged` scripts in both the `frontend` and the `backend` folders, and they will respect individual configurations of these folders.
