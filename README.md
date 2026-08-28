# Gardeners (Community Management)

- [**Client Live (Firebase)**](https://gardener-connect.web.app)
- [**API Live (Vercel)**](https://gardener-connect.vercel.app)

Gardeners is a community management web application designed to connect gardening enthusiasts with talented gardeners, share gardening tips, and build a vibrant green community. Users can explore featured gardeners, trending gardening tips, and participate in community events.

> [!TIP]
> **Test User Credentials**  
> **Email**: tahmid@engineer.com  
> **Password**: Abc@123456

## Features

- **User Authentication**: Register, login, and manage your profile securely.
- **Browse Gardeners**: Explore gardeners from diverse backgrounds with detailed profiles.
- **Share & Manage Tips**: Create, update, view, and delete gardening tips.
- **Trending Tips**: Discover top liked and public gardening tips.
- **Community Events**: Stay updated with gardening-related events.
- **Dark Mode Support**: Toggle between light and dark themes for comfortable browsing.
- **Responsive Design**: Fully mobile-friendly layout built with Tailwind CSS.

## Tech Stack

- **React**: Frontend UI development.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **MongoDB**: NoSQL database for storing users, gardeners, and tips.
- **Express.js**: Backend server framework.
- **Firebase**: Authentication and hosting.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/tahmid-sarker/gardeners.git
   cd gardeners
   ```

2. **Install root, client, and server dependencies**:

   ```bash
   npm install
   npm run install:all
   ```

3. **Set up environment variables**:

   Copy `client/.env.example` to `client/.env.local` and `server/.env.example` to `server/.env.local`, then fill in your values.

4. **Start client and server together** (from the project root):

   ```bash
   npm run dev
   ```

   This runs the Express API and the Vite client at the same time. To run them separately: `npm run dev:server` or `npm run dev:client`.

5. Open `http://localhost:5173` in your browser to view the project.

## How It Works

- Users can **register** or **login** to access personalized features.
- Browse **featured gardeners** and explore their profiles.
- View **top trending gardening tips** sorted by popularity.
- Create and manage your own gardening tips.
- Participate in community events showcased on the homepage.
- Toggle between light and dark modes for preferred viewing.
- Protected routes ensure user-only access to profile and tip management.

### Routing Overview

| Route               | Description                                                     |
| ------------------- | --------------------------------------------------------------- |
| `/`                 | Home page with Hero, How It Works, Events, Featured Gardeners, Trending Tips, and Testimonials |
| `/register`         | User registration page                                          |
| `/login`            | User login page                                                 |
| `/forget-password`  | Password recovery page                                          |
| `/gardeners`        | Browse all gardeners                                            |
| `/tips`             | View all tips                                                   |
| `/tips-details/:id` | Detailed view of a specific gardening tip                      |
| `/add-tip`          | Form to create a new gardening tip                             |
| `/my-tips`          | User's own tips                                                 |
| `/my-tips/:id/update` | Update a specific tip by ID                                    |
| `/my-profile`       | User's profile page                                            |
| `/update-profile`   | Form to update user profile information                         |
| `/*`                | Custom 404 error page                                           |

## Project Structure

      client/
      └── src/
         ├── assets/
         ├── components/
         │   ├── common/
         │   │   ├── Header.jsx
         │   │   └── Footer.jsx
         │   ├── Home/
         │   │   ├── Hero.jsx
         │   │   ├── HowItWorks.jsx
         │   │   ├── Events.jsx
         │   │   ├── FeaturedGardeners.jsx
         │   │   ├── TopTrendingTips.jsx
         │   │   └── Testimonials.jsx
         │   └── shared/
         │       ├── DynamicTitle.jsx
         │       └── DarkModeToggler.jsx
         ├── config/
         │   └── firebase.config.js
         ├── context/
         │   ├── AuthContext.jsx
         │   ├── AuthProvider.jsx
         │   ├── DataContext.jsx
         │   ├── DataProvider.jsx
         │   ├── ThemeContext.jsx
         │   └── ThemeProvider.jsx
         ├── layouts/
         │   └── MainLayout.jsx
         ├── pages/
         │   ├── Auth/
         │   │   ├── Login.jsx
         │   │   ├── Register.jsx
         │   │   └── ForgetPassword.jsx
         │   ├── Profile/
         │   │   ├── MyProfile.jsx
         │   │   └── UpdateProfile.jsx
         │   ├── Tips/
         │   │   ├── Tips.jsx
         │   │   ├── TipsDetails.jsx
         │   │   ├── MyTips.jsx
         │   │   └── UpdateTip.jsx
         │   ├── Home.jsx
         │   ├── Error.jsx
         │   └── Gardeners.jsx
         ├── routes/
         │   ├── Router.jsx
         │   └── PrivateRoutes.jsx
         ├── main.jsx
         ├── index.css
         └── index.html
      server/
      └── index.js

## Credits

This project was developed by [Tahmid Sarker](https://tahmid-sarker.github.io).