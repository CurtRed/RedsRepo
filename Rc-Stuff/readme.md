# RC and Fpv Notes

  ### Diff all's
  - [Nano Goblin ANALOG](./Planes/GoblinAnalog/readme.md)
  - [Nano Goblin DIGITAL](./Planes/GoblinDigital/readme.md)
<!-- >  - [Atomrc Penguin](./Planes/Penguin) -->
<!-- >  - [Atomrc Dolphin](./Planes/Dolphin) -->

 

## Random Useful Info

  ### Stick Commands while unarmed
![StickPositions](https://github.com/user-attachments/assets/a892b04a-b837-475a-94b3-e3f0f344b8c6)


  - **This allows you to arm w/out gps lock, etc. Used for testing.**
      > set `nav_extra_arming_safety = ALLOW_BYPASS`    
![Bypass](https://github.com/user-attachments/assets/ce84dd5b-9d7e-4238-b9d9-3df9faea9d1a)



  - **Bypass Autolaunch**  
WIGGLE PITCH/ROLL STICK + Thr Low to disable Autolaunch. 

    >### Accidental disarm mid-air.  
    >After disarm,  
    >1. THROTTLE Low  
    >2. Re-arm
    >3. Wiggle PITCH/ROLL



## Inav Settings Reference  
  ### [Inav Settings](https://github.com/iNavFlight/inav/blob/master/docs/Settings.md)  



### Autolaunch info  
>I set nav_fw_launch_idle_thr to 0 for light models. If the plane has a hard time gaining control authority after throw, it can be helpful to use. Just remember to watch the prop when used.






