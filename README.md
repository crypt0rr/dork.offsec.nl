# Google Dorks for Bug Bounty

A list of Google Dorks for Bug Bounty, Web Application Security, and Pentesting

<p>
Credits to TakSec: https://taksec.github.io/google-dorks-bug-bounty/
</p>

---

### Broad domain search w/ negative search

> site:target.com -www -shop -share -ir -mfa

### Find subdomains

> site:*.target.com

### Find exposed documents

> site:"target[.]com" ext:doc | ext:docx | ext:odt | ext:pdf | ext:rtf | ext:sxw | ext:psw | ext:ppt | ext:pptx | ext:pps | ext:csv

### Find exposed git files

> site:target.com "index of" inurl:.git

> site:target.com "intitle:"index of" .git/hooks/

> site:target.com filetype:git | ext:git

### Directory listings

> site:target.com intext:"index of /"

> site:target.com intitle:"index of" "docker-compose.yml"

> site:target.com intitle:"index of"|"access_token.json"

> site:target.com intitle:"index of" "config.json"

> site:target.com intitle:"index of" "service-Account-Credentials.json" | "creds.json"

> site:target.com intitle:"index of" "db.json"

> site:target.com intitle:"index of" "credentials.json"

> site:target.com intitle:"index of" "awsconfig.json"

> site:target.com intext:"index of" /etc/passwd

> site:target.com intext:"index of" /etc/shadow

> site:target.com "index of" id_rsa

> site:target.com "index of" private.key

> site:target.com "index of" inurl:.git

> site:target.com "intitle:"index of" .git/hooks/

### PHP extension w/ parameters

> site:target.com ext:php inurl:?

### Disclosed XSS and Open Redirects

> site:openbugbounty.org inurl:reports intext:"target.com"

### Juicy Extensions

> site:"target[.]com" ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

### Code Leaks / External websites leaks

> site:pastebin.com "target.com"

> site:jsfiddle.net "target.com"

> site:codebeautify.org "target.com"

> site:codepen.io "target.com"

> site:scribd.com "target.com"

> site:npmjs.com "target.com"

> site:npm.runkit.com "target.com"

> site:libraries.co "target.com"

> site:ycombinator.com "target.com"

> site:coggle.it "target.com"

> site:papaly.com "target.com"

> site:trello.com "target.com"

> site:prezi.com "target.com"

> site:jsdelivr.net "target.com"

> site:codeshare.io "target.com"

> site:sharecode.io "target.com"

> site:repl.it "target.com"

> site:gitter.im "target.com"

> site:bitbucket.org "target.com"

> site:zoom.us "target.com"

> site:atlassian.com "target.com"

> inurl:gitlab "target.com"

### Cloud Storage

> site:s3.amazonaws.com "target.com"

> site:blob.core.windows.net "target.com"

> site:googleapis.com "target.com"

> site:drive.google.com "target.com"

> site:dev.azure.com "target[.]com"

> site:onedrive.live.com "target[.]com"

> site:digitaloceanspaces.com "target[.]com"

> site:sharepoint.com "target[.]com"

> site:s3-external-1.amazonaws.com "target[.]com"

> site:s3.dualstack.us-east-1.amazonaws.com "target[.]com"

> site:dropbox.com/s "target[.]com"

> site:box.com/s "target[.]com"

> site:docs.google.com inurl:"/d/" "target[.]com"

### XSS prone parameters

> inurl:q= | inurl:s= | inurl:search= | inurl:query= inurl:& site:target.com

### Open Redirect prone parameters

> inurl:"url=" | inurl:"return=" | inurl:"next=" | inurl:"redir=" | inurl:"http" | inurl:"%3Dhttp" | inurl:"%3D%2F" | inurl:"redirect"= | inurl:"redirecturl=" | inurl:"redirect_url=" | inurl:"returnurl=" | inurl:"relaystate=" | inurl:"forward=" | inurl:"forwardurl=" | inurl:"forward_url=" | inurl:"uri=" | inurl:"dest=" | inurl:"destination=" site:target.com

### SQLi Prone Parameters

> inurl:id= | inurl:pid= | inurl:category= | inurl:cat= | inurl:action= | inurl:sid= | inurl:dir= inurl:& site:target.com

### SSRF Prone Parameters

> inurl:http | inurl:url= | inurl:path= | inurl:dest= | inurl:html= | inurl:data= | inurl:domain=  | inurl:page= inurl:& site:target.com

### LFI Prone Parameters

> inurl:include | inurl:dir | inurl:detail= | inurl:file= | inurl:folder= | inurl:inc= | inurl:locate= | inurl:doc= | inurl:conf= inurl:& site:target.com

### RCE Prone Parameters

> inurl:cmd | inurl:exec= | inurl:query= | inurl:code= | inurl:do= | inurl:run= | inurl:read=  | inurl:ping= inurl:& site:target.com

### SQL errors

> site:target.com intext:"sql syntax near" | intext:"syntax error has occurred" | intext:"incorrect syntax near" | intext:"unexpected end of SQL command" | intext:"Warning: mysql_connect()" | intext:"Warning: mysql_query()" | intext:"Warning: pg_connect()"

### Configuration files

> inurl:config | inurl:env | inurl:setting | inurl:backup | ext:xml | ext:conf | ext:cnf | ext:reg | ext:inf | ext:rdp | ext:cfg | ext:txt | ext:ora | ext:ini site:target[.]com

### Sensitive Parameters

> inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:target[.]com

### JFrog Artifactory

> site:jfrog.io "target[.]com"

### Firebase

> site:firebaseio.com "target[.]com"

### API Docs

> inurl:apidocs | inurl:api-docs | inurl:swagger | inurl:api-explorer site:"target[.]com"

> site:target.com inurl:/swagger-ui.html

> site:target.com inurl:/api/swagger

> site:target.com inurl:/api/v1/docs | inurl:/api/v2/docs | inurl:/api/v3/docs

> site:target.com inurl:/api/apidocs

### File upload endpoints

> site:target.com ”choose file”

### Dependency confusion (packages files)

> site:*target.com inurl:/ui/package.json

> site:*target.com inurl:/ui/package-lock.json

> site:*target.com inurl:/package.json

### Cached versions

> cache:target.com

### Linked websites

> link:target.com

### Find employees

> site:linkedin.com "target[.]com"

## Dorks that work better w/o domain

### Bug Bounty programs and Vulnerability Disclosure Programs

> "submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"

> site:*/security.txt "bounty"

### Apache Server Status Exposed

> site:*/server-status apache

### WordPress

> inurl:/wp-admin/admin-ajax.php

> intext:"Index" inurl:"wp-" -wordpress.org -stackexchange -github

> inurl:"/wp-json/wp/v2/users/" "id":1,"name":" -wordpress.stackexchange.com -stackoverflow.com

> inurl:"/wp-content/uploads"

> inurl:"wp-register.php" -wordpress.com -wordpress.org -github

> intitle:"index of" "wp-config.php.bak"

### Drupal

> intext:"Powered by" & intext:Drupal & inurl:user

> intext:"Powered by Drupal" inurl:"/node/1" -drupal.com -drupal.org -github

> inurl:"sites/all/modules/ckeditor" -drupalcode.org

### Joomla

> site:*/joomla/login

> inurl:"/libraries/joomla/database/"

> inurl:"/v1/config/application"

### Symfony

> intitle:"index of" "symfony/config"

> inurl:"_fragment" | inurl:"_profiler"

> inurl:"_profiler/phpinfo"

> inurl:"_profiler/open"

### Ruby on rails

> inurl:"index.rb"

> inurl:"/config/database.yml"

> inurl:"/config/initializers/secret_token.rb"

> inurl:"/db/seeds.rb"

> inurl:"/db/development.sqlite3"


---

Medium articles for more dorks:

https://thegrayarea.tech/5-google-dorks-every-hacker-needs-to-know-fed21022a906

https://infosecwriteups.com/uncover-hidden-gems-in-the-cloud-with-google-dorks-8621e56a329d

https://infosecwriteups.com/10-google-dorks-for-sensitive-data-9454b09edc12

Top Parameters:

https://github.com/lutfumertceylan/top25-parameter

Proviesec dorks:

https://github.com/Proviesec/google-dorks
