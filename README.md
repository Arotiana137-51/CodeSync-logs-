# 🚀 TypeScript Microservices Architecture

Enterprise-grade microservices template built with TypeScript, Node.js, Express, and modern tooling. Features clean architecture, event-driven communication, and full observability.

![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)
![Node](https://img.shields.io/badge/Node.js-20.x-green)
![Express](https://img.shields.io/badge/Express-4.x-lightgrey)
![Jest](https://img.shields.io/badge/Jest-29.x-red)

## ✨ Core Features

- 💪 100% TypeScript with strict mode
- 🎯 Domain-Driven Design (DDD) principles
- 🔄 Event-driven architecture using RabbitMQ
- 🔍 OpenAPI/Swagger documentation
- 📊 Structured logging with ******
- 🧪 Comprehensive testing setup
- 🔒 Built-in security features
- 📈 Prometheus metrics & tracing

## 🏗 Project Structure

```
├── services/
│   ├── user-service/
│   ├── product-service/
│   ├── order-service/
│   └── notification-service/
├── libs/
│   ├── common/
│   ├── event-bus/
│   └── testing/
└── tools/
    ├── generators/
    └── scripts/
```

Each service follows clean architecture:
```
service/
├── src/
│   ├── domain/          # Business entities & logic
│   ├── application/     # Use cases & ports
│   ├── infrastructure/  # External implementations
│   ├── interfaces/      # Controllers & DTOs
│   └── main.ts         # Service entry point
├── test/
│   ├── unit/
│   ├── integration/
│   └── e2e/
└── package.json
```

## 🛠 Tech Stack

- **Runtime:** Node.js 20+
- **Language:** TypeScript 5
- **Framework:** Express with routing-controllers
- **Database:** TypeORM with PostgreSQL
- **Messaging:** RabbitMQ with TypeScript events
- **Validation:** class-validator & class-transformer
- **Testing:** Jest, Supertest
- **Documentation:** TypeDoc, Swagger
- **Monitoring:** Prometheus, OpenTelemetry
- **DevOps:** Docker, Docker Compose

## 🚀 Quick Start

1. **Clone and Install**
```bash
git clone https://github.com/your-username/ts-microservices.git
cd ts-microservices
npm install
```

2. **Environment Setup**
```bash
cp .env.example .env
# Configure your environment variables
```

3. **Start Development Environment**
```bash
# Start infrastructure
docker-compose up -d

# Start all services in development mode
npm run dev
```

## 📦 Available Services

### User Service (Port 3001)
```typescript
// Example user entity
interface User {
  id: string;
  email: string;
  profile: UserProfile;
  roles: UserRole[];
}
```

### Product Service (Port 3002)
```typescript
// Example product entity
interface Product {
  id: string;
  name: string;
  price: Money;
  inventory: Inventory;
}
```

### Order Service (Port 3003)
```typescript
// Example order entity
interface Order {
  id: string;
  userId: string;
  items: OrderItem[];
  status: OrderStatus;
}
```

## 🔧 Development

### Service Generation
```bash
npm run generate:service -- --name=new-service
```

### Type Safety
```bash
# Run type checking
npm run type-check

# Generate types from OpenAPI
npm run generate:types
```

### Testing
```bash
# Unit tests
npm run test

# Integration tests
npm run test:integration

# E2E tests
npm run test:e2e

# Test coverage
npm run test:coverage
```

## 📊 Event Flow

```mermaid
graph LR
    A[User Service] -->|UserCreated| B[Notification]
    C[Order Service] -->|OrderPlaced| B
    C -->|InventoryCheck| D[Product Service]
```

## 🔒 Security Features

- JWT authentication
- Request validation
- Rate limiting
- CORS configuration
- Helmet security headers
- SQL injection prevention

## 📈 Monitoring

### Metrics
```typescript
// Example metric collection
@Metrics()
class OrderService {
  @Counter('orders_total')
  async createOrder() {
    // Implementation
  }
}
```

### Logging
```typescript
// Structured logging
logger.info('Order created', {
  orderId: order.id,
  userId: order.userId,
  amount: order.total
});
```

## 🚢 Deployment

### Docker
```bash
# Build all services
docker-compose build

# Run production mode
docker-compose -f docker-compose.prod.yml up -d
```

### Kubernetes
```bash
# Apply configurations
kubectl apply -f k8s/

# Verify deployment
kubectl get pods
```

## 👥 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing`)
3. Run tests (`npm run test`)
4. Commit changes (`git commit -m 'Add feature'`)
5. Push to branch (`git push origin feature/amazing`)
6. Open a Pull Request

### Coding Standards

```json
{
  "extends": [
    "airbnb-typescript/base",
    "plugin:@typescript-eslint/recommended",
    "prettier"
  ],
  "rules": {
    "@typescript-eslint/explicit-function-return-type": "error",
    "@typescript-eslint/no-explicit-any": "error"
  }
}
```

## 📚 API Documentation

- REST API docs: `http://localhost:3000/api-docs`
- TypeDoc: `http://localhost:3000/docs`

## 📄 License

MIT © [Your Name]

---

Built with TypeScript 💙<<<<<<< HEAD
Contribution: 2023-12-09 20:00

Contribution: 2023-12-09 20:01

Contribution: 2023-12-09 20:02

Contribution: 2023-12-11 20:00

Contribution: 2023-12-11 20:01

Contribution: 2023-12-11 20:02

Contribution: 2023-12-11 20:03

Contribution: 2023-12-11 20:04

Contribution: 2023-12-11 20:05

Contribution: 2023-12-15 20:00

Contribution: 2023-12-15 20:01

Contribution: 2023-12-15 20:02

Contribution: 2023-12-15 20:03

Contribution: 2023-12-17 20:00

Contribution: 2023-12-17 20:01

Contribution: 2023-12-18 20:00

Contribution: 2023-12-18 20:01

Contribution: 2023-12-18 20:02

Contribution: 2023-12-18 20:03

Contribution: 2023-12-20 20:00

Contribution: 2023-12-20 20:01

Contribution: 2023-12-21 20:00

Contribution: 2023-12-21 20:01

Contribution: 2023-12-21 20:02

Contribution: 2023-12-21 20:03

Contribution: 2023-12-21 20:04

Contribution: 2023-12-21 20:05

Contribution: 2023-12-24 20:00

Contribution: 2023-12-24 20:01

Contribution: 2023-12-24 20:02

Contribution: 2023-12-24 20:03

Contribution: 2023-12-24 20:04

Contribution: 2023-12-26 20:00

Contribution: 2023-12-26 20:01

Contribution: 2023-12-28 20:00

Contribution: 2023-12-28 20:01

Contribution: 2023-12-28 20:02

Contribution: 2023-12-28 20:03

Contribution: 2023-12-28 20:04

Contribution: 2023-12-28 20:05

Contribution: 2024-01-06 20:00

Contribution: 2024-01-06 20:01

Contribution: 2024-01-06 20:02

Contribution: 2024-01-06 20:03

Contribution: 2024-01-06 20:04

Contribution: 2024-01-09 20:00

Contribution: 2024-01-09 20:01

Contribution: 2024-01-09 20:02

Contribution: 2024-01-09 20:03

Contribution: 2024-01-09 20:04

Contribution: 2024-01-15 20:00

Contribution: 2024-01-15 20:01

Contribution: 2024-01-15 20:02

Contribution: 2024-01-15 20:03

Contribution: 2024-01-15 20:04

Contribution: 2024-01-19 20:00

Contribution: 2024-01-19 20:01

Contribution: 2024-01-19 20:02

Contribution: 2024-01-19 20:03

Contribution: 2024-01-19 20:04

Contribution: 2024-01-19 20:05

Contribution: 2024-01-20 20:00

Contribution: 2024-01-20 20:01

Contribution: 2024-01-20 20:02

Contribution: 2024-01-20 20:03

Contribution: 2024-01-20 20:04

Contribution: 2024-01-20 20:05

Contribution: 2024-01-21 20:00

Contribution: 2024-01-23 20:00

Contribution: 2024-01-23 20:01

Contribution: 2024-01-23 20:02

Contribution: 2024-01-23 20:03

Contribution: 2024-01-23 20:04

Contribution: 2024-01-23 20:05

Contribution: 2024-01-23 20:06

Contribution: 2024-02-03 20:00

Contribution: 2024-02-03 20:01

Contribution: 2024-02-03 20:02

Contribution: 2024-02-03 20:03

Contribution: 2024-02-05 20:00

Contribution: 2024-02-09 20:00

Contribution: 2024-02-09 20:01

Contribution: 2024-02-09 20:02

Contribution: 2024-02-09 20:03

Contribution: 2024-02-11 20:00

Contribution: 2024-02-11 20:01

Contribution: 2024-02-16 20:00

Contribution: 2024-02-16 20:01

Contribution: 2024-02-21 20:00

Contribution: 2024-02-21 20:01

Contribution: 2024-02-22 20:00

Contribution: 2024-02-22 20:01

Contribution: 2024-02-24 20:00

Contribution: 2024-02-24 20:01

Contribution: 2024-02-24 20:02

Contribution: 2024-02-24 20:03

Contribution: 2024-02-27 20:00

Contribution: 2024-02-27 20:01

Contribution: 2024-03-01 20:00

Contribution: 2024-03-01 20:01

Contribution: 2024-03-02 20:00

Contribution: 2024-03-02 20:01

Contribution: 2024-03-07 20:00

Contribution: 2024-03-07 20:01

Contribution: 2024-03-07 20:02

Contribution: 2024-03-07 20:03

Contribution: 2024-03-07 20:04

Contribution: 2024-03-07 20:05

Contribution: 2024-03-07 20:06

Contribution: 2024-03-08 20:00

Contribution: 2024-03-08 20:01

Contribution: 2024-03-08 20:02

Contribution: 2024-03-08 20:03

Contribution: 2024-03-13 20:00

Contribution: 2024-03-13 20:01

Contribution: 2024-03-13 20:02

Contribution: 2024-03-14 20:00

Contribution: 2024-03-15 20:00

Contribution: 2024-03-15 20:01

Contribution: 2024-03-15 20:02

Contribution: 2024-03-15 20:03

Contribution: 2024-03-15 20:04

Contribution: 2024-03-15 20:05

Contribution: 2024-03-15 20:06

Contribution: 2024-04-05 20:00

Contribution: 2024-04-05 20:01

Contribution: 2024-04-05 20:02

Contribution: 2024-04-05 20:03

Contribution: 2024-04-16 20:00

Contribution: 2024-04-16 20:01

Contribution: 2024-04-16 20:02

Contribution: 2024-04-16 20:03

Contribution: 2024-04-20 20:00

Contribution: 2024-04-20 20:01

Contribution: 2024-04-20 20:02

Contribution: 2024-04-20 20:03

Contribution: 2024-04-20 20:04

Contribution: 2024-04-20 20:05

Contribution: 2024-04-20 20:06

Contribution: 2024-05-02 20:00

Contribution: 2024-05-04 20:00

Contribution: 2024-05-04 20:01

Contribution: 2024-05-04 20:02

Contribution: 2024-05-04 20:03

Contribution: 2024-05-04 20:04

Contribution: 2024-05-07 20:00

Contribution: 2024-05-07 20:01

Contribution: 2024-05-07 20:02

Contribution: 2024-05-07 20:03

Contribution: 2024-05-07 20:04

Contribution: 2024-05-07 20:05

Contribution: 2024-05-07 20:06

Contribution: 2024-05-12 20:00

Contribution: 2024-05-12 20:01

Contribution: 2024-05-12 20:02

Contribution: 2024-05-12 20:03

Contribution: 2024-05-12 20:04

Contribution: 2024-05-12 20:05

Contribution: 2024-05-12 20:06

Contribution: 2024-05-13 20:00

Contribution: 2024-05-13 20:01

Contribution: 2024-05-13 20:02

Contribution: 2024-05-13 20:03

Contribution: 2024-05-13 20:04

Contribution: 2024-05-17 20:00

Contribution: 2024-05-17 20:01

Contribution: 2024-05-17 20:02

Contribution: 2024-05-17 20:03

Contribution: 2024-05-25 20:00

Contribution: 2024-05-25 20:01

Contribution: 2024-05-27 20:00

Contribution: 2024-05-27 20:01

Contribution: 2024-05-27 20:02

Contribution: 2024-05-27 20:03

Contribution: 2024-05-27 20:04

Contribution: 2024-05-27 20:05

Contribution: 2024-06-03 20:00

Contribution: 2024-06-03 20:01

Contribution: 2024-06-03 20:02

Contribution: 2024-06-03 20:03

Contribution: 2024-06-03 20:04

Contribution: 2024-06-03 20:05

Contribution: 2024-06-03 20:06

Contribution: 2024-06-04 20:00

Contribution: 2024-06-04 20:01

Contribution: 2024-06-04 20:02

Contribution: 2024-06-04 20:03

Contribution: 2024-06-04 20:04

Contribution: 2024-06-07 20:00

Contribution: 2024-06-07 20:01

Contribution: 2024-06-12 20:00

Contribution: 2024-06-12 20:01

Contribution: 2024-06-15 20:00

Contribution: 2024-06-16 20:00

Contribution: 2024-06-16 20:01

Contribution: 2024-06-16 20:02

Contribution: 2024-06-17 20:00

Contribution: 2024-06-17 20:01

Contribution: 2024-06-17 20:02

Contribution: 2024-07-03 20:00

Contribution: 2024-07-03 20:01

Contribution: 2024-07-03 20:02

Contribution: 2024-07-03 20:03

Contribution: 2024-07-03 20:04

Contribution: 2024-07-03 20:05

Contribution: 2024-07-03 20:06

Contribution: 2024-07-04 20:00

Contribution: 2024-07-04 20:01

Contribution: 2024-07-04 20:02

Contribution: 2024-07-04 20:03

Contribution: 2024-07-07 20:00

Contribution: 2024-07-07 20:01

Contribution: 2024-07-07 20:02

Contribution: 2024-07-07 20:03

Contribution: 2024-07-09 20:00

Contribution: 2024-07-09 20:01

Contribution: 2024-07-12 20:00

Contribution: 2024-07-12 20:01

Contribution: 2024-07-12 20:02

Contribution: 2024-07-12 20:03

Contribution: 2024-07-12 20:04

Contribution: 2024-07-12 20:05

Contribution: 2024-07-12 20:06

Contribution: 2024-07-17 20:00

Contribution: 2024-07-17 20:01

Contribution: 2024-07-17 20:02

Contribution: 2024-07-17 20:03

Contribution: 2024-07-17 20:04

Contribution: 2024-07-18 20:00

Contribution: 2024-07-18 20:01

Contribution: 2024-07-18 20:02

Contribution: 2024-07-18 20:03

Contribution: 2024-07-18 20:04

Contribution: 2024-07-18 20:05

Contribution: 2024-07-18 20:06

Contribution: 2024-07-19 20:00

Contribution: 2024-07-19 20:01

Contribution: 2024-07-19 20:02

Contribution: 2024-07-21 20:00

Contribution: 2024-07-24 20:00

Contribution: 2024-07-24 20:01

Contribution: 2024-07-24 20:02

Contribution: 2024-07-24 20:03

Contribution: 2024-07-24 20:04

Contribution: 2024-07-24 20:05

Contribution: 2024-07-24 20:06

Contribution: 2024-07-26 20:00

Contribution: 2024-07-26 20:01

Contribution: 2024-07-26 20:02

Contribution: 2024-08-01 20:00

Contribution: 2024-08-01 20:01

Contribution: 2024-08-01 20:02

Contribution: 2024-08-04 20:00

Contribution: 2024-08-08 20:00

Contribution: 2024-08-08 20:01

Contribution: 2024-08-08 20:02

Contribution: 2024-08-08 20:03

Contribution: 2024-08-12 20:00

Contribution: 2024-08-12 20:01

Contribution: 2024-08-12 20:02

Contribution: 2024-08-12 20:03

Contribution: 2024-08-12 20:04

Contribution: 2024-08-12 20:05

Contribution: 2024-08-13 20:00

Contribution: 2024-08-13 20:01

Contribution: 2024-08-13 20:02

Contribution: 2024-08-16 20:00

Contribution: 2024-08-16 20:01

Contribution: 2024-08-16 20:02

Contribution: 2024-08-16 20:03

Contribution: 2024-08-16 20:04

Contribution: 2024-08-18 20:00

Contribution: 2024-08-18 20:01

Contribution: 2024-08-18 20:02

Contribution: 2024-08-18 20:03

Contribution: 2024-08-18 20:04

Contribution: 2024-08-19 20:00

Contribution: 2024-08-19 20:01

Contribution: 2024-08-19 20:02

Contribution: 2024-08-20 20:00

Contribution: 2024-08-20 20:01

Contribution: 2024-08-20 20:02

Contribution: 2024-08-24 20:00

Contribution: 2024-08-24 20:01

Contribution: 2024-08-25 20:00

Contribution: 2024-08-26 20:00

Contribution: 2024-08-26 20:01

Contribution: 2024-08-26 20:02

Contribution: 2024-08-26 20:03

Contribution: 2024-08-29 20:00

Contribution: 2024-08-29 20:01

Contribution: 2024-08-29 20:02

Contribution: 2024-08-31 20:00

Contribution: 2024-08-31 20:01

Contribution: 2024-09-04 20:00

Contribution: 2024-09-05 20:00

Contribution: 2024-09-05 20:01

Contribution: 2024-09-05 20:02

Contribution: 2024-09-09 20:00

Contribution: 2024-09-09 20:01

Contribution: 2024-09-09 20:02

Contribution: 2024-09-09 20:03

Contribution: 2024-09-09 20:04

Contribution: 2024-09-14 20:00

Contribution: 2024-09-18 20:00

Contribution: 2024-09-18 20:01

Contribution: 2024-09-22 20:00

Contribution: 2024-09-22 20:01

Contribution: 2024-09-28 20:00

Contribution: 2024-09-28 20:01

Contribution: 2024-09-30 20:00

Contribution: 2024-09-30 20:01

Contribution: 2024-10-06 20:00

Contribution: 2024-10-06 20:01

Contribution: 2024-10-06 20:02

Contribution: 2024-10-11 20:00

Contribution: 2024-10-11 20:01

Contribution: 2024-10-11 20:02

Contribution: 2024-10-11 20:03

Contribution: 2024-10-11 20:04

Contribution: 2024-10-13 20:00

Contribution: 2024-10-13 20:01

Contribution: 2024-10-13 20:02

Contribution: 2024-10-14 20:00

Contribution: 2024-10-14 20:01

Contribution: 2024-10-14 20:02

Contribution: 2024-10-14 20:03

Contribution: 2024-10-14 20:04

Contribution: 2024-10-14 20:05

Contribution: 2024-10-14 20:06

Contribution: 2024-10-15 20:00

Contribution: 2024-10-15 20:01

Contribution: 2024-10-15 20:02

Contribution: 2024-10-20 20:00

Contribution: 2024-10-20 20:01

Contribution: 2024-10-20 20:02

Contribution: 2024-10-20 20:03

Contribution: 2024-10-20 20:04

Contribution: 2024-10-20 20:05

Contribution: 2024-10-21 20:00

Contribution: 2024-10-21 20:01

Contribution: 2024-10-21 20:02

Contribution: 2024-10-21 20:03

Contribution: 2024-10-21 20:04

Contribution: 2024-10-21 20:05

Contribution: 2024-10-24 20:00

Contribution: 2024-10-24 20:01

Contribution: 2024-10-31 20:00

Contribution: 2024-10-31 20:01

Contribution: 2024-10-31 20:02

Contribution: 2024-10-31 20:03

Contribution: 2024-11-01 20:00

Contribution: 2024-11-03 20:00

Contribution: 2024-11-05 20:00

Contribution: 2024-11-05 20:01

Contribution: 2024-11-05 20:02

Contribution: 2024-11-05 20:03

Contribution: 2024-11-05 20:04

Contribution: 2024-11-05 20:05

Contribution: 2024-11-05 20:06

Contribution: 2024-11-08 20:00

Contribution: 2024-11-08 20:01

Contribution: 2024-11-08 20:02

Contribution: 2024-11-08 20:03

Contribution: 2024-11-08 20:04

Contribution: 2024-11-08 20:05

Contribution: 2024-11-08 20:06

Contribution: 2024-11-12 20:00

Contribution: 2024-11-12 20:01

Contribution: 2024-11-15 20:00

Contribution: 2024-11-15 20:01

Contribution: 2024-11-15 20:02

Contribution: 2024-11-21 20:00

Contribution: 2024-11-21 20:01

Contribution: 2024-11-25 20:00

Contribution: 2024-11-25 20:01

Contribution: 2024-11-27 20:00

Contribution: 2024-11-27 20:01

=======
# Vijaa Frontend Monorepo

# Next.js + React + React Native

## You have to only use Yarn don't use npm

Install Dependencies:

```sh
$ yarn install 
```

If you want to install package from npm:

```sh
$ yarn workspace @frontend/web add <package name>
```

# Next.js Web

Run Web Next.js:

```sh
$ yarn web
```

# Storybook

To run stories of your storybook open a new termianl and run:

```sh
$ yarn web:storybook
```

# Run Test Cases

To run Cypress test cases for web react components(headless - tests will run in terminal without opening the browser)

```sh
$ yarn web:test
```

![cypress headless](https://github.com/Codemarket2/drreamz-frontend2/blob/vivekt/images/cypress_headless.jpg?raw=true)

To run Cypress test cases for web react components(head - tests will run in browser)

```sh
$ yarn web:test:head
```

![cypress web](https://github.com/Codemarket2/drreamz-frontend2/blob/vivekt/images/cypress_web.jpg?raw=true)
Build Web:

If you only want to run a single test then you can use this command

```sh
$ yarn workspace @frontend/web run cypress run-ct --spec ./src/components/<path-to-your-test-file>
```

```sh
$ yarn web:build
```

Deploy Web:

```sh
$ yarn web:deploy
```

# React Native

Install Pod Dependencies (Only on Mac OS):

```sh
$ yarn pod:install (if yarn didn't work try npm install pod-install)
```

Start metro server:

```sh
$ yarn mobile
```

Run android:

```sh
$ yarn android
```

Run ios:

```sh
$ yarn ios
```

# Android Build

Clean the build folders:

```sh
$ yarn android:clean
```

Create build:

```sh
$ yarn android:build
```

# iOS Build

Open project in xcode:

```sh
$ yarn xcode
```
>>>>>>> 2423047 (Initial commit)
