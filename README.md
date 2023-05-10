"# ws2024s17hu-r3-docker"

# WS2024 S17 R3 HU Test Project

## Setup

### **Laravel Backend + Laravel Admin**

```shell
docker-compose -f docker-compose.yml -f backend.laravel.docker-compose.yml -f admin.laravel.docker-compose.yml up -d
```

### **Laravel Backend + JS Admin**

```shell
docker-compose -f docker-compose.yml -f backend.laravel.docker-compose.yml -f admin.js.docker-compose.yml up -d
```

### **Node.js Backend + JS Admin**

```shell
docker-compose -f docker-compose.yml -f backend.nodejs.docker-compose.yml -f admin.js.docker-compose.yml up -d
```

### _Node.js Backend + Laravel Admin_

```shell
docker-compose -f docker-compose.yml -f backend.nodejs.docker-compose.yml -f admin.laravel.docker-compose.yml up -d
```

## URLs

- Admin app: http://admin.ub2023-YY.hu
- Runner app: http://runner-app.ub2023-YY.hu
- Stage Planner app: http://stage-planner.ub2023-YY.hu
- Backend: http://backend.ub2023-YY.hu
- Backend-2: http://backend-2.ub2023-YY.hu
- PhpMyAdmin: http://pma.ub2023-YY.hu

In local environment:
- Admin app: http://admin.localhost
- Runner app: http://runner-app.localhost
- Stage Planner app: http://stage-planner.localhost
- Backend: http://backend.localhost
- Backend-2: http://backend-2.localhost
- PhpMyAdmin: http://pma.localhost


## Development

### Frontend

#### With framework

1. Copy the base project from the assets folder to the www/[task].src folder
2. Start the app with `npm run start`. You will be able to preview your work on localhost.
3. When you are done, **deploy it** by building, and moving the compiled assets to the www/[task] folder

#### Without framework

1. Work in the www/[task] folder
2. You will be able to preview your work on http://[task].ub2023-YY.hu (http://[task].localhost)

---

### Backend

#### Database

- Host: `db.ub2023.hu`
- Username: `root`
- Password: `password`

#### Laravel

1. Work in `www/backend-laravel`.
2. Preview your work at http://backend.ub2023-YY.hu (http://backend.localhost)

#### Node.js

1. Work in `www/backend-nodejs`. The entrypoint for your application is `www/backend/app.js`.
2. Preview your work at `http://backend.ub2023-YY.hu`. The application automatically reloads using nodemon.
3. To view the console, use the following command:

```shell
docker-compose -f docker-compose.yml -f docker-compose.nodejs.yml logs -ft backend
```

---

### Admin

#### Laravel

- Work in `www/admin-laravel`.
- Preview your work at http://admin.ub2023-YY.hu (http://admin.localhost)

#### JS Framework

- Deploy your work to `www/admin-js`.
- Preview your deployed work at http://admin.ub2023-YY.hu (http://admin.localhost)
