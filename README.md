# Travel Tracker

Travel Tracker is a web application to track visited countries.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)

## Setup

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/travel-tracker.git
    cd travel-tracker
    ```

2. **Install dependencies:**

    ```bash
    npm install
    ```

3. **Create a PostgreSQL Database:**

    - Open PostgreSQL and create a new database named `world`.

4. **Import the Countries CSV:**

    - In the PostgreSQL database `world`, import the `countries.csv` file provided in the project:

    ```bash
    COPY countries FROM '/path/to/countries.csv' DELIMITER ',' CSV HEADER;
    ```

5. **Configure Database Connection:**

    - Open `index.js` and update the PostgreSQL connection parameters in the `db` configuration:

    ```javascript
    const db = new pg.Client({
      user: "your-postgres-username",
      host: "localhost",
      database: "world",
      password: "your-postgres-password",
      port: 5432,
    });
    ```

6. **Run the Application:**

    ```bash
    npm start
    ```

    The application will be accessible at [http://localhost:3000](http://localhost:3000).
