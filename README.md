# Backend Project

This is a backend project for a video streaming platform. It provides APIs for user authentication, video management, subscriptions, playlists, likes, comments, and more.

## Features

- **User Management**: User registration, login, logout, and profile updates.
- **Video Management**: Upload, update, delete, and fetch videos.
- **Subscriptions**: Subscribe to channels and manage subscriptions.
- **Playlists**: Create, update, and manage playlists.
- **Likes and Comments**: Like videos, tweets, and comments, and manage comments.
- **Authentication**: JWT-based authentication with access and refresh tokens.
- **Healthcheck**: API to check the health of the server.

## Technologies Used

- **Node.js**: Backend runtime.
- **Express.js**: Web framework.
- **MongoDB**: Database for storing data.
- **Mongoose**: ODM for MongoDB.
- **Cloudinary**: For file uploads.
- **JWT**: For authentication.
- **Multer**: For handling file uploads.
- **dotenv**: For environment variable management.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd backend-project
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and configure it based on `.env.sample`.

4. Start the development server:
   ```bash
   npm run dev
   ```

## API Endpoints

### User Routes
- `POST /api/v1/users/register`: Register a new user.
- `POST /api/v1/users/login`: Login a user.
- `POST /api/v1/users/logout`: Logout a user.
- `GET /api/v1/users/current-user`: Get the current logged-in user.

### Video Routes
- `GET /api/v1/videos`: Get all videos.
- `POST /api/v1/videos`: Upload a new video.
- `PATCH /api/v1/videos/:videoId`: Update video details.
- `DELETE /api/v1/videos/:videoId`: Delete a video.

### Subscription Routes
- `POST /api/v1/subscriptions/c/:channelId`: Subscribe to a channel.
- `GET /api/v1/subscriptions/c/:channelId`: Get subscribed channels.

### Playlist Routes
- `POST /api/v1/playlist`: Create a new playlist.
- `GET /api/v1/playlist/:playlistId`: Get playlist details.

### Like Routes
- `POST /api/v1/likes/toggle/v/:videoId`: Toggle like on a video.

### Healthcheck
- `GET /api/v1/healthcheck`: Check server health.

## Folder Structure

```
backend-project/
├── src/
│   ├── controllers/       # API controllers
│   ├── models/            # Mongoose models
│   ├── routes/            # API routes
│   ├── utils/             # Utility functions
│   ├── middlewares/       # Middleware functions
│   ├── db/                # Database connection
│   ├── app.js             # Express app setup
│   ├── index.js           # Entry point
├── public/                # Public assets
├── .env.sample            # Environment variable sample
├── package.json           # Project metadata and dependencies
├── README.md              # Project documentation
```

## Environment Variables

The following environment variables are required:

- `PORT`: Server port.
- `MONGODB_URI`: MongoDB connection string.
- `ACCESS_TOKEN_SECRET`: Secret for JWT access tokens.
- `REFRESH_TOKEN_SECRET`: Secret for JWT refresh tokens.
- `CLOUDINARY_CLOUD_NAME`: Cloudinary cloud name.
- `CLOUDINARY_API_KEY`: Cloudinary API key.
- `CLOUDINARY_API_SECRET`: Cloudinary API secret.

## License

This project is licensed under the ISC License.
