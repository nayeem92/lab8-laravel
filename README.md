# Laravel Inventory Management

This project is an inventory management system built with Laravel and MySQL, containerized using Docker. It includes a MySQL database and a Laravel application that interacts with the database.

## Prerequisites

- Docker
- Docker Compose

## Setup

1. Clone the repository to your local machine.
2. Navigate to the project directory:
   ```bash
   cd path/to/your/project
   ```

3. Build and start the containers using Docker Compose:
```bash
docker-compose up -d
```
4. The application will be accessible at http://localhost:8000, and the MySQL database will be running on port 3306.

## Configuration

The Laravel application is configured to connect to the MySQL database running in the `mysql_db` container.  
Environment variables are defined in the `docker-compose.yml` file:

- **DB_CONNECTION**: mysql
- **DB_HOST**: db
- **DB_PORT**: 3306
- **DB_DATABASE**: inventory_db
- **DB_USERNAME**: custom_user
- **DB_PASSWORD**: custom_password

## Running Migrations

Before using the application, run the database migrations to set up the necessary tables:

```bash
docker-compose exec app php artisan migrate --force
```
## Usage

- The Laravel application will be running at [http://localhost:8000](http://localhost:8000).
- The MySQL database is accessible on port `3306`.

### Screenshots

1. ![Screenshot 1](screenshots_N01608790/lar1.PNG) 
2. ![Screenshot 1](screenshots_N01608790/lar2.PNG) 
3. ![Screenshot 1](screenshots_N01608790/lar3.PNG) 
4. ![Screenshot 1](screenshots_N01608790/lar4.PNG) 

## Troubleshooting

If you encounter any issues, check the logs of the containers:

```bash
docker logs mysql_db
docker logs inventory_manager
```