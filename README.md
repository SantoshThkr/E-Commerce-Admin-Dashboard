# E-Commerce Admin Dashboard

A small admin dashboard for managing products, orders and customers.

## Features

* Dashboard with sales, orders, products and customer stats
* Product management
* Search products by name
* Filter products by category
* Automatic stock status
* Order list with status updates
* Customer list
* Product form validation
* Loading and error states
* Responsive layout

## Tech Stack

**Frontend**

* React
* JavaScript
* Axios
* React Router
* CSS

**Backend**

* Node.js
* Express
* MongoDB
* Mongoose

**Testing**

* Jest
* React Testing Library

## Setup

Make sure Node.js and MongoDB are installed.

Install dependencies:

```bash
cd server
npm install

cd ../client
npm install
```

Seed sample data:

```bash
cd server
npm run seed
```

By default, the server uses:

```text
mongodb://127.0.0.1:27017/ecommerce-admin
```

You can change the database with `MONGO_URI` and the API port with `PORT`.

## Run

Start the API:

```bash
cd server
npm start
```

Start the React app in another terminal:

```bash
cd client
npm start
```

Open `http://localhost:3000`.

## API

| Method | Endpoint            | Description                       |
| ------ | ------------------- | --------------------------------- |
| GET    | `/api/dashboard`    | Dashboard stats and recent orders |
| GET    | `/api/products`     | List products                     |
| POST   | `/api/products`     | Create product                    |
| PUT    | `/api/products/:id` | Update product                    |
| DELETE | `/api/products/:id` | Delete product                    |
| GET    | `/api/orders`       | List orders                       |
| PUT    | `/api/orders/:id`   | Update order status               |
| GET    | `/api/customers`    | List customers                    |

## Project Structure

```text
client/
└── src/
    ├── components/
    ├── pages/
    ├── services/
    ├── styles/
    └── App.js

server/
├── models/
├── routes/
├── seed.js
└── server.js
```

## Notes

Stock status is based on the current stock level:

```text
0       → Out of Stock
1–4     → Low Stock
5+      → Active
```

Dashboard sales include all orders except cancelled orders.

## Test

```bash
cd client
npm test
```
