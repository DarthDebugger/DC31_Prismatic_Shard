# The Prismatic Shard Badge
**An unofficial Defcon 31 Badge Compatible Electronic Shard**

[The Prismatic Shard Badge](https://www.cybercircuitry.com/)


This guide is intended to provide a basic explanation of the Prismatic Shard Badge and its functions.  There may inadvertently be some *minor spoilers
so if you are hoping to do this badge totally on your own as a journey of discovery you may want to tread lightly.
However, If you are having an issue or questions about the different functions and just need a little guidance, this is the place for you. 

The Prismatic Shard Badge is designed to be an interactive and captivating piece of hardware and art, providing a unique and memorable experience to enjoy during and after the con. We hope you'll enjoy exploring the features and possibilities that the Prismatic Shard has to offer.

## Table of Contents
- [Introduction](#prismatic-shard---defcon-31-electronic-badge)
- [Features](#features)
- [Getting Started](#getting-started)
- [FAQ](#faq)
- [License](#license)

## Features

- Eye-catching LED matrix for Bling
- [ATTiny1616](https://www.microchip.com/en-us/product/ATTINY1616) Microcontroller-based design
- Interactive buttons and Social IR Communicator and Battle system
- USB-C rechargeable LIR2032 battery (included)
- Open-source firmware (After the con)
- Defcon 31 compatibility for badge holder system (hopefully - I have not seen a real one)

## Getting Started

To get started with your Prismatic Shard Badge, follow these steps:

1. **Insert the Battery**  
Please be very careful with the polarity (direction) of the battery.  Putting it in backwards will cause permanent damage to the board instantly.
The battery is a type LIR2032 and is rechargeable.  The shard comes with a built in charging controller and you can charge the battery simply by plugging in the USB-C port to power.
The onboard USB-C port is also a serial adapter and you can perform some very basic interaction with the badge over the serial interface.  (115200 8N1)

2. **Power Up** 
Turn on your Prismatic Shard badge.  The power switch is located next to the USB-C port. 

3. **Modes**  
Get ready to explore its features! The Badge has 4 modes of operations.

![Prismatic Shard Modes](https://github.com/DarthDebugger/DC31_Prismatic_Shard/blob/main/includes/media/Modes.png)

Transitioning from one mode to the next is as easy as pressing the mode button on the front of the Badge.
![Prismatic Shard Mode Button](https://github.com/DarthDebugger/DC31_Prismatic_Shard/blob/main/includes/media/mode_Btn.PNG)

1. Bling Mode - 
Bling can drain the battery.  The LED brightness and routines have been created with the battery in mind, but its also rechargeable so enjoy that bling and turn some heads at the con!
![Bling Mode Button](https://github.com/DarthDebugger/DC31_Prismatic_Shard/blob/main/includes/media/Bling_action_btn.PNG)

2. Meld Mode - Allows Friendly interaction with other badges.
![Meld Mode Button](https://github.com/DarthDebugger/DC31_Prismatic_Shard/blob/main/includes/media/Meld_Greet.PNG)

3. Battle Mode - Fight with other badges to grow your powers.
Battle mode auto selects from the powers you have achieved and auto heals periodically. Befriending and Battling other badges helps you to progress and unlock features in the badge.
![Battle Mode Button](https://github.com/DarthDebugger/DC31_Prismatic_Shard/blob/main/includes/media/Battle_Btn.PNG)


4. CMD mode - 
There is a Serial Terminal on the badge that you can interact with.
One command you will want to know is  "LED".  Entering LED will cycle through the badges lighting power levels.  The higher the level the faster the battery will be drained (Max draw in my bench testing was close to 30mA at brightness of 100 which caused some instability and MCU brown outs, so the max brightness has been limited to 60 which is still quite bright). 
The ATTiny1616 has a whopping 16kb of Flash, 2k of sram and a 256 byte EEPROM.  the CMD shell very, very limited, however there are some commands that may unlock other features.
![CMD Mode](https://github.com/DarthDebugger/DC31_Prismatic_Shard/blob/main/Photos/14%20CMD%20mode.PNG)



## How to play with others

### General Rules
Be polite, when you greet other badge owners. Introduce yourself and ask them how they are enjoying the con.  Offer the Meld with their badge or battle if they would like.
Be understanding if someone does not want to battle as it does take a little while and they may be headed to a talk.

### Meld Mode
Place your badge into meld (Friend) mode and hold it vertically (like its native position in the badge) at the other badge. This will align the IR LED and receiver with the other badge.
Press the greet button to sync with the other badge. This will add them as a new friend and possibly give you a new mutation.

Mutations can make your attack spells stronger or give you a native defense against a specific attack type.

##Battle Mode
The same as meld mode hod your badge vertically and point it at your opponent.  You can battle friends without damaging your friendship status so you don’t have to worry about losing mutations.
It is best to attack one at a time.  If you attack at the same time the attacks will cancel like that scene from harry potter.
When you score a hit, the badge will flash showing your remaining health.

You are killed when you have no health left.  (Health recharges over time)
When you are killed your badge will flash red and your opponents badge should play a victory animation.

Leveling:  Battleing helps you level.  This gives you more health and makes your attacks stronger.   It can also unlock new spells.


## FAQ


### **1. Can I customize the LED patterns on the badge?**
Not until the source code is released but then absolutely.  The Prismatic Shard badge is designed to be highly customizable. You can modify anything once the source code is posted at the end of the con.  
For now there are preprogrammed bling routines you can cycle through, and more may be available as you progress in the badge

### **2. How do I recharge the badge's battery?**
The badge comes with a USB-rechargeable battery. To recharge, simply connect it to any standard USB port using a USB-C cable.
Please DO NOT use a non-rechargeable battery like the CR2032.  (If the charging circuit is engaged with this type battery it could set fire!)

### **3. Is the badge compatible with Defcon 31 badge holder?**
the Prismatic Shard badge is designed to and always intended to be fully compatible with Defcon 31 badge as far as we know.  
I 3D printed a replica from the [defcon.org](https://media.defcon.org/DEF%20CON%2031/DEF%20CON%2031%20badge/) [blender file](https://media.defcon.org/DEF%20CON%2031/DEF%20CON%2031%20badge/DC31BADGE-CHAMBER.blend) and triple checked measurements against the [PDF posted](https://media.defcon.org/DEF%20CON%2031/DEF%20CON%2031%20badge/Badge%20Add-On.pdf), but that is still no guarantee that it will be a perfect match.  
I will say that it is possible that the small "mouse bites" on the Prismatic Shard's edges may need some gentle trimming for the shard to easily side in and out of the holder.  
I did some of that during depanelization.  If you decide to use sand paper on the badge, I would recommend the approach of taping the sand paper to a table or hard surface and gently rubbing the badge against it.  
Just be extra careful not to sand off any of the coating or traces on the front or back of the shard as this may permanently damage the badge.


We hope you enjoy your Prismatic Shard badge! If you have any questions or need assistance, please feel free to reach out to us through the issue tracker or via email. Happy hacking!
