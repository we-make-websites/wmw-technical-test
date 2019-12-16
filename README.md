# We Make Websites - Technical Test

> This is an entry level test that we require all front-end developer candidates trial before proceeding into the final stage. We do not pay or use any of the work produced on a commercial environment.

If you have come directly to this repository without a reference and curious to trial out this test - then please contact daniel@wemakewebsites.com to get yourself started!

## Brief
You have been provided a link to a Shopify development theme which contains only a basic header and also a list of unstyled product cards. The link should contain a `?preview_theme_id=YOUR_THEME_ID` suffixed at the end of the url.

We would like you to **only** style the Featured Collection section in the `featured-collection.liquid` file in your starter theme to match the supplied designs.

We have supplied both mobile and desktop designs but we would like you to have a think on how the components respond to the sizes in between. The solution is open for interpretation.

The Invision prototype also includes a style guide. We recommend using the Invision inspect tool - this is an easy way to sample the colours, copy font values and get the correct dimensions of each element in the design.

The `/src/sections/featured-collection.liquid` contains the necessary Liquid markup and content required for the design to function - but you are encouraged to add in your own custom HTML/Liquid to make your build work with the designs.

#### Tips
- We recommend using Flickity to build the featured collection carousel.
- One of the products have a `badge: sale` tag that had been added behind the scenes. Try to use that tag in order to display the badge on the product in the carousel. You can read more about `product.tags` under `The product object` article and how to manipulate strings in the `String filters` article shown in the Useful Resources section below.

### Bonus
The following instructions are not required for a successful submission. They are purely for us to better measure your eye for detail and bringing a static design to life. But even if the tasks are not required for submission, we still try to make the tasks as fun and useful for both parties. We will always provide feedback for the bonus tasks if we see room for improvement.

- **User interactions**

  One of the most important things in eCommerce design is user experience through interactivity. We would like you to have a think about how you could improve the experience by adding an extra layer of interactions.

- **Javascript**

  If time allows and you’re up for a fun challenge, then you can also look into creating a basic Quick Add functionality. A standard Quick Add in eCommerce is when a user clicks on the Add to cart button - which will in turn - add the product into the user’s cart without refreshing the page.

  You can find some relevant documentation for this task below in the Useful Resources section regarding making AJAX calls in Shopify.

  There is also a `featured-collection.js` script in the `/src/sections/` directory which already registers the Section in Shopify. All your functionality should be contained in this file. You are open to use third party packages as well as a JS Framework if you feel more comfortable.

  > You can test if the function has been successful by navigating to the `https://wmw-technical-test.myshopify.com/cart` page or by visiting the  `https://wmw-technical-test.myshopify.com/cart.json` url to see if a product data has been added to your cart.

## Getting started

1. **Create a self-signed SSL certificate**

    Before getting started, you will need to have created a self-signed SSL certificate to serve your assets locally. Please follow this guide before proceeding. [Create a self signed SSL certificate](https://github.com/Shopify/slate/wiki/4.-Create-a-self-signed-SSL-certificate)

2. **Install project dependencies**

    You will need to make a clone of this repo and run the following command in the project folder. This will install the Shopify theme dependencies as well as third party packages required for the local theme development.

```
$ yarn install
```

3. **Set up your .env file**

   You will need to edit the sample `.env` file using the contents below in the project directory. The password and theme id will have been emailed to you:

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
SLATE_IGNORE_FILES=/config/settings_data.json:
```

4. **Start Node.js Express server and begin watching assets**

   The command will compile the assets within `/src` into a `/dist` directory - which are all the necessary files for your theme to run.

```
$ yarn start
```

5. **Start developing!**

   The terminal should provide you with a preview link to your theme, and will automatically inject and refresh the browser when changes are made. The preview link should like either of the following:

   `https://localhost:3000/?preview_theme_id=THEME_ID`

   `https://172.16.120.157:3000/?preview_theme_id=THEME_ID `

> If you are getting localhost or certificate issues, then please follow this guide to troubleshoot the issue.
> [Create a self signed SSL certificate](https://github.com/Shopify/slate/wiki/4.-Create-a-self-signed-SSL-certificate)

## Reviewing and submitting your results
1. **Deploy**

   Once you have finished and ready for a review, then you will need to run the following command for us to see the results on your theme:
```
$ yarn deploy
```

2. **Let someone know**

   When the deployment has finished, then you can test the same preview link that you have been developing on inside any browser.

   If all is good - then contact the interviewer or daniel@wemakewebsites.com that the test is ready for review with a link to a GitHub repo - and we will get back to you as soon as we can regarding your results!

## Useful resources
- [Starter Theme - Wiki](https://github.com/Shopify/starter-theme)
- [Liquid basics](https://help.shopify.com/en/themes/liquid/basics#objects)
- [The collection object](https://help.shopify.com/en/themes/liquid/objects/collection)
- [The product object](https://help.shopify.com/en/themes/liquid/objects/product)
- [The variant object](https://help.shopify.com/en/themes/liquid/objects/variant)
- [Creating AJAX calls with Shopify](https://help.shopify.com/en/themes/development/getting-started/using-ajax-api)
- [String filters](https://help.shopify.com/en/themes/liquid/filters/string-filters)

## System requirements
You’ll want to ensure you have the following already installed on your local machine before getting started with Starter theme:

- **Node:** The current LTS (long-term support) release. We like to use a Node Version Manager like [NVM](https://github.com/creationix/nvm).

- **NPM 5+ or Yarn:** Both of these package managers have [ups and downs](https://blog.risingstack.com/yarn-vs-npm-node-js-package-managers/), choose whichever you prefer. Follow the installation instructions [for Yarn](https://yarnpkg.com/en/docs/install) or [NPM](https://www.npmjs.com/get-npm) to make sure you're using the latest version.

