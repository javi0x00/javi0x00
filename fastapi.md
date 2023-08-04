# :memo: Notes
## FASTAPI
---
### Resources
- [FastAPI](https://fastapi.tiangolo.com/)
- [FastAPI in Containers - Docker](https://fastapi.tiangolo.com/deployment/docker/)
- [The OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification)
- [Starlette](https://www.starlette.io/)
- [Pydantic](https://docs.pydantic.dev/)
- [Uvicorn](https://www.uvicorn.org/)
- [Gunicorn](https://gunicorn.org/)
- [Swagger UI](https://github.com/swagger-api/swagger-ui)
- [Redoc](https://github.com/Redocly/redoc)
### Requirements
- [Python](https://www.python.org/)
### Terms and concepts
1. What and why
2. What do
3. Why use
4. Getting started
5. Concepts
6. Code samples
7. API documentation
- Python
- Python module
- Python types
- Python web framework
- Installation
- API
- Rest API
- Routes
* Parameters
  - Path
  - Query
* Automatic API documentation
  - Interactive API docs
  - Alternative API docs
### Setup
#### Create a FastAPI project in virtual environment
#### Create a FastAPI project in Docker
requirements.txt
```
fastapi==0.100.1
pydantic==2.1.1
uvicorn==0.23.1
```
Dockerfile
```
FROM python:3.11.4
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
WORKDIR /core
COPY requirements.txt ./
RUN python -m pip install -r requirements.txt
COPY ./src ./src
```
compose.yaml
```
version: '3.8'
services:
  api:
    container_name: <name>
    build: .
    working_dir: /core
    command: uvicorn src.main:api --host 0.0.0.0 --reload
    volumes:
      - .:/core
    ports:
      - 8000:8000
```
---
## Software Developer
Built by [Javi](https://javierandres.dev) :copyright: 2023
Found a bug or have an idea? [Contact me](https://javierandres.dev).
