# Movie Booking System

This Movie Booking System is a simple web application built using React for the frontend and Node.js with Express for the backend. It allows users to select a movie, a time slot, and book seats for a movie show. The application also displays the details of the last booking made.

## Getting Started

### Prerequisites

You need to have Node.js and npm (Node Package Manager) installed on your machine.

### Installation

1. Clone the repository to your local machine:

git clone https://github.com/Nishantsingh11/Bookingapp


2. Change to the project directory:

cd Bookingapp



3. Install the backend dependencies:

cd backend
npm install



4. Install the frontend dependencies:

cd client
npm install



### Configuration

Before running the application, you need to configure the MongoDB connection URI in the `server/index.js` file. Replace the `mongoURI` variable with your MongoDB connection URI.

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
Choose a time slot for the movie show.
Select the number of seats you want to book for each seat category (e.g., A1, A2, D1, etc.).
Click the "Book Now" button to make the booking. You will receive a confirmation message upon successful booking.
Viewing Last Booking Details
The application displays the details of the last booking made on the right-hand side of the page. If no previous bookings exist, it will display a message indicating that no bookings were found.

## API
The backend of this application provides two API endpoints:

GET /api/booking: Retrieves a list of all booked movies.
POST /api/booking: Allows users to book movie tickets by providing the movie, time slot, and selected seats.
Built With
# Frontend:

React - A JavaScript library for building user interfaces.
Axios - A promise-based HTTP client for making API requests.
# Backend:

Node.js - A JavaScript runtime for building server-side applications.
Express - A web application framework for Node.js.
MongoDB - A NoSQL database for storing booking data.
License
This project is licensed under the ISC License. See the LICENSE file for details.

## Acknowledgments
This project was created as a simple movie booking system for educational purposes.
Feel free to contribute to this project or use it as a starting point for your own movie booking system. Enjoy booking your favorite movies!

Live Demo
