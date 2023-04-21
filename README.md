# Strapi application

The steps below assume an environment that meets the prerequisites in the [Strapi deployment page](https://docs-v3.strapi.io/developer-docs/latest/setup-deployment-guides/deployment.html).

## Configure the application
The app requires the following environment variables:
- `DATABASE_URL`: the postgres connection string (`postgres://<user>:<password>@<host>:<port>/<database>?<query>`)
- `MY_HEROKU_URL`: public url of the server (or `''`). Used to generate links (e.g. admin)

## Launch the server
Build the admin panel:
```shell
NODE_ENV=production npm run build
```

Run the server:
```shell
NODE_ENV=production npm start
```

## Configure permissions
1. Go to the admin panel and click on the **Settings** in the **General** section of the left menu.
2. Click on the **Roles** tab in the **Users and Permissions Plugin** section of the sub-menu.
3. Edit the `Public` role and check off the following permissions:
  * BATHROOMS: find
  * ERROR-404-PAGE: find
  * HOME-PAGE: find

## Configure locales
1. Go to the admin panel and click on **Settings**.
2. In the sub-menu, click on *Global Settings > Internationalization*.
3. Add the following locales:
- es 

## Populate the pages
  In the admin panel, under Single Types, populate the following: (save and then publish)
- Error 404 Page (en and es)
- Home Page

Every page must be populated in both the en and es locales.

---------------------------
SIngle Types -> Home Page
