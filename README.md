# Autocomplete_backend

This is a user seach example providing a REST API for the end user people in the db.
The service is stored in Google's cloud as a VM instance.
I used WPF as firewall and NGINX used as a reverse proxy i have created an SSL certificate using certbot SSL.

## Get list of saved users

### Request

`GET /users`

### Response

    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2

      [
        {
            "_id": "**************",
            "Name": "Farrell David",
            "WorkTitle": "asdasd",
            "ImageUrl": "https://randomuser.me/api/portraits/med/men/2.jpg",
            "__v": 0
        }...
    ]


### Request

`POST /users`

    curl -i -H 'Accept: application/json' http://localhost:3000/users/

    {
    "Name": "Name",
    "WorkTitle": "WorkTitle",
    "ImageUrl": "https://randomuser.me/api/portraits/med/men/2.jpg"
  }

### Response
    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2

    {"id":"*************","Name":"name","WorkTitle":"WorkTitle", "ImageUrl": "https://randomuser.me/api/portraits/med/men/2.jpg"}


## Authors

- [@avi413](https://www.github.com/avi413)


## Demo

[Demo](https://api.autocomplete.avidalal.net/users)