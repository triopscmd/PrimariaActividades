## Project Plan: Primary School Educational Platform

This document outlines the initial project plan for the development of a comprehensive educational platform for primary school students. The application will leverage Vite, React, TypeScript, and TailwindCSS for the frontend, with a Node.js/Express backend powered by Prisma for robust data persistence.

### Feature: Initial Project Setup & Core Configuration
This feature covers the foundational setup of the project, including frontend build tools, styling, quality control, environment management, and basic CI/CD pipelines.
- package.json
- vite.config.ts
- tsconfig.json
- tsconfig.node.json
- src/main.tsx
- src/App.tsx
- src/index.css
- tailwind.config.ts
- postcss.config.js
- .env.example
- .eslintrc.json
- .prettierrc
- .gitignore
- .github/workflows/ci.yml
- .github/workflows/cd.yml
- public/index.html
- src/router/index.tsx
- src/components/layout/Header.tsx
- src/components/layout/Footer.tsx
- src/pages/HomePage.tsx
- src/api/axiosConfig.ts
- src/utils/helpers.ts

### Feature: Database & Backend Foundation
This feature establishes the robust backend infrastructure and database layer using Node.js, Express, and Prisma. It includes core server setup, authentication mechanisms, and the foundational database schema.
- server/package.json
- server/tsconfig.json
- server/src/index.ts
- server/src/app.ts
- server/src/db.ts
- server/src/middleware/authMiddleware.ts
- server/src/utils/jwt.ts
- server/src/routes/authRoutes.ts
- server/src/controllers/authController.ts
- server/src/services/authService.ts
- prisma/schema.prisma
- prisma/seed.ts

### Feature: Student Profile & Progress Tracking
This feature implements the core functionality for managing student accounts, tracking their grade levels, performance, and completed activities, providing a personalized experience.
- src/pages/student/DashboardPage.tsx
- src/pages/student/ProfilePage.tsx
- src/components/student/ProfileDetails.tsx
- src/components/student/ProgressOverview.tsx
- src/api/studentApi.ts
- server/src/routes/studentRoutes.ts
- server/src/controllers/studentController.ts
- server/src/services/studentService.ts

### Feature: Curriculum & Content Management
This feature focuses on the backend logic and API definitions for managing the educational content, including courses, subjects (mathematics, science), grade levels (1st-6th), and specific topics. The admin portal UI for this will be covered in a separate feature.
- server/src/routes/curriculumRoutes.ts
- server/src/controllers/curriculumController.ts
- server/src/services/curriculumService.ts
- src/api/curriculumApi.ts
- src/types/curriculum.ts

### Feature: Dynamic Exam Generation & Interactive Interface
This feature covers the system for dynamically generating exams from a categorized question bank, based on selected courses or topics, and provides an intuitive interface for students to take these exams.
- src/pages/student/ExamConfigurationPage.tsx
- src/pages/student/ExamTakingPage.tsx
- src/components/exam/QuestionDisplay.tsx
- src/components/exam/ExamNavigation.tsx
- src/utils/examLogic.ts
- src/api/examApi.ts
- server/src/routes/examRoutes.ts
- server/src/controllers/examController.ts
- server/src/services/examService.ts

### Feature: Visual Performance Analytics & Reporting
This feature implements the generation of comprehensive visual reports after each completed exam, including a final grade, percentages by topic and course, and interactive charts (bar, pie).
- src/pages/student/ExamResultsPage.tsx
- src/components/charts/BarChart.tsx
- src/components/charts/PieChart.tsx
- src/components/charts/OverallReport.tsx
- src/api/analyticsApi.ts
- server/src/routes/analyticsRoutes.ts
- server/src/controllers/analyticsController.ts
- server/src/services/analyticsService.ts

### Feature: Administrator Content Management Portal
This feature provides a secure web portal for educators and administrators to manage educational content, questions, and student data, leveraging the backend services defined in other features.
- src/pages/admin/AdminDashboardPage.tsx
- src/pages/admin/ManageCoursesPage.tsx
- src/pages/admin/ManageQuestionsPage.tsx
- src/pages/admin/ManageUsersPage.tsx
- src/components/admin/CourseForm.tsx
- src/components/admin/QuestionForm.tsx
- src/components/admin/UserTable.tsx
- src/api/adminApi.ts
- server/src/routes/adminRoutes.ts
- server/src/controllers/adminController.ts
- server/src/services/adminService.ts
