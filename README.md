# Beyond API

Welcome to the backend of the Beyond Platform! This platform aims to bring together individuals passionate about contributing to projects such as Local Blood Drives, Scoping Climate Models, Black Lives Matter Rallies or any other social good projects that target sustainable development goals. It is designed in the spirit of open-source software, allowing for collaborative contributions.


## Features

### 1. Member Profiles:
- View a list of members, their current projects, and ideas.
- Members can specify their set of skills, things they're willing to contribute, availability, topics of interest, and languages spoken.

### 2. Open Projects & Ideas Directory:
- Browse the list of open projects and ideas.
- Filter projects based on specific criteria.
- View individual project and idea pages.
- Suggest or make edits to projects and ideas that are visible to all members.

### 3. Location-based Collaboration:
- Discover projects based on your location.
- Collaborate with local members to make a tangible impact in your community.

## Tech Stack

- **Web Framework**: [FastAPI](https://fastapi.tiangolo.com/)
- **Database**: [MongoDB](https://www.mongodb.com/) with [Motor](https://motor.readthedocs.io/en/stable/)
- **Containerization**: [Docker](https://www.docker.com/)

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Docker
- docker-compose

## Setup & Installation

1. Clone/Fork project
2. cd into the project



### Edit Environment Variables
Edit the `.env` file within the project folder.

### Run Tests
```sh
make test
```

### Build Docker Image
```sh
make docker-build
```

### Docker-compose
```sh
make docker-compose-up
make docker-compose-down
```

### Run Service Locally
```sh
make dev
```
This will create a MongoDB container as well.

### Check Swagger API Document
Go to ` http://localhost:8888/docs`.

Your backend server should now be running at `http://localhost:8000`.

### Database Migrations

Whenever there are changes to the database schema, run the migration script:

```bash
docker-compose exec backend python migrate.py
```

## API Routes

- **Members**:
  - `GET /members`: Retrieve a list of all members.
  - `POST /members`: Add a new member.
  - `GET /members/{id}`: Retrieve details of a specific member.
  - `PUT /members/{id}`: Update a member's details.
  - `DELETE /members/{id}`: Delete a member.

- **Projects**:
  - `GET /projects`: Retrieve a list of all open projects and ideas.
  - `POST /projects`: Create a new project or idea.
  - `GET /projects/{id}`: Retrieve details of a specific project or idea.
  - `PUT /projects/{id}`: Update a project or idea's details.
  - `DELETE /projects/{id}`: Delete a project or idea.


## Contributing

Contributions are welcomed! Please read our [Contributing Guide](CONTRIBUTING.md) for details on the process and guidelines.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.md) file for details.
