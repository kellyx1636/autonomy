# Entry 5: Learning Cross-site Request Forgery and Needing To Focus Even More 
In this entry, I learn that there is another kind of security flaw that a site can have and it is called, cross-site request forgery. To learn more about what it means, read on! :)   

##### Some Side Notes: 
If you would like to follow along with what you will read in my entry, click on this link: [Hacksplaining: Cross-site Request Forgery](https://www.hacksplaining.com/exercises/csrf). 

When you click on the link, you will notice that there are circles on the top-left corner. Those circles are like the steps or slides of a presentation. You can click on them to go back and forward. 

## Cross-site Request Forgery 
**_Circle 1-3_**

While a website is being made, a programmer usually makes the client-side (front-end) and server-side (back-end). For the front-end, the client would be approached with forums where he/she enters input information. On the other hand, the back-end is where the inputs are being processed and URLs being used, which then, leads to the result(s) or output(s) to appear.  

The possibility of having requests being made to the server-side of the code varies, and it does not have to be from the client-side. From having inputs, outputs, and requests being involved, sites/pages are connected, which is "one of the most powerful" feature of how the internet is wired (according to Hacksplaining. With these sites/pages being connected, there is still a common security flaw that can cause problems and that would be cross-sire request forgery(CSRF).  

This security flaw takes place when a user is fooled into using the hacker's/attacker's site, which will create a request to your site. Your server would process this attack with its HTTP request (as in like a URL) and believe that it is made from a legitimate user. 

**_Circle 3-12_**

At this point of the Hacksplaining lesson, it leads me to a simulation of this security flaw taking its course. The simulation seems to be modeled like Twitter, which I have never used before. 

Once again, hacker Mal found a way to destroy my site by seeing that it depends on GET requests, which is how a user can request for something in return from a specific data storage. This means that Mal can get and modify the URL of the requests that are being made. When Mal is able to modify, a malicious [payload](https://en.wikipedia.org/wiki/Payload_(computing)) could be introduced and the user would be fooled into going to that site. 

My play-pretend user, Vic, his email was able to be found out by Mal. Mal then emails Vic a link that grabs Vic's attention, making Vic actually click on it. Once the link is clicked, Vic gets a notification saying that he posted something, which spreads the link that Mal sent to Vic's followers. This leads to an effect called, [worms](https://www.hacksplaining.com/glossary/worms). When one user clicks on Vic's link (while it is really Mal's link), it posts the link on that other user's timeline, which exposes the link to another set of users.  

**_Circle 13_** 

To see if your site is possibly vulnerable to cross-site request forgery, you can look at this site that Hacksplaining suggested: [Netsparker Web Application Security Scanner](https://www.hacksplaining.com/exercises/csrf#/finish)  

