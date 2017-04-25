# Lab03 - Policy Enforcement

This illustrates how you can give different access rights to different classes of API Consumer.

1. Go to API -&gt; Application Plans -&gt; click the Basic Plan which opens it. ![](/assets/lab03-1.png)
2. Disable method get-_flights by clicking its Enabled _check box. ![](/assets/lab03-2.png)
3. Go back to your terminal window and run the curl twice\*. 
4. Access will be denied
   \*requires 2 as policy information in the cache will show success from the previous call and allow the first through. The 2nd will use freshly populated data and block access.
5. Now we’re going to change the access rights this API consumer has. Open Applications -&gt; then click on the Developer’s App. ![](/assets/lab03-3.png)
6. Next we further illustrate Access Policy enforcement
7. This _application_ represents our API Consumer. You can see the User Key on the left – the one we’ve been attaching to our 3scale managed API calls. The access rights this consumer gets is defined by the Plan this Application subscribes to: _**Basic **_ on the top right. The Basic Plan has disabled access to _get-flights _– hence we’re blocked as you’ve seen. Now we’re going to change the level of access this Developer App has. Change the Plan to _Unlimited _– which does have access to _get-flights. _![](/assets/lab03-4.png)
8. Go back to terminal and hit the API again – this time it succeeds because the application subscribes to a plan \(i.e., Unlimited\) that allows access to _flightsList_



