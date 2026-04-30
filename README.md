# CA Monk - Blog Application Assignment


## Installation

### Prerequisites
- Node.js (v18 or higher)
- Git
- React.js knowledge
- Familiarity with TanStack Query, Tailwind CSS, and shadcn/ui.

### Setup Instructions

1. **Fork the repository**
   - Click **Fork** on GitHub to create a copy in your account.
   - Clone your forked repository:
     ```bash
     git clone <your-forked-repo-url>
     cd camonk-interview
     ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Install required libraries for the assignment** , ie, TanStack Query, Tailwind CSS, and  shadcn/ui
4. **Start the JSON Server (Backend API)**
   ```bash
   npm run server
   ```
   The API will run on `http://localhost:3001`

5. **Start the Development Server (in a new terminal)**
   ```bash
   npm run dev
   ```
   The app will run on `http://localhost:5173`

## Assignment Tasks

You are required to build a blog application with the following features:

### Required Technologies
- ✅ **TanStack Query** - For server state management and data fetching
  - 📚 [Documentation](https://tanstack.com/query/latest)
- ✅ **Tailwind CSS** - For styling
  - 📚 [Documentation](https://tailwindcss.com/docs)
- ✅ **shadcn/ui** - For UI components
  - 📚 [Documentation](https://ui.shadcn.com/)

## UI Reference

Here's a reference design for the blog application layout:

![Blog Reference](image.png)

**Left Panel:** Blog list view showing blog cards with category, title, and description  
**Right Panel:** Blog detail view displaying cover image, full content

UI IMAGE - ![UI-refernece](ui.jpeg)

> **Note:** This is just a reference design. Your implementation does not have to look exactly like this. 

For the blog content, use plain text — no need to use HTML-formatted text.

### Tasks to Complete

#### 1. **Get All Blogs**
- Create a component to display all blogs using `GET /blogs`
- Use TanStack Query for data fetching
- Handle loading and error states

#### 2. **Get Blog by ID**
- Implement single blog view using `GET /blogs/:id`
- Use TanStack Query for data fetching

#### 3. **Create a New Blog**
- Build a form to create a new blog using `POST /blogs`
- Invalidate queries after successful creation

> Organize your components in a suitable file structure within the `src/` directory.

### API Endpoints

The JSON Server provides the following endpoints:

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/blogs` | Get all blogs |
| GET | `/blogs/:id` | Get a specific blog by ID |
| POST | `/blogs` | Create a new blog |

### Evaluation Criteria

Your submission will be evaluated on:
- ✅ Correct implementation of TanStack Query hooks
- ✅ Proper use of Tailwind CSS for styling
- ✅ Integration of shadcn/ui components
- ✅ Code organization and structure
- ✅ Error handling and loading states
- ✅ Responsive design []
- ✅ User experience and UI polish



## Sample Blog Object

```json
{
  "id": 1,
  "title": "Future of Fintech",
  "category": ["FINANCE", "TECH"],
  "description": "Exploring how AI and blockchain are reshaping financial services",
  "date": "2026-01-11T09:12:45.120Z",
  "coverImage": "https://images.pexels.com/photos/6801648/pexels-photo-6801648.jpeg",
  "content": "Full blog content..."
}
```

description: A short summary of the blog  
content: The full content of the blog

## Tips

- Set up TanStack Query's `QueryClientProvider` in your app root
- Configure Tailwind CSS properly in your config files
- Use shadcn components like `Card`, `Button`, `Input`, etc.
- Handle loading states with skeletons
- Implement proper error boundaries
- Consider using React Router for navigation (optional)

## Submission

Once you've completed the assignment:
1. Ensure all tasks are working correctly
2. Commit your changes with clear commit messages
3. Push your changes to your **forked** repository
4. Share the link to your forked repository for review in the Google Form provided

## FAQ

**Do I need to deploy the code?**  
No. Simply work on your forked repository, commit and push your changes, and share the repository link via the Google Form.

**Is it mandatory to use TypeScript and TanStack Query?**  
Yes, using both TypeScript and TanStack Query is compulsory for this assignment.

**Is using JSON Server mandatory, or can I create my own server?**  
Using JSON Server is mandatory. Please use the provided JSON Server setup rather than creating your own backend.

**What should I use for styling?**  
Use **Tailwind CSS** and **shadcn/ui** for styling. You are expected to install, configure, and use both Tailwind CSS and shadcn/ui components in your implementation.

**What are the main things you will evaluate?**  
We will mainly look at:
- Correct use of the required technologies (TypeScript, TanStack Query, Tailwind CSS, shadcn/ui)  
- Code quality and structure  
- UI/UX, including responsiveness and overall experience  

**What happens after I submit the assignment?**  
If you are shortlisted, you will receive an email about the next round. The next round will be a task-based session focused on your coding skills and React knowledge.

**Will my solution be used commercially?**  
No. This assignment is only for the hiring process and will not be used commercially.

**Have more questions?**  
If you have any additional doubts, feel free to reach out at: `developer@camonk.com`.

Good luck! 🚀












AFTER COMPLETION (AIMED README)

# CA Monk – Blog Application

A modern blog application built as part of the **CA Monk Frontend Assignment**.  
The app allows users to view all blogs, read a single blog in detail, and create new blog posts using a mock backend powered by JSON Server.

---

## 🚀 Features

- 📄 View all blogs with title, category, and description
- 🔍 View detailed blog content by selecting a blog
- ✍️ Create a new blog post
- ⚡ Efficient server-state management using TanStack Query
- 🎨 Clean and responsive UI with Tailwind CSS & shadcn/ui
- ⏳ Proper loading and error handling states

---

## 🛠️ Tech Stack

- **React** (with **TypeScript**)
- **TanStack Query** – Server state management & data fetching
- **Tailwind CSS** – Utility-first styling
- **shadcn/ui** – Reusable UI components
- **JSON Server** – Mock backend API
- **Vite** – Development & build tool

---

## 📁 Project Structure

src/
├── components/
│ ├── BlogCard.tsx
│ ├── BlogList.tsx
│ ├── BlogDetail.tsx
│ └── BlogForm.tsx
├── hooks/
│ └── useBlogs.ts
├── pages/
│ └── Home.tsx
├── services/
│ └── api.ts
├── types/
│ └── blog.ts
├── App.tsx
└── main.tsx


---

## 🔌 API Endpoints (JSON Server)

| Method | Endpoint        | Description              |
|------|-----------------|--------------------------|
| GET  | `/blogs`        | Get all blogs            |
| GET  | `/blogs/:id`    | Get blog by ID           |
| POST | `/blogs`        | Create a new blog        |

### Sample Blog Object

```json
{
  "id": 1,
  "title": "Future of Fintech",
  "category": ["FINANCE", "TECH"],
  "description": "Exploring how AI and blockchain are reshaping financial services",
  "date": "2026-01-11T09:12:45.120Z",
  "coverImage": "https://images.pexels.com/photos/6801648/pexels-photo-6801648.jpeg",
  "content": "Full blog content..."
}


⚙️ Installation & Setup
Prerequisites
Node.js v18 or higher


Steps
Fork the repository

Clone your fork

git clone <your-forked-repo-url>
cd camonk-interview
Install dependencies

npm install
Start JSON Server

npm run server
Backend runs at: http://localhost:3001

Start development server

npm run dev
App runs at: http://localhost:5173

🧠 Implementation Details
TanStack Query is configured using QueryClientProvider at the app root

Queries are invalidated after creating a new blog to refresh the list

Loading states are handled using skeletons

Error states are handled gracefully with fallback UI

UI components are built using shadcn/ui and styled with Tailwind CSS

Plain text is used for blog content (no HTML formatting)

📱 Responsive Design
Fully responsive layout

Blog list and blog detail panels adapt to screen size

Optimized for both desktop and mobile views

✅ Evaluation Checklist
 TanStack Query hooks implemented correctly

 Tailwind CSS styling

 shadcn/ui components used

 TypeScript enforced throughout the app

 Proper folder structure

 Loading and error handling

 Responsive and polished UI
