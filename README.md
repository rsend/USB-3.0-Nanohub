# USB-3.0-Nanohub
Fixed version of Muxtronic's USB 3.0 Nanohub

[Muxtronics.nl](https://muxtronics.nl) made some excellent miniature USB hubs for embedded systems and hackers. They used to be for sale on Tindie, but have been out of stock for a long time (based on the reviews, the last time anyone reviewed them was in 2019).

-https://www.tindie.com/products/mux/usb-30-nanohub/

-https://www.tindie.com/products/mux/nanohub-tiny-usb-hub-for-hacking-projects/

I'm specifically interested in the USB 3.0 hub, for which Mux has an initial page here: https://muxtronics.nl/nanohub-usb3.html

There is also a Hackaday page for the project (https://hackaday.io/project/20790-nanohub-tiny-usb-20-and-30-hubs) which has not been updated since 2017. 

However, it DOES include downloadable files for both the USB 2.0 and USB 3.0 hub! 

The update posts mentions a 2nd version of the USB 3.0 hub that looks a bit different based on the pictures and has some improvements, but sadly it is neither available for purchase nor do the aforementioned files include that version.

I tried making the version of the files that IS available, which look like this:

![image](https://user-images.githubusercontent.com/2659987/178582313-c1c4244f-b2cd-45c7-b611-dc404fa062bb.png)

...but turns out this version has some errors. In particular, it appears RX and TX lines for USB 3.0 are switched, so no devices are ever detected and an error is reported when it is plugged in. The chip also generates a fair amount of heat.

Based on the Hackaday blog post, Mux did make an update from a TI TUSB8020 to a Microchip USB5742 and made the board a bit smaller - but like I said, it was / is not available and sources were not posted.

So, I decided to modify the initial files to fix the issues, and make it as small as I could. Because no schematic was provided I tweaked the layout directly.

My version looks like this:

![image](https://user-images.githubusercontent.com/2659987/178583483-e2c9e9d0-b11b-4ae6-a138-689d00f1c7e9.png)

It works correctly, and I also got it made using thicker copper and a fatter PCB to improve the heat problem.

I'll try to add a proper BOM later so other people can get them made more easily if they want.

