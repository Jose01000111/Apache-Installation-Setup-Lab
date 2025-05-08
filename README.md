### 🧪 Apache Installation & Setup Lab on Ubuntu

https://imgur.com/oxR6rxc

***

In this lab, I’m setting up Apache on an Ubuntu system. The goal is to get Apache running, configure it to serve web pages, and learn how to manage basic tasks like checking the status, opening the firewall, and customizing the web server with my own content. This is all about getting comfortable with how Apache works and picking up some troubleshooting skills that will come in handy for future web server setups and Linux work.

#### ✅ Step 1: Get Apache Installed
I started by updating my system and installing Apache using apt. Once it was installed, I checked the service status to make sure it was running properly. Seeing "active (running)" confirmed that Apache was up and ready.

https://imgur.com/mLfrF5e

***

https://imgur.com/WqKF7Wt

***

https://imgur.com/H885ayC

***

#### ✅ Step 2: Open the Firewall
To let web traffic through, I opened the firewall for Apache using UFW. This allowed HTTP requests on port 80, which I verified by checking the firewall status right after.

https://imgur.com/HmKVjj3

***

https://imgur.com/WABoBNs

***

#### ✅ Step 3: See the Default Page
After confirming Apache was running and open to traffic, I went to http://localhost in my browser. The default Apache page popped up, showing that my web server was working correctly.

https://imgur.com/tAqRpRW

***

#### ✅ Step 4: Add My Own Web Page
Next, I created a basic custom web page by overwriting the default with a simple HTML message. When I refreshed the browser, my custom message appeared — a quick way to confirm I could serve my own content.

https://imgur.com/itQWgfI

***

https://imgur.com/0JnJ3nG

#### ✅ Step 5: Turn on a Module & Check Logs
Finally, I enabled the rewrite module and restarted Apache to apply the change. Then I checked which modules were active and used the logs to see how Apache tracks access and errors — super helpful for future troubleshooting.

https://imgur.com/5ZyXjp4

***

https://imgur.com/RZHIBYG

***

https://imgur.com/1U1MKjw

***

#### 🧰 Technology Stack
OS: Ubuntu 22.04 LTS (Server/VM)

Web Server: Apache 2.4

Tools: apt, systemctl, ufw, bash, echo, tee

Access: Terminal with sudo privileges

#### 🎯 Goal Accomplished
Successfully deployed a basic Apache web server, made it accessible over the network, replaced the default page with a custom one, and demonstrated the ability to manage modules and analyze logs.

Let me know if you’d like a similar lab for NGINX, MySQL, PHP, or WordPress next!
