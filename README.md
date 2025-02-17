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

The foundation of this home lab begins with a fresh installation of Raspberry Pi OS (formerly Raspbian) on a high-speed SD card.  This involves downloading the latest Raspberry Pi OS image from the official Raspberry Pi website and flashing it onto the SD card using a tool like the Raspberry Pi Imager.  Once the image is written, the SD card is inserted into the Raspberry Pi 5, and the device is powered on.  The initial boot process involves configuring basic settings such as the hostname, setting up a user account, enabling SSH for remote access (essential for headless operation), and connecting to the local network.  Expanding the file system to utilize the entire SD card capacity is also a crucial first step.  From this point, the Pi is ready for further configuration, including installing necessary software packages and preparing for the Portainer installation, which will form the basis of our application deploymen

### **Features**




