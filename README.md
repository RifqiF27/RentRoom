## Rent Room Web App

The Rent Room Web App simplifies the process of finding, booking, and managing rooms. This platform allows users to create profiles, browse listings with detailed room information, view photos, and explore amenities. Smart filters are provided to refine searches and enhance the user experience.

### Features

- **User Profiles:**
  - Users can create and manage profiles, providing necessary information.
  - Profile data includes personal details, contact information, and preferences.

- **Room Listings:**
  - Detailed room information, including facilities, room capacity, location, and pricing.
  - High-quality photos to showcase each room.

- **Smart Filters:**
  - Users can refine their searches using smart filters such as location.

- **Management Dashboard:**
  - Dashboard for users to manage their bookings, view reservation history, and update personal information.

### Getting Started

Follow the steps below to set up and run the Rent Room Web App locally.

### Prerequisites

- Node.js: [Download and Install Node.js](https://nodejs.org/)
- PostgreSQL: [Install PostgreSQL](https://www.postgresql.org/download/)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/RifqiF27/RentRoom.git
   ```

2. Navigate to the project directory:

   ```bash
   cd RentRoom
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Set up environment variables:

   - Create a `.env` file in the root directory.
   - Define the following variables:

     ```env
     PORT=3000
     DATABASE_URL=postgres://your-username:your-password@localhost:5432/rentroom
     SECRET_KEY=your_secret_key
     ```

   - Replace `your-username` and `your-password` with your PostgreSQL username and password.

5. Start the application:

   ```bash
   npm start
   ```

6. Open your web browser and visit [http://localhost:3000](http://localhost:3000) to access the Rent Room Web App.


### API Documentation

Explore the API endpoints and authentication details in the [API Documentation](https://github.com/RifqiF27/RentRoom/blob/main/server/Restfull-Api-Doc.md).

### Technologies Used

- Node.js
- Express.js
- PostgreSQL
- HTML, CSS, JavaScript
- Vue
- Pinia
- AWS
- Firebase
- Bootstrap
