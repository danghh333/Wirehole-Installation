# Wirehole-Installation
Private VPN server with adblocker
Installation
1. Clone the repository
`git clone https://github.com/danghh333/Wirehole-Installation.git`
2. Run the installation script
    `cd Wirehole-Installation`
    `chmod +x install.sh`
    `./install.sh`
3. Configure the Wirehole server
`cd wirehole-ui`
   
Edit the file with your Public IP and password
`nano docker-compose.yml`
`WG_HOST=your_public_ip`
"PASSWORD=your_password"
Save and exit

4. Start the Wirehole server
`docker-compose up -d`

5. Access the Wirehole UI with your password
`http://your_public_ip:51821`

Bonus!
In case you want to utilize the DNS server for adblocking without the VPN server, you can config the AllowedIPs from your client
`AllowedIPs = 0.0.0.0/0, ::/0` to `AllowedIPs = 10.2.0.0/24`



