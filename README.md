# DotNetLinuxDeploy
Files related to a sample video created to help .Net developers to publish a simple .Net web app to Linux server

-To learn `nano` (Command-line text editor used here)  

-WinSCP website : https://winscp.net



1- `sudo apt-get update`

2-`sudo apt-get install dotnet-sdk-7.0`

3-`sudo apt-get install dotnet-runtime-7.0`

4-`sudo apt-get install aspnetcore-runtime-7.0`

5-`dotnet --info`

6-`sudo apt-get install nginx`

7-`sudo nano /etc/nginx/sites-available/default`

8-
`cd /var/www`

`sudo mkdir app`

`sudo chmod 777 app`
 
`sudo chown [UserName] app`


