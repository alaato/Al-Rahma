# BackEnd

## Home page
- query latest 4 announcments
- query latest 4 events
- query latest 4 recurring

## Events route (recurring and annoucment)
- check query
- extract the page number from query
- offset = !page ? 0 : (page - 1) * 10
- skip offset amount and fetch 10 latest events

## Show Event route POST
- grab id from route
- query database.
- if no id, return 404;
- return event data
## Create Event POST
- check if admin
- validate data
- save data in database
- reroute to event show page and return status
- if error return status 500
## delete route POST
- grab id
- check if admin
- delete post
- refresh page and make a toast
## Edit Route POST
- grab id
- check if admin
- save post
- reroute to event show page and return status

