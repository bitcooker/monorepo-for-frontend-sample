## Sample monorepo for frontend project using lerna

### Technologies
- Frontend : Next.js, Redux
- Build System : Lerna
- Typescript
- Docker

### Getting the app up and running
- In the root directory, `npm i` to install every required dependencies.
- Run `npx lerna clean -y`, this will clean up the node_modules folders of sub apps.
- `npm run dev` to start up development environment.

#### Installing additional packages and dependencies
In case the client or server sub-application requires additional package, follow these steps:

Move to the appropriate sub directory, e.g. cd packages/frontend-web-app
Install the package `npm i ....`
After installation has finished, move back to the root directory.
Run `npx lerna clean -y`, this will clean up the node_modules folders of sub apps.


### Docker Deployment
To build and run the Docker container:
1. Build the Docker image:
   `docker build -t frontend-web-app`
2. Run the Docker container:
   `docker run -p 3000:3000 frontend-web-app`
