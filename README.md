**Code**: <a href="https://github.com/kamilszczepanik/meteorological-station" target="_blank">https://github.com/kamilszczepanik/meteorological-station</a>  
**Year**: 2023  
**Timespan**: 20 hours  

## Overview

## Tech Stack

- • **Language**: Typescript, Python
- • **Frameworks/Libraries**: React, FastAPI, Axios, SQLModel, PostgreSQL, TanStack React Query, React Hook Form
- • **Styling**: Tailwind, Chakra UI
- • **Other tools**: Docker

## Key Features

- • Add, edit, delete weather forecast for next week
- • Current weather & weather history for specific city
- • Error handling & validation
- • Designed UX/UI
- • Pagination

This one was an assignment.


# FastAPI Project - Development

## Docker Compose

* Start the local stack with Docker Compose:

```bash
docker compose watch
```

* Now you can open your browser and interact with these URLs:

Frontend, built with Docker, with routes handled based on the path: http://localhost:5173

Backend, JSON based web API based on OpenAPI: http://localhost:8000

Automatic interactive documentation with Swagger UI (from the OpenAPI backend): http://localhost:8000/docs

Adminer, database web administration: http://localhost:8080

Traefik UI, to see how the routes are being handled by the proxy: http://localhost:8090


To check the logs, run (in another terminal):

```bash
docker compose logs
```

To check the logs of a specific service, add the name of the service, e.g.:

```bash
docker compose logs backend
```

## Local Development

The Docker Compose files are configured so that each of the services is available in a different port in `localhost`.

For the backend and frontend, they use the same port that would be used by their local development server, so, the backend is at `http://localhost:8000` and the frontend at `http://localhost:5173`.

This way, you could turn off a Docker Compose service and start its local development service, and everything would keep working, because it all uses the same ports.

For example, you can stop that `frontend` service in the Docker Compose, in another terminal, run:

```bash
docker compose stop frontend
```

And then start the local frontend development server:

```bash
cd frontend
npm run dev
```

Or you could stop the `backend` Docker Compose service:

```bash
docker compose stop backend
```

And then you can run the local development server for the backend:

```bash
cd backend
fastapi dev app/main.py
```
