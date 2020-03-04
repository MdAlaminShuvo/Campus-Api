# Campus-Api
FORMAT: 1A
HOST: https://127.0.0.1:4000/

# Campus API

Campus API is a simple API of user information

## User Collection [/capmus/user]

### List All Users [GET]

+ Response 200 (application/json)

        [
            {
                 "status": "success",
                 "result": 2,
                 "data": {
                        "users": [
                            {
                                "_id": "5e0cac88dd30799095c842f7",
                                 "name": "Harun Or Rashid",
                                 "roll": 113,
                                 "phone": "01741551374",
                                 "__v": 0
                             },
                            {
                                "_id": "5e0cac72dd30799095c842f6",
                                "name": "Khairul Bashar",
                                "roll": 143,
                                "phone": "01774242362",
                                "__v": 0
                            }
                        ]
                }
        }
        ]
        
        


### Create a New User [POST]

You may create new user using this action. It takes a JSON
object containing user name, roll and phone.

+ Request (application/json)

        {
            "name": "User Name",
            "roll": 113,
            "phone":"01741551374"
        }

+ Response 201 (application/json)


    + Body

            {
                "name": "User Name",
                "roll": 113,
                "phone": "01741551374",
                "_id": "5e0c391201c20f9345e7ae4e",
                "__v": 0
            }





## User Retrieve Update and Delete [/capmus/user/5e0cac88dd30799095c842f7]

### Get single User [GET]

+ Response 200 (application/json)

        
        {
            "status": "success",
            "data": {
                 "users": {
                  "_id": "5e0cac88dd30799095c842f7",
                  "name": "Harun Or Rashid",
                  "roll": 113,
                  "phone": "01741551374",
                  "__v": 0
                }    
            }
        }
    


### Update a User [PATCH]

You may update a  user using this action. It takes a JSON
object containing update user information.

+ Request (application/json)

        {
            "phone":"01790362665"
        }

+ Response 200 (application/json)


    + Body

            {
                "name": "Harun Or Rashid",
                "roll": 113,
                "phone": "01790362665",
                "_id": "5e0cac88dd30799095c842f7",
                "__v": 0
            }

### Delete a User [DELETE]

You may delete a user using this action.


+ Response 200 (application/json)

    + Headers
