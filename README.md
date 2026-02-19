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

The ends of the amortizers, and the pistons we connect to the base of the car, but the piston and the amortizer cant be connected like this, so i connected the end of a amortizer to a servo motor(instead of a piston), and that servo motor will be connected to the base.
And i will not use two motors like i mentioned earlier because i came up to this problem. Yes it would be better and nicer but it just isnt worth it, it is better just to find a stronger motor.
So now we have this:

![Image](https://github.com/user-attachments/assets/17e0f79f-ba1e-46d9-a853-59b16b50e56f)

OK, now we have a idea of how the back wheels will work

And now lets get to front wheels and the main wheel(left,right).

I am a few hours is figuring out how the steering should work, and no doubt this is the hardest part.
I will be using these:

<img width="602" height="597" alt="Image" src="https://github.com/user-attachments/assets/47b51dc2-7f08-41ee-808c-3fcfba242cbe" />

 So the design will look like this:
 
<img width="1600" height="576" alt="Image" src="https://github.com/user-attachments/assets/c5ba05f7-dc83-45d1-8c36-76721a082644" />

<img width="1122" height="1600" alt="Image" src="https://github.com/user-attachments/assets/9949b921-f074-474e-8434-94eb0db9ab89" />

Lets ugree to something, this sketch is trash. BUT it has the mechanism we need.
Note: I connected the amortizer(and bouncer) to the steering knucle, it is better to connect it to the arm(the long plate), so i will try both ways.

The steering mechanism isnt clearly shown, but this is the same principle used like on the picture below i foud on the internet, picture is below:

<img width="384" height="110" alt="Image" src="https://github.com/user-attachments/assets/34d50403-7859-4537-b55b-5ad31a814349" />

And now we have a idea of how the car mechanism will work!

Now lets make small ajustments to the design so far:

We dont need a antenna for this, we can use the esp32 with a integrated bluetooth antenna. Like this one:

<img width="600" height="568" alt="Image" src="https://github.com/user-attachments/assets/67a27285-c28d-4736-8fc1-d4a4a12d0142" />

Yes the range will be shorter but why do we need over 100m range if at that range you cant even see the rc car. Mabey if i add a camera to it, but that will be for a different time.

Now lets update the circuit diagrams:

<img width="1046" height="506" alt="Image" src="https://github.com/user-attachments/assets/d8ea2ff9-33ed-4d39-90a1-9d4dbdd0a246" />

And design the PCB:


This is the the TX circuit diagram that i will be using, I am making this PCB in easyEDA.com

Now lets se the PCB

<img width="637" height="451" alt="Image" src="https://github.com/user-attachments/assets/a045e032-25ea-4fe5-9c37-72be0863f3cd" />

Great! we made the PCB design. But we are far from over, but for now lets to the RX.

Lets update the circuit diagram:


<img width="1109" height="645" alt="Image" src="https://github.com/user-attachments/assets/bc674269-1721-4dee-aa1b-2098286a8e40" />

<img width="942" height="667" alt="Image" src="https://github.com/user-attachments/assets/e34f7540-a876-471d-b12b-455f00cfe874" />


Now lets do the RX(remote).

This is the updated circuit:

<img width="984" height="556" alt="Image" src="https://github.com/user-attachments/assets/180914a1-754e-4440-af7a-c094c0bb4a2f" />

I will connect the elements with wires because I will later design my lowrider base and see where will I put them. 

Heres the PCB:

<img width="623" height="428" alt="Image" src="https://github.com/user-attachments/assets/864c319e-addb-4c1f-b770-00babfc22d60" />

<img width="630" height="492" alt="Image" src="https://github.com/user-attachments/assets/bda00355-0001-48a8-a942-20d9009b2ec6" />

<img width="646" height="458" alt="Image" src="https://github.com/user-attachments/assets/def5ec60-6d2f-43f2-b6c1-25f2da691d69" />



For the main motor circuit we will use BTS7960 H bridge module insead of building my own(cheaper,better, faster), which is often used in rc cars.

<img width="495" height="443" alt="Image" src="https://github.com/user-attachments/assets/0c798c07-094d-42ba-b1c5-018932c3edda" />


So far so good! Now lets finnish the design of the TX(remote):

We will use a lithium 3.7V battery to power the TX, with a charging module.
For the TX we need:
  *ESP32-DevKitC
  *Our TX PCB
  *Battery charging module(type C)
  *3.7V lithium battery
  (without a 3d printer and a soldering iron this is impossible)
(i will put everything we need list in a different code)


Now lets finnish the RX(the car):

We will use a 7.4V lithium battery, and also we will add a charging module for it.
7.4V goes to the 5 servos and the main motor, but we will add a converter to put a smaller voltage to the ESP.
This is what we need for this:
For the eletrical part:
   *ESP32-DevKitC
   *Our RX PCB
   *7.4V lithium battery
   *2N2222(NPN) transistor
   *1k resistor
   *300ohm or 2x150ohm resistor
   *2x white 5mm LEDS
   *Small speaker
   *PAM8403(audio amplifier)
   *540 40T brushed motor
   *BTS7960(H bridge for the main motor)
   *5x 20kg DS3218 High Torque Digital Servo Motor(one for the wheel and four for the BOUNCERS!)

For the mechanical part:
   *Knuckle C Hubs Suspension Arms CVD Shaft(for the front wheels)
   *Axle Differential Mechanism of RC Cars(for the back wheels)
   *Drive Shaft
   *Wheel hubs
   *Ball bearings(for the wheel hubs)
   *Adjustable Link Rods
   *Four wheels(i might buy them or make them)

  




