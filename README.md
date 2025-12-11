
# PeerLink – Peer-to-Peer File Sharing

PeerLink is a simple project that lets users share files directly between two devices using a small invite code. It uses a Java backend for handling file transfers and a Next.js frontend for the user interface.

## What It Does
- Upload a file from your device  
- Get an invite code (a port number)  
- Share the invite code with someone else  
- They enter the code and download the file directly from you  

The main idea is to avoid storing files on a server and instead connect two users directly.

## Project Structure
- **Backend (Java / Maven):** Handles file uploads, generates invite codes, starts a small file server for each file  
- **Frontend (Next.js / React):** Simple UI for uploading files and entering invite codes  
- **Scripts:** `start.sh` and `start.bat` for quickly starting both backend and frontend

## How It Works (Simple Flow)
1. You upload a file  
2. Backend saves it and opens a temporary port  
3. Backend gives you that port as the invite code  
4. Another user enters the invite code  
5. The file transfers directly from your machine to theirs  

## Getting Started

### Backend
```bash
mvn clean package
java -jar target/p2p-1.0-SNAPSHOT.jar
````

### Frontend

```bash
cd ui
npm install
npm run dev
```

Visit the app at: **[http://localhost:3000](http://localhost:3000)**

## Tech Used

* **Backend:** Java, Maven
* **Frontend:** Next.js, React
* **Other:** WebSockets, REST APIs


