# E-commerce Application with Angular, NgRx, and .NET Microservices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A full-stack e-commerce application demonstrating **NgRx state management** (Angular) and **microservices architecture** (.NET Core).

---

## Features
- **Frontend (Angular)**:
  - Product listing, add/remove items
  - Order placement with NgRx state persistence
  - Loading states and error handling
- **Backend (.NET Core Microservices)**:
  - **Product Service**: CRUD operations for products
  - **Order Service**: Order creation and history
  - REST APIs with Entity Framework Core + SQL Server


---

## Technologies
| Component       | Stack                          |
|-----------------|--------------------------------|
| **Frontend**    | Angular 16, NgRx, RxJS         |
| **Backend**     | .NET Core 7, EF Core, SQL Server |
| **Tools**       | Postman, Swagger, Azure CLI    |

---

## Installation

### Prerequisites
- Node.js v18+
- .NET Core SDK 7.0
- SQL Server
- Angular CLI: `npm install -g @angular/cli`

### Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/ecommerce-app.git
   cd ecommerce-app

    Frontend Setup:
    bash
    Copy

    cd frontend
    npm install
    # Configure environment variables in `src/environments/environment.ts`
    ng serve

    Backend Setup:

        Product Service:
        bash
        Copy

        cd backend/ProductService
        dotnet restore
        # Update SQL connection string in `appsettings.json`
        dotnet run

        Order Service:
        bash
        Copy

        cd backend/OrderService
        dotnet restore
        # Update SQL connection string in `appsettings.json`
        dotnet run

API Endpoints
Product Microservice
Endpoint	Method	Description
/api/products	GET	Fetch all products
/api/products	POST	Add a product
/api/products/{id}	DELETE	Delete a product
Order Microservice
Endpoint	Method	Description
/api/orders	POST	Place a new order
/api/orders/{userId}	GET	Fetch order history
NgRx State Management Flow
plaintext
Copy

UI Component → Action → Reducer → Store → Selector → UI Update
                          ↓
                  Effect (HTTP Call → Microservice)


Project Structure
Copy

├── frontend/               # Angular app
│   ├── src/app/
│   │   ├── store/          # NgRx setup (actions, reducers, effects)
│   │   ├── features/       # Product/Order modules
│   │   └── services/       # HTTP services
│
├── OrderService/   # .NET Core order microservice
│── ProductService/   # .NET Core product microservice
│   
│
└── docs/                   # Swagger

Contributing

    Fork the repository.

    Create a feature branch: git checkout -b feature/your-feature.

    Commit changes: git commit -m 'Add your feature'.

    Push to the branch: git push origin feature/your-feature.

    Submit a pull request.

License

Distributed under the MIT License. See LICENSE for details.
Acknowledgments
