# Lab04 - Swagger & Basic Developer Portal Configuration

3scale uses the popular API Documentation and testing tool Swagger. We’re now going to configure it then display it in the Developer Portal.

* 1. Swagger. Open Active Docs menu item on the top left. ![](/assets/lab04-1.png)
  2. Open Echo link and the left and Delete it. ![](/assets/lab04-2.png)![](/assets/lab04-3.png)
  3. Create new Spec. ![](/assets/lab04-4.png)

     * Name it flights-docs \(both Name and System Name\) and click Publish. ![](/assets/lab04-5.png)
     * Paste in the JSON in Appendix 1 – Swagger below into API JSON Spec\*
     * Replace the string &lt;yours&gt; with the host you've been using in your curls, e.g. api-2445581074662.staging.apicast.io
     * Create Service
     * Open it by clicking flights-docs. ![](/assets/lab04-6.png)
     * click in the user\_key field \(select pop up\) and Try it out! \(\*\*Note, this is a test API on Heroku. The first time it is hit every hour is slow\) 

     ![](/assets/lab04-7.png)

  4. Developer Portal. Now we’re going to configure a page and a logo that will be _**viewable by an API consumer **_– in our example could be someone like Expedia or CheapOAir2 very common items needed for POCs: 1\) Swagger in Portal, 2\) Custom Logo for API Provider – a very basic customization
  5. Add Swagger Page

     * Click on Developer Portal menu item then New Page -&gt; New Page. ![](/assets/lab04-8.png)
     * Fill it in as follows:

       * Add a name and Add Path: /testdocs
       * Expand Advanced options and click Liquid Enabled
       * Paste in Code snippet \( below in Appendix 2 – Dev Portal Swagger JavaScript\)
       * Replace "&lt;system-name&gt;" with your Swagger System Name above \(5.a.iii.1\), flights-docs
       * Create Page. 

       ![](/assets/lab04-9.png)

     * After Create Page, Publish it. Note there are 2 modes you can save in: Draft \(clicking Save\) and Published- obviously clicking Publish.

  6. Set your Dev Portal credentials.
     * Open Developers menu item, then open the Developer Account. ![](/assets/lab04-10.png)
     * Click on the 1 User, click the user. ![](/assets/lab04-11.png)
     * Edit then add a password and Update User. ![](/assets/lab04-12.png)
  7. Login to the Dev Portal. Note be aware we are now switching the other web console – the one we setup for API Consumers, where \_**users **\_of the API \(e.g. Expedia or CheapOAir\) onboard and learn about the API.
     * On Developer Portal Menu, click Visit Developer Portal. This is the out of the box Developer Portal. ![](/assets/lab04-13.png)
     * Sign in – using email and password of the user you just edited.
     * Inside Developer Portal, choose the Documentation menu or append the path you added to your Portal page you defined above and hit that URL, e.g.  [https://atlanta-training.3scale.net/testdocs](https://atlanta-training.3scale.net/testdocs)
       Swagger page appears.
     * You can TRY IT OUT! As you did previously inside the Admin Portal.
  8. Add custom Logo – example of very basic Developer Portal customization.

     * Back in the Admin console, in the Developer Portal section, add a new File. ![](/assets/lab04-14.png)
       ![](/assets/lab04-15.png)
     * Set the Section to be images and the Path to be /images/threescale-logo.png, Choose File and browse to threescale-logo.png that accompanies this document \(You’ll need to download it off the google drive and save it
       locally on your hard drive first\) 
       Create File then Save
     * Now Add this file to the main layout page.  
       Scroll down and click the Main Layout – Left Hand Side near the bottom.    ![](/assets/lab04-16.png)  
       At line 46. Replace line:   
       `<a class="navbar-brand" href="/">{{  provider.name }}</a>`  
       With:  
           `<div class="logo">`

       `<a href="#">`  
       `<img src="/images/threescale-logo.png " alt="" style="height:50px; width:150px;">`  
       `</a>`  
       `</div>`   
       Publish it.

     * Go Back to the Dev Portal and refresh.
     * ADJUST THE WIDTH/HEIGHT \(in red above\) TO LOOK RIGHT

     You’re done! You’ve completed the steps to do a minimal 3scale POC!



