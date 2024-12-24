# Wirehole-Installation
Private VPN server with adblocker<br />

1. Clone the repository
Install `git` first in case you did not<br />
`sudo apt-get install -y git`<br />
`git clone https://github.com/danghh333/Wirehole-Installation.git`<br />
2. Run the installation script<br />
    `cd Wirehole-Installation`<br />
    `chmod +x install.sh`<br />
    `./install.sh`<br />
3. Configure the Wirehole server<br />
`cd wirehole-ui`<br />
   
Edit the file with your Public IP and password<br />
`nano docker-compose.yml`<br />
`WG_HOST=your_public_ip`<br />
`PASSWORD=your_password`<br />
Save and exit

4. Start the Wirehole server<br />
`docker-compose up -d`<br />

5. Access the Wirehole UI with your password<br />
`http://your_public_ip:51821`<br />

Bonus!
In case you want to utilize the DNS server for adblocking without the VPN server, you can config the AllowedIPs from your client<br />
`AllowedIPs = 0.0.0.0/0, ::/0` to `AllowedIPs = 10.2.0.0/24`<br />



