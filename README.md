# HodlInfo Replica

This project is a replica of the HodlInfo webpage. It fetches top 10 results from the WazirX API and displays them in a table format. The frontend is styled to closely resemble the original HodlInfo webpage.

## Features

- Fetches top 10 results from the [WazirX API](https://api.wazirx.com/api/v2/tickers)
- Stores data in a PostgreSQL database
- Serves the data using an Express server
- Frontend styled to closely match the original [HodlInfo webpage](https://hodlinfo.com/)

## Prerequisites

- Node.js
- npm
- PostgreSQL

## Installation

1. **Clone the repository:**

    ```sh
    git clone https://github.com/your-username/hodlinfo-replica.git
    cd hodlinfo-replica
    ```

2. **Install dependencies:**

    ```sh
    npm install
    ```

3. **Set up PostgreSQL:**

    - Install PostgreSQL from [here](https://www.postgresql.org/download/).
    - Create a database named `hodlinfo` and a user with password `12345`.

4. **Create the `tickers` table:**

    Open PostgreSQL Query Tool and run the following SQL command:

    ```sql
    CREATE TABLE tickers (
        id SERIAL PRIMARY KEY,
        name VARCHAR(255),
        last DECIMAL,
        buy DECIMAL,
        sell DECIMAL,
        volume DECIMAL,
        base_unit VARCHAR(255)
    );
    ```

5. **Download CSS files:**

    Download the following CSS files and place them in the `public/css` directory:
    - [main.a829415c.chunk.css](https://hodlinfo.com/static/css/main.a829415c.chunk.css)
    - [styles.css](https://hodlinfo.com/static/css/styles.css)
    - [index.css](https://hodlinfo.com/static/css/index.css)
    - [bootstrap.css](https://hodlinfo.com/static/css/bootstrap.css)
    - [2.320202e0.chunk.css](https://hodlinfo.com/static/css/2.320202e0.chunk.css)

## Usage

1. **Start the server:**

    ```sh
    node index.js
    ```

2. **Open your browser and visit:**

    ```
    http://localhost:3000
    ```

## File Structure

