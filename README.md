# Big File Sharing - Server Less
This is a python based project for windows / Linux / mac.

**Goal**

To make a chat+file sharing application which bypasses NAT without the need of a server or configuring the router for port forwarding.

**Idea**

The principle is simple. To fool the NAT, the application keeps sending out a dummy packet from the specific port whose destination is the other user public IP. Given the application knows which port it will be using, and at least one user knows the public IP of the other user (Who is sending the giant file), It is possible to make a TCP connection between them without the need of a server. And thereby sending files directly from one user to another. 

**To do**
<ol>
<li>
  Wrapper for the application using tkinter.
 
  </li>
<li>
  Encrypting the chat using cryptography. based on the pre shared keys.
  </li>
  
<li>
  Sending out the dummy packet. And securing against attacks.
</li>
  
</ol>
**Usage**
The server_messager.py needs to be set on an server which has router permissions (port forwarding). The client_messager can be used behind a nat with the public IP of the server and the port. 
Once connected:
You can use 'file' to send any file from the client to server/server to client. use ctrl+c to disconnect. Currently only supports one file :(
