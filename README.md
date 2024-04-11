# Technical Test - Readme

## 1. Local Development Guideline

### Prerequisites

- `Docker` & `Docker Compose`
- NodeJS (v10 or above), `npm` and `yarn`
- `Makefile`

### Setup Local Development Environment

1. Clone the project to local machine and go to the folder

```
git clone https://github.com/DaiThanh97/chat-app.git
cd chat-app
```

2. Run `make bootstrap` cli to bootstrap all the application

**OR**

1. Start local DB with Docker-CLI (Can change env values if you want)

```
 docker run --name postgres -e POSTGRES_USER=root -e POSTGRES_PASSWORD=root123123 -e POSTGRES_DB=chat -p 5432:5432 -d postgres
```

2. Run the back-end in development mode (live-reload support). Change `.env.example` to `.env` to bootstrap correctly.

```
cd backend && npm run dev
```

3. Run the frontend in development mode (live-reload support). Change `.env.example` to `.env` to bootstrap correctly.

```
cd frontend && npm run dev
```

4. The app should be accessible at http://localhost:3000. The API can be accessed at http://localhost:5000/api/v1

**NOTE**: The local DB will use port **5432**. If the port is being used, please change it to a different port in `docker-compose.yml` and `backend/.env.example`

### Useful commands

1. If you want to reset client or server separately, go to `frontend`, `backend` folders and run `npm run dev`, `npm run dev` in each folder.

## 2. Other Notes

### What I have completed

### 1. Functionalities

1. Login: Feature to log user in
2. Sign Up: Register user into the system
3. Chat
4. Share videos: Share youtube videos which receives array of youtube video urls `(Only logged in user can shared)`.

### 2. Others

1. Local Development Setup script (1 line setup with Docker)
