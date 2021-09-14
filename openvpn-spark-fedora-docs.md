# OPENVPN AND SPARK IN FEDORA LINUX DISTRO DOCS

## OpenVPN Client to RPM based Linux Distro

### Installing Openvpn3 (INSTALL VIA TERMINAL)
If installing Openvpn to Redhat and its clone, firstly install fedora epel packages visit this link: [Fedora Epel Repo](https://docs.fedoraproject.org/en-US/epel/). Since im using Fedora Distro I am good to do the first step:
- First step

  `sudo dnf install yum-plugin-copr`
- Second step

  `sudo dnf copr enable dsommers/openvpn3`
- Third step

  `sudo dnf install openvpn3`

#### Navigating Openvpn3 (CONNECT VIA TERMINAL)
- First step: Import the config file. The file should have an .ovpn file extension, and make sure you are in the same directory of the file.

  `openvpn3 config-import --config file_name.ovpn`
- Second step: Look for the name of the imported file in the config list and copy the name.

  `openvpn3 configs-list`
- Third step: Start a session.

  `openvpn3 session-start --config copied_name`
- Fourth step: Login your credetials the username and password and you're done. (Credentials are given by the DOST thru email)
- Optional step: Look for open sessions

  `openvpn3 sessions-list`

## Spark 2.9.4 Messaging software to RPM based Linux Distro.

### Installing Spark 2.9.4 (INSTALL VIA TERMINAL)
- First Step: Download the spark binary build at [Spark Download](https://igniterealtime.org/downloads/) and choose linux distro then download the **spark_2_9_4.tar.gz**
- Second Step: Extract the **spark_2_9_4.tar.gz**

  `tar -zxvf spark_2_9_4.tar.gz`
- Third Step: Move the Spark directory to the /opt/ folder and the setup is done.

  `sudo mv -r Spark /opt/`

### Running Spark 2.9.4 (EXECUTE VIA TERMINAL)
- First step: You need to run the spark application using the command line.

  `/opt/Spark/Spark`
- Optional: if you want to make your life easier create a .desktop config file for the spark in order to see it on the desktop. You may check this [link](https://www.2daygeek.com/install-spark-im-client-on-ubuntu-centos-debian-fedora-mint-rhel-opensuse/) for reference 
