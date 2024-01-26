# GK-NVIDIA-Jetson-Neno
Learning


UART Connection with Jetson Nano 

I followed this link to connect to UART. 

https://jetsonhacks.com/2019/10/10/jetson-nano-uart/

but it did not work. 


Later, I found this post.

https://forums.developer.nvidia.com/t/trying-to-use-uart2-but-dev-ttyths1-doesnt-exist/262036/8

Then I tried the loopback test in Jetson Nano Orin.

$ sudo su
# stty -F /dev/ttyTHS0 115200 raw -echo
# cat /dev/ttyTHS0 &
# echo "test" > /dev/ttyTHS0

on the Windows PC, I open Putty and select Serial, COM5 (need to see in which com in Device Manager or Geräte Manager), 115200 Bradrate

Then it works, but not expected. 

Later, I ran sudo python3 uart_example.py, and it worked.  

in the uart_example.py have changed the board name to 'NVIDIA Jetson Nano Orin Developer Kit,' and now the script is also working. 

But it should connect from the beginning so that, using UART, I can also log into Jetson. 





