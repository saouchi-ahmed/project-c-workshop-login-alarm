Steps to Set Up the Project
Copy data.txt to your server

Upload the data.txt file to your server using an FTP client or SSH.

Upload login.php to your server

Upload the login.php file to the appropriate directory on your server (e.g., /var/www/html).

Update the index.php code for your server domain

Open the index.php file in a text editor.

Change the code to use your server domain instead of localhost. For example:

php
Copier
Modifier
$domain = "http://your-domain.com";
Upload index.php to your server

Upload the index.php file to your server’s root directory (e.g., /var/www/html).

Integrate the Arduino project with the deployed code (Controlled-RGB-Led.ino)

Open the Arduino IDE.

Load the Controlled-RGB-Led.ino file.

Select COM4 as the port (for your PC).

Upload the code to your Arduino board and ensure the RGB LED is properly connected.

Run the C code and index.php simultaneously

Run C code:

Compile and run your C program:

bash
Copier
Modifier
gcc -o myprogram myprogram.c
./myprogram
Start the PHP server:

Ensure that Apache (or another PHP web server) is running:

bash
Copier
Modifier
sudo service apache2 start
Access the login page by navigating to http://your-domain.com/index.php.

Login

Navigate to http://your-domain.com/index.php in your browser.

Use the credentials:

Username: admin

Password: 0000

If you enter incorrect credentials, the Arduino should trigger the alarm by lighting up the blue and red LEDs.
