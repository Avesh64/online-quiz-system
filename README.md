# online-quiz-system
“A Java Spring Boot–based e-commerce food ordering app offering user authentication, restaurant browsing, menu listing, cart management, and secure order placement. Built with REST APIs, layered architecture, MySQL integration, and seamless user experience.”
# QuickBite — Java Spring Boot E-commerce Food Ordering App

**Short description (300 chars):**
A Java Spring Boot–based e-commerce food ordering app offering user authentication, restaurant browsing, menu listing, cart management, and secure order placement. Built with REST APIs, layered architecture, MySQL integration, and seamless user experience.

---

## Features

* User registration & authentication (JWT)
* Restaurant & menu browsing
* Add to cart, update quantity, remove items
* Place orders & view order history
* Admin panel for managing restaurants, menus, and orders
* RESTful API design with layered service & repository patterns
* MySQL persistence and Flyway/Liquibase-compatible migrations

## Tech Stack

* Java 17+ (or specified JDK)
* Spring Boot (Web, Data JPA, Security)
* MySQL (or MariaDB)
* Maven/Gradle
* JWT for authentication
* Thymeleaf / React (optional frontend)

## Project Structure

```
src/
├─ main/
│  ├─ java/com/yourorg/quickbite
│  │  ├─ controller
│  │  ├─ service
│  │  ├─ repository
│  │  ├─ model
│  │  └─ config
│  └─ resources
│     ├─ application.properties
│     └─ db/migration
└─ test/
```

## 300-character Project Description (for GitHub):

> A Java Spring Boot–based e-commerce food ordering app offering user authentication, restaurant browsing, menu listing, cart management, and secure order placement. Built with REST APIs, layered architecture, MySQL integration, and seamless user experience.

## Prerequisites

* JDK 17+
* Maven or Gradle
* MySQL server
* (Optional) Node.js if using a separate frontend

## Setup & Run (local)

1. Unzip source (uploaded): `/mnt/data/guviii.zip`
2. Configure database in `src/main/resources/application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/quickbite
spring.datasource.username=your_db_user
spring.datasource.password=your_db_password
spring.jpa.hibernate.ddl-auto=update
```

3. Build and run:

* With Maven: `mvn clean spring-boot:run`
* With Gradle: `./gradlew bootRun`

## Environment Variables

You can use environment variables instead of plaintext properties. Example:

```
SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/quickbite
SPRING_DATASOURCE_USERNAME=root
SPRING_DATASOURCE_PASSWORD=secret
JWT_SECRET=your_jwt_secret
```

## API Endpoints (examples)

* `POST /api/auth/register` — register user
* `POST /api/auth/login` — login (returns JWT)
* `GET /api/restaurants` — list restaurants
* `GET /api/restaurants/{id}/menu` — get menu
* `POST /api/cart` — add item to cart
* `POST /api/orders` — place order

## Admin

* Admin endpoints under `/api/admin/**` for managing restaurants, menus, and orders.
* Protect admin routes using role-based authorities (ROLE_ADMIN).

## Testing

* Unit tests with JUnit 5
* Integration tests with Spring Boot Test
* Postman collection: create a collection with the endpoints above for manual testing

## Docker (optional)

Provide a `Dockerfile` and `docker-compose.yml` to run the app + MySQL. Example `docker-compose.yml` should define `app` and `db` services.

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit changes and push
4. Open a Pull Request describing your changes

## Troubleshooting

* DB connection errors: verify MySQL is running and credentials are correct
* JWT issues: ensure `JWT_SECRET` matches in env and config

## License

Choose a license (MIT, Apache-2.0, etc.) and include `LICENSE` file.

## Contact

For questions or support, open an issue or contact the maintainer.

---

*Note:* The uploaded project archive is available at `/mnt/data/guviii.zip` (use this path to extract the project locally).
