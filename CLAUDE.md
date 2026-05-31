# Project: Ecomexperts Shopify Hiring Test

## Context
Building a custom landing page for a Shopify store using the Dawn theme.
The page has 2 custom sections built from scratch (NO Dawn ready-made sections).
Store uses products imported from HiringExamStoreProducts.csv.

## Tech Stack
- Shopify Liquid templating
- Vanilla JavaScript ONLY (no jQuery)
- CSS (no preprocessors needed)
- Shopify AJAX Cart API (/cart/add.js, /cart.js, /products/<handle>.js)

## Design Reference
- Brand: "TISSO VISON"
- Banner: White bg, line-art illustration, large bold heading bottom-left, black "SHOP NOW →" button with yellow hover fill animation, yellow "CHOOSE GIFT →" nav button top-right, bottom scrolling ticker text strip
- Grid: "Tisso vison in the wild" heading, 3x2 photo grid with tight 4px gap, white "+" circle dot on each card image
- Popup: Compact white card (~560px), small product image left, info right, color as horizontal pill buttons with blue left-border on selected, size as native dropdown with "Choose your size" placeholder, black "ADD TO CART →" button with arrow, light grey backdrop
- Mobile: 2-col grid, centered banner text, stacked popup

## File Structure
sections/custom-banner.liquid
sections/custom-product-grid.liquid
templates/page.custom-landing.json

## Critical Business Rules
1. All banner text editable from Shopify customizer
2. Grid shows 6 products, each selectable from customizer
3. Popup shows: title, price, description, dynamic variants from product JSON
4. Add to Cart via AJAX POST to /cart/add.js
5. SPECIAL RULE: When product with BOTH "Black" AND "Medium" selected is added to cart, auto-add "Soft Winter Jacket" (handle: soft-winter-jacket)
6. No jQuery - vanilla JS only
7. Well-structured, commented, efficient code

## Git Workflow
- Repo name: "Faraz-Khan" (public)
- master branch: clean Dawn theme
- development branch: all custom work
- PR: development → master
- Connect GitHub branch to Shopify store
