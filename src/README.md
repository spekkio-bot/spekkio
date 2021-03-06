# Spekkio - Source Code

This directory contains source code for the main Spekkio app.

## Contents

```
├── app                               # App directory
│   ├── controller                    # App controller
│   │   ├── 404.go                    # 404 handler
│   │   ├── 405.go                    # 405 handler
│   │   ├── common.go                 # Common controller functions
│   │   ├── controller_test.go        # Tests for controller package
│   │   ├── index.go                  # Index route
│   │   ├── scrumify.go               # Scrumify route
│   ├── model                         # App models
│   │   ├── models.go                 # Models for app data
│   ├── app.go                        # Top-level app source code
│   ├── app_test.go                   # Tests for app package
│   ├── middleware.go                 # Middleware for app handlers
│   ├── config.go                     # Functions to configure the app
├── queries                           # Queries to be used by the app
│   ├── graphql
│   │   ├── gqlbuilder.go             # GraphQL query / mutation builder
│   │   ├── gqlbuilder_test.go        # Tests for gqlbuilder package
│   ├── sql
│   │   ├── sqlbuilder.go             # SQL query builder
│   │   ├── sqlbuilder_test.go        # Tests for sqlbuilder package
├── .env                              # Environmental variables
├── main.go                           # Main script
```

## First Time Setup

1. Create a `.env` file. You may copy the `.env.example` file by running:
```
cp .env.example .env
```

2. Configure the following settings in your `.env` file:
```
# Database credentials (currently support Postgres only)
DB_HOST=127.0.0.1
DB_PORT=5432
DB_USER=admin
DB_PASSWORD=samplepassword
DB_SCHEMA=sampledb
DB_SSLMODE=prefer             # if undefined, app defaults to prefer

# Dev server configuration
HOST=127.0.0.1                # if undefined, app defaults to 127.0.0.1
PORT=2000                     # if undefined, app defaults to 2000
PLATFORM=default              # if undefined, app defaults to default

# OPTIONAL: Allowed origins for CORS
ORIGINS_ALLOWED=*             # if undefined, app defaults to no origins
```

## Run the App

### Build and run

1. Run `go build main.go` to build your app.
2. Run `./main dev` to execute your compiled program.

### Run without build

1. Run `go run main.go dev` to run your app without building it.
