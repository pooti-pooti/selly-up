<h1>Sellart</h1>

An integrated platform of three systems that allows the clients to buy and inquire about the sold art, helps the aritst issue invoices and handle request with less time and more efficiency and provides a bidding mechanism for artists to put their work for bidding.

Merging three systems inside one directory and building a homepage file that runs all using Iframes. JavaScript will then dynamically allow the client to do the following :

1: Slide between to a purchase(request) form, in a smooth transition of a sharp HTML and CSS combination.<br>
2: Drag the paintings from one iframe and drop it in the second that has the purchase form in order to inform the artist.<br>

Allows the Artist to do the following : 

1: The aritst looks at the request and identifies which paiting is needed to be sold or inquired about.<br>
2: The artist can then issue invoices and manage clients using the back end of the CRM system while uploading his artwork to the gallery.<br>

### Licenses
All systems are free and allow you to use and distribute for commercial purpose, but never claim to be the creator of the InvoicePlane(sysThree) or make modifications of their logo. Although, you can add your own logo.

The two licenses are :

1. GPL v2
2. InvoicePlane License 


### Requirements

 * A webserver (Apache or nginx recommended)
 * PHP 5.3 or greater (7+ recommended)
 * MySQL 5 or greater or MariaDB equivalent
 * ImageMagick (recommended) or PHP GD
 * If you're using php v8.0, make sure PHP Extension `mcrypt` & `xmlrpc` are enabled 

## Installation

Keep in mind that the root folder containts three other folders for each system and the home.html is the thing that merges them.
Therefore, for each install the directory will be one extra tree, the folders will be called sysOne for `osTicket`, sysTwo for `Piwigo` and sysThree for (InvoicePlane).

1. Install sysOne by going to `http://your-domain.com/sysOne` and following the instruction there.
2. Open the sysTwo in you web browser `http://your-domain.com/sysTwo/piwigo-netinstall.php`
3. Once all files are transfered, go to the web address with a web browser, for example `http://example.com/sysTwo/photos` Piwigo will detect nothing is installed yet, and redirect you to the installation page.
4. Now comes the MySQL database settings and the webmaster account to administer your gallery
5. Fill in MySQL database connection settings, as given by your web hosting provider::

    Host
    User ( Warning, your web hosting provider may provide separate connection settings for FTP and MySQL.)
    Password
    Database name
    A prefix for Piwigo table names (Most often, web hosting providers allow a single database per customer, but you can create as many tables as you want in the same database. To avoid conflicts with other web applications, or allow several Piwigo installations on the same website, the table names have a prefix. By default, this prefix is ”piwigo_”, but you can change it (only alphanumeric characters are allowed).) 

6. Make a copy of the `http://your-domain.com/sysThree/ipconfig.php.example` file and rename this copy to `ipconfig.php`.
7. Open the `ipconfig.php` file and set your URL like specified in the file.
8. Open `http://your-domain.com/sysThree/index.php/setup` and follow the instructions.
9. Open up `http://your-domain.com/home.html` and confirm that the three scripts are loading including the request form on the left.
10. To be continued...



### Security Vulnerabilities

If you discover a security vulnerability please send an e-mail to `management@ushby.org` before disclosing the vulnerability to the public.
All security vulnerabilities will be promptly addressed.
