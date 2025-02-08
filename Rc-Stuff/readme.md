# RC and Fpv Notes


## Table of Contents
- [Useful Info](ee)
- [Radio & Receiver](./Radio.md)
- [Flight Controller](./FlightController.md)
- [INAV](./Inav.md)
- [Esc and Blheli](./Blheli.md)
- 

- My Previous Builds    
  You can download a config and use Notepad++ with the compareplus plugin to see line by line differences.
  Helpful for easy sanity check of your settings.  
  - [Nano Goblin ANALOG](./Planes/GoblinAnalog)
  - [Nano Goblin DIGITAL](./Planes/GoblinDigital)
  - [Atomrc Penguin](./Planes/Penguin)
  - [Atomrc Dolphin](./Planes/Dolphin)
 

  ## Important:

  ### Update Everything
    I reccomend updating everything to the newest stable release before starting.  
The firmware most things ship with is usually way out of date and important fixes happen often.  
Once set up and flying, update only when you want some new feature, etc.  
The "Release Tab" of each project will show highlights of the changes, along with any important info in that update.  
F.y.i. Cool stuff is constantly getting added to everything so its worth occasionally checking.

 To update, use the LATEST release of these updaters:
   - Radio: Edgetx Buddy
   - Transmitter inside radio: Elrs Configurator
   - Reciever on plane: Elrs Configurator
   - Flight Controller: Inav Configurator
   - Esc: [EscConfigurator](escconfigurator.com)
   - Vtx and Vrx may need updating too with Walksnail tool.


# Useful Info and Links

  ### Stick Commands while unarmed
![StickPositions](https://github.com/user-attachments/assets/a892b04a-b837-475a-94b3-e3f0f344b8c6)


  - **This allows you to arm w/out gps lock, etc. Used for testing.**
      > set nav_extra_arming_safety = ALLOW_BYPASS    
![Bypass](https://github.com/user-attachments/assets/ce84dd5b-9d7e-4238-b9d9-3df9faea9d1a)



  - **Bypass Autolaunch**  
WIGGLE PITCH/ROLL STICK to disable Autolaunch.
> If you want to launch the plane manually just move pitch/roll stick after you have armed the plane and you have back throttle control. If you inadvertently disarm mid-air before raising the throttle again (you should lower the throttle to arm again) move pitch/roll stick and you will have throttle control back.  

Accidental disarm mid-air.  
After disarm,  
1. Throttle LOW  
2. Re-arm
3. Wiggle Pitch/Roll




  ### Autolaunch info  
I set launch idle thr to 0 for light models, ADD MORE






