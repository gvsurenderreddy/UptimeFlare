UptimeFlare
==============

A PHP web hook to handle down notifications from uptimerobot. If a DOWN notification is received, then it'll change the A record of a domain on cloudflare to a backup IP set by you.

<br><br>
License: MIT<br>
Depenedencies: Web Server, PHP, php-curl lib
<br><br>

Setup:
1. I suggest you rename the php file to something obsecure.
2. Add / change the global vars section. It constents of credentials and other information that needs to be modified to your needs.
3. Upload this script to the desired server, make sure the script is accessible via the internet.
4. On uptimeRobot:
	Create a new alert contect and select web hook. For url, put in the url to the php script and add "?key=YourKeySetInThePHPScript&". 
	If my $key was set to <b>HelloWorld</b> and I renamed my script to <b>monitorUP.php</b> which is accessible via <b>127.0.0.1</b>, then for the url I would put
	<i>http://127.0.0.1/monitorUP.php?key=HelloWorld&</i> Make sure you have the <b>&</b> at the end.
5. Add this alert type to your websites. It's recommended that you have more than the PHP hook as a notification type, so you can switch it back to the primary server once it's up. With this setup, a website shouldn't have a downtime of more than ~6 minutes, assuming your DNS provider does not cache queries.
<br><br>
You can reach me on <a href="http://twitter.com/blackdotsh/> twitter </a>.