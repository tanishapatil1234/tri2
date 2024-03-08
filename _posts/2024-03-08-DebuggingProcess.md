---
comments: true
layout: post
title: Debugging Process
permalink: debug
unit: 2
---

# Preflight (No running Backend) Error 
## Indication of Preflight Error
A preflight error occurs during cross-origin requests (CORS) when a preflight request fails. Either: 
- The server does not respond with the appropriate CORS headers.
- The server rejects the preflight request due to incorrect CORS configuration.
- There is a network issue preventing the preflight request from reaching the server.

In this case, the third issue is present (because the backend is not running locally, the preflight request does not even reach the serve - as its not up)



<img width="1415" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/a581295e-95ab-4990-b6ee-381e2209b407">
<img width="1184" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/080d1e65-ee8a-4992-9567-ccbf8140b61e">

## Further Invesitgation into the error - in Sources
<img width="1184" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/3c5359a9-1387-49c1-932c-c024b0386ed7">

In sources, the source of the error is more clearly indicated. The error might indicate a failure to make the network request to http://localhost:8085/authenticate. This could happen if the server is not running or if there is an issue with the network connection, which is the case currently. However, let us continue investigating using debugging mode to confirm . 

## Debug 

First in debug mode I will test the ability to accept the use input of login information as an array. (I know already this is not the issue, but if it were an issue I would not be notified. For this reason I added a breakpoint here. Additionally, this step is important to come BEFORE the server is called)
<img width="1184" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/0729eadf-7f5d-4689-a7dc-0c934d77f9e6">

After stepping over, it is clear that the input of the user is saved as expected. 

<img width="1184" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/c205fea9-77db-44b2-930a-eb2304d6b0ac">


In the next step over, the breakpoint set at the .catch for the js request is highlighted. 
<img width="1184" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/c9dcf831-d9b3-43d2-9a56-4f3856d6f642">

The error message is in the format :
` console.error('Error during login:', error);`

If we check in the console, the error is present as expected along with a network error  : 

<img width="948" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/40a08468-0649-489a-98ef-4c7bc476565b">


## Fix 
With the POST network error coupled with the console response error, it is clear that the issue lies in server connectivity. I went to check and my server was not even running! Once server ws started, error was resolved : 

<img width="1181" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/19e763a5-8545-4173-b20e-30751f148c26">
<img width="1181" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/7c5206d3-9667-4718-bb3e-176480829976">
<img width="1181" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/0a603f06-5b3f-40de-ae3f-432f8ffb8983">
<img width="1181" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/d2cfe21a-6005-4c08-8479-5365e88b3e8f">

Interestingly enough, I found a new  issue. While my login was successful (as shown by the breakpoints and a complete screenshot I will show below), there is a new issue... Apparently in future chrome versions: setting third-party cookies will be blocked. This behavior protects user data from cross-site tracking. Interesting to see how to navigate this, and I plan to read more about it in the article provided : [LINK](https://goo.gle/3pcd-dev-issue)


**LOGIN SUCCESSFUL REDIRECT TO AUTHORIZED PAGE:**
<img width="814" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/aa94ff2b-1620-4f48-ab5f-efc1c44d3a58">

<img width="898" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/48c343fd-7ead-48f6-b17d-444b95828374">



# Unathenticated Error 

Now I want to explore a new error. What happens if somebody tries to access the authenticated page without properlly logging in. What will they see. Should I make a redirect to login page (probably!). This is what I plan to investigate on this page. 

## Start Backend on Debug Mode 
<img width="1280" alt="image" src="https://github.com/Codemaxxers/codemaxxerblog/assets/111611921/beb4647a-17aa-4596-adaa-898338b562e1">


## Cookies Cleared on Authenticate Page 
<img width="828" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/dab7494c-e5df-4e73-95a7-7d076b9c0ba7">


## Error in Console with Cleared Cookies 
<img width="1198" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/5ba0bf45-0a9f-4042-adb0-0f909e52e5e7">


## Sources 
I added breakpoint to fetch, inside .then, inside .fetch

<img width="1169" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/4e993fa9-b96c-48b1-bbc3-fef9a7aa539a">

## Run frontend, screen capture break at fetch while examining Body
<img width="1169" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/787c41f0-afbd-4784-afcb-885b9ff50fa5">

## Press play on frontend, observe stop inside of backend
No Cookies error !

<img width="934" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/d47bae9e-bb0e-4f13-97fe-cf023d4c6e69">

## Press step over on backend until you have obtained data from database, screen capture HashMap or other data Object, Step in until you see data, screen capture capturing break point and Data.


<img width="1218" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/221db56b-e3c6-441f-970c-6ff8bedee0c6">
<img width="723" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/7e438be9-e540-4a08-8c88-cbe2424375fa">


# Further Application 
For my LinkedIn-type application, leveraging the login debug functionality can greatly enhance the user authentication and authorization process. Since the LinkedIn backend is in Python, integrating the login debug feature involves strategically placing breakpoints within the Python codebase to intercept and inspect the authentication flow. By carefully analyzing the request/response cycle at crucial authentication endpoints, such as user login and token generation, developers can gain valuable insights into the authentication process's efficiency, security, and potential vulnerabilities. This debug capability allows for thorough testing and validation of various authentication scenarios, including successful logins, incorrect credentials, expired tokens, and unauthorized access attempts. Moreover, by utilizing logging frameworks or custom logging mechanisms, developers can track and log detailed information about authentication attempts, facilitating comprehensive auditing and troubleshooting. Ultimately, integrating login debug functionality into the LinkedIn-type application's backend empowers developers to ensure robust security measures, streamline user authentication workflows, and deliver a seamless and secure user experience.


I still have to do the frontend, so testing debug doesn't exactly make sense yet. However here is what I have worked on so far : 

<img width="1119" alt="image" src="https://github.com/lightkurve/lightkurve/assets/111611921/57efb334-8ce3-415f-9c03-9a9e40e6a744">
