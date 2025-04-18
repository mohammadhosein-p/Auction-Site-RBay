# RBay

RBay is an online auction platform where users can bid on items, view item details, like items, and chat about items. This project is built using Node.js, Express, Sequelize, and Redis.

## Table of Contents

- [RBay](#rbay)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Installation](#installation)
  - [Usage](#usage)
    - [API Endpoints](#api-endpoints)
      - [Authentication](#authentication)
      - [Users](#users)
      - [Items](#items)
      - [Chats](#chats)
  - [Environment Variables](#environment-variables)
  - [Contributing](#contributing)
  - [License](#license)

## Features

- User authentication (signup, login, logout)
- Create, view, and update items
- Bid on items
- Like and view items
- Chat about items
- Caching with Redis for improved performance

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/RBay.git
    cd RBay
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Set up the environment variables:

    Create a `.env` file in the root directory and add the following variables:

    ```env
    DB_HOST=your_database_host
    DB_PORT=your_database_port
    DB_USERNAME=your_database_username
    DB_PASSWORD=your_database_password
    JWT_SECRET=your_jwt_secret
    ```

4. Start the Redis server:

    ```bash
    redis-server
    ```

5. Run the application:

    ```bash
    npm start
    ```

## Usage

### API Endpoints

#### Authentication

- **POST /api/auth/signup**: Sign up a new user
- **POST /api/auth/login**: Log in an existing user
- **POST /api/auth/signout**: Log out the current user

#### Users

- **GET /api/users/:id**: Get user details by ID
- **PUT /api/users/:id**: Update user details by ID

#### Items

- **POST /api/items**: Create a new item
- **GET /api/items/:id**: Get item details by ID
- **POST /api/items/like**: Like an item
- **POST /api/items/view**: View an item
- **POST /api/items/bid**: Bid on an item
- **GET /api/items/:itemId/bids**: Get bid history for an item
- **GET /api/items/sort/price**: Get items sorted by price
- **GET /api/items/sort/duration**: Get items sorted by duration
- **GET /api/items/sort/views**: Get items sorted by views in the past day

#### Chats

- **GET /api/chats/:itemId**: Get chat messages for an item
- **POST /api/chats/:itemId**: Post a chat message for an item

## Environment Variables

The following environment variables need to be set in your `.env` file:

- `DB_HOST`: The host of your database
- `DB_PORT`: The port of your database
- `DB_USERNAME`: The username for your database
- `DB_PASSWORD`: The password for your database
- `JWT_SECRET`: The secret key for JWT token generation

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.