# How to Print

## Slicer

We use [Lulzbot Cura](https://www.lulzbot.com/cura) at RCL due to its emphasis on stability and robustness. There is a computer setup near the 3D printers that is preconfigured with all the software you need to print on our printers.

## Print Server

Each 3D Printer at RCL has a raspberry pi running [Octoprint ](https://octoprint.org/)on it. The URL for accessing the Octoprint server is located on that printers' wiki page. The login info will be physically located near the printer itself.

## How to Print

1. load an .STL file onto the printer computer
2. Open up Lulzbot Cura
3. Ensure you have the correct printer selected at the top
4. Configure your job and slice the model
5. Open up the Octoprint URL in your web browser and login to Octoprint
6. click "Upload GCode" and select your gcode file.
7. click "Print"
8. **IMPORTANT!** Be sure to watch the printer closely when it starts.
   1. Make sure it homes and auto levels without issue
   2. Make sure the first few layers are put down without issue
   3. **If there is any issue whatsoever, immediately turn the printer off.**
9. Once the first few layers are completed without issue, feel free to leave the printer and watch it remotely via the Octoprint URL.
   1. If you see any issues mid-print, please stop the print remotely via the Octoprint UI.

