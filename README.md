# Bruno Starter Guide

## Table of Contents
1. [Basics](#01---bruno-basics)
2. [Environment and Collection](#02---environment-and-collection)
3. [Send Request](#03---send-request)
4. [Response Data & Debugging](#04---response-data-and-debugging)
5. [Authorization with News API](#05---authorization-with-news-api)
6. [Secret Management with .env](#06---secret-management-with-env)
7. [Scripting in Bruno](#07---scripting-in-bruno)
8. [Assert & Testing](#08---assert-and-testing)
9. [Collection Runner](#09---collection-runner)
10. [API Documentation](#10---api-documentation)
11. [Git Collaboration with Bruno](#11---git-collaboration-with-bruno)
12. [Working with OpenAPI Specification](#12---working-with-openapi-specification)
13. [Bruno CLI](#13---bruno-cli)

## ✅ Prerequisites
  
Before you begin, make sure you have the following:
  
- 🧑‍💻 Basic understanding of APIs and HTTP methods (GET, POST, etc.)
- 🧰 [Bruno](https://www.usebruno.com/downloads) installed on your system
- 💾 Git installed and configured (optional but recommended for collaboration)
  
---
  
## 📘 How to Use This Guide
  
Each challenge in this guide follows a consistent structure:
  
- **README Documentation:**  
  Read through the detailed instructions and explanations provided for each challenge in this README. They will guide you through the concepts and tasks.
  
- **Challenge File (Challenge-XX.bru):**  
  Each section has a corresponding Challenge file where you apply what you've learned—run requests, write scripts, and test your understanding.
  
> 💡 Start with reading the instructions for each challenge in this README file, then open the corresponding Challenge-XX.bru file to experiment and complete the challenge.
  
---
  
👉 Ready to begin? Head to the first challenge: **01 - Bruno Basics**

## 01 - Bruno Basics

👋 Welcome to **Day 1** of the Bruno Starter Guide!

In this challenge, you will:

- ✅ Create a new collection
- ✅ Add a folder and a request
- ✅ Use different HTTP methods
- ✅ Write your first script

Make sure to:

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-01.bru` file.

This structure will help you learn by doing—and track your progress throughout the guide!

### Challenge Overview
  
You'll learn the building blocks of Bruno — creating your first Collection, Folder, and Request.
  
### 📌 Prerequisites
  
- Bruno is installed and running
- You know basic API terminology (like GET/POST)
  
---
  
### 📚 Instructions
  
#### 🔧 Step 1: Create a Collection
  
1. Click on the **context menu (...)** next to the Bruno logo.
2. Select **Create Collection**.
3. Name it `First Collection` and choose a local path to save.
  
---
  
#### 📁 Step 2: Add a Folder
  
1. Right-click on the newly created collection.
2. Select **Create Folder**.
3. Name it `Basics`.
  
---
  
#### 🌐 Step 3: Add a Request
  
1. Inside `Basics` folder, click **(...)** → **Create Request**.
2. Name it `First Request`.
3. Set method to **POST**.
4. Enter URL: `https://echo.usebruno.com`

## 02 - Environment and Collection

In this challenge, you'll learn how to use **environment variables** in Bruno. You'll be able to create and manage different environments to test your APIs under various conditions. This is a crucial step in making your API testing more flexible and efficient.

By the end of this challenge, you'll understand how to:

- Set up different environments at the collection level.
- Use environment variables to make your API tests dynamic.

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-02.bru` file to test the environment variables.

### Challenge Overview
  
### Instructions
  
#### Creating Environments
  
1. Navigate to the **Environment** section (top right).
2. Click on **No Environment** and select **Configure**.
3. Click **Create Environment** and name it `echo bruno`.
4. Under your `echo bruno` environment, click **Add Variable**.
5. Enter the variable name as `base-url` and set the value to `https://echo.usebruno.com`
  
🎉 **Congratulations!** You've successfully created an environment for your collection.
  
> **Note:** Environment variables are specific to the **collection level** and can be reused across requests and folders within that collection.
  
---
  
#### Using Environments
  
1. Open the request in `Challenge-02` and enter the `{{base-url}}` in URL placeholder.
2. Ensure that you have selected the `echo bruno` environment from the environment dropdown in the top-right corner.
  
---
  
### 📌 Summary  
In this challenge, you created an environment (`echo bruno`) and used an environment variable (`base-url`) in your API request. You've now set up a flexible environment system that allows you to switch between different environments easily.

## 03 - Send Request

In the previous challenge, you learned how to create a request. In this challenge, you'll learn how to **send a request**, select the appropriate **HTTP methods**, and send data through the body.

By the end of this challenge, you'll be able to:

- Select an HTTP method (e.g., `POST`, `GET`).
- Add JSON data to the request body.
- Send the request and view the response.

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-03.bru` file to send a request using the `POST` method.

### Challenge Overview 
  
### Instructions
  
#### Step 1: Create a New Request
  
1. Click on the **Context Menu** (...) and select **New Request**.
2. Name your request as `Your Name`.
3. Set the **Request URL** to `{{base-url}}` and make sure to select `echo-bruno` as environment.
  
#### Step 2: Set HTTP Method to POST
  
1. In your new request, select the **POST** method from the dropdown next to the URL field.
  
#### Step 3: Add JSON Body Data
  
1. In the **Body** section, select **JSON** from the dropdown.
2. Add the following JSON data to the body of the request:
  
```json
{
  "title": "Bruno",
  "role": "Chief Joy Officer"
}
```
  
#### Step 4: Execute the Request
  
Click on **->** to execute the request.
  
You should receive the following response:
  
```json
{
  "title": "Bruno",
  "role": "Chief Joy Officer"
}
```
  
### 📌 Summary
  
In this challenge, you learned how to:
  
- ✅ Send a request using the **POST** method  
- ✅ Add **JSON data** to the request body  
  
Great job completing this challenge! 🎉

## 04 - Response Data & Debugging

Welcome to **Day 4** of the Bruno Starter Guide!  
Today, you're going to level up your testing game using Bruno's `req` object.

### 🎯 What You'll Learn

- 🧠 How to access and understand the `req` (request) object.
- 📬 How to view and understand API responses in the **Response** tab

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-04.bru` file

### Challenge Overview
  
In the previous challenge, you sent a `POST` request and got a JSON response using Bruno's echo server.
  
---
  
### Instructions
  
> 💡 **Tip:**  
> - The `req` object is only available in the **Pre-Script** section.  
  
#### ✅ Step 1: Use `req` object in Pre-Script
  
1. Open your request from `Challenge-03`.
2. Go to the **Pre Script** section.
3. Add the following code:
  
```js
   req.setBody({
   "name": "Bruno",
   "role": "Chief Joy Officer"
   })
``` 
  
4. Click **->** to execute the request.
  
🔍 You should see the the data we sent in your response tab.
  
---
  
### 📌 Summary
In this challenge, you learned how to:
  
✅ How to set request body using `req.setBody()` in the pre-script
  
Keep experimenting and have fun with the `req` object! 🎮

## 05 - Authorization with News API

Welcome to **Day 5** of the Bruno Starter Guide!  
Today, you'll learn how to use **API Key Authentication** to access secure APIs — specifically the **News API**.

### 🎯 What You'll Learn

- 🌐 How to get and use an **API key** for authentication
- 🔑 Storing API keys securely using **Environment Variables**
- 🔎 Sending authenticated requests using **Query Params** in Bruno

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-05.bru` file.

### Challenge Overview
  
#### 📰 What is News API?
  
**News API** is a simple HTTP API for searching and retrieving live articles from all over the web.
  
- **Website:** [https://newsapi.org](https://newsapi.org)
- **Use case:** Pull breaking news headlines or search through millions of articles in real time.
  
---
  
### Instruction
  
#### 🗝️ Step 1: Get Your API Key
  
1. Go to [https://newsapi.org](https://newsapi.org)
2. Sign up or log in to your account.
3. From your dashboard, **copy your API Key**.
  
---
  
#### 🔐 Step 2: Store the API Key as an Environment Variable
  
To keep your API key secure and reusable:
  
1. Go to Bruno Starter Guide collection.
2. Navigate to the **Environment Variables** (top right).
3. Configure new enviroment called **NEWS_API**
4. Click on **Add Variable**.
5. Add:
  
   - **Key:** `news-api-key`
   - **Value:** *(paste your News API key)*
  
> 🛡️ Tip: Avoid hardcoding your API key directly in requests—use variables instead!
  
---
  
#### 🔄 Step 3: Create Request Using the API Key
  
Let's send a request to News API to get news articles about Tesla.
  
1. Create a new request named `News Articles`.
2. Set the **Method** to `GET`.
3. Use the following URL:
```bash  
  https://newsapi.org/v2/everything?q=tesla&from=2025-03-22&sortBy=publishedAt
```
4. Go to the **Auth** tab of your request.
5. Choose **API Key** from the dropdown.
6. Fill in the following:
   - **Key:** `apiKey`
   - **Value:** `{{news-api-key}}`
7. Set the **Add To** option to: `Query Params`
  
✅ Bruno will now append your API key to the URL as a query parameter.
  
---
  
### 🚀 Step 5: Execute the Request
  
Click **Send** to run the request.
  
You should receive a JSON response with a list of news articles related to **Tesla**.
  
### 📝 Summary
  
In this challenge, you:
  
- ✅ Got an API key from NewsAPI.org
- ✅ Configured a NEWS_API environment in Bruno
- ✅ Stored your API key as an Environment Variable
- ✅ Used Bruno's API Key Auth tab with Query Params
- ✅ Retrieved and viewed real-world news data

## 06 - Secret Management with .env

Welcome to Day 6 of the Bruno Starter Guide!

Bruno is a local-first API client, and one of its key features is the ability to safely manage secrets like API keys, tokens, and passwords—directly through environment variables.

In this challenge, you'll learn how to mark sensitive values as secrets in Bruno environments. This ensures that these values are handled securely and never logged or exposed accidentally.

### 🎯 What You'll Learn

- 🔐 How to mark variables as secrets in Bruno environments
- 🛡️ How secrets behave securely in Bruno (e.g., redacted in logs)
- 💡 (Optional) How to use a .env file for secret management

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-06.bru` file.

### Secret Management
  
### 📘 Challenge Overview
  
### Instructions
  
#### Step 1: Mark Environment Variable as Secret
  
1. Open Bruno and select your environment.
  
2. Add a new variable:
  
```json
  Key: my_secret_key
  Value: Bruno'
```
  
3. Enable the "Secret" checkbox next to the variable.
  
Bruno will now treat this value as a secret—redacting it from logs and previews to protect sensitive data.
  
#### ✉️ Step 2: Use the Secret Variable in a Request
  
1. In your collection, create a request named: `env-secret`.
  
2. Set the method to POST.
  
3. Enter `{{base-url}}` URL placeholder and select `echo bruno` as environment.
  
4. Go to the Body tab and select JSON.
  
5. Add this JSON:
  
```json
{
  "secret": "{{my_secret_key}}"
}
```
  
6. Run the request.
  
You'll see the secret value reflected in the response—but it remains hidden in logs and previews for safety.
  
  
### ✅ Summary
In this challenge, you learned how to:
  
- ✅ Mark environment variables as secrets in Bruno
  
- ✅ Use secret variables securely in requests
  
You're one step closer to mastering secure and private API testing with Bruno! 🔐🚀

## 07 - Scripting in Bruno

Welcome to Challenge 07!

In this challenge, you'll learn how to use scripts in Bruno to dynamically set request data like method, headers, body — and log responses.

### 🎯 What You'll Learn

By completing this challenge, you'll:

- ✅ Learn how to use the req and res objects
- ✅ Write basic scripts using Bruno's Pre-Script and Post-Script tabs
- ✅ Understand how scripting gives you full control over request execution

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-07.bru` file.

### Challenge Overview
  
We'll set up the request dynamically using JavaScript in the `Pre-Script`, and then log the response using `Post-Script`.
  
### Instruction 
  
#### Step 1: Create a Request
  
1. Create a new request inside your Bruno collection
  
2. Name it: **first-script** and use URL: `https://echo.usebruno.com`
  
#### Step 2: Pre-Script - Set Up the Request
  
1. Go to the request -> Script tab
2. Paste the following code:
  
```javascript
req.setBody({
  "title": "Bruno",
  "Challenge No": "07"
});

req.setHeaders("Content-Type: application/json");
req.setMethod("POST");
```
  
##### ✅ This script:
  
- Sets the request method to POST
  
- Sets the content type header
  
- Sets a JSON body dynamically
  
#### Step 3: Post-Script — Log the Response
  
1. Go to the Script tab → Select Post-Script
2. Paste the following code:
```js
console.log(res.body);
console.log(res.status);
```
  
#### Step 4: Run and Observe
- Execute the request
- Open Console (via context menu ... or press Ctrl + I)
  
You should see the following logged:
  
```json
{
  "title": "Bruno",
  "Challenge No": "07"
}
```
  
### ✅ Summary
  
In this challenge, you learned how to:
  
- Write Pre-Scripts to dynamically set method, headers, and body
  
- Use Post-Scripts to log and debug responses
  
- Leverage Bruno's scripting engine to make your API testing more flexible

## 08 - Assert & Testing

Welcome to **Challenge 08** of the Bruno Starter Guide! 

In this challenge, you'll explore how **assertions** and **test scripts** work in Bruno.

### 🎯 What You'll Learn

- ✅ How to write assertions using Bruno's **built-in expression UI**
- ✅ How to write custom **test scripts** using JavaScript and Chai
- ✅ Understand the difference between Assertions and Test Scripts in Bruno

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-08.bru` file.

### Challenge Overview 
  
### Instructions
  
#### 📁 Step 1: Create a Request
  
1. In your Bruno collection, create a new request named: `assert-testing`.
2. Set the **method** to `POST`.
3. Use the following **URL**:
  
```js
https://echo.usebruno.com
```
  
4. Go to the **Body** tab.
5. Select `JSON` and paste the following payload:
  
```json
{
  "challenge_no": 8,
  "title": "Assert and Testing",
  "you_love_bruno": true
}
```

#### Step 2: Add an Assertion
  
Bruno lets you create basic assertions without writing code.
  
- Go to the Assert tab.
- Add following details:
  
✅ This assertion will check that the response status code is 200.
  
#### Step 3: Add a Test Script
  
- Go to the `Test` tab.
  
- Add the following code:
  
```js
test("Check response body contains 'title' property", function () {
  expect(res.getBody()).to.have.property("title");
});

test("You must love Bruno! 🧡", function () {
  const body = JSON.parse(res.getBody());
  expect(body.youLoveBruno).to.be.true;
});
```
  
#### Step 4: Run the Request
- Execute the request.
  
- Go to the Test section to see both your assertion and test case results.
  
You should see both tests pass! ✅
  
### 🎉 Summary
In this challenge, you learned how to:
  
- ✅ Use Bruno's built-in assertion UI
- ✅ Write custom test scripts
- ✅ Validate both status codes and response data programmatically
  
You're officially testing like a pro in Bruno! 🧪🔥

## 09 - Collection Runner

Welcome to Challenge 09 — Time to power up with Bruno Collection Runner!

Bruno's Runner lets you execute all requests in a collection, test performance, and run data-driven tests using CSV or JSON files.

### What You'll Learn

- ✅ Use the Collection Runner to run all your requests
- ✅ Load external data using CSV or JSON
- ✅ Access variables dynamically using {{var}} and bru.getVar()

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-09.bru` file.

### Challenge Overview 
  
### Instructions
  
#### Step 1: Setup the Collection
  
- Open Bruno
  
- Create a collection: `runner-example`
  
- Add a request: `runner-request`
  
- Set Method: `POST`
  
- URL: `https://echo.usebruno.com`
  
- Go to request **Body** section and select JSON from dropdown and add following code.
  
```json
{
  "name": "{{name}}",
  "job": "{{job}}"
}
```
#### Step 2: Create a Data File
  
- Create CSV or JSON file.
- Add the below data in CSV file 
  
```
name,job
John Doe,Software Engineer
Jane Smith,Product Manager
Mark Lee,Data Scientist
```
  
#### Step 3: Run the Collection
  
- Click the Runner icon (right sidebar)
  
- Check "Run with Parameters"
  
- Upload your CSV or JSON file
  
- Click Run Collection
  
You'll see each request executed with different data from your file ✅
  
### ✅ Summary
  
- You ran multiple requests using data-driven testing
  
- Automated API testing with `CSV/JSON` and Bruno Runner
  
Great job! You're now officially automating like a pro 🚀

## 10 - API Documentation

### 🎯 Goal
Help users learn how to:

- Add documentation at the collection, folder, and request levels
- Use Markdown syntax to write clean, structured, and readable API docs
- Understand the importance of documenting APIs for collaboration and long-term maintenance

### ✅ What You'll Learn
- 🗂️ Structure docs clearly at each level (collection > folder > request)
- ✍️ Use markdown features like headings, lists, code blocks, and tables
- 📚 Document request purpose, parameters, and expected responses

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-10.bru` file.

### Challenge Overview 
  
### 📁 Challenge Setup
  
- Create a new collection called `doc-demo`
  
- Inside it, create a folder: `user-endpoints`
  
- Inside the folder, create a request: `Echo Bruno`
  
- Select method: `POST` and URL: `https://echo.usebruno.com`
  
  
### ✍️ Instructions
  
#### Step 1: Add Collection-Level Docs
  
1. Right-click on the doc-demo collection → Edit Docs
  
2. Add this sample Markdown:
  
```md
# 🧾 API Collection - doc-demo
  
This collection includes user-related API endpoints.
  
## 🧰 Technologies Used
- API Client: Bruno
- Language: JavaScript (for scripting)
- Docs Format: Markdown
```
  
#### Step 2: Add Folder-Level Docs
  
1. Right-click on the user-endpoints folder.
2. Select setting and Go to Docs tab from 
  
Add:
  
```md
  
# 👤 User Endpoints
  
This folder includes requests related to user management.
  
- Get all users
- Create new user
- Update user
```
  
#### Step 3: Add Request-Level Docs
  
1. Click on the Get Users request.
2. Go to `Docs` section.
  
Add:
  
```md
# 📥 Get Users
  
**Method**: GET  
**URL**: `https://reqres.in/api/users`
  
## 🔍 Description
Fetches a list of users from the server.
  
## 📤 Response
Returns a paginated list of user objects.
  
## Example Response
  
```json
{
  "page": 1,
  "data": [
    { "id": 1, "name": "John Doe" }
  ]
}
```
## ✅ Summary
  
In this challenge, you:
  
- Learned how to add docs at collection, folder, and request levels
- Used Markdown to write beautiful API docs
- Made your Bruno collection more collaborative and readable! ✨
```

## 11 - Git Collaboration with Bruno

Welcome to Challenge 11 — Time to collaborate using Git inside Bruno! 🧑‍💻

Bruno makes it easy to manage your collections with Git version control, whether you're using the built-in UI or the Bruno CLI. This challenge will guide you through both methods so you can choose the one that works best for your setup.

> 🔐 Note: Git UI is only available in the paid plan. If you're on the free plan, you can still follow the same steps using CLI.

### 🎯 What You'll Learn
- ✅ Initialize a Bruno collection with Git
- ✅ Commit and push changes to GitHub
- ✅ Collaborate using either Bruno UI or Bruno CLI

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-11.bru` file.

### 🧑‍💻 Git Collaboration with Bruno
  
Learn how to use Git with Bruno collections for version control and collaboration.
  
#### Step 1: Create a New Collection
  
1. Open Bruno
2. Create a new collection named `git-collaboration`
3. This will be your workspace for this challenge
  
#### Step 2: Initialize Git (Choose your method)
  
##### Option A: Using Bruno UI (Paid Plan)
1. Click the Git icon near the Safe Mode toggle
2. Select "Initialize Git Repository"
3. Bruno initialize a Git repo inside the collection folder
  
##### Option B: Using CLI (Free Plan Compatible)
```bash
cd path/to/your/bruno-collection
git init
```
  
> [!NOTE]
> Bruno collections are stored as plain files, so Git works naturally with them.
  
#### Step 3: Commit Changes
  
##### Using Bruno UI
1. Make edits (e.g., add headers, body, etc.)
2. Open the Git panel via the Git icon -> Git UI.
3. Stage changes with the + icon
4. Enter a commit message:
   ```
   Initial commit of Bruno Git Collaboration collection
   ```
5. Click Commit
  
##### Using CLI
```bash
git add .
git commit -m "Initial commit of Bruno Git Collaboration collection"
```
  
#### Step 4: Create GitHub Repository
  
1. Go to GitHub and log in
2. Click New Repository
3. Name it `bruno-git-collab` (or similar)
4. Choose visibility: public or private
5. Click Create Repository
6. Copy the HTTPS URL:
   ```
   https://github.com/yourusername/bruno-git-collab.git
   ```
  
#### Step 5: Add Remote and Push
  
##### Using Bruno UI (Paid Plan)
1. In Bruno's Git panel, go to Remotes > Add Remote
2. Name: `origin`
3. URL: Paste your GitHub URL
4. Click Push to upload your collection
  
##### Using CLI (Free Plan Compatible)
```bash
git remote add origin https://github.com/yourusername/bruno-git-collab.git
git branch -M main
git push -u origin main
```
  
### Summary
  
In this challenge, you successfully:
  
- ✅ Created a new Bruno collection
- ✅ Initialized Git using UI or CLI
- ✅ Committed and pushed changes to GitHub
- ✅ Learned how to collaborate using Bruno + Git
  
Whether you're working solo or as part of a team, Bruno's Git integration supports flexible workflows to match your tools and license.
  
Happy collaborating! 🚀

## 12 - Working with OpenAPI Specification

Welcome to Challenge 12 of the Bruno Starter Guide!

In this challenge, you'll learn how to view and import OpenAPI Specifications (OAS) into Bruno as a collection and view OAS files.

### 🎯 What You'll Learn
- ✅ How to import an OpenAPI V3 spec into Bruno
- ✅ View and explore an API definition as a Bruno collection
- ✅ Understand how Bruno converts OpenAPI endpoints into testable requests

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-12.bru` file.

## 13 - Bruno CLI

Welcome to Challenge 13 — Let's run your API tests from the terminal like a real automation pro!

Bruno CLI lets you run your collections directly from the command line, perfect for CI/CD pipelines and automated workflows.

### What You'll Learn

- ✅ Install and use the Bruno CLI tool
- ✅ Run requests and collections via terminal
- ✅ Use environments in CLI runs
- ✅ Validate status codes directly from the command line

### Prerequisites
Make sure you have:

1. Node.js installed
2. A Bruno collection ready with at least one request

### 📘 How to Follow This Challenge

1. **Read the instructions** below.
2. **Execute the steps** in the `Challenge-13.bru` file.

### 📝 Challenge Overview
  
  
In this challenge, you'll:
  
- Install the Bruno CLI tool
  
- Create an environment for your collection
  
- Run the request using CLI and verify the output
  
Let's get started!
  
### Instructions
  
#### Step 1: Install Bruno CLI
  
Open your terminal and run:
  
```bash
 npm install -g @usebruno/cli
```
  
#### 📁 Step 2: Navigate to Your Bruno Collection
  
Use cd to go into the root folder of your Bruno collection:
  
```bash
 cd path/to/your/bruno-collection
```
  
#### 🌍 Step 3: Create an Environment
  
In Bruno:
  
1. Go to the Environment dropdown (top right)
  
2. Click Configure
  
3. Create a new environment called: `prod`
  
4. Add a variable: `base-url → https://echo.usebruno.com` and Save the environment.
 
5. Use `{{base-url}}` variable in URL input.
  
  
#### 🚀 Step 4: Run Collection with Environment
  
In the terminal, run the following:
  
```bash
bru run --env prod
```
  
✅ Your requests will run, and you should see a `200` OK response printed in the console.
  
### ✅ Summary
  
In this challenge, you:
  
- Installed Bruno CLI using npm
  
- Configured an environment
  
- Ran your collection through the terminal
  
- Verified successful API execution via status codes
  
🎉 You're now ready to integrate Bruno into automation and CI workflows like a boss!