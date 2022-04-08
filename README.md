# Simple php image uploader 

This is a simple and lightweight image uploder, that you can use to build a bigger project with. 
The uploader is a simple php file that saves an image from a POST request to a folder and sends you the url to access the image.

All images / Files are going to embed in applications like discord/ whatsapp.

# Setup:

1. Copy the upload.php file and upload it to your web server. (Example: /var/www/website/upload.php)
2. Customize the script:
  -> Line 3: Exchange the SECRET KEY with your upload key 
  -> Line 4: Exchange the uploadhost with the domain that has the upload script: (Ex: https : //domain .wtf/images/upload.php)
  -> Line 5: Optioal: Add a redirect url, that you get redirected to, in care someone calls the website without a image uploader.
3. Run the .sxcu file from the repo, and customize the custom uploader settings to fir your configuration of the upload.php
  -> k = secret key
  -> File from name: d
  -> Destination Type: Image uploader
  -> Method: POST
  -> Request URL: https:// yourdomain .com/upload.php
4. Upload images.

# Troubleshooting:

Some errors you may encounter:
  
Error 404:
  -> Make sure you actually call the php script, and not some other website / make sure apache / nginx is running
  
Sorry, your file could not be uploaded:
  -> Make sure you have php 7.4 installed & that the service is running (systemctl status php7.4-fpm)
  -> make sure your php script hast permissions to create files (sudo chown -R www-data:www-data /var/www)
  
 
