# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

## Step1:
Initiate the MobileRobot.

## Step2:
Connect your PC with the MobileRobot through WiFi.

## Step3:
Open battery_level.py file and check the battery.

## Step4:
Open the other python files and program the movements of the robot using python.

## Step5:
Execute the python program and record the movements

## Program
```
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_led.set_led(comp="all",r=100,g=100,b=0,effect="on")
    
    ep_chassis.move(x=0.7, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=100,b=0,effect="on")   
    
    ep_chassis.move(x=0, y=0, z=83, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=2.85, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.move(x=0, y=0, z=85, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=100,b=100,effect="on")
    
    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
    
    ep_led.set_led(comp="all",r=0,g=100,b=100,effect="on")
    ep_chassis.move(x=0, y=0, z=55, xy_speed=1).wait_for_completed()
    
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.drive_speed(x=0.5,y=0,z=-20)
    time.sleep(14)
    ep_chassis.drive_speed(x=0,y=0,z=0)
    
    ep_robot.close()
    
    
```

## MobileRobot Movement Image:
## Initial Position
![image](https://github.com/naren2704/mobilerobot-openloopcontrol/assets/118706984/76791e1e-bb09-487b-9bc4-87e1175b9e17)
## Final Position
![image](https://github.com/naren2704/mobilerobot-openloopcontrol/assets/118706984/cbcf59b1-73e8-42b9-89d9-2c3033ce3750)



## MobileRobot Movement Video:
https://www.youtube.com/shorts/t8nVyGZvT7w



## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.



```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
