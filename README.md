# E-commerce Application with Angular, NgRx, and .NET Microservices

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A full-stack e-commerce application demonstrating **NgRx state management** with Angular and **microservices architecture** using .NET Core.

---

## Features
### Frontend (Angular)
- Product listing with add/remove items functionality.
- Order placement with NgRx state persistence.
- Loading states and error handling implementation.

### Backend (.NET Core Microservices)
- **Product Service**: Handles CRUD operations for products.
- **Order Service**: Manages order creation and history.
- REST APIs using Entity Framework Core and SQL Server.

---

## Technologies Used

| Component       | Stack                          |
|----------------|--------------------------------|
| **Frontend**   | Angular 16, NgRx, RxJS        |
| **Backend**    | .NET Core 7, EF Core, SQL Server |
| **Tools**      | Postman, Swagger, Azure CLI   |

---

## Installation
### Prerequisites
- Node.js v18+
- .NET Core SDK 7.0
- SQL Server
- Angular CLI: `npm install -g @angular/cli`

### Setup Instructions
1. **Clone the Repository**
   ```bash
   git clone https://github.com/ecommerce-app.git
   cd ecommerce-app
   ```
2. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   ng serve
   ```
3. **Backend Setup**
   - **Product Service**
     ```bash
     cd backend/ProductService
     dotnet restore
     dotnet run
     ```
   - **Order Service**
     ```bash
     cd backend/OrderService
     dotnet restore
     dotnet run
     ```

---

## API Endpoints
### Product Microservice
| Endpoint        | Method | Description          |
|----------------|--------|----------------------|
| `/api/products` | GET    | Fetch all products  |
| `/api/products` | POST   | Add a product       |
| `/api/products/{id}` | DELETE | Delete a product |

### Order Microservice
| Endpoint        | Method | Description           |
|----------------|--------|-----------------------|
| `/api/orders`  | POST   | Place a new order     |
| `/api/orders/{userId}` | GET | Fetch order history |

---

## NgRx State Management Flow
```
UI Component → Action → Reducer → Store → Selector → UI Update
                          ↓
                  Effect (HTTP Call → Microservice)
```

---

## Project Structure
```
├── frontend/               # Angular application
│   ├── src/app/
│   │   ├── store/          # NgRx setup (actions, reducers, effects)
│   │   ├── features/       # Product/Order modules
│   │   └── services/       # HTTP services
│
├── OrderService/           # .NET Core order microservice
├── ProductService/         # .NET Core product microservice
│
└── docs/                   # API documentation using Swagger
```

---

## Contribution Guidelines
1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit changes:
   ```bash
   git commit -m 'Add your feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Submit a pull request for review.

---

## License
Distributed under the MIT License. See LICENSE for details.

---

## Acknowledgments
Special thanks to the open-source community for their valuable contributions.
