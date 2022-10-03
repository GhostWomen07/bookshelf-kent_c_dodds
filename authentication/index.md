## 26/sep/2022
# Authentication

1. import auth from authentication
2. create state for user
3. create login function and setuser in user state using using auth.login
4. create register function and setuser in user state using auth.register
5. create logout function and null the user state
6. if user is available then show authenticated app otherwise show unauthenticated app and pass props to them

## 2nd Part:-
problem:-when user refresh the web page its automatically logout or moves on login page, we want on refresh user still on login page.
solution:- 

1. create getUser function in which we take the token from auth(auth.getToken()) or if token is available then return user and save it on user state by calling getusers function
2. not call the function get user and set its retrn user in user state (setUser(user))
3. do changes in api-client.exercise.js
4.pass props to client:-
    {token, headers: customHeaders, ...customConfig} = {}
    headers: {
        Authorization: token ? `Bearer ${token}` : undefined,
        ...customHeaders,
      },


