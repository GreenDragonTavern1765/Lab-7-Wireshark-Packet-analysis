# **Assignment 7 Wireshark and TCP**
**Description:** In this assignment, you'll examine pre-captured packets with Wireshark. The purpose of the assignment is to see real protocols in action. 
## Installing Wireshark 
Wireshark is already installed on the Linux partitions on the lab computers. You'd need to have administrative privileges in order to capture packets, but this isn't necessary for this assignment. If you'd prefer, you may work on this assignment at home. Wireshark and instructions for installing it on your operating system of choice may be found on the Wireshark website. To answer the questions, download the following pcap file and open it in Wireshark.
## Questions
**1. In which packet can you find an HTTP GET?** Packet 7, 39, 56, 57, 60, 95, 97, 98

**2. What web page was visited?** http://spongebob.wikia.com/wiki/Greasy_Buffoons

**3. What browser was used?** Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/535.1 (KHTML, like Gecko) Chrome/13.0.782.220 Safari/535.1

**4. What version of HTTP was used?** HTTP/1.1

**5. Was persistent or non-persistent HTTP used? How can you tell?** Connection: Keep-alive, so persistent.

**6. In the client's request, what other information about the browser and client OS were sent to the web server?** Mozilla/5.0 on Windows NT 6.1

**7. In the HTTP server's response, what information was sent about the server, e.g., what server software was used?** Server: Apache

**8. If we look at the content of the HTTP data, (click on one of the early segments in a TCP session on then go Tools, then Follow TCP Stream), why is it that we can't read the content of the files? (Hint: what does the server header Content-encoding: gzip mean?)** GZip compresses the content, so it isn't able to be read. GZIP is not compatible with modern browsers.

**9. In which packets do you see a TCP three-way handshake?** Packets 2, 3, 4

**10. What does Wireshark say the client's initial sequence number is? In my version of Wireshark, it says relative sequence number. What does this mean?** Sequence Number: 0 (Relative Sequence Number) Sequence Number (raw): 563351264, This means that all SEQ and ACK numbers always start at 0 for the first packet seen in each conversation.

**11. What is ACK number sent by the server during the second leg of the three-way handshake?** Acknowledgment number: 1 (relative ack number) Acknowledgment number (raw): 563351265

**12. What sequence number is sent by the server during the second leg of the three-way handshake?** Sequence number: 0 (relative sequence number), Sequence number (raw): 801751991

**13. What is the ACK number sent by the client during the third leg of the three-way handshake?** Acknowledgment number: 1 (relative ack number) Acknowledgment number (raw): 801751992

**14. In the first leg of the three-way handshake, how large is the TCP header? Is this larger than TCP's minimum header?** 1000 .... = Header Length: 32 bytes (8)

15. Is any data sent during the third leg of the three-way handshake? If so, what is it? 

16. During the three-way handshake, what is the client's TCP advertised receive window? How does this value relate to the maximum possible? 

**17. What are the source and destination ports of the segments traveling from the client to the server?** 

18. What are the source and destination IP addresses of the datagrams traveling from the client to the server? 

19. What are the source and destination ports of the segments traveling from the server to the client? 

20. What are the source and destination IP addresses of the datagrams traveling from the server to the client? 

21. In which segments do you find a TCP connection close? How can you tell? 

22. In the packet containing the first leg of the three-way handshake, what is the value of the protocol (i.e., upper-layer-protocol) field in the IP header? 

23. In this same packet's IP header, what is the value of the Identification field? What is the purpose of the Identification field? In what case would we expect to find the same Identification value in other packets?  


