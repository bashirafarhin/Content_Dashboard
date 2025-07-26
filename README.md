# 🧠 Content Dashboard

## 📄 Overview

This is a **Content Dashboard** built as part of improving frontend skills. It enables users to view, search, filter, and manage personalized content including **news** and **movie recommendations** from multiple APIs.

> **Tech Stack**: Next.js (App Router) • React • TypeScript • Redux Toolkit • Tailwind CSS • Framer Motion • Axios • i18n • NextAuth.js

---

## 🔗 Live Demo

https://content-dashboard-ten.vercel.app/

---

## 🔗 Website demo

Will be added soon...

---

## ✅ Core Features

### 1. Content Feed

- **User Preferences**:
  - Users can choose favorite categories like *Technology*, *Sports*, *Business*, etc.
  - Preferences are persisted using **Redux Toolkit** and **localStorage**.

- **API Integrations**:
  - **News API**: Top headlines fetched using filters like category, country, and query.
  - **TMDB API**: Fetches movies using endpoints like `popular`, `top_rated`, and `search`.

- **Interactive Cards**:
  - Responsive `NewsCard` and `MovieCard` components.
  - Show image, title, description, author/source, and CTA like **Read More**.
  - Fallback handling for broken images and external domains.

- **Infinite Scrolling**:
  - Implemented using **IntersectionObserver** in a custom `useInfiniteScroll` hook.
  - Optimized for both News and Movie pages.

---

### 2. User Dashboard Layout

- **Main Layout**:
  - responsive header with user controls.
  - Top header includes:
    - Search bar (debounced)
    - Dark mode toggle
    - Language switch
    - User login/logout (Google)

- **Sections**:
  - **Feed**: Unified view of news, movies.
  - **Trending**: Shows trending movies and top news using `HorizontalScroller`.
  - **Favorites**: Content added to favorites is available across sessions via Redux store.

---

### 3. Search Functionality

- **Debounced Search**:
  - Implemented via custom `useDebounce` hook to reduce API load.
  - Integrated into `TopBar`, it searches both News and Movies.

- **Search Across Content**:
  - Supports keyword search using `/search/movie` and `q` param in News API.

---

### 4. Advanced UI/UX Features

- **Drag-and-Drop**:
  - implemented using `React DnD`.

- **Dark Mode**:
  - Implemented using Tailwind CSS + CSS custom properties.
  - State is persisted via `localStorage`.

- **Animations**:
  - Smooth transitions using **Framer Motion** for hover, scroll, and section shifts.

---

### 5. State Management & Logic

- **Redux Toolkit**:
  - Slices for `news`, `movies`, `trendingNews`, `favourites`, etc.

- **Async API Handling**:
  - `createAsyncThunk` + Axios used for all async API actions.

- **Persistence**:
  - User theme and category settings saved to `localStorage`.

---

### 6. Authentication

- Implemented via **NextAuth.js**.
- Supports **Google OAuth** for user login/logout.
- User name and image shown in header.

---

### 7. Internationalization (i18n)

- Implemented with **react-i18next**.
- Supports English and Hindi with dynamic language toggle.

---

```bash
# Will be implemented after stabilizing code base
```
---

## 🔗 Project Setup

```bash
npm install
npm run dev
```

### Environment Variables

Create a `.env` file:

```

NEWS_API_KEY=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
NEXTAUTH_SECRET=your-secret-key
TMDB_API_KEY=
```
