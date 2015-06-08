# Phase 2: Viewing Shops and Reviews

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
* BlogForm
* BlogShow (composite view, contains PostsIndex subview)
* PostsIndex (composite view, contains PostsIndexItem subviews)
* PostsIndexItem
* PostShow

## Gems/Libraries
