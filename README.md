<div align="center">
  <h3>
    <b>
      RPI5
    </b>
  </h3>
  <b>
    Homelab setup and configuration using the latest Paspberry 5.
  </b>
  <p>

![Static Badge](https://img.shields.io/badge/IoT-Raspberry_Pi_5-%23C51A4A?style=flat)
  </p>
  <br />
</div>

_All file and scripts can be found in the main branch  [**RPI5 HomeLab**](https://github.com/studio6six/rpi5) to learn more about the app._

I've been a Raspberry Pi enthusiast for years, using them for everything from offline media players to secondary coding machines.  This experience has led me to my most ambitious Pi project yet: building a home lab using the Raspberry Pi 5.  This blog will detail the setup and implementation of this lab, focusing on how I'll use Portainer to orchestrate and manage key applications such as MySQL, Postgres, and Grafana for monitoring.  The ultimate aim is to replace my existing server infrastructure with this efficient and compact Pi-based solution."


I intend to use this as guide 

## Features
- **Raspberry Pi 5 as the core**: Leveraging the increased processing power and capabilities of the Pi 5.
- **Portainer for container orchestration**: Simplifying application management and deployment.
- **MySQL database**: Providing a relational database for various applications.
- **Postgres database**: Offering another robust relational database option.
- **Grafana for monitoring**: Visualizing system performance, application metrics, and other data.
- **Home lab functionality**: Replacing your existing server setup with the Pi-based solution.
- **Compact and efficient design**: Taking advantage of the Pi's small footprint and low power consumption.
- **Documented build process**: Sharing your journey, challenges, and solutions through your blog.
- **Potential for expansion**: The Pi and containerization allow for easy addition of future services. (This is implied but good to call out)
- **Cost-effectiveness**: Building a powerful home lab at a potentially lower cost than traditional server hardware. (Also implied, but worth mentioning)

## Raspberry Pi 5

The foundation of this home lab begins with the Official MicroSD Card With Raspberry Pi OS 64-bit - 32GB. The initial boot process involves configuring basic settings such as the hostname, setting up a user account, enabling SSH for remote access (essential for headless operation), and connecting to the local network.  Expanding the file system to utilize the entire SD card capacity is also a crucial first step.  From this point, the Pi is ready for further configuration, including installing necessary software packages and preparing for the Portainer installation, which will form the basis of our application deployment

### Initial Setup
 Setting Up Your Raspberry Pi 5 Home Lab

This document outlines the initial setup and configuration of your Raspberry Pi 5 for use as a home lab, focusing on preparing the system for Portainer and application deployment.

## Initial Setup Steps

**Step 1: Boot the Pi and Complete Initial Configuration**

Insert the prepared SD card (with Raspberry Pi OS installed) into the Raspberry Pi 5 and power it on.

*   **Monitor, Keyboard & mouse:** Using a monitor and peripherals, complete the initial setup wizard. This will typically involve setting your region, language, keyboard layout, and creating a user account.

**Step 2: Configure the Hostname**

A descriptive hostname makes it easier to identify your Pi on the network.  You can change the hostname using `raspi-config`:

```bash
sudo raspi-config
```
Navigate to "System Options" -> "Hostname" and follow the prompts. 

Alternatively, you can edit the /etc/hostname and /etc/hosts files directly, but raspi-config is generally recommended.

We will rename the hostname from raspberrypi to  **pilab**

**Step 3: Configure SSH (Essential for Headless Configuration)**

SSH allows you to access and manage your Pi remotely. It's crucial for headless operation. Enable SSH using raspi-config:

```Bash
sudo raspi-config
```
Go to "Interface Options" -> "SSH" and enable it.

**Step 4: Assign the Pi a Static IP Address on the Home Network**

A static IP address ensures that your Pi always has the same IP, making it easier to connect to. This is usually done through your router's configuration interface.

Router Configuration (Recommended): Find the Pi's current IP address (check your router), then reserve or assign that IP to the Pi's MAC address in your router's DHCP settings. This process varies depending on your router model, so consult its documentation.
Static IP on Pi (Alternative): You can configure a static IP directly on the Pi, but managing it through the router is generally preferred.

**Step 5: Connect via SSH and Begin Configuration**

Once the static IP is set (and your Pi has rebooted to use it), you can connect to your Pi using SSH from another computer on your network. Open a terminal or SSH client and use the following command (replace pi with your username and 192.168.1.100 with your Pi's static IP):


```Bash
ssh pi@10.0.0.25
```
You'll be prompted for your password. After successfully logging in, you can begin the configuration and installation of dependent items for running Portainer, as well as any other software you intend to use.  This includes installing Docker, which is a prerequisite for Portainer.  Further instructions on installing and configuring Portainer will follow in subsequent sections.



