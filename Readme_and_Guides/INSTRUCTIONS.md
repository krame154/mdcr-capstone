# Reproducing MDCR Results

### Description
This guide will show you how to utilize this program’s interface to extract data from a contractor’s excel spreadsheet and have a data analysis performed on said data.

In summary, the program will open a GUI interface which will require contractor demographic data as input. The program will take that data and find the ratios of each demographic (white male, white female, hispanic, non-hispanics, etc.). 

The equation for the demographic ratio is:

$$
\text{Demographic Ratio} = \frac{\text{Number of employees of that demographic}}{\text{Total number of employees}}
$$

Once these ratios are calculated, the program will take regional census demographic ratios and subtract the differences. The differences are then added to a word doc, with positive value meaning that the demographic is over-represented, and negative value meaning that the demographic is underrepresented.

### Install Instructions
Please see the INSTALL.md markdown file for the step-by-step process on how to install the program in its current state.

### Running the Program
After following the install guide and setting up the environment, you will be able to run the GUI interface to generate the word document.

In your terminal, navigate to where the repository was downloaded. This can be performed by using the ```cd``` command to navigate to the proper repository.
(Example)

```
cd path/to/mdcr-capstone
```

Once inside the directory, type the following command in your terminal to start the program. Once this command is run, give it a few seconds and an interface should appear.

Windows:
```
python program.py
```

macOs / Linux:
```
python3 program.py
```

#### Option Selections
Once the interface pops-up, it should look something like this:<br>
<img width="371" height="279" alt="example" src="https://github.com/user-attachments/assets/5e1b8fc4-5d67-46b8-802e-11351b04b2ca" />

We can ignore the checkboxes for the moment, all we need is an input file and an output destination.

For the purposes of showing how the program works, we will use some example data obtained from Teams. To find the example data, go the the CMSE 495 channel, and in the general chat, navigate:
<br>CMSE 495 Teams Channel > General > Shared > MDCR > Demo Data<br>
Then install the Contractor Workforce Data D CSV file.

Once you have this file installed, go back to the interface and now choose to select an input file by clicking the “Browse…” button. This will open a file explorer where you can navigate through the files on your own device; use this to find the recently installed contractor data file. Once you find it, select it in the file explorer and it will then be selected as an input file for the program.

Next you will need to select an output destination for your file. Click the “Choose Output Folder…” button and this will open a file explorer. This time, you need to find a folder in which you would like the word document to be saved to. Once you navigate to that folder, click the “Select Folder” button in the file explorer and it will be set for the output.

Now that the input files and output destination has been specified, we can run the program. For now the checkboxes do not change the result of the program, so we can ignore those. To run the program, click the button at the bottom that says “Process Data.”

**NOTE**: While the data is being processed, do NOT click anywhere on the interface program as it will freeze. Give it some time to run, and progress can be seen through the terminal which you used to run the program.

Once the program is finished running, the text below the button should say that processing was finished. Once this appears, the program is safe to exit which can be done just like exiting any normal application by clicking the close button at the top right. On your own file explorer, you can navigate to the folder which you specified as the output folder and you will see a word document file titled “contractor_analysis.docx”. You can open this file to view the results.

### Document Overview
The returned template document is mostly left empty for reporters to fill out. As of now, the only section that is filled out by the program is the workforce data analysis section. In this section, a brief paragraph is written describing the difference in ethnic ratios of a chosen contractor compared to the US census ratios. So, for example, if a contractor has a smaller ratio of Hispanic employees compared to the ratio of Hispanic workers in the US, it’ll show a negative difference in the paragraph.


