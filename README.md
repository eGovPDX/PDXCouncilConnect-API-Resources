#PDXCouncilConnect API

##What
The PDXCouncilConnect API allows you to retrieve City of Portland, OR Council agenda data through an easy to use RESTful interface. The API returns agenda, session, and item information. This includes location, times, bureaus affected, and even voting records when they exist.

##The API

The base URL for the API is:

    http://api.portlandoregon.gov/councilagenda/

The base URL returns the latest published agenda including the sessions and items.

To get a specific agenda, session, or item you use this format:

    http://api.portlandoregon.gov/councilagenda/{agenda|session|item}/{id}/

For example:

    http://api.portlandoregon.gov/councilagenda/agenda/294/
    http://api.portlandoregon.gov/councilagenda/session/302/
    http://api.portlandoregon.gov/councilagenda/item/890/

You can list all of a certain type by using the type in a plural:

    http://api.portlandoregon.gov/councilagenda/agendas/
    http://api.portlandoregon.gov/councilagenda/sessions/
    http://api.portlandoregon.gov/councilagenda/items/

You can also list children types of a specific ID by using the types in plural format like so:

    http://api.portlandoregon.gov/councilagenda/agenda/294/sessions/
    http://api.portlandoregon.gov/councilagenda/session/302/items/

###Filters

####`count`

The `count` param will cut your results down from infinite to whatever you put here. 

_Example:_

    http://api.portlandoregon.gov/councilagenda/agendas/?count=5

Currently there is only one filter, but there is more coming such as a `search`.