# Starting to monitor Wifi network

### Introduction

In this example, we will use the [aircrack-ng] tools suite and the OS is the Ubuntu.

### Installation

Install the aircrack-ng.

```sh
sudo apt-get –y install aircrack-ng
```

### Steps

* **Enable monitor mode on wireless interface**  
  * Enter `iwconfig` to show you the current status of the wireless interfaces.  
  * Do  `sudo airmon-ng start "interface"` to start "interface" in monitor mode  
  * Enter `iwconfig` again to see that an interface is in monitor mode.  
* **Determine if you card successfully supports injection**  
  * Enter `aireplay-ng -9 "interface in monitor mode"`  
  * If you have **"Injection is working!"** in response, then it is confirmed that your card can inject  
  * The **"Found x APs"** answer indicates that these access points (APs) were found either through the broadcast probes or received beacons.  
* To stop the "interface" in monitor mode, enter `sudo airmon-ng stop "interface"`  

### Final considerations

To build your basic skills and get you familiar with the concepts, I suggest you follow the [Simple WEP Crack].

[//]: # (References)

   [aircrack-ng]: <https://aircrack-ng.org/>
   [Simple WEP Crack]: <https://aircrack-ng.org/doku.php?id=simple_wep_crack>
