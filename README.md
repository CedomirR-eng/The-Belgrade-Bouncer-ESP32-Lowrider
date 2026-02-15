# The-Belgrade-Bouncer-ESP32-Lowrider
I made a wireless rc dc motor in my last project, so for my next project lets make a rc car! And lets make it a lowrider, because why not?
But we will make a radio frequency control system instead of a IR remote system like last time.(RF is more suited for this job)

So we need to make a TX(the remote) and the RX(the car), and instead of the car simply going forward backward left and right, lets add some spice to it.
Lets make it so it can bounce like a real lowrider! Also we will add front lights and a horn, because why not.
  Now i will show you my first skeches of the car:

![Image](https://github.com/user-attachments/assets/1c23ca25-4f5e-4a58-9824-5f9c5eb1ca78)

This is my first sketch of the TX(remote)

![Image](https://github.com/user-attachments/assets/2a9fc8c4-f375-4c09-a0d1-d81c3ea02574)

But now we arrive on the tricky part. The car...
First lets see what the circuit diagram looks like:

![Image](https://github.com/user-attachments/assets/2d9129d8-031c-4585-9363-16a5dd951fb3)

Now we have a principle of how it will work.
The TX joystick Y-Axis controls the main motor direction(forward or backward), while the X-Axis controls the servo motor(wheel).
Meanwhile the SW(press the mushroom) of the joystick is controling the horn, and the switch is controling the lights. 
Also B1,B2,B3,B4 control the mail thing. THE BOUNCERS!
Renember, we are talking about TX components controling the RX.

Now that we did the electronic part, we go to the mechanical part.
So far we exlained how will this work and mentioned the tasks the RX will do acording to the instuction it gets. but now we need to put it all together.

First we will do the main motor:

![Image](https://github.com/user-attachments/assets/64bbbcda-e1ef-4b95-91b0-82f355e3e092)

We see here two options of which i think option 2 is much better because of the symmetry, the weight of the motor is in the center, but the gear and the motor cant both be in the center so it isnt symmetrical.
But what if we use two motors from both sides  in option 1?!

![Image](https://github.com/user-attachments/assets/d33c5656-3789-482b-a290-91ccb4ea5bd5)

BUT WHAT IF WE COMBINE THE TWO AND GET THIS:

![Image](https://github.com/user-attachments/assets/3fb6566b-ae68-4872-809b-5d193b212aa6)

I think this is what I am looking for. It is symmetical and powerful, but it requires two same dc motors.
The motors need to rotate in different directions to work. And that can be done by connecting the motor poles differently.

But this has a major problem, this axis needs to move!
We need to add amortizers so the car slides like a real lowrider. And most importantly, THE BOUNCERS!
So about a hour later, i learned alot about car mechanics and came up with this:

![Image](https://github.com/user-attachments/assets/6a9606ab-9dcc-4a3f-a6ff-9035c5fb9fcd)


