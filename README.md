# MovieMatch

## Overview

MovieMatch is a Java-based movie recommendation application that helps users discover new movies based on titles they already enjoy. The application utilizes the TasteDive API to retrieve movie recommendations, stores movie data locally in JSON format, and allows users to maintain personalized watchlists, favorites, and recently watched movies.

The project demonstrates core Java development concepts including API integration, object serialization, JSON processing, lambda expressions, regular expressions, database interaction, file persistence, custom UI design, and unit testing.

---

## Features

### Movie Search
- Search for movies by title.
- Retrieve recommendations using the TasteDive API.
- Display related movie suggestions in an easy-to-use interface.

### Personalized User Experience
- Save favorite movies.
- Track recently watched movies.
- Maintain a personal watchlist.
- Persist user-specific data between application launches.

### Advanced Filtering & Sorting
- Sort recommendations alphabetically.
- Sort by user ratings or popularity.
- Filter movie results based on user input.
- Utilize Java Streams and Lambda Expressions for data processing.

### Input Validation
- Validate movie titles using Regular Expressions.
- Prevent invalid characters and malformed inputs.
- Display user-friendly validation error messages.

### Custom UI
- Custom application styling and theme.
- Multiple screens/views for enhanced user navigation.
- Responsive and user-friendly interface.

---

## Application Views

### Home/Search View
The primary screen where users can:

- Search for movies
- View recommended movies
- Apply sorting and filtering options
- Add movies to favorites or watchlists

### User Library View
The personal library where users can:

- View favorite movies
- View watchlist entries
- View recently watched movies
- Manage stored movie collections

---

## Technologies Used

### Java
Core application logic and object-oriented design.

### JavaFX
User interface creation and styling.

### TasteDive API
Movie recommendation data retrieval.

### JSON
Storage and management of movie recommendation data.

### MySQL Database
Stores user-specific information including:

- Favorites
- Watchlist entries
- Recently watched movies
- User preferences

### JUnit
Unit testing framework used to validate application functionality.

---

## Learning Objectives Demonstrated

### Lambda Expressions
The application uses lambda expressions to:

- Sort movie collections
- Filter search results
- Process recommendation data
- Improve code readability and maintainability

Example:

```java
movies.stream()
      .filter(movie -> movie.getTitle().contains(searchTerm))
      .sorted((a, b) -> a.getTitle().compareTo(b.getTitle()))
      .toList();
```

### Regular Expressions
Regex is used to validate user-entered movie titles and prevent invalid input.

Example:

```java
^[A-Za-z0-9\\s:'\\-!,\\.]{1,100}$
```

This pattern allows realistic movie titles while rejecting invalid characters.

### Object Serialization
User data is persisted between application launches through object encoding and decoding.

Example technologies:

- ObjectOutputStream
- ObjectInputStream

This ensures user preferences can be restored when the application is reopened.

---

## Data Persistence

MovieMatch utilizes multiple persistence methods:

### JSON Storage
- Stores TasteDive movie recommendation data.
- Reduces unnecessary API calls.
- Enables local movie data management.

### Database Storage
- Stores user-specific information.
- Maintains favorites.
- Maintains watchlists.
- Maintains recently watched history.

### Object Serialization
- Saves application state and user preferences.
- Demonstrates Java object encoding and decoding.

---

## Testing

The application includes both happy path and negative path unit tests.

### Happy Path Tests

- Valid movie title input
- Successful recommendation retrieval
- Database record creation
- Correct sorting functionality

### Negative Path Tests

- Invalid movie title input
- Empty search submissions
- Invalid database operations
- Missing or corrupted data files

---

## Requirements Fulfilled

### Required Features

✅ Custom styling/theming

✅ At least 2 separate views

✅ Input validation

✅ Object encoding/decoding persistence

✅ Lambda functions

✅ Complex regex validation

✅ Happy path unit tests

✅ Negative path unit tests

---

## Future Enhancements

Potential future improvements include:

- AI-powered recommendation engine
- Movie rating system
- User accounts and authentication
- Additional movie data APIs
- Animated UI transitions
- Social sharing features
- Advanced filtering options

---

## Author

Final Java Application Project

MovieMatch demonstrates the practical application of Java programming concepts learned throughout the course, combining API integration, persistence, validation, testing, database management, and modern Java programming techniques into a complete and functional application.
