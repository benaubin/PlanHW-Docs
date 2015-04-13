#Login

Logining in. It's one of the first things you want to do when connecting with the api.

##Overview:
You'll get info about the currently logged user. You will also get a token* to use features of the API that require authenication.

##URI:

`https://api.planhw.com/login`

|Params 	| Required |
|-------	|:--------:|
|username  	| Yes      |
|password  	| Yes	   |


##Example Response:

	{
		"student": {
			"username": "penne12",
			"name": "Ben",
			"email": "ben@bensites.com",
			"admin": true,
			"id": 1
		},
		"login": {
			"token": "{{FILTERED}}",
			"token_expires_at": "2015-04-13T19:40:09.491Z"
		}
	}



*Each user can have one token at a time that expires after 6 hours (working on a more permanent [JWT](http://jwt.io) solution).