Prompt-Powered Kickstart: Getting Started with Go (Golang)
1. Title & Objective
Technology Chosen: Go (Golang)
Why I Chose Go

I chose Go because it is a beginner-friendly, modern programming language that is widely used in backend development and cloud systems. It is simple to read, fast, and powerful.

Go is also used to build major real-world tools, which makes it a valuable skill to learn.

End Goal

The goal of this toolkit is to:

Install Go

Set up a simple project

Build and run a minimal HTTP web server

Display the message:

Hello, World from Go!
2. Quick Summary of the Technology

Go (also called Golang) is a programming language created by Google in 2009.

What is Go?

Go is a compiled, statically typed programming language designed to be:

Simple

Fast

Efficient

Easy to maintain

Where is it used?

Go is commonly used for:

Backend APIs

Cloud computing

DevOps tools

Microservices

Web servers

Real-World Examples

Some popular tools written in Go include:

Docker

Kubernetes

Terraform

3. System Requirements

To follow this guide, you need:

Operating System: Windows, macOS, or Linux

Terminal or Command Prompt

Internet connection

Text editor (VS Code recommended)

Check if Go is installed:

go version

If installed correctly, it should show something like:

go version go1.21.0 windows/amd64
4. Installation & Setup Instructions
Step 1: Install Go

Visit the official website:
https://go.dev/dl/

Download the installer for your operating system.

Run the installer and follow the setup instructions.

Verify installation:

go version
Step 2: Create a New Project Folder

Open your terminal and run:

mkdir go-hello-world
cd go-hello-world
Step 3: Initialize a Go Module
go mod init hello

This creates a go.mod file to manage dependencies.

Step 4: Create main.go

Create a file named main.go and paste the following code:

package main

import (
	"fmt"
	"net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintln(w, "Hello, World from Go!")
}

func main() {
	http.HandleFunc("/", handler)
	fmt.Println("Server running at http://localhost:8080")
	http.ListenAndServe(":8080", nil)
}
Step 5: Run the Program

In your terminal, run:

go run main.go

You should see:

Server running at http://localhost:8080

Open your browser and go to:

http://localhost:8080

Expected output:

Hello, World from Go!
5. Minimal Working Example Explanation

This program:

Imports Go’s built-in net/http package.

Creates a function called handler.

Starts a web server on port 8080.

Displays a message when someone visits the homepage.

This is a minimal backend server built entirely with Go’s standard library.

6. AI Prompt Journal

Prompt 1

Prompt Used:

“Give me a beginner-friendly step-by-step guide to build a simple HTTP server in Go.”

AI Response Summary:

The AI explained:

How to install Go

How to initialize a module

How to create a main.go file

How to start an HTTP server

Helpfulness Evaluation:

Very helpful. It simplified complex concepts and gave me structured steps to follow.

Prompt 2

Prompt Used:

“I am getting error: go: command not found. How do I fix it?”

AI Response Summary:

The AI explained that:

Go might not be installed

The PATH variable may not be configured

Restarting terminal may fix the issue

Helpfulness Evaluation:

Helped me troubleshoot installation issues quickly.

Prompt 3

Prompt Used:

“Explain what http.HandleFunc does in simple terms.”

AI Response Summary:

AI explained that:

It connects a URL path to a function

When someone visits that URL, the function runs

Helpfulness Evaluation:

Improved my understanding of how routing works in Go.

Reflection on AI Usage

Using AI:

Reduced setup confusion

Helped debug errors faster

Made complex documentation easier to understand

Increased my confidence as a beginner

AI significantly improved my learning speed and clarity.

7. Common Issues & Fixes
Problem	                        Cause	                        Solution
go: command not found	Go not installed or PATH not set	Reinstall Go and restart terminal
cannot find module	    Module not initialized	            Run go mod init hello
port already in use	    Another program using port 8080	    Change port to 9090 in code
Browser shows nothing	Server not running	                Make sure go run main.go is active

8. Testing & Peer Feedback

I asked a peer to follow my setup guide.

Feedback received:

The instructions were clear.

Installation steps were easy to follow.

Adding screenshots would improve clarity.

Improvements made:

Added clearer command formatting.

Included expected output examples.

9. References

Official Go Documentation: https://go.dev/doc/

Go Tour: https://go.dev/tour/

Go by Example: https://gobyexample.com/

YouTube: Go Crash Course Tutorials