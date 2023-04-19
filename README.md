"# ws2024s17hu-r3-docker" 

# WS2024 S17 R3 HU Test Project
## Setup
### PHP / Laravel backend

```shell
docker-compose -f docker-compose.yml -f docker-compose.php.yml up -d
```
### Node.js backend

```shell
docker-compose -f docker-compose.yml -f docker-compose.nodejs.yml up -d
```
## URLs
- Admin app: http://admin.localhost
- Runner app: http://runner-app.localhost
- Stage Planner app: http://runner-app.localhost
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
2. You will be able to preview your work on http://[task].localhost

---

### Backend
#### Database
- Host: `db`
- Username: `root`
- Password: `password`

#### Laravel
1. Work in `www/backend-laravel`.
2. Preview your work at `http://backend.localhost`

#### Node.js
1. Work in `www/backend-nodejs`. The entrypoint for your application is `www/backend/app.js`.
3. Preview your work at `http://backend.localhost`. The application automatically reloads using nodemon.
4. To view the console, use the following command: 
```shell
docker-compose -f docker-compose.yml -f docker-compose.nodejs.yml logs -ft backend
```