# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Initiate the MobileRobot.

Step2:

Connect your PC with the MobileRobot.

Step3:

Program the movements of the robot using python code

Step4:

Execute the python program.

## Program
```
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

    ep_chassis.move(x=2.7, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=55, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=204,effect="on")

    ep_chassis.move(x=0.7, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=55, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=204,effect="on")

    ep_chassis.move(x=0.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=60, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0.7, y=0, z=-50, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=100, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")

    ep_chassis.move(x=0, y=1.2, z=0, xy_speed=2).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=230, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")
    
    ep_chassis.move(x=-1.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-155, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")

    ep_chassis.move(x=.7, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=60, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=.4, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=204,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```
## MobileRobot Movement Image:

![robo](./img/robomaster.png)

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://youtube.com/watch?v=Yj-F8mBArS4&feature=shared

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
