# Install Dependencies
npm install express jsonwebtoken bcryptjs

# How to Generate SBOM
https://www.npmjs.com/package/@cyclonedx/cyclonedx-npm \
npm install --global @cyclonedx/cyclonedx-npm \
cyclonedx-npm --help


# How to Use JWT Authentication

##  Register a User

Send a **POST** request to `http://localhost:3000/register` with:

```json
{
  "username": "testuser",
  "password": "securepassword"
}
```

 **Response:**

```json
{ "message": "User registered successfully" }
```

---

##  Login to Get a Token

Send a **POST** request to `http://localhost:3000/login` with:

```json
{
  "username": "testuser",
  "password": "securepassword"
}
```

 **Response:**

```json
{ "token": "your.jwt.token.here" }
```

 **Copy the token**, as it will be required for accessing protected routes.

---

##  Access Protected Route (`/items`)

Send a **GET** request to `http://localhost:3000/items`

### **Add the Authorization Header:**

```makefile
Authorization: Bearer your.jwt.token.here
```

✅ **If the token is valid, you will get:**

```json
[
  { "id": 1, "name": "Item One" },
  { "id": 2, "name": "Item Two" }
]
```

 **If the token is missing or invalid, you get:**

```json
{ "message": "Access denied. No token provided." }
```

or

```json
{ "message": "Invalid token" }
```

