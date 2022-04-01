# Covid_Vaccine Registration
## Badges
## Introduction
The deployment of covid-19 vaccines in India was done in a sudden burst and thus the tracking became very complicated. Due to multiple input and output commands on the server, it resulted in several slow running issues and crashes. The Aadhar details were used to allot the vaccines and hence it operated on a central server. To avoid the use of central server for all commmands, a local server will be loaded with the vaccine-registered data. Local verification and completion of vaccination data will be processed locally and will be loaded back to the main server by the end of day.

Each vaccine centre will operate locally to register and allot vaccines. The basic registration can be done online and schedules are set as desired by the patient. Assuming a vaccination centre can vaccinate around 100 people in a day. The data handling for online basic registration will be mostly done in the day time and the data acquired by the local centres of vaccinated people can be handled in the night.

The local server must store the data of around 100 people where the allocated online registration data will be loaded onto the local server of that local centre. Verification of the data is done based on the details provided by the patient. Once completed, the data of the vaccinated will be sent back for future use and reference.


## Folder Structure
|Folder             | Description |
|-------------------| -----------------------------------------|
| `1_Requirements`   | Documents detailing requirements and research|
| `2_Architecture`         | Documents specifying design details|
| `3_Implementation` | All code and documentation|
| `4_Testplan`      | Documents with test plans and procedures|
|  `Images`       | Project Images |

## Aim
* Smoother vaccination registration process
* Reduced data traffic in the main server
* Operation of registration and verification is localized
## Input
* Pre-registered list of patients for vaccination
* New registration of patients for vaccination
## Process
* Pre registered patients who had appointments verify the documents
* Verification is done with pre registered data of patients
* New registrations are added to the vaccinated log
* Total number of vaccine vials consumed is tracked for both type of vaccines
## Output
* Vaccinated data log is updated and new registrations are added to the end of the pre data list
* List of vaccinated patients along with total vials consumed is printed

