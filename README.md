


# Golang Restaurant Management Backend

A complete backend solution for managing restaurant operations built using **Golang**. This project focuses on **authentication**, **CRUD operations**, **menu management**, **order handling**, and **invoice generation**, with integration to **MongoDB** for data storage.

## Features

- **Authentication System**: User sign-up, login, and JWT token-based authentication.
- **CRUD Operations**: Create, read, update, and delete food items, menus, and orders.
- **Order Management**: Handle orders, update their status, and generate invoices.
- **Modular Design**: Organized structure for controllers, models, and middleware for easy maintenance and scalability.
- **MongoDB Integration**: Use MongoDB for dynamic data handling (menus, food items, orders).
- **Security**: Password hashing with bcrypt for secure storage of user credentials.

## Tech Stack

- **Backend**: Golang
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Hashing**: bcrypt
- **API Framework**: Gin (Golang web framework)

## Getting Started

### Prerequisites

To run this project locally, you need:

- **Golang**: Make sure you have Go installed. You can download it from the [official site](https://golang.org/dl/).
- **MongoDB**: You need a local or cloud MongoDB instance for data storage. You can use [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) for cloud hosting or run MongoDB locally.

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/golang-restaurant-management-backend.git
   cd golang-restaurant-management-backend
   ```

2. **Install Dependencies**

   You may need to install the required dependencies. For example:

   ```bash
   go get github.com/gin-gonic/gin
   go get github.com/dgrijalva/jwt-go
   go get golang.org/x/crypto/bcrypt
   go get go.mongodb.org/mongo-driver/mongo
   ```

3. **Configure MongoDB**

   Set up your MongoDB connection in the `config/config.go` file:

   ```go
   // Example MongoDB URI
   const MongoURI = "mongodb://localhost:27017"
   ```

4. **Run the Application**

   Start the Golang server:

   ```bash
   go run main.go
   ```

   The application will run on `http://localhost:8080`.

## Endpoints

### Authentication

- **POST /auth/signup**: User registration (email, password).
- **POST /auth/login**: User login (email, password), returns JWT token.

### Menu Management

- **POST /menus**: Create a new menu (requires authentication).
- **GET /menus**: Get all menus.
- **GET /menus/{id}**: Get a specific menu by ID.
- **PUT /menus/{id}**: Update a menu.
- **DELETE /menus/{id}**: Delete a menu.

### Food Item Management

- **POST /food-items**: Add a new food item (requires authentication).
- **GET /food-items**: Get all food items.
- **GET /food-items/{id}**: Get a specific food item by ID.
- **PUT /food-items/{id}**: Update a food item.
- **DELETE /food-items/{id}**: Delete a food item.

### Order Management

- **POST /orders**: Create a new order (requires authentication).
- **GET /orders**: Get all orders.
- **GET /orders/{id}**: Get a specific order by ID.
- **PUT /orders/{id}**: Update an order (e.g., change status).
- **DELETE /orders/{id}**: Delete an order.

### Invoice Handling

- **GET /invoices/{orderId}**: Generate invoice for an order.

## Project Structure

- **controllers**: Contains handler functions for routes.
- **models**: Defines database models for menus, food items, orders, and users.
- **middleware**: Functions for authentication and authorization.
- **routes**: Defines all the API routes and their associated controllers.
- **config**: Configuration files for setting up MongoDB connection and server settings.

## Security

This project uses **JWT** for authentication and **bcrypt** for password hashing, ensuring that sensitive data like passwords are stored securely.

- Passwords are hashed before storage using `bcrypt`.
- JWT tokens are used for user authentication in the backend.

## Contributing

Feel free to fork this repository and submit pull requests. Please make sure to follow the code style and include tests for new features or bug fixes.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add feature-name'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or issues, feel free to open an issue or reach out to me via email at [deshdeepakkant@gmail.com].

---

Made with ❤️ by Desh Deepak Kant
