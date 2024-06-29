# Network and services and protocols

## file transfer protocol (FTP)

- File Transfer Protocol (FTP) is used to copy or transfer files between hosts, usually the file server and the file client. It is a TCP-based protocol and uses two ports. TCP 20 is used for data transfer, and TCP 21 is used for connection control. It is not a secure protocol since the data is sent in clear text format. In practice, Secure File Transfer Protocol (SFTP) should always be used instead of FTP because SFTP runs over SSL and enables encrypted data transfer. It is also a TCP protocol and uses port number 22.

## Trivial file transfer protocol (TFTP)

- Trivial File Transfer Protocol (TFTP) is also used for file transfer. It is a UDP-based protocol and uses port 69. It is mostly used to transfer configuration files or software (firmware) to and from the network devices. Unlike FTP, it does not require authentication for it to work. It is also client- server based. When using TFTP on the server, port UDP 69 must be open in all firewalls between the device and the server.

## Server Message Block (SMB)

- Server Message Block (SMB) protocol is used in computer networks for file sharing. It enables different users and applications to use shared network resources and open and edit shared files.
- SMB uses TCP port 445 for communication and many request-response messages to establish a client/server connection.
- It has one huge drawback - vulnerability and presents a security risk when allowed on hosts. Ransomware is based on SMB vulnerability.
- There are three different versions of SMB: SMBv1, SMBv2 and SMBv3

## Telnet and SSH

- Telnet and Secure Shell (SSH) are TCP protocols used for remote access to network devices or hosts like Linux machines. Telnet works on TCP port 23 and is an unsecure protocol because it transfers data in cleartext. On the other hand, SSH works on port 22, which is a secure port because communication is encrypted. It is widely used for accessing network devices and linux hosts.

## SMTP and SMTP TLS

- Email protocols are used to establish a connection between the sender, recipient, and mail server. The most commonly used email protocols are SMTP, POP3, IMAP, and their secure variant.
- SMTP is a network protocol used in mail communication over the internet. it is mostly used in `mail relaying` that is sending and recieve email between mail servers.
- When the sender sends an email, the Mail Transfer Agent (MTA) will push the new message to the mail server. The mail server will then establish communication with the recipient’s mail server, which will receive, process, and deliver it to the correct mailbox.
- SMTP uses different ports for submission and relay. Submission operation occurs when an email client connects to the mail server and submits the message. Relay operation is the sending and receiving of emails between two mail servers.
- TCP port 25 - Primarily used for SMTP relay between two email servers. It can be used for submission but is unsecure and vulnerable to attacks. Hence most Internet Service Providers block this port because of the number of spam messages that are relayed from compromised computers. More secure protocols are usually used for submissions.
- TCP port 587 - It is the default port for mail submission and is used for Secure Sockets Layer (SSL )/Transport Layer Security (TLS). This means that in the handshake process between a client and the server, the client will try to upgrade to an encrypted connection. If the server is compatible, that is, supports SSL/TLS, a secured TLS connection will be established. If the server is not compatible, a connection will still be established but for a plain-text transmission.
- TCP port 465 - It is an alternative port for mail submission and is used for implicit SSL/TLS. This means that in the handshake process between a client and the server, a client will try to upgrade to an encrypted connection but will not check for server compatibility. If the server supports SSL/TLS, the connection will be established and is secure. If the server is not compatible, the connection will be dropped, and transmission will not occur.

## IMAP and POP3

- 