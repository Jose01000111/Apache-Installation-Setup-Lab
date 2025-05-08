## 🧪 Apache Installation & Setup Lab on Ubuntu

<p align="center">
<img src="https://i.imgur.com/oxR6rxc.png" alt="osTicket logo"/>
</p>

***

In this lab, I’m setting up Apache on an Ubuntu system. The goal is to get Apache running, configure it to serve web pages, and learn how to manage basic tasks like checking the status, opening the firewall, and customizing the web server with my own content. This is all about getting comfortable with how Apache works and picking up some troubleshooting skills that will come in handy for future web server setups and Linux work.

### ✅ Step 1: Get Apache Installed
I started by updating my system and installing Apache using apt. Once it was installed, I checked the service status to make sure it was running properly. Seeing "active (running)" confirmed that Apache was up and ready.


<p align="center">
<img src="https://i.imgur.com/mLfrF5e.png" alt="osTicket logo"/>
</p>

#### sudo apt update 🗂️→ This command checks for any updates and refreshes the software list, so your system knows about the latest versions available.

***

<p align="center">
<img src="https://i.imgur.com/WqKF7Wt.png" alt="osTicket logo"/>
</p>

#### sudo apt install apache2 -y 📥→ This installs the Apache web server, and the -y automatically agrees to install everything without asking for confirmation.

***

<p align="center">
<img src="https://i.imgur.com/H885ayC.png" alt="osTicket logo"/>
</p>

#### sudo systemctl status apache2 ✅→ This shows the status of Apache to confirm that it’s running correctly. You should see "active (running)" if everything is working.

***

### ✅ Step 2: Open the Firewall
To let web traffic through, I opened the firewall for Apache using UFW. This allowed HTTP requests on port 80, which I verified by checking the firewall status right after.

<p align="center">
<img src="https://i.imgur.com/HmKVjj3.png" alt="osTicket logo"/>
</p>

#### sudo ufw allow 'Apache' 🚪→ This tells the firewall to allow web traffic through, letting people access your Apache web server over HTTP (the web).


***

<p align="center">
<img src="https://i.imgur.com/WABoBNs.png" alt="osTicket logo"/>
</p>

#### sudo ufw status 📜→ This shows the current firewall settings and confirms that Apache is allowed to receive traffic.

***

### ✅ Step 3: See the Default Page
After confirming Apache was running and open to traffic, I went to http://localhost in my browser. The default Apache page popped up, showing that my web server was working correctly.

<p align="center">
<img src="https://i.imgur.com/tAqRpRW.png" alt="osTicket logo"/>
</p>

***

### ✅ Step 4: Add My Own Web Page
Next, I created a basic custom web page by overwriting the default with a simple HTML message. When I refreshed the browser, my custom message appeared — a quick way to confirm I could serve my own content.

<p align="center">
<img src="https://i.imgur.com/itQWgfI.png" alt="osTicket logo"/>
</p>

***

<p align="center">
<img src="https://i.imgur.com/0JnJ3nG.png" alt="osTicket logo"/>
</p>

### ✅ Step 5: Turn on a Module & Check Logs
Finally, I enabled the rewrite module and restarted Apache to apply the change. Then I checked which modules were active and used the logs to see how Apache tracks access and errors — super helpful for future troubleshooting.

<p align="center">
<img src="https://i.imgur.com/5ZyXjp4.png" alt="osTicket logo"/>
</p>

#### sudo a2enmod rewrite 🔧→ This enables the “rewrite” module in Apache, which is useful for creating clean and user-friendly URLs (like /about-us instead of /index.php?page=about).

#### sudo systemctl restart apache2 🔄→ This restarts Apache, applying any changes you've made, like enabling new features or modules.

#### apache2ctl -M 📋→ This lists all the active modules (like the rewrite module) that are currently enabled in Apache.

***

<p align="center">
<img src="https://i.imgur.com/RZHIBYG.png" alt="osTicket logo"/>
</p>

#### sudo tail /var/log/apache2/access.log 👀→ This shows recent access logs, so you can see who is visiting your site.

***

<p align="center">
<img src="https://i.imgur.com/1U1MKjw.png" alt="osTicket logo"/>
</p>

#### sudo tail /var/log/apache2/error.log ⚠️→ This shows error logs, which help you troubleshoot any problems Apache has encountered.

***

### 🧰 Technology Stack
OS: Ubuntu 22.04 LTS (Server/VM)

Web Server: Apache 2.4

Tools: apt, systemctl, ufw, bash, echo, tee

Access: Terminal with sudo privileges

### 🎯 Goal Accomplished
Successfully deployed a basic Apache web server, made it accessible over the network, replaced the default page with a custom one, and demonstrated the ability to manage modules and analyze logs.

Let me know if you’d like a similar lab for NGINX, MySQL, PHP, or WordPress next!
