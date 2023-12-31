# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1: Initiate the MobileRobot.
### Step2: Connect your PC with the MobileRobot through Wi-Fi.
### Step3: Open batter_level.py file and check the battery.
### Step4: Open the other Python files and Program the movements of the robot using python.
### Step5: Execute the python program and record the movements.

## Program
```python

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x=0.3, y=0, z=80, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=-1.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=50, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
   
    ep_chassis.move(x=0, y=-1.35, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-130, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")

    ep_chassis.move(x=0, y=1.55, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")

    ep_chassis.move(x=2.05, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=51,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=80, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0.65, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=102,b=153,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")



    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![image](https://github.com/Gokhulraj2005/mobilerobot-openloopcontrol/assets/138849253/f08129f6-118c-474c-87f7-2974ee0de6a2)


## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://youtu.be/Wipkv_B-eLA

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
GOKHULRAJ V
212223230064
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
