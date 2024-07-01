# UAA Server

The UAA Server acts as the authorization server that issues tokens.

## Prerequisites

- JDK 21
- Gradle
- Spring Boot 3.1.5

## Configuration

**Port:** 8080

## Endpoints

- `/oauth2/token`: Obtain an access token

## Running the Service

1. Navigate to the project directory:
    ```bash
    cd uaa-server
    ```

2. Build and run the project:
    ```bash
    ./gradlew bootRun
    ```

## Testing the Setup

### Obtain a Token

To obtain a token from the UAA Server, use the following command:

```bash
curl -X POST http://localhost:8080/oauth2/token \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -u client-id:client-secret \
     -d "grant_type=client_credentials"
