#Students


Method  | Route         | Explanation 
------- | ------------- | -----------------
[POST]  | /students     | [Signup](#signup)
[GET]   | /students     | [Index](#index)
[GET]   | /students/:id | [Profile](#profile)
[PUT]   | /students/:id | [Update](#update)
[DELETE]| /students/:id | [Delete](#delete)

##<a id="signup">Signup</a>
Letting students sign up is great, it means they don't have to go anywhere else, and they can start using PlanHW right away!

`[POST] /students`

|Params                 | Required      |
|:---------------------:|:-------------:|
|`name`                 | No            |
|`username`             | Yes           |
|`email`                | Yes           |
|`password`             | Yes           |
|`password_confirmation`| Yes           |

##<a id="index">Index</a>
Shows a list of all students.

`[GET] /students`

|Params                 | Required      |
|:---------------------:|:-------------:|
|None                   | N/A           |

###Example Response

~~~
{
    "students": [
        {
            "student": {
                "username": "penne12",
                "name": "Ben",
                "admin": true,
                "id": 1
            }
        },
        {
            "student": {
                "username": "test",
                "name": "Testy",
                "admin": false,
                "id": 2
            }
        },
        ...
    ]
}
~~~

##<a id="profile">Profile</a>
Shows more detailed info on the student with :id provided. We also included links to gravatar images, so have fun with that.

`[GET] /students/:id`

|Params                 | Required      |
|:---------------------:|:-------------:|
|`id`                   | Yes           |

###Example Response

~~~
{
    "student": {
        "username": "penne12",
        "name": "Ben",
        "admin": true,
        "id": 1,
        "avatar": {
            "default": "https://secure.gravatar.com/avatar/320ce4f1f71747d993980a97bc43a5f4.png?d=monsterid&r=G",
            "size25": "https://secure.gravatar.com/avatar/320ce4f1f71747d993980a97bc43a5f4.png?d=monsterid&r=G&s=25",
            "size50": "https://secure.gravatar.com/avatar/320ce4f1f71747d993980a97bc43a5f4.png?d=monsterid&r=G&s=50",
            "size125": "https://secure.gravatar.com/avatar/320ce4f1f71747d993980a97bc43a5f4.png?d=monsterid&r=G&s=125",
            "size250": "https://secure.gravatar.com/avatar/320ce4f1f71747d993980a97bc43a5f4.png?d=monsterid&r=G&s=250"
        }
    }
}
~~~

##<a id="update">Update</a>
Updates the student.

`[PUT] /students/:id`

|Params                 | Required      |
|:---------------------:|:-------------:|
|`id`                   | Yes           |
|`token`                | Yes           |
|`name`                 | No            |
|`username`             | No            |
|`email`                | No            |
|`password`             | No            |
|`password_confirmation`| With password |

##<a id="delete">Delete</a>
Deletes the student

`[DELETE] /students/:id`

|Params     | Required |
|-------    |:--------:|
|id         | Yes      |
|token      | Yes      |