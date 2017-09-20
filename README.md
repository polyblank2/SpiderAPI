FORMAT: 1A
HOST: http://api.spiderlog.net

# Spider Log API
Provides services for the Spider Log app family, recording the world's spider sightings

#Group Spiders
Access to Spider resources

## My Spiders [/spiders{?page,size}]
### Get all my spider sightings [GET]
+ Parameters

    + page (required, number, 1)... page number
    
    + size (required, number, 10)... page size
    
+ Request

    + Header
    
        Authorization: Basic dXNlcjpwYXNzd29yZA==
        x-api-version: 1.0
        
+ Response 200 (application/json)

    + Header
    
        ETag : "euyfewuyfvew76f7"
        cache-control: max-age=600
        
    +Body
        {
            "page" :
            {
                "number" : 1,
                "size": 10,
                "totalPages": 20
            },
            "spiders" :
            [
                {
                    "sightedAt" : "2014-08-29T07:00",
                    "imageUrl" : "https://s3-eu-west-1.amazonaws.com/uid-19247681/201408/14562881200_046a7f4d3d_z.jpg",
                    "description" : "Spider I saw on the train",
                    "tags": [
                        "big",
                        "stripy"
                    ]
                }
            ]
        }