# **AxiomFlow - Backend-First Learning Project**  

**Description:**  
AxiomFlow is a **backend-focused learning project** where I'm building a RESTful API for a finance dashboard application. This phase focuses on developing the server-side infrastructure—authentication, data models, ML prediction endpoints, and database integration—before connecting it to a frontend.

Since this is a **learning project**, the backend is being developed independently. The frontend dependencies and structure are outlined for future integration but are not currently implemented.

---

## **Backend Implementation**

### **Dependencies (Already Installed):**
```bash
npm i --save express cors pino dotenv helmet morgan logger mongoose-currency @typegoose/typegoose http-status-codes mongoose@~6.10.0
npm i --save-dev @types/cors @types/express pino-pretty ts-node-dev typescript @types/mongoose-currency
```

### **Project Structure:**
```
axiomflow-backend/
├── src/
│   ├── controllers/     # Route controllers
│   ├── models/         # TypeGoose schemas
│   ├── routes/         # Express routes
│   ├── middleware/     # Auth, validation, error handling
│   ├── utils/         # Helpers, ML prediction logic
│   ├── types/         # TypeScript interfaces
│   └── app.ts         # Express app setup
├── .env               # Environment variables
├── package.json
└── tsconfig.json
```

### **Environment Variables (.env):**
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/axiomflow
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
```

### **Key Backend Features Being Built:**

1. **Authentication & Authorization**
   - JWT-based user registration/login
   - Protected routes with middleware
   - Role-based access control

2. **Data Models (TypeGoose/Mongoose)**
   - User schema with financial preferences
   - Transaction/Expense tracking
   - Financial metrics and predictions
   - Dashboard configurations

3. **Machine Learning Endpoints**
   - `/api/predict/regression` - Financial forecasting
   - `/api/analyze/spending` - Pattern detection
   - `/api/metrics/summary` - Aggregated insights

4. **API Features**
   - Request validation with Zod/Joi
   - Structured logging with Pino
   - Security headers with Helmet
   - Rate limiting
   - Comprehensive error handling

5. **Database Operations**
   - CRUD operations for financial data
   - Aggregation pipelines for analytics
   - Data seeding for testing

---

## **Frontend (Future Integration)**

### **Frontend Dependencies (To be installed later):**
```bash
npm i --save react-redux @reduxjs/toolkit react-router-dom @mui/material @emotion/react @emotion/styled @mui/icons-material @mui/x-data-grid
npm i --save-dev @types/react-dom eslint eslint-config-react-app @types/node
```

### **Frontend Environment Variable:**
```env
VITE_BASE_URL=http://localhost:5000  # Points to this backend
```

---

## **Current Development Focus**

Since this is a **learning-phase project**, I'm concentrating on:

1. **Building robust backend foundations**
2. **Implementing proper TypeScript patterns**
3. **Creating secure authentication flows**
4. **Designing scalable database schemas**
5. **Developing accurate ML prediction algorithms**
6. **Writing comprehensive tests**
7. **API documentation with Swagger/OpenAPI**

---

## **API Endpoints Being Developed**

```typescript
// Example routes structure
GET    /api/health          # Service status
POST   /api/auth/register   # User registration
POST   /api/auth/login      # User login
GET    /api/users/me        # Get current user
POST   /api/transactions    # Add financial transaction
GET    /api/transactions    # Get user's transactions
POST   /api/predict/finance # ML prediction endpoint
GET    /api/dashboard       # Dashboard data aggregation
```

---

## **Learning Objectives**

This backend-first approach allows me to:
- Master Node.js/Express with TypeScript
- Implement proper authentication/authorization
- Work with MongoDB and TypeGoose
- Create machine learning integrations
- Build production-ready API architecture
- Practice testing and deployment strategies

**Note:** The frontend React application will be built separately and connected to this backend once the API is fully functional and tested.

---

## **Running the Backend**

```bash
# Development
npm run dev

# Production build
npm run build
npm start

# Testing
npm test
```

This project structure ensures a solid backend foundation before frontend integration, following best practices for scalable application development.
