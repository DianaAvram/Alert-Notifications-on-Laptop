# Alert-Notifications-on-Laptop


HARDWARE NEEDED: 1 x nRF52840 Board, 1 x micro USB cable

The HW setup is the following:
[PC] ----micro USB----[nRF52840]

SOFTWARE NEEDED:
- The PC needs to have Segger Embedded Studio & nRF Connect for Desktop (available here: https://www.nordicsemi.com/Software-and-tools/Development-Tools/nRF-Connect-for-desktop/Download#infotabs)

How this example works:
- The board will indicate different alert states, which may simulate missed calls or received emails. Using the laptop and/or the board’s buttons, we are able to change the states’ values. Furthermore, we may explicitly see these states’ values using Putty.
- This example is useful, in order to understand what “writing into a characteristic” means (i.e. setting a new value to a characteristic).
- For a better understanding of Bluetooth Characteristics, please follow this tutorial: Bluetooth low energy Characteristics, a beginner's tutorial - https://devzone.nordicsemi.com/nordic/short-range-guides/b/bluetooth-low-energy/posts/ble-characteristics-a-beginners-tutorial  

Steps, to run the notifications example on the board and the laptop:
- In principle, the steps presented here should be followed: Alert Notification Application -
https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v15.0.0%2Fble_sdk_app_alert_notification.html

- The main project will be found below this folder: your install folder for the latest nRF5_SDK and then:
\examples\ble_peripheral\ble_app_alert_notification. After this, depending on the nRF52840’s specs, one of the PCA folders needs to be chosen.
- The pca number is written on the board.
- Navigate to the specific folder, until the EMPROJECT file and open it. It should open with Segger.
- For examnple, if the board has PCA10056, then the project file will be located in:
\nRF5_SDK\examples\ble_peripheral\ble_app_alert_notification\pca10056\s140\ses
- After the project is open, we need to build and load the program on the nRF board like this:

1. Build the project: Top Menu → Build → Build … (name of project)
2. Connect to the board via the usb: Top Menu → Target → Connect J-Link.
3. Next, from the same menu, we “Erase All”, so that the memory of the board is not overloaded.
4. Following, from the same menu, we “Download … (name of project)”
5. Finally, the steps of checking the functionality of the code should be followed, according to the official tutorial: Alert Notification Application -
https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v15.0.0%2Fble_sdk_app_alert_notification.html  
