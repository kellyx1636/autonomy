# Entry #2: Continuing Learning  
For this week, I continued to learn the topics that were presented to me. The one that I learned was Directory Traversal. 

##### Some Side Notes: 
If you would like to follow along with what you will read in my entry, click on this link: [Hacksplaining: Direct Traversal](https://www.hacksplaining.com/exercises/directory-traversal). 

When you click on the link, you will notice that there are circles on the top-left corner. Those circles are like the steps or slides of a presentation. You can click on them to go back and forward. [Here is how they look!](../images/meaning-of-circles.lnk)

## Directory Traversal
"What is directory traversal?", you may ask. Well, the purpose of directory traversal is to prevent hackers from being able to locate sensitive files of a user through a file path (URL).  

The first three circles/parts for this topic only gave me some information directly. 
* 1st circle: There are two types of websites. Some are made to be accessible by the user's browser and others are not. For the ones that are made to be accessible, it could be through the usage of JavaScript and CSS files. 
* 2nd circle: URLs are usually used in web servers to specify template files and assests in a file system. If you compare how you got to access a specific file and its URL structure, you can see that they show the same thing.  
* 3rd circle: If your server is not wired well and fails to keep certain files away from the public's view, that could be another way for hackers to obtain your files. 

After learning about these facts, I am presented with a simulation. I was told to pretend that I have a website that holds menus from restaurants that users can find and download. Then, I was presented with the following URL: ```foodle.com/menus?menu=arachnaburger.pdf``` 

**Break Down of This URL:** 
* ```foodle.com``` --> Website's homepage URL 
* ```menu``` --> Parameter value  
* ```/menus``` --> Goes into the website's storage of menus  
* ```arachnaburger.pdf``` --> What the user requested the website's server to find 

In this case, when a raw file name is used when user is downloading. With that, a hacker/attacker can use it to go to the files' directory and access another file. Some servers do no check on the file paths that are given, which leads to the hacker given the ability to access other sensitive files. 

### My Interaction With The Simulation 
For those who are following my entry while using the link I provided, this section my entry is where I am in circle 9. 

I was presented with this URL: ```foodle.com/menus?menu=../../../../```. Then, I was told to enter ssl/private.key at the end of it. Once I did that, I realized that I just downloaded something that was not suppose to be shared to the public (remember, this is a simulation). 

At the end of these circles, I am shown a resource. This resource scans websites to see if there are any vulnerabilities. If you would like to check it out, head onto this link: [Netsparker](https://www.netsparker.com/netsparker-web-application-security-scanner/dead-accurate-automated-web-vulnerability-scanner/?utm_source=hacksplaining.com&&utm_content=is+website+vulnerable+lesson&utm_medium=banner&utm_campaign=nc+advert)   

#### Takeaways 
* There are two types of websites: accessible by browser and ones that are not accessible by browsers. 
* URL is like a file path. Since it can show where it came from, user would need to be careful with what the URL gives other users access to. 
* Structure of a URL: websitename.com/folder-name?parameter=user-request 

#### Next Step(s)
Since there are 25 topics to cover in this website (presented in 5 by 5), I will try to learn about the next 4 topics this week. While doing so, I will also try to review every now and then so that I do not forget what I learned before.  


