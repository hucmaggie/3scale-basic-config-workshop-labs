# Lab01 - Integrate an Endpoint

1. Login to your domain with your activated account.
2. Dismiss Greeting Message.
3. Navigate to API &gt; Integration.![](/assets/lab01-1.png)
4. This is where you configure your gateway which will communicate with the 3scale Platform. Make the following entries:

   1. Private Base URL\*: [https://tc-apis.herokuapp.com:443](https://tc-apis.herokuapp.com:443). ![](/assets/lab01-2.png)

      After entering this, click Update & Test Staging Configuration towards the bottom of the page \(you are about to leave this page momentarily so this is necessary to save your Private Base URL\) ![](/assets/lab01-3.png)

   2. Mapping Rules. This is where you map URL patterns of endpoints to Methods and Metrics \(enabling you to track usage and control access\)

      * Define a Method \(logical representation of an Endpoint\) by clicking Define. ![](/assets/lab01-4.png)

      * Create a New Method. ![](/assets/lab01-5.png)

      * Name  it something like get-flights \(System and Friendly\). ![](/assets/lab01-6.png)

      * Add a Mapping Rule to it back on Integration screen. ![](/assets/lab01-7.png)

      * Replace the default Mapping to hits by editing it. ![](/assets/lab01-8.png)

      * Replace the Pattern with the URL path to our endpoint \(/flights/intl/flights\) and select our new method get-flights. Use the same path \(/flights/intl/flights\) in API test GET request then click Update and Test Staging Configuration. ![](/assets/lab01-9.png)

      * If all goes well, status will turn green – indicating your configuration has been deployed to the 3scale Nginx on AWS. You can now test your managed API endpoint using the curl in the screenshot above – or just pasting the URL into a browser. 

        \(\*\*Note, this is a test API on Heroku. The first time it is hit every hour is slow\)



