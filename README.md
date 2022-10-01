# Zendesk Marketing App Template

This project contains the basics needed to publish a marketing only app on the Zendesk Marketplace.

Follow the steps below to tweak the projects settings to get the desired app in Zendesk.

## Creating a new app

1. Copy this whole project into another folder

2. Edit the `zat/manifest.json` file
    * Change the application name
    * Change the author details if required
    * Remove any location you are not interested in. This setting specifies which area of Zendesk the app will live in for your customers. [See here for more details](https://developer.zendesk.com/documentation/apps/app-developer-guide/setup/#setting-the-app-location)
    * If you wish for a language other than English to be the default, change the language code. Make sure you have a `translation.json` file to match if you do.

3. Copy over the following assets in the `zat/assets` folder. [See here for more information about asset requirements](https://developer.zendesk.com/documentation/apps/publish-your-app-or-theme/create_assets/#marketing-assets)
    * `logo.png` - Main logo show in the marketplace. Must be 320x320 pixels, PNG format, no rounded corners
    * `logo-small.png` - Most seen logo. Must be 128x128 pixels, PNG format, visible on both light and dark backgrounds, no rounded corners
    * `screenshot-[0,1,2].png - Three screenshots must be supplied. The number gives the order they will be show (0 first). 1024x768 pixels, PNG format, no rounded corners.

4. Edit the copy inside each of the `translations` json files with the desired copy for each language you want to support. If you want to add languges just create a file with the two letter ISO code for the language you wish to support and copy one of the examples given. [See here for more information on the translation files](https://developer.zendesk.com/documentation/apps/publish-your-app-or-theme/create_content/#enjson-file)
    * `name` - The application name
    * `short_descrpition` - The short tagline under the app name in the marketplace
    * `long_descriptiion`- The long description for the app in the **Description** tab. This field supports markdown which you can use to format the content. [Read more about Markdown formatting here](https://daringfireball.net/projects/markdown/syntax)
    * `install_instructions` - The content that will live in the **How to setup** tab. Also supports markdown for formatting.

5. Create a **zip** archive of the `zat` folder. Use whatever tool your OS provides for making `.zip` files to do this.
**NOTE** you need to make sure you are not just zipping up the zat folder. It must be the contents of it for Zendesk to accept it.

6. Head to your Zendesk apps account and to the apps section. Upload the zip file created in step 5 and submit for approval. [See here for more details on app submission](https://developer.zendesk.com/documentation/apps/publish-your-app-or-theme/submit_your_app/)