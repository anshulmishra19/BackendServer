# BackendServerform

# Google Forms Replica - Backend

## Overview

This is the backend server for the Google Forms Replica project. It is built using Express and TypeScript, and uses a JSON file as a database to store submissions.

## Prerequisites

- Node.js and npm

## Setup Instructions

### Step 1: Clone the Repository

```bash

git clone https://github.com/yourusername/GoogleFormsReplica.git
Step 2: Navigate to the Backend Directory
bash
Copy code
cd GoogleFormsReplica/BackendServer
Step 3: Install Dependencies
bash
Copy code
npm install
Step 4: Configure TypeScript
Ensure the tsconfig.json is correctly set up. It should look like this:

json
Copy code
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true
  },
  "include": ["src"],
  "exclude": ["node_modules"]
}
Step 5: Add Start Script in package.json
Add the following script in your package.json:

json
Copy code
"scripts": {
  "dev": "ts-node-dev src/index.ts"
}
Step 6: Run the Server
Start the server using the following command:

bash
Copy code
npm run dev
API Endpoints
Ping - /ping [GET]
Always returns true.

Response:

json
Copy code
{
  "success": true
}
Submit - /submit [POST]
Submits a new form entry.

Parameters:

json
Copy code
{
  "name": "string",
  "email": "string",
  "phone": "string",
  "github_link": "string",
  "stopwatch_time": "string"
}
Response:

json
Copy code
{
  "message": "Submission saved successfully"
}
Read - /read [GET]
Retrieves a submission by index.

Query Parameter:

json
Copy code
{
  "index": 0
}
Response:

json
Copy code
{
  "name": "string",
  "email": "string",
  "phone": "string",
  "github_link": "string",
  "stopwatch_time": "string"
}
or

json
Copy code
{
  "message": "Submission not found"
}
Database Structure
The submissions are stored in a JSON file named db.json. Each submission is an object with the following structure:

json
Copy code
{
  "submissions": [
    {
      "name": "string",
      "email": "string",
      "phone": "string",
      "github_link": "string",
      "stopwatch_time": "string"
    }
  ]
}
Contribution
Contributions are welcome! Open an issue or submit a pull request.

License
MIT License

less
Copy code

Make sure to replace `https://github.com/yourusername/GoogleFormsReplica.git` 
