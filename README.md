# Small Business Order and Invoice Management System

A web-based **Order and Invoice Management System** developed to help small businesses manage products, customers, orders, invoices, and sales operations efficiently.

This project is developed as part of the **CT-365 Software Engineering – Complex Computing Problem (CCP), Topic 7**.

## Project Overview

The system provides a simple and user-friendly interface for managing daily business activities. It helps organize product records, process customer orders, manage invoices, and monitor business performance through a dashboard.

## Features

- **User Authentication:** Secure login using password hashing and JWT authentication.
- **Role-Based Access:** Different access permissions for administrators and sales staff.
- **Dashboard:** View business statistics and order information.
- **Product Management:** Add, view, update, and manage products.
- **Order Management:** Create and manage customer orders.
- **Inventory Management:** Automatically update product stock when orders are placed.
- **Invoice Management:** Generate and manage invoices.
- **PDF Generation:** Generate downloadable PDF invoices.
- **User Management:** Manage system users.
- **Input Validation:** Validate incoming data before processing.
- **Database Management:** Store business information using SQLite.

## Technologies Used

| Technology | Purpose |
|---|---|
| Node.js | Backend runtime |
| Express.js | Web application framework |
| SQLite | Database |
| HTML5 | Frontend structure |
| CSS3 | Frontend styling |
| JavaScript | Frontend functionality |
| JWT | Authentication |
| bcryptjs | Password hashing |
| PDFKit | PDF invoice generation |
| Jest | Testing |
| Supertest | API testing |

## Project Structure

```text
Order-Invoice-Management-System/
│
├── db/
│   ├── database.js
│   ├── schema.sql
│   └── seed.js
│
├── middleware/
│   ├── auth.js
│   ├── requireRole.js
│   └── validate.js
│
├── routes/
│   ├── auth.routes.js
│   ├── dashboard.routes.js
│   ├── invoices.routes.js
│   ├── orders.routes.js
│   ├── products.routes.js
│   └── users.routes.js
│
├── services/
│   ├── calc.js
│   ├── invoice.service.js
│   ├── order.service.js
│   └── pdf.service.js
│
├── public/
│   ├── css/
│   ├── js/
│   ├── dashboard.html
│   ├── login.html
│   ├── new-order.html
│   ├── orders.html
│   ├── products.html
│   ├── users.html
│   └── invoice.html
│
├── tests/
│   └── api.test.js
│
├── app.js
├── server.js
├── package.json
├── .env.example
└── README.md
```

## Installation and Setup

### Prerequisites

- Node.js 22.13 or newer
- npm
- Git (optional)

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the Project Folder

```bash
cd Order-Invoice-Management-System
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a `.env` file using `.env.example`.

On Windows PowerShell:

```powershell
copy .env.example .env
```

Configure your environment variables and use a strong, private JWT secret.

### 5. Start the Application

```bash
npm start
```

The application will run on:

```text
http://localhost:3000
```

## Demo Login Credentials

| Username | Password | Role |
|---|---|---|
| admin | Admin@123 | Administrator |
| sales1 | Staff@123 | Sales Staff |

**Important:** These are demonstration credentials. Change or remove them before making the application publicly accessible.

## Database and Inventory Management

The application uses SQLite to store business records.

When an order is placed, product stock is updated through a database transaction. If sufficient stock is unavailable, the transaction is rolled back to prevent incorrect inventory records.

## Running Tests

To execute the automated test suite:

```bash
npm test
```

The project includes 51 integration and unit tests covering application functionality.

## Online Deployment

The application is prepared for cloud deployment using Railway.

Deployment requirements:

- GitHub repository containing the project.
- Railway account.
- Persistent storage volume for the SQLite database.
- A secure JWT secret.
- Environment variables configured in the hosting dashboard.

For cloud deployment, configure:

```env
JWT_SECRET=your_strong_secret
DB_PATH=/data/database.db
TAX_RATE=18
```

Mount a persistent volume at `/data` to preserve database records across deployments and restarts.

After successful deployment, generate a public domain through the hosting provider.

## Future Improvements

- Advanced sales reports and analytics.
- Customer management improvements.
- Inventory alerts for low stock.
- Email notifications.
- Advanced invoice customization.
- Additional security improvements.

## Academic Information

**Course:** CT-365 Software Engineering  
**Project:** Complex Computing Problem (CCP)  
**Project Title:** Small Business Order and Invoice Management System  
**Department:** Computer Science & Information Technology  
**Institute:** Thar Institute of Engineering, Sciences and Technology (TIEST), Constituent College of NED University of Engineering & Technology.

## License

This project is developed for academic and educational purposes.
