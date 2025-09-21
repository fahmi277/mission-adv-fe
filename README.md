# Harisenin Course Platform

Platform pembelajaran online yang dibangun menggunakan React + TypeScript + Vite dengan fitur lengkap untuk manajemen kursus, autentikasi, dan pembelajaran terintegrasi dengan Mock API.

## 🚀 Tech Stack

- **Frontend Framework**: React 19 dengan TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS + PostCSS
- **Routing**: React Router DOM v7
- **Icons**: Lucide React + FontAwesome
- **State Management**: React useState, useReducer & useContext
- **API Integration**: MockAPI.io untuk backend simulation
- **Component Architecture**: Atomic Design Pattern
- **Type Safety**: Full TypeScript implementation

## 📁 Project Structure

```
src/
├── components/
│   ├── atoms/              # Komponen dasar (Typography, Button, Input)
│   │   └── Typography.tsx  # ✅ Reusable typography component
│   ├── molecules/          # Kombinasi atoms dengan business logic
│   │   ├── AddCourseForm.tsx      # ✅ Form untuk menambah kursus baru
│   │   ├── FilterMenu.tsx         # ✅ useState untuk filter state
│   │   ├── CategoryTabs.tsx       # ✅ useState untuk active category
│   │   ├── CourseCard.tsx         # ✅ Props dari parent component
│   │   ├── UserListCard.tsx       # ✅ Integrasi dengan API users
│   │   ├── BannerCard.tsx         # ✅ Landing page banner
│   │   ├── Breadcrumb.tsx         # ✅ Navigation breadcrumb
│   │   └── CustomPagination.tsx   # ✅ Pagination component
│   ├── organisms/          # Komponen kompleks
│   └── HeaderDashboard.tsx # ✅ Main dashboard header
├── pages/                  # Halaman aplikasi dengan routing
│   ├── Dashboard.tsx              # ✅ useState & API integration
│   ├── LoginPage.tsx              # ✅ Auth dengan APIService
│   ├── RegisterPage.tsx           # ✅ User registration
│   ├── AllProducts.tsx            # ✅ Course listing page
│   ├── DetailProduct.tsx          # ✅ Course detail dengan params
│   ├── OrderHistory.tsx           # ✅ Order management
│   ├── PaymentPage.tsx            # ✅ Payment processing
│   └── PaymentCompleted.tsx       # ✅ Payment success page
├── services/               # API integration layer
│   └── api.ts                     # ✅ MockAPI service dengan CRUD operations
├── context/                # Global state management
│   ├── AuthContext.tsx            # ✅ useReducer untuk authentication
│   ├── CourseContext.tsx          # ✅ Course management dengan API
│   └── AppContext.tsx             # ✅ Global app state
├── hooks/                  # Custom React hooks
│   └── useCart.ts                 # ✅ useState untuk cart management
├── types/                  # TypeScript definitions
│   ├── user.ts                    # ✅ User, Auth & MockCourse interfaces
│   ├── course.ts                  # ✅ Course related types
│   ├── chip.ts                    # ✅ Component prop types
│   └── heading.ts                 # ✅ Typography types
├── utils/                  # Utility functions
│   ├── courseTransform.ts         # ✅ Data transformation
│   └── status.ts                  # ✅ Status management
└── data/                   # Mock data dan constants
    ├── coursesData.ts             # ✅ Local course data
    ├── userProfile.ts             # ✅ User profile data
    └── avatarImage.ts             # ✅ Avatar image paths
```

## ✨ Features

### 🎯 Core Features
- **User Authentication**: Login & Register dengan MockAPI integration
- **Course Management**: CRUD operations untuk kursus menggunakan real API
- **Dashboard Kursus**: Tampilan grid kursus dengan filter dan pencarian
- **Pencarian & Filter**: Filter berdasarkan kategori, harga, dan durasi
- **Detail Kursus**: Informasi lengkap kursus dengan routing parameter
- **User Management**: Daftar pengguna dari MockAPI dengan real-time data
- **Order History**: Manajemen riwayat pembelian dengan array operations
- **Payment System**: Multi-step payment flow dengan confirmation
- **Responsive Design**: Optimized untuk semua device dengan Tailwind CSS

### 🔌 API Integration
- **MockAPI.io Integration**: `https://68c521bea712aaca2b67edde.mockapi.io/api/v1`
- **User Endpoints**: GET, POST operations untuk user management
- **Course Endpoints**: Full CRUD (GET, POST, PUT, DELETE) untuk courses
- **Authentication Flow**: Login/register dengan email validation
- **Error Handling**: Comprehensive error handling untuk API calls
- **Type Safety**: Full TypeScript interfaces untuk API responses

### 🛠 Technical Features
- **useState Implementation**: ✅ Local state management untuk komponen
  - AddCourseForm: useState untuk form validation dan submission
  - FilterMenu: useState untuk filter state dengan controlled inputs
  - CategoryTabs: useState untuk active category switching
  - UserListCard: useState untuk loading dan error states
- **useReducer Implementation**: ✅ Complex state management
  - AuthContext: useReducer untuk authentication flow dengan actions
  - CourseContext: useReducer untuk course CRUD operations
- **API Service Layer**: ✅ Centralized API calls dengan error handling
  - APIService class dengan static methods
  - Async/await pattern untuk semua API calls
  - Response type safety dengan TypeScript interfaces
- **Context API**: ✅ Global state sharing
  - AuthContext untuk user authentication state
  - CourseContext untuk course data management
  - Provider pattern untuk component tree injection
- **React Router**: ✅ Multi-page routing dengan parameter handling
  - Dynamic routing untuk course details
  - Protected routes untuk authenticated pages
  - Navigation dengan programmatic routing

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 atau lebih baru)
- npm atau yarn
- Git

### Installation

1. **Clone repository**
   ```bash
   git clone <repository-url>
   cd mission-fe-adv
   ```

2. **Install dependencies**
   ```bash
   npm install
   # atau
   yarn install
   ```

3. **Start development server**
   ```bash
   npm run dev
   # atau
   yarn dev
   ```

4. **Build untuk production**
   ```bash
   npm run build
   # atau
   yarn build
   ```

### 🌐 API Configuration

Project ini menggunakan MockAPI.io sebagai backend:
- **Base URL**: `https://68c521bea712aaca2b67edde.mockapi.io/api/v1`
- **Users Endpoint**: `/users` - User management
- **Courses Endpoint**: `/course` - Course CRUD operations

### Available Scripts

- `npm run dev` - Start development server dengan hot reload di port 5173
- `npm run build` - Build aplikasi untuk production (TypeScript + Vite)
- `npm run lint` - Run ESLint untuk code quality check
- `npm run preview` - Preview production build locally

## 🎨 Design System

### Color Palette
- **Primary**: Orange (#FF5722)
- **Secondary**: Dark Blue (#1E293B)
- **Success**: Green (#22C55E)
- **Warning**: Yellow (#F59E0B)
- **Error**: Red (#EF4444)

### Typography
- **Font Family**: Inter
- **Headings**: font-semibold, font-bold
- **Body**: font-normal, font-medium

### Spacing & Layout
- **Container**: max-width dengan padding responsive
- **Grid**: CSS Grid dan Flexbox untuk layout
- **Breakpoints**: Tailwind default breakpoints (sm, md, lg, xl, 2xl)

## 📱 Responsive Design

Aplikasi fully responsive dengan breakpoints:
- **Mobile**: < 640px
- **Tablet**: 640px - 1024px  
- **Desktop**: > 1024px

## 🔧 Development Guidelines

### API Integration Pattern
```typescript
// Contoh penggunaan APIService
import APIService from '../services/api';

// Get all courses
const courses = await APIService.getAllCourses();

// Create new course
const newCourse = await APIService.createCourse(courseData);

// Authentication
const response = await APIService.login(credentials);
```

### useState Implementation
- Identifikasi komponen yang memerlukan local state
- Gunakan useState untuk form inputs, loading states, dan UI interactions
- Lift state up ke parent component jika diperlukan oleh multiple children

### useReducer untuk Complex State
```typescript
// AuthContext example
const authReducer = (state: AuthState, action: AuthAction): AuthState => {
  switch (action.type) {
    case 'AUTH_START':
      return { ...state, loading: true, error: null };
    case 'AUTH_SUCCESS':
      return { ...state, user: action.payload, isAuthenticated: true };
    // ... other cases
  }
};
```

### Component Architecture
- Follow Atomic Design Pattern (atoms → molecules → organisms)
- Maintain single responsibility principle
- Use TypeScript interfaces untuk prop definitions dan API responses
- Implement proper error boundaries dan loading states

### API Service Architecture
- Centralized API calls dalam `services/api.ts`
- Consistent error handling dengan try/catch
- Type-safe responses dengan TypeScript interfaces
- RESTful endpoint patterns

## 🚀 Deployment

### Build Production
```bash
npm run build
```

### Deploy ke Vercel
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

### Deploy ke Netlify
```bash
# Install Netlify CLI
npm i -g netlify-cli

# Build dan deploy
npm run build
netlify deploy --prod --dir=dist
```

## 📝 ESLint Configuration

Untuk production application, update ESLint configuration:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      ...tseslint.configs.recommendedTypeChecked,
      ...tseslint.configs.strictTypeChecked,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```

## 🤝 Contributing

1. Fork repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👥 Team

**Harisenin Bootcamp - Mission Frontend Advanced**

## 📚 Learning Objectives Achieved

✅ **React Hooks Mastery**
- useState untuk local component state management
- useReducer untuk complex state logic (Auth & Course management)
- useContext untuk global state sharing
- Custom hooks untuk reusable logic

✅ **TypeScript Integration**
- Full type safety dengan interfaces dan types
- API response typing untuk MockAPI integration
- Component props typing dengan proper inheritance
- Generic types untuk reusable components

✅ **API Integration**
- Real API consumption dengan MockAPI.io
- CRUD operations (Create, Read, Update, Delete)
- Error handling dan loading states
- Authentication flow dengan API validation

✅ **State Management Patterns**
- Local state dengan useState
- Global state dengan Context API
- Complex state dengan useReducer
- State lifting dan prop drilling prevention

✅ **Modern React Patterns**
- Functional components with hooks
- Component composition over inheritance
- Render props dan custom hooks
- Performance optimization dengan proper dependencies

---

**Happy Coding! 🚀**