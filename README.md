1- Pair bluetooth and serial port (Shimmer password: 1234)

2- hcitool scan //It shows the macaddress of device. for shimmer it is 00:06:66:F0:95:95

3- vim /etc/bluetooth/rfcomm.conf 
     write the below line in it:
          rfcomm0{ bind no; device 00:06:66:F0:95:95; channel 1; comment "serial port" }
4- sudo rfcomm connect rfcomm0 00:06:66:F0:95:95 // This is for reading bluetooth data from a serial port

5- Run python3 shimmer_Bt.py

