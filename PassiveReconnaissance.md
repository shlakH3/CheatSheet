# Google Dorks
~~~
site:<keyword>
~~~

~~~
inurl:<keyword>
~~~

~~~
filetype:<keyword>
~~~

~~~
intitle:<keyword>
~~~

# Domain
~~~
whois <domain>
~~~

~~~
host <domain>
~~~

~~~
dnsrecon -d <domain>
~~~
~~~
dnsrecon -d <domain> -axfr
~~~

~~~
Sublist3r -d <domain> -e <SearchEngine>
~~~

bash script
~~~
for ip in $(<Subdomainlist>); do host $ip.<TargetHost>; done
~~~
~~~
for ip in $(seq <from> <to>); do host x.x.x.$ip; done | grep -v "not found”
~~~
site
~~~
https://dnsdumpster.com/
~~~

# Password
~~~
https://scatteredsecrets.com/
~~~

~~~
https://haveibeenpwned.com/
~~~

# Web
~~~
whatweb <URL>
~~~

~~~
Wappalyzer 
~~~

~~~
https://sitereport.netcraft.com/
~~~

# Github
~~~
owner:<> path:users
~~~

# Other
SSL
~~~
https://securityheaders.com/
~~~

Metadata(.pdf ...etc)
~~~
exiftool
~~~

~~~
https://archive.org/
~~~
