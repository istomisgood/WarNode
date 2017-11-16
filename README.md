# Bootiful War Node

## SpringBoot 2 War backend. NodeJs (React) frontend. Best of both worlds

With help from:

* https://stackoverflow.com/questions/17875576/gradle-projects-depending-on-artifacts-created-by-sibling-projects
* https://github.com/ThomasBem/spring-boot-create-react-app
* http://www.davidtanzer.net/getting_started_with_react_and_spring_boot

## Requirements

This has been developed against npm 5.5.1 and node 8.9.1

## Development

### Backend

During development the backend is a typical SpringBoot application using war packaging. The content of backend is mostly Spring Initializer output. The build.gradle file gets 3 extra lines to assist with the final build.

### Frontend

During development the frontend is a typical create-react-app application. The content of frontend is simply create-react-app output. The build.gradle file gets some attention to assist with the final build. This means the frontend isn't using gradle during development. The frontend only uses gradle for the final build.

### Distribution

The distribution project is only for building the final artifact.

## CI Build

The build server gets its own task to execute - `cibuild`.

```
./gradlew cibuild
```

## TODO

Move all logic to distribution/build.gradle. This way backend and frontend are kept as straight forward as possible.

