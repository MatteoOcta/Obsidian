
```
##
# @package    Joomla
# @copyright  Copyright (C) 2005 - 2019 Open Source Matters. All rights reserved.
# @license    GNU General Public License version 2 or later; see LICENSE.txt
##

##
# READ THIS COMPLETELY IF YOU CHOOSE TO USE THIS FILE!
#
# The line 'Options +FollowSymLinks' may cause problems with some server configurations.
# It is required for the use of mod_rewrite, but it may have already been set by your
# server administrator in a way that disallows changing it in this .htaccess file.
# If using it causes your site to produce an error, comment it out (add # to the
# beginning of the line), reload your site in your browser and test your sef urls. If
# they work, then it has been set by your server administrator and you do not need to
# set it here.
##

## No directory listings
<IfModule autoindex>
  IndexIgnore *
</IfModule>

## Suppress mime type detection in browsers for unknown types
<IfModule mod_headers.c>
Header always set X-Content-Type-Options "nosniff"
</IfModule>

## Can be commented out if causes errors, see notes above.
Options +FollowSymlinks
Options All -Indexes

## Mod_rewrite in use.

RewriteEngine On

## Begin - Rewrite rules to block out some common exploits.
# If you experience problems on your site then comment out the operations listed
# below by adding a # to the beginning of the line.
# This attempts to block the most common type of exploit `attempts` on Joomla!
#
# Block any script trying to base64_encode data within the URL.
RewriteCond %{QUERY_STRING} proc/self/environ [OR]
RewriteCond %{QUERY_STRING} mosConfig_[a-zA-Z_]{1,21}(=|\%3D) [OR]
RewriteCond %{QUERY_STRING} base64_(en|de)code[^(]*\([^)]*\) [OR]
# Block any script that includes a <script> tag in URL.
RewriteCond %{QUERY_STRING} (<|%3C)([^s]*s)+cript.*(>|%3E) [NC,OR]
# Block any script trying to set a PHP GLOBALS variable via URL.
RewriteCond %{QUERY_STRING} GLOBALS(=|\[|\%[0-9A-Z]{0,2}) [OR]
# Block any script trying to modify a _REQUEST variable via URL.
RewriteCond %{QUERY_STRING} _REQUEST(=|\[|\%[0-9A-Z]{0,2})
# Return 403 Forbidden header and show the content of the root home page
RewriteRule .* index.php [F]
#
RewriteCond %{REQUEST_METHOD} GET
RewriteCond %{QUERY_STRING} [a-zA-Z0-9_]=http:// [OR]
RewriteCond %{QUERY_STRING} [a-zA-Z0-9_]=(\.\.//?)+ [OR]
RewriteCond %{QUERY_STRING} [a-zA-Z0-9_]=/([a-z0-9_.]//?)+ [NC]
RewriteRule .* - [F]
#
RewriteCond %{QUERY_STRING} \=PHP[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12} [NC]
RewriteRule .* - [F]
## Back-end protection
RewriteRule ^administrator/?$ - [L]
RewriteRule ^administrator/index\.(php|html?)$ - [L]
RewriteRule ^administrator/index[23]\.php$ - [L]
RewriteRule ^administrator\/components\/com_joomlaupdate\/restore\.php$ - [L]
RewriteRule ^administrator/(components|modules|templates|images|plugins|cache)/.*\.(webp|jpe|jpg|jpeg|jp2|jpe2|png|gif|bmp|css|js|swf|html|mpg|mp3|mpeg|mp4|avi|wav|ogg|ogv|xls|xlsx|doc|docx|ppt|pptx|zip|rar|pdf|xps|txt|7z|svg|odt|ods|odp|flv|mov|htm|ttf|woff|eot|JPG)$ - [L]
RewriteRule ^administrator/ - [F]
## Explicitly allow access only to XML-RPC's xmlrpc/index.php or plain xmlrpc/ directory
RewriteRule ^xmlrpc/(index\.php)?$ - [L]
RewriteRule ^xmlrpc/ - [F]
## Allow limited access for certain Joomla! system directories with client-accessible content
RewriteRule ^(components|modules|templates|images|plugins|media|libraries|media/jui/fonts|cache)/.*\.(webp|jpe|jpg|jpeg|jp2|jpe2|png|gif|bmp|css|js|swf|html|mpg|mp3|mpeg|mp4|avi|wav|ogg|ogv|xls|xlsx|doc|docx|ppt|pptx|zip|rar|pdf|xps|txt|7z|svg|odt|ods|odp|flv|mov|ico|htm|ttf|woff|woff2|eot|JPG)$ - [L]
RewriteRule ^(components|modules|templates|images|plugins|media|libraries|media/jui/fonts|cache)/ - [F]
## Disallow front-end access for certain Joomla! system directories (unless access to their files is allowed above)
RewriteRule ^includes/js/ - [L]
RewriteRule ^(cache|includes|language|logs|tmp)/ - [F]
## Disallow access to rogue PHP files throughout the site, unless they are explicitly allowed
RewriteCond %{REQUEST_FILENAME} (\.php)$
RewriteCond %{REQUEST_FILENAME} !(/index[23]?\.php)$
RewriteCond %{REQUEST_FILENAME} !(/rappel/appel.php)$
RewriteCond %{REQUEST_FILENAME} -f
RewriteRule (.*\.php)$ - [F]
RewriteRule ^(htaccess\.txt|configuration\.php-dist|php\.ini)$ - [F]
## End - Rewrite rules to block out some common exploits.

## Begin - Custom redirects
#
# If you need to redirect some pages, or set a canonical non-www to
# www redirect (or vice versa), place that code here. Ensure those
# redirects use the correct RewriteRule syntax and the [R=301,L] flags.
RewriteCond %{HTTP_HOST} !^www\..+$ [NC]
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}/$1 [R,L]
#
## End - Custom redirects

##
# Uncomment the following line if your webserver's URL
# is not directly related to physical file paths.
# Update Your Joomla! Directory (just / for root).
##

RewriteBase /

## Begin - Joomla! core SEF Section.
#
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
#
# If the requested path and file is not /index.php and the request
# has not already been internally rewritten to the index.php script
RewriteCond %{REQUEST_URI} !^/index\.php
# and the requested path and file doesn't directly match a physical file
RewriteCond %{REQUEST_FILENAME} !-f
# and the requested path and file doesn't directly match a physical folder
RewriteCond %{REQUEST_FILENAME} !-d
# internally rewrite the request to the index.php script
RewriteRule .* index.php [L]
#
## End - Joomla! core SEF Section.
```