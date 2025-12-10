# Google Docs Clone

Simple MERN-style doc editor with user auth and MongoDB-backed storage.

## Prerequisites
- Node.js and npm
- MongoDB running locally on `mongodb://127.0.0.1:27017` (adjust as needed)

## Backend (Express + MongoDB)
```bash
cd backend
npm install
# ensure mongod is running locally
npm start
```
Default server: `http://localhost:3000`

## Frontend (React + Vite)
```bash
cd frontend
npm install
npm run dev
```
Default dev server: `http://localhost:5173`

## API base URL
Frontend expects the backend at `http://localhost:3000` (see `frontend/src/Helper.js`). Update there if your backend runs elsewhere.

## Typical workflow
1) Start MongoDB locally.
2) Run the backend (`npm start` in `backend`).
3) Run the frontend (`npm run dev` in `frontend`) and open the shown URL.

## Recreate the project from scratch (optional)
If you want to reproduce this setup in a fresh folder:
```bash
# Backend
npx express-generator backend --view=ejs
cd backend
npm install
npm install bcryptjs jsonwebtoken mongoose cors

# Add your models/routes (see this repo's backend/ for reference)

# Frontend
cd ..
npm create vite@latest frontend -- --template react
cd frontend
npm install
npm install react-router-dom react-icons react-avatar

# Add your pages/components and point API calls to your backend
```
