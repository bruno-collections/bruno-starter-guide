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

## 01 - Bruno Basics

👋 Welcome to **Day 1** of the Bruno Starter Guide!

In this challenge, you will:

- ✅ Create a new collection
- ✅ Add a folder and a request
- ✅ Use different HTTP methods
- ✅ Write your first script

Make sure to:

1. **Read the instructions** provided inside the `Instruction` folder (Docs tab).
2. **Execute the steps** in the `Challenge-01` file.

This structure will help you learn by doing—and track your progress throughout the guide!

## 02 - Environment and Collection

In this challenge, you'll learn how to use **environment variables** in Bruno. You'll be able to create and manage different environments to test your APIs under various conditions. This is a crucial step in making your API testing more flexible and efficient.

By the end of this challenge, you'll understand how to:

- Set up different environments at the collection level.
- Use environment variables to make your API tests dynamic.

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-02` file to test the environment variables.

## 03 - Send Request

In the previous challenge, you learned how to create a request. In this challenge, you'll learn how to **send a request**, select the appropriate **HTTP methods**, and send data through the body.

By the end of this challenge, you'll be able to:

- Select an HTTP method (e.g., `POST`, `GET`).
- Add JSON data to the request body.
- Send the request and view the response.

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-03` file to send a request using the `POST` method.

## 04 - Response Data & Debugging

Welcome to **Day 4** of the Bruno Starter Guide!  
Today, you're going to level up your testing game using Bruno's `req` object.

### 🎯 What You'll Learn

- 🧠 How to access and understand the `req` (request) object.
- 📬 How to view and understand API responses in the **Response** tab

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-04` file

## 05 - Authorization with News API

Welcome to **Day 5** of the Bruno Starter Guide!  
Today, you'll learn how to use **API Key Authentication** to access secure APIs — specifically the **News API**.

### 🎯 What You'll Learn

- 🌐 How to get and use an **API key** for authentication
- 🔑 Storing API keys securely using **Environment Variables**
- 🔎 Sending authenticated requests using **Query Params** in Bruno

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `challenge-05` file.

## 06 - Secret Management with .env

Welcome to Day 6 of the Bruno Starter Guide!

Bruno is a local-first API client, and one of its key features is the ability to safely manage secrets like API keys, tokens, and passwords—directly through environment variables.

In this challenge, you'll learn how to mark sensitive values as secrets in Bruno environments. This ensures that these values are handled securely and never logged or exposed accidentally.

### 🎯 What You'll Learn

- 🔐 How to mark variables as secrets in Bruno environments
- 🛡️ How secrets behave securely in Bruno (e.g., redacted in logs)
- 💡 (Optional) How to use a .env file for secret management

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-06` file.

## 07 - Scripting in Bruno

Welcome to Challenge 07!

In this challenge, you'll learn how to use scripts in Bruno to dynamically set request data like method, headers, body — and log responses.

### 🎯 What You'll Learn

By completing this challenge, you'll:

- ✅ Learn how to use the req and res objects
- ✅ Write basic scripts using Bruno's Pre-Script and Post-Script tabs
- ✅ Understand how scripting gives you full control over request execution

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-07` file.

## 08 - Assert & Testing

Welcome to **Challenge 08** of the Bruno Starter Guide! 

In this challenge, you'll explore how **assertions** and **test scripts** work in Bruno.

### 🎯 What You'll Learn

- ✅ How to write assertions using Bruno's **built-in expression UI**
- ✅ How to write custom **test scripts** using JavaScript and Chai
- ✅ Understand the difference between Assertions and Test Scripts in Bruno

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-08` file.

## 09 - Collection Runner

Welcome to Challenge 09 — Time to power up with Bruno Collection Runner!

Bruno's Runner lets you execute all requests in a collection, test performance, and run data-driven tests using CSV or JSON files.

### What You'll Learn

- ✅ Use the Collection Runner to run all your requests
- ✅ Load external data using CSV or JSON
- ✅ Access variables dynamically using {{var}} and bru.getVar()

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-09` file.

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

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-10` file.

## 11 - Git Collaboration with Bruno

Welcome to Challenge 11 — Time to collaborate using Git inside Bruno! 🧑‍💻

Bruno makes it easy to manage your collections with Git version control, whether you're using the built-in UI or the Bruno CLI. This challenge will guide you through both methods so you can choose the one that works best for your setup.

> 🔐 Note: Git UI is only available in the paid plan. If you're on the free plan, you can still follow the same steps using CLI.

### 🎯 What You'll Learn
- ✅ Initialize a Bruno collection with Git
- ✅ Commit and push changes to GitHub
- ✅ Collaborate using either Bruno UI or Bruno CLI

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-11` file.

## 12 - Working with OpenAPI Specification

Welcome to Challenge 12 of the Bruno Starter Guide!

In this challenge, you'll learn how to view and import OpenAPI Specifications (OAS) into Bruno as a collection and view OAS files.

### 🎯 What You'll Learn
- ✅ How to import an OpenAPI V3 spec into Bruno
- ✅ View and explore an API definition as a Bruno collection
- ✅ Understand how Bruno converts OpenAPI endpoints into testable requests

### 📘 How to Follow This Challenge

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-12` file.

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

1. **Read the instructions** in the `Instructions` folder.
2. **Execute the steps** in the `Challenge-13` file. 
