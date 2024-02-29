# Python for Data Science - Data Network Assessment Example
---
## Project Overview:
---
This project focuses on using Python Pandas library to perform a simple Network Assessment based on a specific provided Data Set, privately provided by 3rd party sofware.

During the process, we will interrogate the Data Set and extract answers based on provided data:

* How many devices does this network have?
* Per Column Data completion rate?
* Which Protocols or Features are available and or running on network devices?
* How many devices are running each protocol / feature?
* What percentage of the total do those values represent?
* How many "Unique" software versions are the devices running and which ones are those?
* Whats the number of device vendors (and which ones) used on the reference network?
* What device models are used and what percentage of total do those represent?
* Provide a list of features and protocols used / running per device
* Number of features and protocols running per device
* Which are the top devices, using the number of features and running protocols as selection criteria?

Project code and results can be found in file "simple_network_assessment.ipynb".


## Data:
---
This Data set has been extracted from a Lab environment and you have permission to use it.
Format: CSV
File: Lab Network Devices DataFrame.csv
Size: 43KB

The reference file contains a listof network devices that highlight on a per-row basis:

* Device Type
* Vendor
* Model
* Software Version
* EIGRP Running (True / False)
* ISIS Running (True / False)
* OSPF Running (True / False)
* BGP Running (True / False)
* MC-LAG Running (True / False)
* VXLAN Running (True / False)
* NAT Running (True / False)

For data treatment details, please refer to the "ipynb" file.


## Conclusion:
---
This project outlines a clear procedure for conducting a Network Assessment using a provided dataset.

One important aspect to note is that the solution has been designed with scalability in mind. This means that individuals who can generate a similarly formatted dataset, with minimal adjustments, such as adapting the built-in complementary Python List containing device "protocols and features" - "run_protocols," will find that the underlying code can execute checks accordingly. These checks are based on the existing columns containing present protocols and features.

#### Remarks and findings:

##### Network Size
* Device wise, the network size is 416

##### Running Protocols and Features
* There are 193 Devices that Run OSPF - Which Represents 46.39% of the total
* There are 23 Devices that Run EIGRP - Which Represents 5.53% of the total
* There are 15 Devices that Run ISIS - Which Represents 3.61% of the total
* There are 81 Devices that Run BGP - Which Represents 19.47% of the total
* There are 3 Devices that Run MC-LAG - Which Represents 0.72% of the total
* There are 4 Devices that Run VXLAN - Which Represents 0.96% of the total
* There are 16 Devices that Run NAT - Which Represents 3.85% of the total

##### Software Version Info
* Out of the 416 devices, there are 104 unique software versions running
* This mean, there is a unique software version running every 4 devices (this is someple math, not included on the actual code, but could have been)
* This leads to indicate that the environment does not have an acceptable standard in place, if any
* Complete list of the reference particualr versions can be found in the code file

##### Verndor and Model Info
* The network is built using 15 different vendors (List available in the code file)
* From the reference vendors mentioned on the previous item, there are 89 different device models (details on the code file)
* These respond to 26 different Device Types (this is a category mainly used for data collection and parsing)

##### Running Protocols List and Counts
* The 2 new columns added to the Data Frame, provide some level of background on how critical those might be for operations
* There is only 1 device running 4 protocols / features, which makes the device a criticial focal point for further checks and assessments (details about which ones in code file)
* There are 184 device that dont run any of the listed features or protocols (details about which ones in code file)
* 142 Devices run 1 of the listed protocols or features (details about which ones in code file)
* 78 Devices run 2 of the listed protocols or features (details about which ones in code file)
* 11 Devices run 3 of the listed protocols or features (details about which ones in code file)

## Final Notes:
---
The information presented above offers a valuable approach to network analysis and assessment. While there are numerous additional calculations and operations that could have been included based on the provided dataset, doing so would go beyond the scope of the project.

With more complex datasets, the potential for scalability in checks and verifications becomes virtually limitless.

Thank you in advance for your interest in this project!

CDP