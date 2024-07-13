
# Department Management API

This is a .NET API for managing departments and their hierarchical sub-departments.

## Requirements

- ASP.NET Core
- Entity Framework Core or Dapper
- SQL Server

## Features

- CRUD operations for departments and sub-departments
- JWT authentication
- Authorization (Admin role)
- Input validation
- Swagger for API documentation
- AES encryption for department names

## Endpoints

### Create Department

- Method: POST
- Endpoint: `/api/departments`
- Request Body:
  ```json
  {
    "name": "Department Name",
    "parentDepartmentId": null
  }
  ```

### Get Department by ID

- Method: GET
- Endpoint: `/api/departments/{id}`

### Get All Departments

- Method: GET
- Endpoint: `/api/departments`

### Update Department

- Method: PUT
- Endpoint: `/api/departments/{id}`
- Request Body:
  ```json
  {
    "name": "Updated Department Name",
    "parentDepartmentId": null
  }
  ```

### Delete Department

- Method: DELETE
- Endpoint: `/api/departments/{id}`
- Response: `204 No Content`

## Authentication

To generate a JWT token, use the following endpoint:

### Generate Token

- Method: POST
- Endpoint: `/api/auth/token`
- Request Body:
  ```json
  {
    "username": "admin",
    "password": "password"
  }
  ```

## How to Run

1. Clone the repository
2. Update the connection string in `appsettings.json`
3. Run the application using `dotnet run`
4. Access Swagger UI at `https://localhost:7115/swagger/index.html`
