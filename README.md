# Demo — Spring Boot 3.3 + Java 21 + H2

A minimal REST API scaffold with a persistent H2 database.

## Prerequisites

- Java 21+
- Maven 3.9+

## Run

```bash
mvn spring-boot:run
```

The app starts on `http://localhost:8080`. The H2 database file is created at `./data/demodb.mv.db` on first run and persists across restarts.

## H2 Console

```
URL      http://localhost:8080/h2-console
JDBC URL jdbc:h2:file:./data/demodb
User     sa
Password (leave blank)
```

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/api/users` | List all users |
| GET | `/api/users/{id}` | Get user by ID |
| POST | `/api/users` | Create a user |
| DELETE | `/api/users/{id}` | Delete a user |

**Example POST body:**
```json
{ "name": "Jane Doe", "email": "jane@example.com" }
```

## Actuator

Health and metrics are exposed at `/actuator/health` and `/actuator/metrics`.

## Running Tests

```bash
mvn test
```
