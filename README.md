# PICO-W--Micropython-examples-
For the PICO W (RP2040 with WIFI) - A collection of Micropython programs you can use for the following modules:
 - OLED (size 1.3 - that uses the SH1106 driver instead of the SSD1306 driver).
 - BNO0055 module
 - GPS Module

N.B. Be aware that three devices need to be connected to the PICO W. This means 3 pairs of connections to the 3.3V/Gnd power are required, but, there is only one 3.3V pin on the PICO. Rather than using a breadboard, consider creating a split power harness i.e. 1 pair in, 3 pairs out.

N.B. I did not need to add pull up resistors to the SDA and SCL line, consider that your luck may vary

<img src="/images/picow_pinout.png" alt="PICO W Pinout"/>


# Step 1 - Attach OLED and execute "oled_sh1106.py"  
This tests the 1.3 OLED Display that uses a SH1106 driver instead of SSD1306 driver

Attach 1.3 OLED module as follows
 - 3.3V power   -> pin 37 (3v3_en)
 - Grnd         -> pin 38 (Gnd) 
 - SDA          -> pin  1 (GP0)
 - SCL          -> pin  2 (GP1)

# Step 2 - Attach GPS module and execute "gpsDisplay.py" 
This tests both the GPS Module and the OLED

Attach GPS Module as follows
 - 3.3V power   -> pin 37 (3v3_en)
 - Grnd         -> pin 38 (Gnd) 
 - RX           -> pin 11 (GP8)
 - TX           -> pin 12 (GP9)

# Step 3 - Attach BNO0055 and execute "bno055_test.py" 
This tests the BNO055 module and outputs to serial
 - 3.3V power   -> pin 37 (3v3_en)
 - Grnd         -> pin 38 (Gnd) 
 - SDA          -> pin 19 (GP14)
 - SCL          -> pin 20 (GP15)
