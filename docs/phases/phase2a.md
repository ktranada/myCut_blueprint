# Phase 2a: [Landing Page] Viewing Shop Index + Google Maps API

## Rails
### Models

### Controllers
* API::ShopsController (create, destroy, index, show)
* API::ReviewsController (create, show, destroy, update)

### Views
* shops/show.json.builder

## Backbone
### Models
* Shop (parses nested `reviews` association)
* Review

### Collections
* Shops
* Reviews

### Views
* searchView (composite view, contains searchResults (composite view, contains searchResultItem subviews) subviews<br> and a singular mapItem view. 
* newReview
* mewShopForm

Is it bad practice to nest composite views?


## Gems/Libraries
* Google map marker
