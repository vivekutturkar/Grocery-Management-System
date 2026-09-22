# Grocery Management System

A comprehensive grocery management system with a modern web interface for managing inventory, orders, products, and generating reports.

## Features

- **Dashboard Overview**: View key metrics including total sales, items in stock, low stock alerts, and top selling items
- **Inventory Management**: Manage product inventory with categories, stock levels, and pricing
- **Order Processing**: Process and manage customer orders with status tracking
- **Product Details**: View detailed information about individual products including sales history
- **Reports & Analytics**: Generate sales reports and view analytics

## Technology Stack

- **Frontend**: HTML5, Tailwind CSS, Vanilla JavaScript
- **Backend**: Node.js, Express.js
- **Database**: SQLite3

## Project Structure

```
grocery-management-system/
├── public/
│   ├── dashboard.html          # Dashboard page
│   ├── inventory.html          # Inventory management page
│   ├── orders.html             # Order processing page
│   ├── product-details.html    # Product details page
│   ├── reports.html            # Reports & analytics page
│   └── js/
│       ├── dashboard.js        # Dashboard JavaScript
│       ├── inventory.js        # Inventory JavaScript
│       ├── orders.js           # Orders JavaScript
│       ├── product-details.js  # Product details JavaScript
│       └── reports.js          # Reports JavaScript
├── routes/
│   ├── dashboard.js            # Dashboard API routes
│   ├── inventory.js            # Inventory API routes
│   ├── orders.js               # Orders API routes
│   ├── products.js             # Products API routes
│   └── reports.js              # Reports API routes
├── database/
│   ├── init.js                 # Database initialization
│   └── grocery.db              # SQLite database (created on first run)
├── server.js                   # Main server file
├── package.json                # Dependencies
└── README.md                   # This file
```

## Installation

1. **Clone or download the project**

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the server**
   ```bash
   npm start
   ```
   For development with auto-reload:
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

## Usage

### Dashboard
- View overall statistics and key metrics
- Monitor low stock alerts
- See top selling items

### Inventory Management
- View all products in a table format
- Search and filter products
- Add new products (UI ready, functionality to be implemented)
- Edit existing products

### Order Processing
- View all orders with status filters
- Search orders by order number or customer name
- View detailed order information
- Update order status (pending → in progress → completed)
- Cancel orders

### Product Details
- View comprehensive product information
- See stock levels, pricing, and margins
- View sales history and stock levels
- Access supplier information

### Reports & Analytics
- View total sales, profit margin, transactions
- See average basket size
- View top selling products
- Export reports (UI ready)

## API Endpoints

### Dashboard
- `GET /api/dashboard/stats` - Get dashboard statistics
- `GET /api/dashboard/low-stock` - Get low stock items

### Inventory
- `GET /api/inventory` - Get all products
- `GET /api/inventory/:id` - Get single product
- `GET /api/inventory/low-stock` - Get low stock items
- `POST /api/inventory` - Create new product
- `PUT /api/inventory/:id` - Update product
- `DELETE /api/inventory/:id` - Delete product

### Orders
- `GET /api/orders` - Get all orders
- `GET /api/orders/:id` - Get single order with items
- `POST /api/orders` - Create new order
- `PUT /api/orders/:id/status` - Update order status
- `DELETE /api/orders/:id` - Cancel order

### Products
- `GET /api/products/:id` - Get product details with sales history

### Reports
- `GET /api/reports/sales` - Get sales report
- `GET /api/reports/top-products` - Get top selling products

## Database Schema

The system uses SQLite with the following tables:

- **products**: Product information, inventory, pricing
- **orders**: Order headers with customer information
- **order_items**: Order line items
- **suppliers**: Supplier information
- **sales_history**: Sales transaction history

## Development

### Adding New Features

1. Create route handlers in `routes/` directory
2. Update database schema if needed in `database/init.js`
3. Add frontend pages in `public/` directory
4. Create corresponding JavaScript files in `public/js/`

### Database

The database is automatically initialized on first server start. Sample data is seeded for testing.

To reset the database, delete `database/grocery.db` and restart the server.

## Future Enhancements

- User authentication and authorization
- Supplier management
- Barcode scanning
- Email notifications for low stock
- Advanced reporting with charts
- Multi-store support
- Purchase order management

## License

MIT License - feel free to use this project for learning or commercial purposes.

## Support

For issues or questions, please create an issue in the project repository.

