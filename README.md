# Report on E-commerce Application with Angular, NgRx, and .NET Microservices

## Introduction
This report details the development and implementation of a full-stack e-commerce application utilizing Angular, NgRx state management, and .NET Core microservices. The application is designed to provide a seamless shopping experience, including product browsing, order placement, and transaction history.

---

## Features
### Frontend (Angular)
- Product listing with the ability to add/remove items.
- Order placement functionality with NgRx state persistence.
- Implementation of loading states and error handling mechanisms.

### Backend (.NET Core Microservices)
- **Product Service**: Provides CRUD operations for managing products.
- **Order Service**: Handles order creation and order history retrieval.
- REST APIs built using Entity Framework Core and SQL Server for data management.

---

## Technologies Used
The project utilizes the following technologies:

| Component       | Stack                          |
|----------------|--------------------------------|
| **Frontend**   | Angular 16, NgRx, RxJS        |
| **Backend**    | .NET Core 7, EF Core, SQL Server |
| **Tools**      | Postman, Swagger, Azure CLI   |

---

## Installation and Setup
### Prerequisites
- Node.js v18+
- .NET Core SDK 7.0
- SQL Server
- Angular CLI: `npm install -g @angular/cli`

### Installation Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/ecommerce-app.git
   cd ecommerce-app
   ```
2. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   # Configure environment variables in `src/environments/environment.ts`
   ng serve
   ```
3. **Backend Setup**
   - **Product Service**
     ```bash
     cd backend/ProductService
     dotnet restore
     # Update SQL connection string in `appsettings.json`
     dotnet run
     ```
   - **Order Service**
     ```bash
     cd backend/OrderService
     dotnet restore
     # Update SQL connection string in `appsettings.json`
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
The application follows the standard NgRx state management flow:
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
Contributors can follow these steps to contribute:
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
This project is distributed under the MIT License. Refer to the LICENSE file for details.

---

## Acknowledgments
We appreciate the contributions from the development community and the resources provided by open-source platforms that made this project possible.

