
# 📚 Books Management - Docker Compose & Postman Collection

This repository contains the necessary Docker Compose configuration and Postman Collection JSON for testing the Books Management backend (Flask API) and frontend (Angular).

---

## 📁 Prequisites
-Clone those repositories:
- https://github.com/jorgemgordillop/booksappbe
- https://github.com/jorgemgordillop/booksappfe



## 📁 Repository Structure

```
project-root/
├── docker-compose.yml
└── Books_API_Postman_Collection.json
```

---

## 🐳 Docker Compose Setup

Ensure you have [Docker](https://docs.docker.com/get-docker/) and Docker Compose installed.

To build and run the backend, frontend, and PostgreSQL database together, run:

```bash
docker-compose up --build
```

Your services will be available at:

- **Frontend**: `http://localhost:4200`
- **Backend**: `http://localhost:8000`
- **PostgreSQL**: Port `5432`

---

## 🛠️ Docker Compose Services

The provided `docker-compose.yml` contains:

- **PostgreSQL Database**
- **Flask Backend (REST API)**
- **Angular Frontend (served by Nginx)**

You can customize ports and settings by modifying `docker-compose.yml`.

---

## 🚩 Important URLs

- **Frontend Angular App**: [http://localhost:4200](http://localhost:4200)
- **Backend Flask API**: [http://localhost:8000](http://localhost:8000)
- **Backend Swagger UI**: [http://localhost:8000/swagger](http://localhost:8000/swagger)

---

## 🔍 Testing API with Postman

### Importing Collection into Postman:

1. Open Postman.
2. Click **Import → Upload Files**.
3. Select `Books_API_Postman_Collection.json`.
4. Now, endpoints are ready to test.

### Endpoints Included:

- **GET** `/books/`: Retrieve all books.
- **POST** `/books/`: Add a new book.
- **GET** `/books/{id}`: Retrieve a book by ID.
- **PUT** `/books/{id}`: Update a book by ID.
- **DELETE** `/books/{id}`: Delete a book by ID.

**Note**: Ensure you replace `{{book_id}}` with actual IDs when testing requests.

---

## 📋 Environment Requirements

- Docker & Docker Compose
- Postman

---

## ⚠️ Common Issues

### Database Connection Issues:

Make sure your PostgreSQL container is running correctly and matches the configuration in your Flask backend.

### CORS Issues:

Ensure Flask-CORS is configured properly in the backend if accessing from the Angular frontend.

---

## 🤝 Contributing

1. Fork this repository.
2. Create your branch (`git checkout -b feature/new-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to your branch (`git push origin feature/new-feature`).
5. Create a Pull Request.

---

## 📝 License

This project is licensed under the MIT License.
