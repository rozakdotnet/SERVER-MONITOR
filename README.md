<h1 align="center">SERVER MONITOR</h1>
<div align="center">
  <img src="https://raw.githubusercontent.com/rozakdotnet/SERVER-MONITOR/refs/heads/main/img/dash.jpg" width="80%">
</div>

<p>Requirements:</p>
<ol>
  <li>Apache/Nginx/Litespeed/Openlitespeed/any web server</li>
  <li>Php</li>
  <li>Php-curl</li>
</ol>
<br/>
<p><b>Installation:</b></p>
<p>Download and extract the project.</p>
<pre>wget https://github.com/rozakdotnet/SERVER-MONITOR/archive/refs/heads/main.zip -O file.zip && unzip file.zip</pre>
<br/>
<p><b>Setup:</b></p>
<p>1.Run a cron to collect data of cpu load.</p>
<pre>crontab -e
* * * * * php /to-the-path/cron.php</pre>
