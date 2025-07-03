This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/pages/api-reference/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/pages/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn-pages-router) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/pages/building-your-application/deploying) for more details.

# 🚀 Journey Builder

A modular, extensible React application to visualize and configure a **Journey Builder DAG** with forms and dynamic prefill mappings.  
Built with a focus on **clean architecture**, **reusable components**, and **modern React best practices**.

---

## ✨ Features

✅ Visualize forms as a **Directed Acyclic Graph (DAG)**  
✅ Inspect and configure field-level prefill mappings  
✅ Modular, **reusable components** (`JourneyBuilder`, `FormDAG`, `PrefillConfiguration`)  
✅ Dynamically processes form schemas and normalizes data structures  
✅ Fully type-safe with **TypeScript interfaces**  
✅ Designed for **extensibility** and easy integration with real data sources

---

## 📂 Code Organization

- **Clear separation of concerns:**  
  State management and data processing logic live in the parent container (`JourneyBuilder`) while presentation and user interactions are handled by child components.
- **Well-defined interfaces:**  
  All props and data structures are strongly typed using TypeScript interfaces.
- **Thoughtful hierarchy & composition:**  
  Components are designed to be independent and composable for reuse in other contexts.

---

## 🧪 Tests

The project is structured to easily support tests written with:
- [Jest](https://jestjs.io/)
- [React Testing Library](https://testing-library.com/)

Recommended test coverage:
- Component rendering and prop handling
- Form selection and prefill mapping logic
- Data normalization in `useEffect`

🔌 How to Extend
Add new data sources or forms
Open: src/mockData/formData.ts

Update:

mockFormDAGResponse.nodes → add DAG nodes

mockFormDAGResponse.forms → define forms with field_schema

initialPrefillConfig → define default prefill mappings

Integrate real APIs
Replace the mock data import in JourneyBuilder.tsx with a fetch() or Axios call in useEffect, then set the state as shown.

View in Browser
Once the development server is running, open your browser and navigate to: [http://localhost:3000](http://localhost:3000)
