1. Global
  1. The rivets delay issue needs more work. See 1.2
  2. We probably need a global way of dealing with loading delays that affect rendering
  3. Merge the visibility manager and popup js functions together
  4. Move overlay to one intance
  5. z-index manager

## Products

* Error handling
  * Need some!
  * Importantly product quantities aren't limited, so adding more than the available amount leads to nothing

* Compare at price function is not working on variant switch
  * See https://concrete-theme.myshopify.com/products/product-demo-1?variant=32550079759
* The delay on load for the product selection needs work
  * See 1.2
* Can we clean up and combine the following:
  * option selection js from the product page
  * switchVariant from main app.js
  * productImageSwitch from main app.js
  * switchImage from main app.js
  * And see below
* Clean up product image gallery functions and tie them to variant selection more cleanly
  * Ideally should be more easily integrated with sliders etc
  * We will probably need the following options by default
    * Image zoom
    * Popup image gallery
* Add savings as percentage using Cart.js
* Add SKU (default to hidden)
* Add quantity available (default to hidden)

NOTE: We need to keep support for option_selection js

## Accounts

* 'customer/addresses' needs some work
* Orders shows 0, even when 1 unfulfilled order exists - is this only when bogus gateway is used?
* We need to Ajaxify the forms... the old method is too clunky for our default

## Blogs

* Add ajax pagination to blogs in 'reinforced concrete'

## Sections

Increased support for sections https://www.shopify.com/partners/blog/introducing-sections-for-shopify-themes


## Libraries that may or may not be added later

* [FastClick](https://github.com/ftlabs/fastclick) eliminates the 300ms delay on click events on mobile browsers
* Unslider by Idiot http://unslider.com

## Various

* Add lorem ipsum placeholder to labguage file and inclide as placeholder for 'if empty' pages

## Customer Pages

* See if we can reverse the addresses in the customer address template so the default address appears first
  * This does not work:
  ``{% assign addresses = customer.addresses | sort: reversed %}
   {% for address in addresses %}``
