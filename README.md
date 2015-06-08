# MyCut

[Heroku link][heroku]

[heroku]: http://flux-capacitr.herokuapp.com

## Minimum Viable Product
MyCut is a clone of Yelp built on Rails and Backbone. Users can:

<!-- This is a Markdown checklist. Use it to keep track of your progress! -->

- [ ] Create accounts
  - [ ] Create sessions (log in)
- [ ] Create Store
- [ ] Queries
  - [ ] Find
    - [ ] Tags
    - [ ] Shop name
    - [ ] Location
- [ ] View
  - [ ] Geolocation using Google Maps API
  - [ ] Barbershops/salons
  - [ ] Barbers/stylists and their portfolio
- [ ] User supplied photos
- [ ] Read/Write shop reviews
- [ ] Ratings
  - [ ] Star rating of shop
  - [ ] Star rating of barber


## Design Docs
* [View Wireframes][views]
* [DB schema][schema]

[views]: ./docs/views.md
[schema]: ./docs/schema.md

## Implementation Timeline

### Phase 1: User Authentication and Validations (~.5 day)
I will implement user authentication + sessions through standard Rails 
practices and a primary static page to host my Backbone application. I well 
set up the the initial migrations, models, both DB and model level validations,
as well as the necessary associations. At this point I will deploy to Heroku.

**Primary duties**: Authentication, validating models + associations, deploying to Heroku.

[Details][phase-one]

### Phase 2a: Creating/Viewing Shops and Reviews (~1-2 days)
I will add API endpoints to serve shop and review data as JSON,
then add Backbone models and collections that fetch data from those routes. 
I will set up the Backbone views so that users will be able to create and view
shops, tags and reviews.

[Details][phase-two-a]

### Phase 2b: Showing a shop, its barbers, and reviews. ~1-2  day

[Details][phase-two-b]

### Phase 3: Create, view, and edit a barber portfolio (~2 days)
I will add API endpoints and jbuilder views to serve barber data as JSON, and
then I will add a Backbone


[Details][phase-three]

### Phase 4: User Feeds (~1-2 days)
I'll start by adding a `feed` route that uses the `current_user`'s
`subscribed_blogs` association to serve a list of blog posts ordered
chronologically. On the Backbone side, I'll make a `FeedShow` view whose `posts`
collection fetches from the new route.  Ultimately, this will be the page users
see after logging in.

[Details][phase-four]

### Phase 5: Search for shops (~2 days)
I'll need to add `search` routes to both the Shops controller. On the
Backbone side, there will be a `SearchResults` composite view has `BlogsIndex`
and `PostsIndex` subviews. These views will use plain old `blogs` and `posts`
collections, but they will fetch from the new `search` routes.

[Details][phase-five]

### Bonus Features (TBD)
- [ ] Many-to-many association between barber + shop
- [ ] Display shop by average rating 
- [ ] Activity history (e.g. likes, reblogs, taggings)
- [ ] Queries
  - [ ] Search by barber
- [ ] Barber Account
  - [ ] Upload portfolio 
- [ ] Read/leave views
  - [ ] Barber/stylist
- [ ] Modal barber portfolio
[phase-one]: ./docs/phases/phase1.md
[phase-two-a]: ./docs/phases/phase2a.md
[phase-two-b]: ./docs/phases/phase2b.md
[phase-three]: ./docs/phases/phase3.md
[phase-four]: ./docs/phases/phase4.md
[phase-five]: ./docs/phases/phase5.md

