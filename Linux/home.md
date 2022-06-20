## Change Linux HOME


[Jesin's Blog](https://websistent.com/)

Welcome to the Portal of Technology

-   [Facebook](https://www.facebook.com/JesinsBlog)
-   [Github](https://github.com/jesinwp)
-   [G+](https://plus.google.com/+JesinA)
-   [RSS](http://feeds.feedburner.com/jesinsblog)
-   [Twitter](https://twitter.com/jesin_a)

-   [Home](https://websistent.com/)
-   [Categories](#)
    -   [Domains](https://websistent.com/category/domains/)
    -   [Linux](https://websistent.com/category/linux/)
    -   [Networking](https://websistent.com/category/networking/)
    -   [PHP](https://websistent.com/category/php/)
    -   [Virtualization](https://websistent.com/category/virtualization/)
    -   [Web Design](https://websistent.com/category/web-design/)
    -   [Web Servers](https://websistent.com/category/web-servers/)
    -   [Windows](https://websistent.com/category/windows/)
-   [WordPress Plugins](/wordpress-plugins/)
    -   [Custom Error Pages](https://websistent.com/wordpress-plugins/custom-error-pages/)
    -   [HTTP Digest Authentication](https://websistent.com/wordpress-plugins/http-digest-authentication/)
    -   [Mailgun Email Validator](https://websistent.com/wordpress-plugins/mailgun-email-validator/)
-   [Toolbox](/tools/)
    -   [DNS Lookup Tool](https://websistent.com/tools/dns-lookup-tool/)
    -   [htdigest Generator Tool Online](https://websistent.com/tools/htdigest-generator-tool/)
    -   [htpasswd Generator Tool Online](https://websistent.com/tools/htpasswd-generator-tool/)
    -   [HTTP Headers Lookup Tool](https://websistent.com/tools/http-headers-lookup-tool/)
    -   [MD5 Encryption Tool](https://websistent.com/tools/md5-encryption-tool/)
    -   [Open Port Check Tool](https://websistent.com/tools/open-port-check-tool/)
    -   [SHA-1 Encryption Tool](https://websistent.com/tools/sha1-encryption-tool/)
    -   [URL Encoding/Decoding Tool](https://websistent.com/tools/url-encoding-decoding-tool/)
-   [About Me](https://websistent.com/about-me/)
-   [Contact Me](https://websistent.com/contact-me/)
-   [Sitemap](https://websistent.com/sitemap/)



# Change Home Directory in Linux

**Change the home directory of a Linux user** with a simple
**usermod command**. While creating a user if you didn't
specify any --home parameter Linux assumes the home directory
of the user to be /home/username even if you did specify you
can later change it to something else according to your
needs. Apart from changing the home directory using the
usermod command you'll have to assign proper ownership and
permissions to the new folder. You can also change the home
directory by editing the /etc/passwd file. I'll outline both
the steps here.

### Change the home directory using usermod

This method is for command line warriors.
Before you use the usermod command the new home directory
should be created, ownership should be assigned to the new
user and the folder should be chmoded correctly so that no
one else can access it. Run the following commands to do it.\
`mkdir /home/new_home_directory chown username:username /home/new_home_directory chmod 700 /home/new_home_directory usermod --home /home/new_home_directory username`{.source-code}

### Change the home directory by editing /etc/passwd

Alternatively you can also edit the /etc/passwd to change the
home directory. But you should be careful not to edit
anything else. Before editing this file it is always better
to create the new home directory and assign proper
permissions and ownership to it. Execute the following
commands.
`mkdir /home/new_home_directory chown username:username /home/new_home_directory chmod 700 /home/new_home_directory`{.source-code}\
Open the /etc/passwd file using a text editor and locate the
line containing the required username it should look
something like this
`username:x:500:500::/home/username:/bin/bash`{.source-code}\
change it to
`username:x:500:500::/home/new_home_directory:/bin/bash`{.source-code}\
Save the file.

Finally copy all the old content to the new home directory\
`cp -f /home/username/* /home/new_home_dir/`{.source-code}

#### Tools

-   [DNS Lookup Tool](https://websistent.com/tools/dns-lookup-tool/)
-   [htdigest Generator Tool Online](https://websistent.com/tools/htdigest-generator-tool/)
-   [htpasswd Generator Tool Online](https://websistent.com/tools/htpasswd-generator-tool/)
-   [HTTP Headers Lookup Tool](https://websistent.com/tools/http-headers-lookup-tool/)
-   [MD5 Encryption Tool](https://websistent.com/tools/md5-encryption-tool/)
-   [Open Port Check Tool](https://websistent.com/tools/open-port-check-tool/)
-   [SHA-1 Encryption Tool](https://websistent.com/tools/sha1-encryption-tool/)
-   [URL Encoding/Decoding Tool](https://websistent.com/tools/url-encoding-decoding-tool/)
