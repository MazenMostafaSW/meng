# Graduation Project API

[![Node.js](https://img.shields.io/badge/Node.js-v18.x-green.svg)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-v4.21.2-blue.svg)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-v5.9.2-green.svg)](https://www.mongodb.com/)
[![License](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

A robust RESTful API built with Express.js and MongoDB for managing data with features including authentication, file uploads, and data validation.

## Technologies Used

- **Express.js**: Fast, unopinionated web framework for Node.js
- **MongoDB/Mongoose**: NoSQL database and elegant MongoDB object modeling
- **Multer**: Middleware for handling multipart/form-data for file uploads
- **Sharp**: High-performance image processing library
- **Express Validator**: Middleware for data validation
- **UUID**: For generating unique identifiers
- **Slugify**: For creating URL-friendly slugs

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/graduation.git

# Navigate to the project directory
cd graduation

# Install dependencies
npm install

# Set up environment variables
cp config.env.example config.env
# Edit config.env with your configuration

# Start development server
npm run start:dev

# Start production server
npm run start:prod
```

## API Endpoints

### Category Endpoints
- `GET /api/v1/categories` - Get all categories
- `POST /api/v1/categories` - Create a new category
- `GET /api/v1/categories/:id` - Get a specific category
- `PUT /api/v1/categories/:id` - Update a specific category
- `DELETE /api/v1/categories/:id` - Delete a specific category

### Subcategory Endpoints
- `GET /api/v1/subcategories` - Get all subcategories
- `POST /api/v1/subcategories` - Create a new subcategory
- `GET /api/v1/subcategories/:id` - Get a specific subcategory
- `PUT /api/v1/subcategories/:id` - Update a specific subcategory
- `DELETE /api/v1/subcategories/:id` - Delete a specific subcategory
- `GET /api/v1/categories/:categoryId/subcategory` - Get subcategories for a specific category

### Brand Endpoints
- `GET /api/v1/brand` - Get all brands
- `POST /api/v1/brand` - Create a new brand
- `GET /api/v1/brand/:id` - Get a specific brand
- `PUT /api/v1/brand/:id` - Update a specific brand
- `DELETE /api/v1/brand/:id` - Delete a specific brand

### Product Endpoints
- `GET /api/v1/products` - Get all products
- `POST /api/v1/products` - Create a new product
- `GET /api/v1/products/:id` - Get a specific product
- `PUT /api/v1/products/:id` - Update a specific product
- `DELETE /api/v1/products/:id` - Delete a specific product

### Authentication Endpoints

- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/login` - Login a user
- `GET /api/auth/logout` - Logout a user

## Environment Variables

The application uses the following environment variables:

```
PORT=8000
NODE_ENV=development
HOST=0.0.0.0
DB_USERNAME=your_username
DB_PASSWORD=your_password
DB_URI=your_mongodb_connection_string
DB_NAME=your_database_name
```

## Project Structure

```
├── config/             # Configuration files
├── controllers/        # Request handlers
├── middlewares/        # Custom middleware functions
├── models/             # Mongoose models
├── routes/             # API routes
├── utils/              # Utility functions
├── uploads/            # Uploaded files
├── server.js           # Application entry point
└── package.json        # Project dependencies
```

## Features

- **RESTful API Design**: Follows REST principles for intuitive API design
- **MongoDB Integration**: Efficient data storage and retrieval
- **Image Processing**: Resize and optimize uploaded images
- **Data Validation**: Comprehensive request validation
- **Error Handling**: Consistent error responses
- **Environment Configuration**: Different settings for development and production

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.
