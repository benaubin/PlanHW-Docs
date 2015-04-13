# PlanHW Api Docs

PlanHW is an awesome planner, and its API lets you leverage the power of PlanHW for your awesome planner.

##Overview

PlanHW's API can be used for anything the web client can do. Actually, the web client uses the API. So yeah. YOU HAVE THE POWER.
But if you want to make you own planner, hopefully this will help. **PLEASE USE `HTTPS`**, we set it up for a reason :P.

##Root

`https://api.planhw.com/` - It really just gives you a 404 error. Nothing great :(


## API layout

    https://api.planhw.com
        /login                  # [GET] Login
        /test_login             # [GET] Test login
        /logout                 # [DELETE] Logout

        /students
            /                   # [GET] Students Index
            /                   # [POST] Signup
            /new                # [GET] [DEPRICATED] Signup
            /:id
                /               # [GET] Profile of user
                /               # [PUT] Update user
                /               # [DELETE] Delete user
                /hw
                    /           # [GET] Homework index
                    /           # [POST] New homework
                    /:id        
                        /       # [GET] Show homework
                        /       # [PUT] Update Homework
                        /       # [DELETE] Delete Homework
