☑️ Product Inventory API

A RESTful API for managing product inventory built with Node.js, Express, and MongoDB.

☑️ Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- CORS
- dotenv

☑️ Installation

```bash
# Clone the repository
git clone https://github.com/hetdabhi/fullstack-product-app.git

# Navigate to project directory
cd fullstack-product-app

# Install dependencies
npm install
```

☑️ Environment Setup 
Create a  .env  file in the root directory:
```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/productDB
```

☑️ Running the Application
```
# Development mode
npm run dev

# Production mode
npm start
```
☑️  API Endpoints
Products
| **Method** | **Endpoint**            | **Description**           |
| :--------- | :---------------------- | :------------------------ |
| GET        | `/api/products`         | Get all products          |
| POST       | `/api/products`         | Create new product        |
| GET        | `/api/products/:id`     | Get product by ID         |
| PUT        | `/api/products/:id`     | Update product            |
| DELETE     | `/api/products/:id`     | Delete product            |

☑️ Product Model
```
{
  productName: String,    // required
  description: String,    // required
  category: String,       // required, enum: ['Mobile', 'Laptop', 'Tablet']
  quantity: Number,       // required, min: 0
  price: Number,         // required, min: 0
  timestamps: true       // createdAt, updatedAt
}
```
☑️ Example API Requests
### Create Product
```
POST /api/products
Content-Type: application/json

{
  "productName": "iPhone 15 Pro Max",
  "description": "Latest iPhone model",
  "category": "Mobile",
  "quantity": 50,
  "price": 999.99
}
```
### Get All Products
```
GET /api/products
```
## Error Handling
The API returns appropriate HTTP status codes and error messages:
-   200: Success
-   201: Created
-   400: Bad Request
-   404: Not Found
-   500: Server Error

## Directory Structure
```
fullstack-product-app/
├── backend
      ├── config.js
      ├── server.js
      ├── package.json
      ├── .env
      ├── controllers/
      │   └── productControllers.js
      ├── models/
      │   └── productModels.js
      └── routes/
          └── productRoutes.js
```
## Author
Het Dabhi

GitHub: [hetdabhi](https://github.com/hetdabhi)
<br>
Email: hetdabhiengineer@gmail.com
