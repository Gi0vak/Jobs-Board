# Recruitment Application

This is a web application built using React JS that allows users to view job postings from partner companies and apply for them. The application uses NodeJS and MongoDB for the backend, providing a REST API that allows for listing, creating, updating, and deleting job postings. The following dependencies were used in the application:

- "@testing-library/jest-dom": "^5.16.5"
- "@testing-library/react": "^13.4.0"
- "@testing-library/user-event": "^13.5.0"
- "axios": "^1.3.6"
- "cors": "^2.8.5"
- "dotenv": "^16.0.3"
- "moment": "^2.29.4"
- "mongoose": "^7.0.4"
- "react": "^18.2.0"
- "react-dom": "^18.2.0"
- "react-media": "^1.10.0"
- "react-router-dom": "^6.10.0"
- "react-scripts": "5.0.1"
- "web-vitals": "^2.1.4"

There is no real authentication system, but the application has several pages, including a home page, a search page, a page for updating a single job posting, a page for creating a new job posting, a page for displaying a single job posting, and a 404 error page.

## Installation

To install the application, clone the repository and navigate to the project directory. Then, install the dependencies using the following command:

```bash
npm install
```

Create a .env file in the root directory of the project with the following variables:

```bash
DB_HOST=<your MongoDB database URL>
DB_NAME=<name of the MongoDB database>
```

## Running the Application

To run the application in development mode, use the following command:

```bash
npm start
```

This will start the development server on `http://localhost:3000`.

## Backend API

The backend API provides the following endpoints:

### List all job postings

```
GET /api/jobs
```

Returns a list of all job postings in the database.

### Get a single job posting

```
GET /api/jobs/:id
```

Returns a single job posting with the specified ID.

### Create a new job posting

```
POST /api/jobs
```

Creates a new job posting with the specified data.

### Update a job posting

```
PUT /api/jobs/:id
```

Updates the job posting with the specified ID.

### Delete a job posting

```
DELETE /api/jobs/:id
```

Deletes the job posting with the specified ID.

### Search for job postings

```
GET /api/jobs/search?query=<search query>
```

Returns a list of job postings that match the specified search query.

## Job Posting Data Structure

Job postings are structured as follows:

```
id: Number
company: String
logo: String
logoBackground: String
position: String
postedAt: Date
contract: String
location: String
website: String
apply: String
description: String
requirements: {
    content: String,
    items: [String]
}
role: {
    content: String,
    items: [String]
}
```

The `id` field is a unique identifier for the job posting. The `company` field is the name of the company offering the job. The `logo` field is the URL of the company's logo in SVG format. The `logoBackground` field is the background color to be used behind the logo. The `position` field is the name of the job position. The `postedAt`
