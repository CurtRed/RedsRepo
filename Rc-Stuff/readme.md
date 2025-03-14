# RC and Fpv Notes

 
  - [Nano Goblin Diff all/Dump all](./Planes/NanoGoblin/README.md)
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


# General Nano Goblin notes

### Micro-Stalls/Porpising
  
  - [From rc forums](https://www.rcgroups.com/forums/showthread.php?2955321-STRIX-Nano-Goblin/page391)
    > porpoising usually means either too much servo travel on the elevator control or tail heavy. should only be around 5-6mm up from neutral and 5-6mm down for 10mm total, for maiden. If it is like 18mm or more then it makes the plane nigh unflyable at launch. I didn't pay close attntion to this at first and made a bunch of unsuccessful launches. reviewed the build video, lowered my servo throws and then it launched nicely. And planks don't have empennage way back so are more sensitive to CG placement
    > In manual mode, control throws are directly proportional to stick inputs multiplied by the
the pitch Rate value. It's not uncommon for people to let the pitch rates just
be too high for a plank, and they compensate by only moving the stick very little.
Don't do that. Fix the rate value so that you can use a larger stick throw without
hyperstalling the plane. When planks stall (at any speed), they pitch bob.
So decrease the pitch rate until you can make a large pitch inputs without it
immediately going into a pitch bob. You should find that your pitch rate is somewhere
around as 50% of your roll rate (maybe even lower).
    
    > Ok, now why does it pitch bob in ACRO and auto-level modes which run on top of ACRO?
When you're flying in ACRO mode your stick input represents a request
for a specific rate of rotation, which is called the set point. The difference between
the set point, and the actual rate of rotation is the error, and the PID+FF loop's
job is to resolve that error. For actual control you can pretty much ignore
P and D (they're important for instantaneous stabilization against bumps),
which leaves I-term and FF. FF is like manual mode layered on top of PID.
In other words, it is just stick input * FF * rate, so when you move the stick it
moves the control surfaces in that direction, no matter what PID is trying to do.
So I-term.. It is the integral of the error (difference between desired and actual
rotation rate) over time and it will keep moving the surfaces further and further
until they have a large enough effect on the aircraft's rotation to resolve the error.
The roll rate can be quite high so generally iterm + FF can achieve the desired
rate almost immediately, but the true max pitch rate is limited by the capabilities of
the aircraft. Think about it. You could roll at 360-720 degrees per second with
enough airspeed and control throw, but try to pitch up hard and you'd be hard
pressed to achieve 90 degrees/sec (e.g. pitch from level to straight up in one second).
But I-term doesn't know about this limitation. You pull back and it will
attempt to achieve a pitch rate the aircraft is not capable of, and it'll do
that by moving the surfaces further and further until it hyperstalls
and then it just keeps trying even harder.
So... Try this. Fix your pitch rates in manual first, so you can make aggressive
pitch inputs without hyperstalling. Take note of how far your elevons move
in response to pitch.
Then set your pitch I-term value to zero, switch to ACRO and adjust your FF value
until the elevons move in response to pitch inputs about the same or a little less
than they do in manual mode. Go fly, and check that it still flies
OK in ACRO mode without hyperstalling. Now slowly bring up
your pitch I-term until the pitch simply feels a bit "locked in".
Without pitch I-term, if you let go of the stick while in a mild
climb or dive the plane will usually settle itself into
level flight or wander a bit up and down. When I-term is *just enough*
you should be able to let go of the stick and the plane will
hold its pitch attitude. Now make some aggressive inputs
again and make sure you're not hyperstalling. If it does,
then back of I-term a bit, or just ease into
the maneuvers a bit more gently.
But again, this all starts with fixing your pitch rate first. 




