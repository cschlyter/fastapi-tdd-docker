# Summaries API

Welcome to the Summaries API repository. This API provides a text summarization service used for creating article summaries from a given URL.

## Prerequisites

Ensure that you have the following installed on your local machine:
1. [Docker](https://docs.docker.com/get-docker/)
2. [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### How to run the application

Use Docker Compose to run the API service locally. The API runs on port 8004. Run the following command in your terminal:

```bash
docker-compose up
```

This will pull and build all necessary Docker images, then run the containers necessary for the application to function.

### Running the tests

To execute the tests for this project, run the following command in your terminal:

```bash
docker-compose exec web python -m pytest --cov="."
```

This command will run all pytest tests in the project and display a coverage report. You may need to ensure the API service is up and running before executing the tests.

### Running Flake8

Flake8 is a tool for enforcing Python code style. It can be used to catch errors and ensure conformance to PEP8 style guide.

Run the following command to perform a static analysis on the code:

```bash
docker-compose exec web flake8 .
```

This will run Flake8 on all files in the current directory and subdirectories, and it will report any violations of the style guide.

### Running Black Formatter

[Black](https://black.readthedocs.io/en/stable/) is a Python code formatter that reformats your entire file in place. It's consistent, concise and makes your code more readable.

Run the following command to apply Black to all Python files in the project:

```bash
docker-compose exec web black .
```

This command will format all Python files in the current directory and subdirectories in place, according to the Black's code style. Please remember to run this command before submitting your pull requests to ensure all new code adheres to the established style.

### Running isort

[isort](https://pycqa.github.io/isort/) is a Python utility/library to sort imports alphabetically, and automatically separated into sections and by type. It provides a way to standardize and simplify the task of organizing your import statements.

Run the following command to apply isort to all Python files in the project:

```bash
docker-compose exec web isort .
```

This command will sort and organize all import statements in Python files in the current directory and subdirectories. This ensures your imports remain neatly organized and adhere to the project's coding conventions. Please make sure to run this command before committing your code.

### Applying Migrations

[Aerich](https://github.com/tortoise/aerich) is a database migration tool for Tortoise-ORM. It helps to keep your database schema synchronized with the Python data models you define in your code.

Run the following command to apply the migrations to the database:

```bash
docker-compose exec web aerich upgrade
```

This command applies any pending migrations to your database. Ensure to run this command after any changes to the data models or after pulling changes that include updates to the data models.

## API Documentation

Once your API service is running, you can view the API documentation at the following URL:

```
http://localhost:8004/docs
```

The API documentation page provides detailed information about the available endpoints, their request/response structure, and other useful details.

## License

Please check the `LICENSE` file for details on the project's license.
