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

## How to configure permissions
1. Go to the admin panel and click on the **Settings** in the **General** section of the left menu.
2. Click on the **Roles** tab in the **Users and Permissions Plugin** section of the sub-menu.
3. Click on the edit button next to the `Public` role and scroll down to the `Permissions` box.
4. Open the `APPLICATION` dropdown.
5. Check or uncheck permissions for each page. 

## How to add locales
1. Go to the admin panel and click on **Settings**.
2. In the sub-menu, click on *Global Settings > Internationalization*.
3. Click on the `Add a Locale` button to open the editor. 

## How to populate the pages
In the admin panel, under **Single Types**, click on the page to edit its content. The changes must be saved and published.

## How to add seasons and events
To add a season: In the admin panel, under **Collection Types**, click on `Event Seasons`.

To add an event: In the admin panel, under **Collection Types**, click on `Seasonal Events` or `Non-seasonal Events`.

Note: Although Strapi takes care of resolving the event-to-season relationship (so the season can be selected from the event or vice-versa), it is easier to add an `Event Season` first, and then updating the `Event_season` field from an event in `Seasonal Events`. 
