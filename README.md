# API Views

- Read [the guideline](https://github.com/mate-academy/py-task-guideline/blob/main/README.md) before start

Now, you are going to implement views via class-based views.

Create `Genre`, `Actor`, `CinemaHall` models and update `Movie` model to
the ones you wrote in Django ORM module. Modules should have such fields:
- `Actor`: `first_name`, `last_name`
- `Genre`: `name`
- `CinemaHall`: `name`, `rows`, `seats_in_row`
- `Movie`: `title`, `description`, `actors`, `genres`, `duration`. (note: you 
already have a new field here) 

Create serializers for all these models.

Create views for models interaction endpoints via different class-based views:
- For the `Actor` model use an `APIView`
- For the `Genre` model use a `GenericAPIView`
- For the `CinemaHall` model use a `GenericViewSet`
- For the `Movie` model use a `ModelViewSet` and `routers`

For every <entity> from `actors`, `genres`, `cinemahalls`, `movies`, such
endpoints should work:
* `GET api/cinema/<entity>/` - should return a list of the all entity items
* `GET api/cinema/<entity>/<pk>/` - should return an entity with given id 
* `POST api/cinema/<entity>/` - should create a new entity based on passed data
* `PUT api/cinema/<entity>/<pk>/` - should update the entity with given id based on passed data
* `DELETE api/cinema/<entity>/<pk>/` - should delete the entity with given id
