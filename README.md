<<<<<<< HEAD
# Ubuntu Guides

Welcome to the Ubuntu Guides repository. Here, you will find a comprehensive collection of tutorials and guides designed to help you manage, configure, and troubleshoot various aspects of Ubuntu. Our goal is to provide clear, step-by-step instructions for a wide range of topics to assist both new and experienced users.

## Categories

### LightDM Guides
- [Full Auto-Login Configuration](lightdm-guides/full-auto-login.md)
  - This guide provides detailed steps to enable full auto-login for LightDM, ensuring that the system bypasses the login screen and logs in automatically to the XFCE desktop environment.

### Networking Guides
- [Sending Files Between Ubuntu Systems on the Same Network](networking-guides/sending-files-between-ubuntu-systems.md)
  - Learn how to send files between Ubuntu systems on the same network, facilitating easy and efficient file sharing.

 <!--
### Networking Guides
- [Wi-Fi Setup](networking-guides/wifi-setup.md)
  - Step-by-step instructions for setting up Wi-Fi on Ubuntu, including how to connect to networks using command-line tools.

### System Configuration Guides
- [Updating Sources List](system-configuration-guides/update-sources.md)
  - A guide to updating the sources list on Ubuntu, ensuring that your system can access the latest software repositories and updates.

### Software Installation Guides
- [Installing Visual Studio Code](software-installation-guides/install-vscode.md)
  - Instructions for installing Visual Studio Code on Ubuntu, providing a powerful code editor for developers.
-->

## Contributing

We welcome contributions from the community! If you have a tutorial to add or improvements to suggest, please see our [Contributing Guidelines](CONTRIBUTING.md) for more information on how to get involved.

## Getting Help

If you encounter any issues or need assistance, feel free to open an issue in this repository or refer to the individual guides for specific topics. You can also consult the official Ubuntu documentation for more comprehensive information.

## License

This repository is licensed under the MIT License. For more details, see the [LICENSE](LICENSE) file.

Thank you for visiting the Ubuntu Guides repository. We hope you find these tutorials helpful!
=======
# Sending Files Between Ubuntu Systems on the Same Network
In this tutorial, you will learn how to securely transfer files between Ubuntu systems that are on the same network. We will cover two commonly used methods: SCP (Secure Copy Protocol) and SFTP (SSH File Transfer Protocol).

## Prerequisites
* Two Ubuntu systems connected to the same network.
* SSH (Secure Shell) installed and configured on both systems.

## Step 1: Find the IP Address of the Destination System

Before transferring files, you need to know the IP address of the destination system. Here's how you can find it:

1. Using the `ifconfig` command:

Open a terminal on the destination system and type:

```bash
ifconfig
```

Look for the network interface connected to your local network (typically `eth0` or `wlan0`), and locate the `inet` field. The IP address listed in this field is the IP address of the system.

2. Using the hostname command:

Open a terminal on the destination system and type:

```bash
hostname -I
```
This command will display the IP addresses associated with the system.

3. Using a graphical network manager:

If you're using a desktop environment, you can often find network information, including the IP address, through the network manager GUI. Look for network settings or connection information.


## Method 1: Using SCP
SCP allows you to securely transfer files between hosts on a network. It relies on SSH for data transfer and provides the same authentication and security as SSH.

1. Open a terminal on the system from which you want to send the file.

2. Use the following command format to transfer the file:

```bash
scp /path/to/your/file username@destination_host:/path/to/destination/directory
```

### Replace:

* `/path/to/your/file` with the path to the file you want to send.
* username with the username on the destination system.
* destination_host with the IP address or hostname of the destination system.
* `/path/to/destination/directory` with the directory where you want to place the file on the destination system.

### Example:

```bash
scp /home/user/example.txt user@192.168.1.2:/home/user/
```
**You will be prompted for the password of the destination user.**


## Method 2: Using SFTP

SFTP provides a secure way to transfer files between hosts over SSH. It allows interactive file operations, similar to using FTP.

1. Open a terminal on the system from which you want to send the file.
2. Type the following command to start an SFTP session:

```bash
sftp username@destination_host
```
### Replace:
* `username` with the username on the destination system.
* `destination_host` with the IP address or hostname of the destination system.
You'll be prompted for the password of the destination user.

3. Once logged in, you can use commands like put to upload files:

```bash
put /path/to/your/file /path/to/destination/directory
```
### Replace:

* `/path/to/your/file` with the path to the file you want to send.
* `/path/to/destination/directory` with the directory where you want to place the file on the destination system.

### Example:

```bash
put /home/user/example.txt /home/user/
```
This will transfer example.txt to the home directory of the destination user.

Choose the method that best suits your needs and preferences. Both methods provide secure file transfer capabilities within the same network.
>>>>>>> source-repo/main
