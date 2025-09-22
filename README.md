# 📄 Interview Test Project – Development Documentation

This repository documents my approach to tackling a coding interview test.  
The goal was to build a small full-stack project with a **React (Vite) frontend** and a **NestJS + PostgreSQL backend**, while following clean development practices and ensuring fast iteration.

---

## ⚙️ Tech Stack

### Frontend
- **React + Vite** – Lightweight, fast build tool suitable for quick prototyping.  
  *Note: Not as SEO-friendly as Next.js/Remix, but perfectly fine for this test.*
- **Axios** – For HTTP requests, simple yet powerful.
- **TailwindCSS** – Chosen as a requirement for styling.

### Backend
- **NestJS** – Selected over Express for its opinionated structure and modularity.
- **PostgreSQL + TypeORM** – Relational database with ORM for schema and entity management.

### Deployment
- **Vercel** – Hosting the frontend.
- **Railway** – Hosting the backend.
- **Supabase** – Database hosting.

---

## 🚀 Development Workflow

### 1. Frontend Setup
- Initialized a React project using the **Vite template**.
- Configured **TailwindCSS** with the help of Cursor Agent.
- Generated **base components and styles** from Figma using Cursor Agent prompts:
  - One-page structure with modular components.
  - Tailwind classes centralized for reusable styles (e.g., buttons, inputs).
  - **Responsive design** ensured.
  - Used semantic HTML (`<header>`, `<footer>`, etc.) for better accessibility.
- Integrated **React Query + Axios** for global state and data fetching.

### 2. Backend Setup
- Created a `newsletter_subscriptions` **NestJS module**:
  - **Entity:**  
    - `fullName`, `email`, `linkedin`, `message`
    - Constraints:
      - All required except `linkedin`.
      - Max 100 chars for text fields, 1000 chars for `message`.
  - **DTO & Service:**  
    - Validates incoming requests.
    - Saves data into PostgreSQL using TypeORM.
    - Prevents duplicate email subscriptions.
  - **Controller:**  
    - Exposes a `POST /newsletter-subscriptions` route for creating new entries.

### 3. Testing & Rework
- Performed first test round of the page.
- Identified missing reusable components from AI-generated code.
- Refactored UI components for **consistency, reusability, and accessibility**.

---

## 📊 Development Notes
- **Estimated Net Dev Time:** ~4 hours (including documentation, deployment and testing).
- **AI Assistance:** Used **Cursor Agent** to bootstrap boilerplate (Tailwind config, base components, NestJS module, backend unit testing).  
  Manual adjustments were made for reusability and correctness.
  Examples of AI usage are these initial prompts for both repositories. 
  Frontend:
  Create the required files for my React + Vite project to achieve the same page as in the image attached. The strucutre of files I expect should be a single page that imports components representing each section. CSS should be implemented by   always using tailwind. I would like to have styles that tend to repeat, such as buttons or inputs, imported from a single file where we define these classname strings. The design should be responsive. Also consider using semantic HTML tags for header, footer and any other section you deem necessary. Include basic accessibility requirements when developing the components. Also setup the necessary routing files. Global states and backend requests should be handled with react-query and axios. 

Backend
Create a NestJS module called newsletter_subscriptions. It should have an entity file that holds these fields: full name, email, linkedin, message, all required except linkedin. Message should be limited to 1000 chars, all other fields should be limited to 100chars. Create in this module a controller that accepts a POST route. Then create a services file in this module that holds a service file and a dto file. These files should handle logic for saving the received dto into my database using typeorm in the table newsletter_subscriptions. DTO receives the same fields as the entity. We should limit the creation of repeated email subscriptions.

---

## ✅ Summary
This project demonstrates:
- Ability to bootstrap a modern full-stack app quickly.  
- Leveraging AI tools effectively, while applying **critical review & refactoring**.  
- Strong focus on:
  - **Clean architecture**
  - **Reusability**
  - **Accessibility**
  - **Rapid iteration**

---
