# Sinatra CRUD Cheatsheet

- check out beginning of CRUD lecture for explanation

# Create
## New
- displays the form to make the new thing
- get /artists/new
- new.erb

## Create
- processes the form and it actually makes and saves the thing
- post /artists
- no view, redirects to show for that thing or index
- Model.create

# Read
## Index
- show all of the things
- get /artists
- index.erb
- Model.all

## Show
- details on one of the things
- get /artists/:id
- show.erb
- Model.find_by(id: params[:id])

# Update
## Edit
- displays the form to change one thing
- get /artists/:id/edit
- edit.erb
- Model.find_by(id: params[:id])

## Update
- proccesses the form and makes the change
- patch /artists/:id
- no view, redirects to show
- instance = Model.find_by(id: params[:id])
- instance.update(params[:key])


# Delete
## destroy
- process the form and destroys the thing
- delete /artists/:id
- no view, redirect to index
- instance = Model.find_by(id: params[:id])
- instance.destroy
