Thanks for your time working on the tech test for Spoke!

The data for you to work on will be provided by our graphQL endpoint (see env file). We would like you to fetch this data so that you can receive a list of products similar to this:

```
{
    "data": {
        "products": {
            "edges": [
                {
                    "node": {
                        "id": "Z2lkOi8vc2hvcGlmeS9Qcm9kdWN0LzE3MDU0MjY3MTQ2OTM=",
                        "priceRange": {
                            "maxVariantPrice": {
                                "amount": "62.0"
                            }
                        },
                        "images": {
                            "edges": [
                                {
                                    "node": {
                                        "originalSrc": "https://cdn.shopify.com/s/files/1/0057/7260/7557/products/1.Brushed_Smoked_Navy_Flat.jpg?v=1573339343"
                                    }
                                },
                                {
                                    "node": {
                                        "originalSrc": "https://cdn.shopify.com/s/files/1/0057/7260/7557/products/3.Brushed_Smoked_Navy_Mode_Front.jpg?v=1573339343"
                                    }
                                }
                            ]
                        },
                        "productType": "Heroes",
                        "title": "Clay",
                        "tags": [
                            "fabric: 30% off",
                            "feed",
                            "feed-trousers",
                            "hidden sale item",
                            "Published",
                            "sale",
                            "stock-feed"
                        ],
                        "updatedAt": "2020-06-22T13:48:02Z"
                    }
                },
                {...}
            ]
        }
    }
}
```

### Notes on this data:

We need to retrieve the following data for each product:
- ID
- Images
- ProductType
- Title
- Tags
- Price
- UpdatedAt

We would like to fetch the first 50 products from the endpoint and only fetch those product with the following productTypes:
- Heroes
- Sharps
- Polos

We assume that all the products have inventory and can be added to the basket.

Please visit this url for more information on shopify graphql: ```[https://shopify.dev/docs/admin-api/graphql/reference/object/product?api[version]=2020-04]```

### Requirements
- Please use React.js and a state management library (ie. Redux, Hooks) of your preference.
- Please write relevant tests preferably using Jest.
- The designs provided are a basic wireframe of the structure we expect to see. Feel free to experiment with different styles but please provide a responsive UI.

# Layout

### Products List page:
* Lists all products in given category (productType)
* Shows the first image for each product in the list
* Highlights the products with the new badge
* Has filtering functionality for the products (typing the title or the product type will filter correct products)
* Goes to the product page when clicked on a product

### Product page:
* Renders the second image from the data provided
* Shows the product price
* Adds the product to cart

### Cart page:
* Lists the products that are added to the cart
* Has delete from cart functionality
* Shows the total with a dummy `Pay` button

### Bonus:
* Update the item amount in the cart
* Add a promotion input to make 20% discount
* Implement this test within the NextJS framework

Happy hacking!
