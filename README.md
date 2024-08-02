# adam-4xxx
Methods for control of ADAM-4xxx modules

## Generic Vi for Testing Commands
![image](https://github.com/user-attachments/assets/0620fe4f-394b-4724-a18e-8c880ff78758)

## User Interface using State Machine for Analog Data Sampling
![image](https://github.com/user-attachments/assets/e6c081b9-643f-4df1-99e4-064c3e1fa25e)
![image](https://github.com/user-attachments/assets/e3b96b92-593e-4dd2-a1b0-848433636f96)



## Wiring
![image](https://github.com/user-attachments/assets/08e5e9f3-cdbb-4225-b618-eac8455807b8)



## ASCII Commands List
### Module: adam-4069
Command Structure:
`#(AA)(BB)(CC)`
- AA: Module Address (01)
- BB: Channel:
  - 00: All Channels
  - 0B: Channel Number (hex)
- CC: State
  - All Channels: CC (hex)
  - One Channel: 0C (0,1)
  
| Command | Action            |  Valid Response | Invalid Response |
|---      |---                |---              |---               |
| #010000 | All Channels: Off | >               | ?AA AA is module address)            |
| #01000F | All Channels: On  |
| #011000 | Channel 0: Off    |
| #011001 | Channel 0: On     |
| #011100 | Channel 1: Off    |
| #011101 | Channel 1: On     |

### Module: adam-4017+
Command Structure:
`#(AA)(BB)(CC)`
- AA: Module Address (01)
- BB: Channel:
  - 00: All Channels
  - 0B: Channel Number (hex)
- CC: State
  - All Channels: CC (hex)
  - One Channel: 0C (0,1)
  
| Command | Action            |  Valid Response | Invalid Response |
|---      |---                |---              |---               |
| #010000 | All Channels: Off | >               | ?AA AA is module address)            |
| #01000F | All Channels: On  |
| #011000 | Channel 0: Off    |
| #011001 | Channel 0: On     |
| #011100 | Channel 1: Off    |
| #011101 | Channel 1: On     |




### Digital Output Command Structure


\#





## LabView Example for ADAM-4069 Relay Module

 ### Features:
- Relay manual control
- Relay timed control
- Setup via config file
- Safe startup/shutdown
### UI
 ![image](https://github.com/ImogenWren/adam-4069/assets/97303986/7fdd7b80-c65b-4527-a53a-29ff03361982)


 ### Block Diagram

 #### Setup & Settings Recall
 ![image](https://github.com/ImogenWren/adam-4069/assets/97303986/6d77dd08-8947-4233-b4d9-ee85ab8510fc)


 #### Main State Machine
 ![image](https://github.com/ImogenWren/adam-4069/assets/97303986/319e2c4b-f222-47b8-a6c3-c9633bafccf8)

 #### Safe Shutdown
 ![image](https://github.com/ImogenWren/adam-4069/assets/97303986/c706ec72-f9c8-4cf7-9e1d-ffe9976faa28)


