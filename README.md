# Printing @ EPHS
Ocasionally you might wonder how to use the printers at EPHS. This is a short guide that will explain how to connect to the print server. The i-Learn MacBook Airs should already be connected and no special setup is needed. 

## Configuration
This guide will explain how to connect to the Follow_Me_EP printer in the Library, using [CUPS](https://www.cups.org/). First this guide will go over how to connect to the printer with the graphical interface present in CUPS, and then alternatively, using the terminal. 

### Printer Information
The URI of the printer is: `lpd://EPVWINRPS.ad.edenpr.org/Follow-Me`
(It uses a LPD queue)

It is located in the library.

The driver PPD file is located in this repository, and will show up as 'uniFlowPPD' in CUPS. 

[Follow_Me_EP.ppd](Follow_Me_EP.ppd)

### Configuration in CUPS
Navigate to the web interface (http://localhost:631). Click 'Add Printer' (under Printers). If the site asks for a username/password, enter in your local account Username/Password (make sure you are an administrator). 

In the connection prompt at the next screen, type/paste in the printer URI, with your STUDENTID (ex: `90301234`) before the '@,' like so:
`lpd://STUDENTID@EPVWINRPS.ad.edenpr.org/Follow-Me`

For the name/description/location, you may choose what you would like to call the printer. The standard name is `Follow_Me_EP.` You do not need to share the printer. 

The next screen will ask you to select the make/model or provide a PPD file. Download the [Follow_Me_EP.ppd](Follow_Me_EP.ppd) file from this repository, and click browse to navigate and USE the downloaded file. Click 'Add Printer.'

Your printer should now be set up. You can use CUPS to print a test page. Make sure to use your STUDENTID like normal to sign in to the printer. 

### Using the terminal
Run this command. 

`# lpadmin -p EP_Follow_Me -E -v lpd://STUDENTID@EPVWINRPS.ad.edenpr.org/Follow-Me -m path/to/EP_Follow_Me.ppd`

STUDENTID is your student id (ex: 90301234) and the [Follow_Me_EP.ppd](EP_Follow_Me.ppd)  is the one found in this repository. 



