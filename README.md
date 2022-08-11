<h1>Sellart</h1>

An integrated platform of two systems that allows the clients to buy and inquire about the sold art, helps the aritst issue invoices and handle request with less time and more efficiency.

Merging two systems inside one directory and building a homepage file that runs both using Iframes. JavaScript will then dynamically allow the client to do the following :

1: Slide between the two iframes in a smooth transition of a sharp HTML and CSS combination.
2: Drags the paintings from one iframe and drop it in the second that has the CRM's public form in order to inform the artist.
3: The artist can then issue invoices and manage clients using the back end of the second system while uploading his artwork to the first.

Licenses of both systems are free and allow you to use and distribute for commercial purpose.
The two licenses are :
osTicket
Piwigo

The two licenses are under :
GPL v2 - https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html


## Requirements

 * A webserver (Apache or nginx recommended)
 * PHP 5.3 or greater (7+ recommended)
 * MySQL 5 or greater or MariaDB equivalent
 * ImageMagick (recommended) or PHP GD
 * If you're using php v8.0, make sure PHP Extension mcrypt & xmlrpc are enabled 

### Installation

Keep in mind that the root folder containts two other folders for each system and the home.html is the thing that merges them.
Thereforem for each install the directory will be one extra tree, the folders will be called sysfirst for `osTicket` and systwo for `Piwigo`

#### Installing the osTicket (sysfirst)
----------
osTicket now supports bleeding-edge installations. The easiest way to
install the software and track updates is to clone the public repository.
Create a folder on you web server (using whatever method makes sense for
you) and cd into it. Then clone the repository (the folder must be empty!):

    `git clone https://github.com/osTicket/osTicket`

And deploy the code into somewhere in your server's www root folder, for
instance

    `cd osTicket`
    `php manage.php deploy --setup /var/www/htdocs/sysfirst/osticket/`

Then you can configure your server if necessary to serve that folder, and
visit the page and install osTicket as usual. Go ahead and even delete
setup/ folder out of the deployment location when you’re finished. Then,
later, you can fetch updates and deploy them (from the folder where you
cloned the git repo into)

    `git pull`
    `php manage.php deploy -v /var/www/htdocs/sysfirst/osticket/`

#### Installing Piwigo Gallery

1. Open the second script in you web browser `http://your-domain.com/secondsys/piwigo-netinstall.php`
2. Once all files are transfered, go to the web address with a web browser, for example http://example.com/secondsys/photos Piwigo will detect nothing is installed yet, and redirect you to the installation page.
3. Now comes the MySQL database settings and the webmaster account to administer your gallery
4. Fill in MySQL database connection settings, as given by your web hosting provider::

    Host
    User ( Warning, your web hosting provider may provide separate connection settings for FTP and MySQL.)
    Password
    Database name
    A prefix for Piwigo table names (Most often, web hosting providers allow a single database per customer, but you can create as many tables as you want in the same database. To avoid conflicts with other web applications, or allow several Piwigo installations on the same website, the table names have a prefix. By default, this prefix is ”piwigo_”, but you can change it (only alphanumeric characters are allowed).) 

5. After installing both systems, go to `http://your-domain.com/home.html` and confirm that both systems are loading
6. Leaving the gallery script unedited for later, jump to the invoice plane to create a public form by going to 

#### Remove `index2.php` from the URL

If you want to remove `index2.php` from the URL, follow these instructions. However, this is an _optional_ step and not a requirement. If it's not working correctly, take a step back and use the application with out removing that part from the URL.

1. Make sure that [mod_rewrite](https://go.invoiceplane.com/apachemodrewrite) is enabled on your web server.
2. Set the `REMOVE_INDEXPHP` setting in your `ipconfig.php` to `true`.
3. Rename the `htaccess` file to `.htaccess`


### Security Vulnerabilities

If you discover a security vulnerability please send an e-mail to `mail@invoiceplane.com` before disclosing the vulnerability to the public.
All security vulnerabilities will be promptly addressed.



