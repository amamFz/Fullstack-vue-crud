# My Full Stack App

This is a simple full stack application using Node.js, Express, Vue.js, and Prisma connected to a MySQL database.

## Getting Started

Follow these instructions to set up and run the project locally.

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine.
- [Git](https://git-scm.com/) installed on your machine.
- [MySQL](https://www.mysql.com/) installed and running on your machine.

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/amamFz/Fullstack-vue-crud.git
    ```

2. Set up environment variables:

    ```bash
    cd backend-express
    cp .env.example .env
    ```

    Edit the `.env` file with your database credentials:

    ```env
    DATABASE_URL="mysql://USER:PASSWORD@HOST:PORT/DATABASE"
    ```

    Replace `USER`, `PASSWORD`, `HOST`, `PORT`, and `DATABASE` with your MySQL database details.

3. Install backend dependencies:

    ```bash
    npm install
    ```

4. Set up the database:

    ```bash
    npx prisma migrate dev --name init
    npx prisma generate
    ```

5. Install frontend dependencies:

    ```bash
    cd frontend-vue
    npm install
    ```

### Running the Application

1. Start the backend server:

    ```bash
    cd backend
    npm start
    ```

2. Start the frontend development server:

    ```bash
    cd ../frontend
    npm run serve
    ```
