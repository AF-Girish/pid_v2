# Instructions for Running Peak Works on Raspberry Pi 4

 Make sure you read all the following 16 steps before you start run.

## Before you start
### Components Table
Core of analysis done by Peak works on Rpi   is based on  Components Table. You can see this from Methods->Components Mapping of Retention time   to compounds is programmed here.  Review this table before you start. Make sure you have the Retention time against each compound and windows times are recorded properly.


(a) The  information  which is displayed in the Components table  is stored in Components.csv file
(b) You can edit using Microsoft Execl.
(c) Current version of Peak works allow you to edit the Retention time for each compound, but does not save that information back into csv file.
(d) So if  you want to modify the Mapping of Compound names with Peak Retention time, you need to edit the CSV file

I recommend you to use Microsoft excel for editing the Components CSV file  and not to edit manually using text editor, as there is a chance of making errors.

### Electrical Connections
Connect the analog data source to A0 and A1 of ADS1115 Card and not to any other analog port
The current version of Peak works read data only from these two ports.

## How to Run Peak Works on Rpi and Analyze peaks

Step 1 : Press the *"New"* Icon the first icon on the Icon Bar (This will not display anything) so Just press once and leave.
               (Internally it resets everything for new Run)

Step 2 : Click on Method ->Detector A (This will give you a pop up)
              (a) Select ON/OFF and enable the sensor (Tick mark)
              (b) At the bottom of pop up select the Save to CSV (Tick Mark)

Step 3:    Click on Method ->Detector A (This will give you a pop up)
              (a) Select ON/OFF and enable the sensor (Tick mark)
              (b) At the bottom of pop up select the Save to CSV (Tick mark)
Step 4:  Press the Run Icon (Sixth Icon from the left in the icon bar) the one which shows a Desktop and RED flame - This will start
              the data capture from A2D convertors and pop up two Live Graph windows. You can see the graph in real time.

Step 5:  I assume you are using two potentiometers to simulate GC units. If that is the case, now turn the knobs you
              can see peaks on the live graph. Connect the analog data source to A0 and A1 of ADS1115 Card and not to any other analog port
              The current version of Peak works read data only from these two ports.
 
Step 6:  Once you are done with Data Capture PRess the  STOP Icon this will stop the run. Now the data captured in the memory  and not saved

Step 7:   Click on the File Menu (The first one in the Menu Bar) and Select Save File->Save now it will ask for a file name- Specifiy the file name
               (This will save the setting to .JOB file and
               captured data from A2D coverter to two CSV files)
                Wait for a minute so that the data is fully saved into .csv files
                Note: IF you do not do a save all the data captured will be lost

Step 8: Click New Icon Again (Reset every thing as we are getting ready for analysis)

Step 9:  Click File Menu  and select Open (File->Open). This will show you file selection pop up

Step 10: Select the JOB file into which you had saved and press OK

Step 11: It will pop up two graphs based on the data you had captured with peaks numbers at this point, based on Peak retention times
                the compounds would have been detected.

Step 12:  Select Window-> Table A This will show you table with the compound detected based on Retention times.
                It uses the existing standards Table  (Method-> Standards) to map peaks to Compounds.

Step 13 :  If you want a PDF report of the analysis generated Select File->Report Give few minutes, wait till pop up comes up, and press OK

Step 14:  Now you can see the PDF report in the folder pointed by "WorkSpace" folder (PIDSettings.json)

Step 15:  Printer interface is not implemented however you can, print or email the PDF file.

Step 16:  Now you can quit the Peak work using File->Exit button

The .csv file generated can be opened in MS excel and can be used for further processing
