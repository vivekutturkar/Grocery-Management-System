# Quick Start Guide

## Getting Started in 3 Steps

### Step 1: Install Dependencies
```bash
npm install
```

### Step 2: Start the Server
```bash
npm start
```

The server will start on `http://localhost:3000`

### Step 3: Open in Browser
Navigate to `http://localhost:3000` and you'll see the Dashboard.

## Available Pages

1. **Dashboard** - `http://localhost:3000/dashboard`
   - Overview of key metrics
   - Low stock alerts
   - Sales performance charts

2. **Inventory** - `http://localhost:3000/inventory`
   - View all products
   - Manage inventory levels
   - Search and filter products

3. **Orders** - `http://localhost:3000/orders`
   - View all orders
   - Process orders
   - Update order status

4. **Product Details** - `http://localhost:3000/product/[product-id]`
   - Detailed product information
   - Sales history
   - Stock levels

5. **Reports** - `http://localhost:3000/reports`
   - Sales analytics
   - Top selling products
   - Revenue reports

## Sample Data

The system comes pre-loaded with sample data:
- Products (Organic Bananas, Apples, Milk, Bread, etc.)
- Sample orders
- Initial inventory levels

## Testing the System

1. **View Dashboard**: See overall statistics
2. **Check Inventory**: Browse products in the inventory page
3. **View Orders**: See sample orders and update their status
4. **View Product Details**: Click "View" on any product in inventory
5. **Generate Reports**: Check the reports page for analytics

## Troubleshooting

### Port Already in Use
If port 3000 is already in use, set a different port:
```bash
PORT=3001 npm start
```

### Database Issues
If you encounter database errors, delete `database/grocery.db` and restart the server. The database will be recreated with fresh sample data.

### Dependencies Not Installing
Make sure you have Node.js (v14 or higher) installed. Run:
```bash
node --version
```

If Node.js is not installed, download it from [nodejs.org](https://nodejs.org/)

## Next Steps

- Customize the product catalog
- Add your own products
- Create orders
- Generate custom reports

For more details, see the main [README.md](README.md) file.

