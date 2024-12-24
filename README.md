# Wirehole-Installation
Private VPN server with adblocker
Installation
1. Clone the repository
Install `git` first in case you did not
`sudo apt-get install -y git`<br />
`git clone https://github.com/danghh333/Wirehole-Installation.git`<br />
2. Run the installation script
    `cd Wirehole-Installation`<br />
    `chmod +x install.sh`<br />
    `./install.sh`<br />
3. Configure the Wirehole server
`cd wirehole-ui`<br />
   
Edit the file with your Public IP and password
`nano docker-compose.yml`<br />
`WG_HOST=your_public_ip`<br />
`PASSWORD=your_password`<br />
Save and exit

4. Start the Wirehole server
`docker-compose up -d`<br />

5. Access the Wirehole UI with your password
`http://your_public_ip:51821`<br />

Bonus!
In case you want to utilize the DNS server for adblocking without the VPN server, you can config the AllowedIPs from your client
`AllowedIPs = 0.0.0.0/0, ::/0` to `AllowedIPs = 10.2.0.0/24`<br />



