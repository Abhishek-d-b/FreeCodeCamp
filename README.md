# Timestamp Microservice

This is a simple **Timestamp Microservice** built with Node.js and Express. The service provides a date in both Unix and UTC formats based on a user-supplied date or Unix timestamp. If no date is provided, it returns the current date.

## Project Purpose

This project is part of the [FreeCodeCamp Back End Development and APIs](https://www.freecodecamp.org/learn/back-end-development-and-apis/) curriculum.

## Features

- Given a valid date, the service returns a JSON response with Unix and UTC time.
- If a Unix timestamp is passed, it will return the corresponding date in UTC.
- If no date is passed, the service returns the current date in Unix and UTC formats.
- Invalid dates return an error message: `{ "error": "Invalid Date" }`.

## API Endpoints

- **`/api/:date?`**
  - `date`: A valid date string or Unix timestamp (optional).
  - Example:
    - `/api/2015-12-25` returns:
      ```json
      { "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }
      ```
    - `/api/1451001600000` returns:
      ```json
      { "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }
      ```
    - `/api/` (no parameter) returns the current date.
    - `/api/invalid-date` returns:
      ```json
      { "error": "Invalid Date" }
      ```

---

## Getting Started

### Prerequisites

Make sure you have the following installed on your local machine:

- [Node.js](https://nodejs.org/) (v12.x or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

1. Clone the repository from GitHub:

   ```bash
   git clone https://github.com/Abhishek-d-b/timestamp-microservice.git
   ```
