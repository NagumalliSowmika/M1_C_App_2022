# Covid Vaccine Registration

![Screenshot (45)](https://user-images.githubusercontent.com/64276267/161389752-3b852a85-8341-4795-a341-047501161446.png)

## Introduction

The deployment of covid-19 vaccines in India was done in a sudden burst and thus the tracking became very complicated. 
Due to multiple input and output commands on the server, it resulted in several slow running issues and crashes. 
The Aadhar details were used to allot the vaccines and hence it operated on a central server.
To avoid the use of central server for all commmands, a local server will be loaded with the vaccine-registered data. 
Local verification and completion of vaccination data will be processed locally and will be loaded back to the main server by the end of day.

Each vaccine centre will operate locally to register and allot vaccines. 
The basic registration can be done online and schedules are set as desired by the patient. Assuming a vaccination centre can vaccinate around 100 people in a day. 
The data handling for online basic registration will be mostly done in the day time and the data acquired by the local centres of vaccinated people can be handled in the night.

The local server must store the data of around 100 people where the allocated online registration data will be loaded onto the local server of that local centre. 
Verification of the dat r online basic registration will be mostly done in the day time and the data acquired by the local centres of vaccinated people can be handled in the night.

### Advantages
* Smoother data handling.
* Pre data readily available for verification.
* Flexibility to add new registrations limited with server alloted memory.

### Disadvantages
* Cannot add large number of new registrations due to local server limitations.
* Encryption is not enabled to protect the data.
* OTP verification is not activated for new registrations.

## SWOT Analysis
![SWOT analysis](https://user-images.githubusercontent.com/89698000/132556785-561d19ab-c53d-4658-8138-401da25ce78e.png)
## 4 W's and 1 H
### Who
* Patient who needs to be vaccinated.
### What
* Verify the details of the patient using the alloted data.
### When
* During the time alloted for vaccination.
### Where
* Local vaccination centre.

## High Level Requirements
| ID | Description | Status (Implemented/Future) |
| --- | --- | --- |
| HR01 | System should be able to access pre loaded registration data for verification | Implemented |
| HR02 | User should be able to add new registrations | Implemented |
| HR03 | System should recognize vaccinated patients | Implemented |
| HR04 | OTP generated verification for secure registration | Future |
| HR05 | System should recognize invalid credentials | Future |
| HR06 | System should be updated with the time interval between two doses | Future |

## Low Level Requirement
| ID | Description | Status (Implemented/Future) |
| --- | --- | --- |
| LR01 | Only new user must be given an option to select vaccine type | Implemented |
| LR02 | Total quantity of vaccines used must be shown by EOD | Implemented |
| LR03 | Full list of patients vaccinated must be set as output | Implemented |
| LR04 | Remaining and present stock of vaccines must be tracked | Future |
| LR05 | Vaccine vials must be tracked for its use within a day | Future |

## Architecture
* Structural Diagram
* Behavioural Diagram
## 1. Structural Diagram
Structural diagrams are a type of visual design that depicts the stages required to solve a problem. The structural diagram depicts the hierarchy or structure of the system's many components or modules, as well as how they connect and interact with one another.

## FLOW CHART

![Screenshot (48)](https://user-images.githubusercontent.com/64276267/161387475-15978551-52c1-46ab-976f-1d0f5a9a674b.png)


## 2. Behavioural Diagram
Behaviour diagrams depict the item in a system's dynamic behaviour which can be represented as a series of changes over time. A behaviour diagram is intended to provide clarity.

## UML USECASE

![Screenshot (47)](https://user-images.githubusercontent.com/64276267/161387278-5b5c3592-47ac-4dcd-ad6c-ea63250ee420.png)

## Test Plan

## High Level Test Plan
| Test ID | Description | Input | Expected output | Actual Output |
| --- | --- | --- | --- | --- |
| 01 | Check patient registration status | 123 (aadhar no) | {-1} |  (not found) |
| 02 | Check patient registration status | 123 (aadhar no) | {0,1} |  (found) |
| 03 | Check patient vaccination status | 3 (patient id) | {>0} | (vaccinated) |
## Low Level Test Plan
| Test ID | Description | Input | Expected output | Actual Output |
| --- | --- | --- | --- | --- |
| 01 | Check patient registration status | 125 (aadhar no) | 0 | 0 (registered, not vaccinated) |
| 02 | Check patient registration status | 130 (aadhar no) | 1 | 1 (registered, vaccinated) |
| 03 | Check patient vaccination status | 3 (patient id) | 1 | 1 (first dose) |
| 04 | Check patient vaccination status | 3 (patient id) | 2 | 2 (second dose) |
| 05 | Check patient vaccination status | 3 (patient id) | 3 | 3 (already vaccinated) |

## Output

