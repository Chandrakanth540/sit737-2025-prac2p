# Express Addition Service

## Overview
This is a simple **Express.js** service that performs an addition operation based on user-provided query parameters. The service includes error handling and logging using the **Winston** library.

## Features
- REST API to add two numbers
- Error handling for invalid inputs
- Logging using **Winston** (logs stored in `error.log` and `combined.log`)
- Runs on **port 3040**

## Installation
### Prerequisites
Ensure you have **Node.js** installed on your system.

### Steps
1. Clone this repository or copy the project files.
2. Navigate to the project directory.
   ```sh
   cd task2.1p
   ```
3. Install dependencies:
   ```sh
   npm install express winston
   ```
4. Start the server:
   ```sh
   node index.js
   ```

## Usage
The service provides an endpoint:
```http
GET /add?n1=<value>&n2=<value>
```
### Example Request
```http
http://localhost:3040/add?n1=10&n2=20
```
### Example Response
```json
{
  "statuscode": 200,
  "data": 30
}
```
### Error Response Example
If an invalid number is provided:
```json
{
  "statuscode": 500,
  "msg": "Error: n1 incorrectly defined"
}
```

## Logging
- Logs errors in `error.log`
- Stores all logs in `combined.log`

## License
This project is open-source and free to use.

