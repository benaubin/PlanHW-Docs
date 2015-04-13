#Testing a login

It's a quick way to test a login. 


##URI
`https://api.planhw.com/test_login`

###Params

ID is the id of a student you'd like to test. Token is the token returned by logging in.

|Params 	| Required |
|-------	|:--------:|
|id  		| No       |
|token  	| No	   |


##Example Response:

	{
		"correct": true,
		"student": true,
		"token": true
	}

###Explanation:

- `correct` is `true` the token works for a found student provided
- `student` is `true` if the student exists
- `token` is `true` if the token works for the student
- `error` if `student` or `token` are `false`, this shows a human readable explanation.