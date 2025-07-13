---
layout: page
title:  "Configuring Cyberghost VPN on Fedora 42 using OpenVPN and Network Manager"
date:   2025-07-13 15:40:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /configure-cyberghost-openvpn-fedora42

---

Wow. Using OpenVPN files generated through CyberghostVPN website GUI was a ride. After spinning around in the Fedora discussion forum, I finally encountered a workaround to actually use Network Manager GUI to do it. It's [here](https://discussion.fedoraproject.org/t/openvpn-bug-f41/137248) but somehow, from Fedora 41 to 42, the process only necessitates the first 2 options. I'm saving it here in case I may need the last command later if any break of the current solution.
{: style="text-align: justify;"}
<br/>
<br/>
**<u>So here is what I've done : </u>**
<br/>
<br/>
- Go to CyberGhostVPN website, into "Download Hub" to "Other apps" (bottom of the page) and select **"Routers and other devices".**
{: style="text-align: justify;"}
<br/>
- Choose **"OpenVPN" as protocol**, then your country, server, name your device and save the configuration. It'll generate you a username, a password, and a button to download your configuration files. For later, this will be saved in the "Manage Devices" section of the Download Hub if you need it again.
<br/>
![router-manage](/assets/images/router-manage.png)
{: style="text-align: justify;"}
<br/>
- Go to your created Router and **download the configuration files.** It'll be in a .zip file. Keep the tab opened, it enables you to copy/paste the ID and password that will be asked by Network Manager. Remember now that no matter what you do or how many countries you'll be installing, it will be here to grasp the ID/Password, DO NOT use the credentials you use to log into Cyberghost through web or apps. **In that setup, you need the OpenVPN credentials only, so the ones generated along with the config files.**
<br/>
![router-config](/assets/images/router-config.png)
{: style="text-align: justify;"}
<br/>
- Extract your .zip file.
{: style="text-align: justify;"}
<br/>
- Open the terminal, type `cd` (without any argument after) then `ls -lah` to go to the root of your home directory and reveal all the files in it, **including the hidden files**.
{: style="text-align: justify;"}
<br/>
- Check if you have **a `.cert` folder/directory.** Create one with `mkdir .cert` or through the GUI in File Manager if it isn't here yet.
{: style="text-align: justify;"}
<br/>
- Once you're sure to have it, go back to the folder with the configuration files in Downloads, check that there's everything : **`ca.crt`, `client.crt`, `client.key` and the `.ovpn` configuration file** that you can rename (keep the .ovpn filename extension, name it with the country you created it for, for example). **Copy ALL those files to `~/.cert`.**
{: style="text-align: justify;"}
<br/>
- Open the **Network Manager GUI** through the Settings of your device, press the `+` button on the VPN section, then `Import from a file` in the bottom and select your `.ovpn` file that is in the `.cert` directory :
<br/>
![netmanager-options](/assets/images/netmanager-options.png)
{: style="text-align: justify;"}
<br/>
- In "Identity", you can rename your network. In "Authenticate" section, select **"Password with certificates (TLS)". In "Username" and "Password", input the credentials that the web GUI gave to you earlier in "Manage Devices".**
{: style="text-align: justify;"}
<br/>
- Normally, the GUI selected the good `ca.crt`, `client.crt` and `client.key` files. **DOUBLE CHECK if that's really the case, that it takes them from the `.cert` directory.**
{: style="text-align: justify;"}
<br/>
- Before saving, go to the "IPV6" tab and **deactivate IPV6.**
{: style="text-align: justify;"}
<br/>
- **Click on "Add" to save everything.** Normally you don't have any more settings to input.
{: style="text-align: justify;"}
<br/>
- If you want to **add more countries** : create new routers in the Web GUI, extract the zip, **take only the `.ovpn` file**, name it accordingly and copy it into the `.cert` directory. Then go to Network Manager to set everything up. You can select the same ca, client and key from earlier, it causes no issues.
{: style="text-align: justify;"}
<br/>
So basically, once all is copied into the `.cert` directory, all the steps are quite similar to the ["Set Up OpenVPN on Linux Mint via Network Manager" tutorial on Cyberghosts'website](https://support.cyberghostvpn.com/hc/en-us/articles/213651505-Set-Up-OpenVPN-on-Linux-Mint-via-Network-Manager) but finding this single difference took me a while. I'm glad I know about it now. I indicated it to Cyberghost in hope they'd update their Fedora tutorial, because this extra step isn't present on Mint but necessary in Fedora, for some reason. At least I don't have to change of VPN provider, it's a relief !
{: style="text-align: justify;"}
