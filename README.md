# File Transfer
===========================
    By: Jerry Jia
===========================
Demonstrates the different advanced I/O implementation models with TCP and UDP socket programming on Windows.

Server Implementation:
  - Threads: 7
  - TCP : I/O completion routine
  - UDP : Asyncrounous I/O 

Client Implementation:
  - Threads: 3
  - TCP : Async Select
  - UDP : Asynchrounous I/O

To prevent stack overflow errors when recieving UDP datagrams, the application implements a circular buffer that controls the data processing on a seperate thread. Through stress testing, the application is able to send size of 60k datagrams 10000 times without losing a single datagram (Under a fairly stable network).

The application also mimics some of the functionalities provided by WireShark to calculates and display a statistics report on every transmission.
[Append '?ts=4' to the URL to change the tab size to 4 on the file that you are currently viewing]
