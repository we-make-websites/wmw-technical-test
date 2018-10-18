# We Make Websites - Technical Test

> This is an entry level test that we require all front-end developer candidates trial before proceeding into the final stage. We do not pay or use any of the work produced on a commercial environment.

If you have come directly to this repository without a reference and curious to trial out this test - then please contact daniel@wemakewebsites.com to get yourself started!

## Brief
You have been provided a link to a Shopify development environment which contains only a basic header and also a list of unstyled product cards. 

We would like you to *only* style the `featured-collection.liquid` section in your starter theme to match the supplied designs. [Invision Link](#) There are interactions and hotspots within the Invision prototype that you should consider for the bonus tasks.

We have supplied both mobile and desktop designs but we would like you to have a think on how the components respond to the sizes in between. The solution is open for your interpretation.

The `/src/sections/featured-collection.liquid` contains the necessary Liquid markup required for the design to function - but you are encouraged to add in your own custom HTML/Liquid to make your build work with the designs.

*Bonus: User interaction*
One of the most important things in eCommerce is user experience through interactivity. We would like you to have a think about how you could improve the experience by adding an extra layer of interactions.

*Bonus: Javascript*
If time allows and you’re up for the challenge, then you can also look into creating a basic Quick Add functionality. A standard Quick Add in eCommerce is when a user clicks on the Add to cart button - this will directly add the product to the user’s cart via an AJAX call whilst staying on the same page. The desired functionality is shown in the Invision Prototype.

There are some relevant documentation below in the Useful Resources section regarding AJAX calls with Shopify.

There is a `featured-collection.js` script in the `/src/sections/` directory which registered the Section in Shopify. All your functionality should be contained in this file. You are open to use third party packages as well as a Framework if you feel more comfortable.

> You can test if the function has been successful by navigating to the `https://wmw-technical-test.myshopify.com/cart` page or by visiting the  `https://wmw-technical-test.myshopify.com/cart.json` url to see if a product data has been added to your cart.

## Getting started

To get started with the technical test, you will need to make a clone of this repo and run the following commands in the project folder:

1. *Install project dependencies*
This command will install the Shopify theme dependencies and third party packages required for the local theme development.

```
$ yarn install
```

2. *Set up your .env file*
You will need to create a `.env` file using the contents below in the project directory. The password and theme id will have been emailed to you:
```
# The myshopify.com URL to your Shopify store 
SLATE_STORE=wmw-technical-test.myshopify.com

# The API password generated from a Private App 
# This will have been emailed to you
SLATE_PASSWORD=

# The ID of the theme you wish to upload files too
# This will have been emailed to you
SLATE_THEME_ID=

# A list of file patterns to ignore, with each list item separated by ':' 
SLATE_IGNORE_FILES=settings_data.json:
```

3. *Start Node.js Express server and begin watching assets*
The command will compile the assets in `/src` into a `/dist` directory -which will contain all the files necessary for your theme to run.

```
$ yarn start
```

4. *Start developing!*
The terminal should provide you with a preview link to your theme, and will automatically inject and refresh the browser when changes are made. The preview link should like the following:
`https://localhost:3000/?preview_theme_id=THEME_ID`
`https://172.16.120.157:3000/?preview_theme_id=THEME_ID `

> If you are getting localhost or certificate issues, then please follow this guide to troubleshoot the issue. 
> [Create a self signed SSL certificate](https://github.com/Shopify/slate/wiki/4.-Create-a-self-signed-SSL-certificate)

## Submitting results
1. *Deploy*
Once you have finished and ready for a review, then you will need to run the following command for us to see the results on your theme:
```
$ yarn deploy
```

2. *Let the someone know*
When the deployment has finished, then you can test the same preview link that you have been developing on inside any browser. 

If all is good - then contact the interviewer or daniel@wemakewebsites.com that the test is ready for review with a link to a GitHub repo - and we will get back to you as soon as we can regarding the results!

## Useful resources
[Starter Theme - Wiki](https://github.com/Shopify/starter-theme)
[Liquid basics](https://help.shopify.com/en/themes/liquid/basics#objects)
[The collection object](https://help.shopify.com/en/themes/liquid/objects/collection)
[The product object](https://help.shopify.com/en/themes/liquid/objects/product)
[The variant object](https://help.shopify.com/en/themes/liquid/objects/variant)
[Creating AJAX calls with Shopify](https://help.shopify.com/en/themes/development/getting-started/using-ajax-api)

## System requirements
You’ll want to ensure you have the following already installed on your local machine before getting started with Starter theme:

- **Node:** The current LTS (long-term support) release. We like to use a Node Version Manager like [NVM](https://github.com/creationix/nvm).

- **NPM 5+ or Yarn:** Both of these package managers have [ups and downs](https://blog.risingstack.com/yarn-vs-npm-node-js-package-managers/), choose whichever you prefer. Follow the installation instructions [for Yarn](https://yarnpkg.com/en/docs/install) or [NPM](https://www.npmjs.com/get-npm) to make sure you're using the latest version.

