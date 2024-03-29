---
layout: leftnav-page-content
title: Set up your Hardware
permalink: /starter-kit/set-up-your-hardware/
second_nav_title: Starter Kit
collection_name: core-products
---

## 1. Wiring up the MANUCA DK

1. Connect the **ESP32 WiFi Module** onto the **WIRELESS MODULE** port on the board as shown below:

![step 1](/images/manuca/hardware-setup/manuca_setup_1_wifi.jpg)

2. Connect the **TTL-USB Cable** to the **SERIAL DEBUG** port, with black wire aligned to the GND pin as shown below:

![step 2](/images/manuca/hardware-setup/manuca_setup_2_ttl.jpg)

3. Connect the **ST-LINK programmer** cable to the **JTAG** pins, with red wire at the top and the cable connected towards the left side of the board as shown below:

![step 3](/images/manuca/hardware-setup/manuca_setup_3_jtag.jpg)

4. Your board set up should look like this:

![step 4](/images/manuca/hardware-setup/manuca_setup_4.jpg)

5. Connect the USB side of the **TTL-USB Cable** and **ST-LINK programmer** to your computer. The board should light up.

<a id="SerialDebug"></a>

## 2. Setting up your MANUCA DK Serial Debug Program

Proceed with the following steps, depending on which OS your computer is running on.

<details>
  
  <summary>Linux</summary>
  
  1. Find out which serial port your **TTL-USB Cable** is connected to by disconnecting your **TTL-USB Cable**, then entering in Terminal:
      ~~~bash
      dmesg | grep tty
      ~~~
      Reconnect your TTL-USB Cable and reenter the `dmesg | grep tty` command.

      You should see something like this:
      ~~~bash
      ~$ dmesg | grep tty
      [12213.614731] usb 1-3: FTDI USB Serial Device converter now attached to ttyUSB0
      ~~~
      Take note of the name of the Serial Device – in the above example, it is ttyUSB0.

2. Run minicom by entering in Terminal:

   ```bash
   sudo minicom -s
   ```

   You should see this configuration window:
   ![linux-minicom-setup](/images/manuca/hardware-setup/linux_debug_setup_1.jpg)
   Use arrow keys/enter to navigate the menu.

3. Go to **Serial port setup**.
   ![linux-minicom-setup](/images/manuca/hardware-setup/linux_debug_setup_2.jpg)
   There are three things you need to do:

   - Change Serial Device to the name of the port that the TTL-USB Cable is connected to. You can change your Serial Device by entering **A**, then editing the name, and press **enter**.

   - Change the Baud Rate to 115200 by entering **E**, then entering **E** again, and press **enter**.

   - Switch off Hardware Flow Control by entering **F**, and press **enter**.

   Leave the Serial port setup by pressing **enter**.

4. Go to **Save setup as dfl** and **enter**. This will save your configuration as default.

5. Go to **Exit** and **enter**. This will bring you to the minicom application in Terminal.
   ![linux-minicom-setup](/images/manuca/hardware-setup/linux_debug_setup_3.png)
   You should see `Welcome to minicom` and the Port should reflect the name of your TTL-to-USB cable port.

   Now your Serial Debugging tool for Linux has been set up successfully.

   You can run minicom again by typing in Terminal:

   ```bash
   sudo minicom
   ```

</details>

<br>
<details>
  
  <summary>MacOS</summary>
  
  1. Find out which serial port your **TTL-USB Cable** is connected to by disconnecting your **TTL-USB Cable**, then entering in Terminal:
      ~~~bash
      ls /dev/tty*
      ~~~ 
      Reconnect your TTL-USB Cable and reenter the `ls /dev/tty*` command. You should see an extra port displayed, `/dev/tty.usbserial-FT9J98X2`

2. Configure minicom by entering in Terminal:

   ```bash
   sudo minicom -s
   ```

   You should see this configuration window:
   ![macos-minicom-setup](/images/manuca/hardware-setup/macos_debug_setup_1.png)
   Use arrow keys/enter to navigate the menu.

3. Go to **Serial port setup**.
   ![macos-minicom-setup](/images/manuca/hardware-setup/macos_debug_setup_2.png)
   There are three things you need to do:

   - Change Serial Device to the name of the port that the TTL-USB Cable is connected to. You can change your Serial Device by entering **A**, then editing the name, and press **enter**.

   - Change the Baud Rate to 115200 by entering **E**, then entering **E** again, and press **enter**.

   - Switch off Hardware Flow Control by entering **F**, and press **enter**.

   Leave the Serial port setup by pressing **enter**.

4. Go to **Save setup as dfl** and **enter**. This will save your configuration as default.

5. Go to **Exit** and **enter**. This will bring you to the minicom application in Terminal.
   ![macos-minicom-setup](/images/manuca/hardware-setup/macos_debug_setup_3.png)
   You should see a message similar to the above image and the Port should reflect the name of your TTL-to-USB cable port.

   Now your Serial Debugging tool for Linux has been set up successfully.

   You can run minicom again by typing in Terminal:

   ```bash
   sudo minicom
   ```

</details>

<br>
<details>
  
  <summary>Windows</summary>
  
  1. Download [Tera Term](https://osdn.net/projects/ttssh2/releases/) for Windows.

2. Run the Tera Term `.exe` file and install the software.

3. A "New connection" window will pop up. Select the **Serial** option if available. If not, click cancel.
   ![windows-teraterm-setup](/images/manuca/hardware-setup/windows_debug_setup_1.PNG)

4. Go to **Setup > Serial port...**
   You should see something like this:
   ![windows-teraterm-setup](/images/manuca/hardware-setup/windows_debug_setup_2.PNG)

   To find out what port your TTL-USB Cable is connected to:

   - Disconnect the cable and close this window.
   - Reopen the window and click on the **Port** dropdown list. Note the ports displayed.
   - Reconnect your cable, and reopen the Serial port setup window. The newly connected TTL-USB Cable will show up on the dropdown list.
     Change **Port** to your TTL-USB Cable port, and the **Baud rate** to **115200**. Click OK.

</details>
