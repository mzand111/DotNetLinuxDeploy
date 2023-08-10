# DotNetLinuxDeploy
Files related to a sample video created to help .Net developers to publish a simple .Net web app to Linux server

* [The tutorial](https://youtu.be/cpkX9mScZEU)
  
* To learn `nano` (Command-line text editor used here)  you can wath [this 5 min video](https://www.youtube.com/watch?v=NV9PyPJKqH4) 

* [WinSCP website](https://winscp.net)


# Commands used in the video

1-`sudo apt-get update`

2-`sudo apt-get install dotnet-sdk-7.0`

3-`sudo apt-get install dotnet-runtime-7.0`

4-`sudo apt-get install aspnetcore-runtime-7.0`

5-`dotnet --info`

6-`sudo apt-get install nginx`

7-`sudo nano /etc/nginx/sites-available/default`

```
   location / {
       proxy_pass http://localhost:5000;
       proxy_http_version 1.1;
       proxy_set_header Upgrade $http_upgrade;
       proxy_set_header Connection keep-alive;
       proxy_set_header Host $host;
       proxy_cache_bypass $http_upgrade;
       proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
       proxy_set_header X-Forwarded-Proto $scheme;
   }
```

8-

  `cd /var/www`
  
  `sudo mkdir app`
  
  `sudo chmod 777 app`
   
  `sudo chown [UserName] app`

9- 

  `cd /var/www/app`
  
  `sudo dotnet [YourAppName].dll`

10-`nano /etc/systemd/system/[YourAppName].service` and then use the `LinuxWebAppTest.service` to create your file. Replace LinuxWebAppTest with your app's name


11-

`sudo systemctl enable [YourAppName].service`


`sudo systemctl start [YourAppName].service`

12-`sudo nginx -s reload`
