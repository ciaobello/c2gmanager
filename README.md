##c2g-manager (contao 2.11.13) installation

(Contao2go for Linux & Osx ..)

The DB, .cto and a contao_new.c2g file you can Download
here >> https://github.com/ciaobello/c2gmanager


```
1) You just have to look that your Webserver works fine and supports contao2.
A good idea would be: https://puphpet.com/
```
```
2) Make sure you use the same Contao Version as the DB is made for.
When i started the Project I made it with contao 2.11.13 (c2gadmin extention will just work in contao 2)
```
```
3) Install first the Extentions c2gadmin & flexi_responsive_template 
(BackupDB is not needet to install if you import the DB over the install.php)
Just delete after in the ER the non existing extention (I used it to export the DB).
```
```
4) I made some changes in the flexi_responsive_template to display the Hosts nicely.
Do not import responsive.cto use the c2g-manager_res.cto (copy it to the tl_files folder first). 
```
```
6) extract the c2g-manager-tl_root.tar.gz archive in to the tl root.
It will ovrewrite the german importC2GFile.php and make it english.
```
```
7)As c2gadmin ist not working with "Request Tokens" you have to desactivate it in the Settings.
```
```
8)If you want to start c2g-admin not as Localhost just add the IP to the Hosts File
 and give a name you like. Mine is named c2g.
So, with c2g as URL I start my conta2go >> c2g-manager gui.
With c2g/vhosts/myproject i open the project i like quickly in the URL.
```
```
*IMPORTANT*
Essential that mod_rewrite works fine on you default Web is:
How to permit changes in the .htaccess file:

To allow the .htaccess file to override standard website configs,
start by opening up the configuration file.
NB: You will need sudo privileges for this step.

----------------------------------------------
sudo nano /etc/apache2/sites-available/default
----------------------------------------------

Once inside that file, find the following section,
and change the line that says AllowOverride from None to All.
The section should now look like this:

 <Directory /var/www/>
                Options Indexes FollowSymLinks MultiViews
                AllowOverride All
                Order allow,deny
                allow from all
 </Directory>

After you save and exit that file, restart apache.

.htacess files will now be available for all of your sites.

----------------------------
sudo service apache2 restart
----------------------------

Now you are all set up to rewrite your site’s URLs.

```
```
9)Just import contao_new.c2g to your c2gmanager and restore the Project.
You will get your first Host in the Overview (Hosts). 
This project is empty and brings up 2 hidden scripts to automate
the installation for yor forther Contao projects.
Just copy it and give it a new project name. Enjoi it and be happy ;)
```


Extra:
http://www.contao2go.org/dokumentation/articles/bestehende-seite-online-in-ein-c2g-packen.html

##Create a .c2g from a existing Online-Website

If you want to bring a online Website in your c2gmanager (contao2go),
grab a script from the Contao2go page (link above).
Extract & copy it to the Website you want to get localy and execute the script
on the Server (example.com/c2g_generate.php).

Copy the generated .c2g File to your webserver in the /backups folder and restore the Project.

Simple and easy ;)

