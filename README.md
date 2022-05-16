# Stackbit Next.js Contentful Starter

A simple starting point for a Stackbit project with [Contentful](https://www.contentful.com/).

## Contributing

To contribute to this starter, please follow the following steps:

1. Clone this repository locally

2. Create a new Space in Contentful

3. Create new Contentful Personal Access Tokens [here](https://app.contentful.com/account/profile/cma_tokens/)

4. Install dependencies

   ```shell
   npm install
   ```

5. Import the Contentful data stored in the `contentful/export.json` file to the new space by running the following command. Replace the `<management_token>` with your Personal Access Token and the `<space_id>` with the new space ID.

   ```shell
   ./contentful/import.js <management_token> <space_id>
   ```

6. Create "**Content Preview API - Access Token**" for the new space via Contentful app "Settings" => "API Keys" => "Content delivery / preview tokens" => "Add API Key".

7. Define the following environment variables to allow Next.js to fetch the content from Contentful when developing or building the site. Replace the `{SPACE_ID}` with your Space ID and the `{CPA}` with the new **Content Preview API - Access Token**.

   ```shell
   export CONTENTFUL_SPACE_ID={SPACE_ID}
   export CONTENTFUL_PREVIEW_TOKEN={CPA}
   ```

8. Lastly, run the Next.js development server:

   ```shell
   npm run dev
   ```

   Navigate to [http://localhost:3000](http://localhost:3000) to see the site.

9. Now you can update site code, and the content in Contentful. The browser will automatically live-update your changes.

10. Once you finish updating the code and contents, export the contents back to the `contentful/export.json` file by running the following command. Replace the `<management_token>` with your Personal Access Token and the `<space_id>` with the new space ID.

    ```shell
    ./contentful/export.js <management_token> <space_id>
    ```

11. Commit, push and submit a pull-request

## Learn the Basics

Follow the [getting started tutorial](https://docs.stackbit.com/getting-started/) while running this project locally to get a feel for how Stackbit works.

Or jump to individual topics [in the docs](https://docs.stackbit.com/).

## Support & Feedback

[Join us on Discord](https://discord.gg/HUNhjVkznH) for community support and to provide feedback to us.
