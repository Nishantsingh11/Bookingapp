# Movie Booking System
This Movie Booking System is a simple web application built using React for the frontend and Node.js with Express for the backend. It allows users to select a movie, a time slot, and book seats for a movie show. The application also displays the details of the last booking made.

## Preview BookingApp 
 [Booking](https://6505401f90e9f36343c200fe--relaxed-biscochitos-28660f.netlify.app/)

## Getting Started
Prerequisites
You need to have Node.js and npm (Node Package Manager) installed on your machine.

## Installation
1. Clone the repository to your local machine:

```shell
git clone https://github.com/Nishantsingh11/Bookingapp
```
2. Change to the project directory:

```shell

cd Bookingapp
```
3. Install the backend dependencies:

```shell
cd backend
npm install
```
4. Install the frontend dependencies:

```shell
cd client
npm install
```
## Configuration
Before running the application, you need to configure the MongoDB connection URI in the server/index.js file. Replace the mongoURI variable with your MongoDB connection URI.

```javascript
const mongoURI = "YOUR_MONGODB_CONNECTION_URI";
```
Running the Application
Start the backend server:

```shell
cd backend
npm start
```
This will start the Express server, which will listen on port 8080 by default.

Start the frontend development server:
```shell

cd client
npm start
```
This will start the React development server and open the application in your default web browser.

## Usage
Booking a Movie
Select a movie from the available options.

Choose a time slot for the movie show. Select the number of seats you want to book for each seat category (e.g., A1, A2, D1, etc.).

Click the "Book Now" button to make the booking. You will receive a confirmation message upon successful booking.

Viewing Last Booking Details
The application displays the details of the last booking made on the right-hand side of the page.

If no previous bookings exist, it will display a message indicating that no bookings were found.

## API Schema Documentation
### Base URL
The base URL for the API is [URL](https://6505401f90e9f36343c200fe--relaxed-biscochitos-28660f.netlify.app/)

### Authentication
The API does not require authentication.

### Endpoints
#### GET /booking
Retrieves a list of all booked movies.

### Request
No request parameters are required.

### Response
The response is a JSON array of objects, where each object represents a booked movie. The object has the following properties:

id (string): The unique identifier of the booking.
movie (string): The name of the movie.
time (string): The time slot of the movie show.
seats (object): An object that maps seat categories to the number of seats booked for that category.
### Example Response:

```json
[
    {
        "id": "1",
        "movie": "Avengers: Endgame",
        "time": "10:00 AM",
        "seats": {
            "A1": 2,
            "A2": 1,
            "D1": 3
        }
    },
    {
        "id": "2",
        "movie": "The Lion King",
        "time": "2:00 PM",
        "seats": {
            "B1": 4,
            "B2": 2,
            "C1": 1
        }
    }
]
```

#### POST /booking
Allows users to book movie tickets by providing the movie, time slot, and selected seats.

### Request
The request body is a JSON object with the following properties:

movie (string, required): The name of the movie.
time (string, required): The time slot of the movie show.
seats (object, required): An object that maps seat categories to the number of seats to book for that category.
Example Request:

```json
{
    "movie": "Avengers: Endgame",
    "time": "10:00 AM",
    "seats": {
        "A1": 2,
        "A2": 1,
        "D1": 3
    }
}
```

### Response
The response is a JSON object with the following properties:

id (string): The unique identifier of the booking.
movie (string): The name of the movie.
time (string): The time slot of the movie show.
seats (object): An object that maps seat categories to the number of seats booked for that category.
### Example Response:

```json
{
  "id": "1",
  "movie": "Avengers: Endgame",
  "time": "10:00 AM",
  "seats": {
    "A1": 2,
    "A2": 1,
    "D1": 3
  }
}
```
## Dependencies
### Backend
- body-parser: Parse incoming request bodies
- cors: Enable Cross-Origin Resource Sharing
- express: Web application framework
- mongodb: MongoDB driver
- mongoose: MongoDB object modeling tool
- node-serialize: Serialization and deserialization utility
- nodemon: Auto-restart server during development
### Frontend
- react: JavaScript library for building user interfaces
- react-dom: React package for working with the DOM

## Acknowledgments
This project was created as a simple movie booking system for educational purposes. Feel free to contribute to this project or use it as a starting point for your own movie booking system. Enjoy booking your favorite movies!
