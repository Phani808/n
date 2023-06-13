Script Installation
Clone the repository or download the script file.
Make sure you have root access or run the script with root privileges.
Ensure that the necessary dependencies are met (Docker and Docker Compose).
Usage
bash
Copy code
./script.sh <site_name> <port> [enable|disable|delete]
Replace <site_name> with the desired name for your WordPress site and <port> with the port number you want to use.

The script supports the following optional commands:

enable: Enable the site (if not already enabled).
disable: Disable the site (if enabled).
delete: Delete the site, including the associated Docker containers and volumes.
Example Usage
To create a new WordPress site and enable it:

bash
Copy code
./script.sh mysite 8080 enable
To disable an existing WordPress site:

bash
Copy code
./script.sh mysite 8080 disable
To delete an existing WordPress site:

bash
Copy code
./script.sh mysite 8080 delete
Important Notes
The script assumes that Docker and Docker Compose are already installed. If not, it attempts to install them.
The script creates a Docker Compose file (docker-compose.yml) in the specified site directory.
The site directory will be located at /var/www/html/<site_name>.
The script uses a MariaDB container for the database and a WordPress container for the web server.
The MariaDB container uses the following credentials:
Root Password: somewordpress
Database Name: wordpress
Database User: wordpress
Database Password: wordpress
The WordPress site will be accessible at http://<site_name> and http://<public_ip>:<port>.
An entry will be added to /etc/hosts for easy access to the site.
Make sure to customize the README.md file according to your specific requirements and provide any additional information or instructions that may be relevant.
