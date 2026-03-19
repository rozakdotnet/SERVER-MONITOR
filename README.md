<h1 align="center">SERVER MONITOR</h1>
<div align="center">
  <img src="https://raw.githubusercontent.com/rozakdotnet/SERVER-MONITOR/refs/heads/main/img/dash.jpg" width="80%">
</div>
<p>Server monitor designed for HomeServer and HomeLab where include Immich and AdguardHome api's, however it still works on vps. The temperature information only allowed by deicated server, storage information access allowed in dedicated server and KVM vps.</p>
<p><b>Requirements:</b></p>
<ol><li>Linux OS</li>
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
<p>2.Edit configuration with following the instruction on the file (conf.ini)</p>
<pre>nano conf/conf.ini</pre>
<br/>
<br/>
<p>Please allow 10 minutes for api to syncron data.</p>
<h2 align="center">Important</h1>
Block direct access to the configuration file (conf.ini).
<p>For Apache:</p>
<pre> &lt;FilesMatch "\.ini$"&gt; 
  Require all denied 
  &lt;/FilesMatch&gt;</pre>
<p>For Nginx:</p>
<pre>location /conf/ {
    deny all;
    access_log off;
    log_not_found off;
}</pre>
<p>For Openlitespeed:</p>
<pre>Login -> Virtual host -> Context -> Static -> URI: /conf/ -> Location: /To-the-path/conf -> Accessible: no -> Expires: no</pre>
<h3><a href="https://bossku.eu.org" target="_new">Live Demo</a></h3>
