# Lab 6: Streaming Platform Database (MongoDB)

A MongoDB project demonstrating a streaming platform database model with movie metadata, user viewing activity, and recommendation queries.

## Database: `streamingDB`

### Collections:
1. **`movies`**:
   - `movieId`: Unique identifier for each movie (e.g., `"MOV101"`).
   - `title`: Title of the film.
   - `genres`: Array of genres (e.g., `["Sci-Fi", "Action", "Thriller"]`).
   - `releaseYear`: Year of release.
   - `director`: Film director.
   - `cast`: Array of leading cast members.
   - `avgRating`: Average viewer rating.
   - `tags`: Keywords and descriptive tags.

2. **`userActivity`**:
   - `userId`: Identifier for the user.
   - `movieId`: Reference to the movie watched.
   - `watchProgressPercentage`: Percentage of the movie viewed.
   - `userRating`: Rating provided by the user.
   - `lastWatched`: Timestamp of the last watch session.

## Queries:
- **Recommendation Query**: Retrieves movies where `genres` contains `"Sci-Fi"` and `avgRating >= 8.5`, projecting only the `title`, `genres`, and `avgRating`, sorted in descending order of rating.

## Usage
Run with the MongoDB Shell (`mongosh`):
```bash
mongosh streaming.js
```

Or open and run [streaming.mongodb.js](file:///c:/Users/User/OneDrive/Desktop/lab6/streaming.mongodb.js) using the VS Code MongoDB Playground extension.
