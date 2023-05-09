# Turborepo project - Github Actions - Azure App Service

This project is a monorepo project using Turborepo and using Github Actions for CI/CD to deploy to Azure App Service.
- [Azure App Service](https://azure.microsoft.com/en-us/products/app-service)
- [Turborepo](https://turbo.build/repo/docs)
- [Github Actions](https://github.com/features/actions)
## Workspaces
- web
  - `main_web-app-2-ws.yml`: workflow file for `web` workspace
- docs
  - `main_docs-app-ws.yml`: workflow file for `docs` workspace

## Configure to start app
- `web` workspace:
  - Update Startup Command in Configuration of Azure App Service: `npm run start:web`
  - Set start `script` in `package.json`
  ```
    "scripts": {
        ...
        "start:web": "node_modules/next/dist/bin/next start apps/web",
        ...
     }
  ```
- `docs` workspace: refer `web` workspace configuration above
