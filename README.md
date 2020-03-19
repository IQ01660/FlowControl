# FlowControl
Flow Control between the Data Link Layers of two hosts

## Stop and Wait Protocol
First, we want to implement the stop and wait protocol
for the flow control between two hosts and their Data Link Layers

The way this works is one host sends frames to the other host
and waits for acknowledgement frame from tthe receiver.
If the sender doesn't get an acknowledgement after some time,
it resends the frame.

As stated on the wikipedia page [Stop-n-Wait Protocol](https://en.wikipedia.org/wiki/Stop-and-wait_ARQ):

>Stop-and-wait ARQ, also referred to as alternating bit protocol, is a method in telecommunications to send information between two connected devices. It ensures that information is not lost due to dropped packets and that packets are received in the correct order. It is the simplest automatic repeat-request (ARQ) mechanism. A stop-and-wait ARQ sender sends one frame at a time; it is a special case of the general sliding window protocol with transmit and receive window sizes equal to one in both cases. After sending each frame, the sender doesn't send any further frames until it receives an acknowledgement (ACK) signal. After receiving a valid frame, the receiver sends an ACK. If the ACK does not reach the sender before a certain time, known as the timeout, the sender sends the same frame again. The timeout countdown is reset after each frame transmission.