<h1>Operation Ocean View</h1>

<h2>Description</h2>
Project Consists the use of network and service analysis to find a programmable Logic controller (PLC) that is actively being attack by an adversary. Through service monitoring, network analysis and firewall management, identify and report the adversary to the intelligence community, implement firewall rule to stop the adversary's access to the PLC and monitor the service-post firewall configuration to ensure the services are running.


<br />


<h2>Languages and Utilities Used</h2>

- <b>Kali</b> 
- <b>nmap</b>
- <b>Firewall</b>
- <b>Wireshark</b>

<h2>Environments Used </h2>

- <b>Project Ares</b> (Cyber Range)

<h2>Program walk-through:</h2>

<p align="center">
Recon to find IP address and open ports of the target network: <br/>
<img src="https://images.squarespace-cdn.com/content/v1/53044d0ae4b0279380896fbb/1639139408443-S6EZZV3Q82CZ2AB7JNG9/oceanview.pptm-3.png?format=500w"/>
<br />
<br />
Use of wireshark to identify beaconing packets, connecting ip address and destination ports:  <br/>
<img src="https://images.squarespace-cdn.com/content/v1/53044d0ae4b0279380896fbb/1639139411417-30TW3RFCP1WEN6KG4T7C/oceanview.pptm-5.png?format=500w"/>
<br />
<br />
Run mslconsole as root  and start the multi handler. use reverse_tcp meterpreter payload to connect to the incoming beacon: <br/>
<img src="https://images.squarespace-cdn.com/content/v1/53044d0ae4b0279380896fbb/1639139415583-8RR7QT4RR8ZYATS1DMVH/oceanview.pptm-7.png?format=500w"/>
<br />
<br />
Download information to kali to extract information to sabotage the water treatment system:  <br/>
<img src="https://images.squarespace-cdn.com/content/v1/53044d0ae4b0279380896fbb/1639139415416-JIZITKAIWTDQ720ZGS32/oceanview.pptm-8.png?format=500w"/>
<br />
<br />
Identify the PLC system that is communicating to the HNI controller. Conduct  a port scan on the IP address:  <br/>
<img src="https://images.squarespace-cdn.com/content/v1/53044d0ae4b0279380896fbb/1639151452190-8GIGTGRDLCRBPR8U3ZD6/oceanview.pptm-9.png?format=500w"/>
<br />
<br />
Initiate a connection to the open modbus port on the PLC system inside the network:  <br/>
<img src="https://images.squarespace-cdn.com/content/v1/53044d0ae4b0279380896fbb/1639151476196-1S4AH3TBGLHSUSFJNORE/oceanview.pptm-10.png?format=500w"/>
<br />
<br />
