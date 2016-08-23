---
layout: post
title: "RF Craft to RailCraft"
description: ""
category: 
tags: [RailCraft,Minecraft,MSI,Coding,Python,mcpi,RF-Craft]
---
{% include JB/setup %}

<img src="/images/RF-RailCraft.gif" width="600">

I'll be leading on a series of workshops at <a href="http://msimanchester.org.uk/whats-on/activity/makefest-2016">MSIMakeFest</a> on August 20th & 21st using the Raspberry Pi version of Minecraft and Martin O'Hanlon's `mcpi` API to celebrate the first railway journeys between Liverpool and Manchester.

Over the past few years a community of makers, developers, artists, designers, gamers and educators have been exploring interesting ways to bring the 'real world' into Minecraft, which I've been calling **The Minecraft Of Things**. Some of the most interesting work has used the Raspberry Pi version of the game and the marvelous <a href="https://www.python.org/">python</a> Minecraft API, `mcpi` distributed and supported by some great tutorials and code written by Martin
O'Hanlon on his <a href="http://www.stuffaboutcode.com/">website</a> and in his <a href="http//eu.wiley.com/WileyCDA/WileyTitle/productCd-111894691X,descCd-buy.html">book</a> he wrote with <a href="http://blog.whaleygeek.co.uk/about-me/">David Whale</a>. 

For MakeFest ew've made a working train you can control with a minecraft Radio messaging system, <a href="https://github.com/cheapjack/RF-Craft">RF-Craft</a>, to work with some special laser-cut buttons and augmented oil lamps from the **MSI handling collection**. Then there's a carriage building game for 3 players and a python model of a level crossing. See the MSI website for details of how to take part. All this is within view of a RailCraft/TrainCraft Minecraft Mod made by **Mr
Brutal** a well known minecraft modder who has modelled an amazing world inspired by the earliest Liverpool to Manchester rail journeys.

I've been working on a few projects that use mcpi like this, to share ideas around the Internet Of Things and basic programming. There is a lot of momentum to **teach kids code** but I prefer to think of what people are doing in the maker/coding/education world as a sort of **data literacy**. It would be unrealistic to think that young people taking part in this sort of thing will be using python 2.7/3 in their jobs of the future; but doing the sort of level of programming the Raspberry Pi and `mcpi` community gets you used to some basic ideas in computer science. Most importantly playing with python in the context of Minecraft gives you a framework to do the most useful kind of learning: learning by design & experimentation, in a language (Minecraft) that you are comfortable with. 

Perhaps the most important thing I think is useful to anything is designing a solution to a set of problems or questions: set yourself the problem of making a train that behaves like a real train from 1m virtual blocks and it takes a fair bit of creative thinking to make a solution you are happy with.

I've tried to do this with a few projects all of which I've made open source and distributed on github, a code sharing platform <a href="https://github.com/cheapjack/Cloudmaker">Cloudmaker</a>, <a href="https://github.com/cheapjack/RF-Craft">RF-Craft</a>, <a href="http://cheapjack.github.io/whitcraft/">WhitCraft</a> and <a href="https://github.com/cheapjack/ShrimpCraft">ShrimpCraft</a>.

That's another concept I think learning with Minecraft gets over, and it's something not all adults understand or see the value in:  the concept of sharing knowledge and information in a way that makes sense, is human friendly and well documented. By coding and making you are interacting and communicating with the world but in a more deeper way than, say watching a video or sharing an image or sending a text based message on social media.   

All the content of the workshops at MSIMakeFest2016 is based on other people's work and knowledge in the same way that Stephenson's Rocket or a particular rail gauge on some track does not belong to just one engineer. Yes there are famous talented engineers who innovate and are first at something but often they implement and build on the work of people before them; Einstein needed Maxwell and Tim Berners Lee needed the <a href="https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force">IEFC</a> to build <a href="https://en.wikipedia.org/wiki/Transmission_Control_Protocol">TCP</a> 

There's a bit of a myth that Minecraft is a universal accessible world of creativity and in some ways it **is** but this creativity is in the diversity of the way you can play/hack/modify/customise/mod the game. Many of the amazing stuff you see made by modders like Mr Brutal who FACT and MSI commissioned for this year's MSIMakeFest need a bit of work to get running with tools like <a href="http://www.enginehub.org/">Engine Hub</a> and <a href="http://files.minecraftforge.net/">Forge</a> and of course it all depends on whether you're playing on PC/Mac/Linux/XBox/PS4/Android/iOS/RaspberryPi or running Forge/Bukkit/CanaryMod/MinecraftEdu/Pocketmine servers. 

What is awesome about mcpi and the Raspberry Pi version of it is that it takes you back to basics of version v0.1.1 alpha with a minimum of setting up so what modifications you do are limited around using python and mcpi to make your mods programmatically. It is also on cheap hardware with a big community. It means people have to forget how they may play minecraft normally and design something in a familiar yet new way. And that's the other myth of Creativity that it's all about freedom, it's not, it is often the limitations of a medium that drive creativity. 

Come along to MakeFest and learn more, build virtual railway infrastructure and see Mr Brutal and the local Minecraft mapping community's amazing creations!!


## Example Code

Below is some example python code for a <a href="https://www.raspberrypi.org/downloads/">Raspbian</a> Raspberry Pi disk image. There are lot's of resources out there to help you get started with using the Raspberry Pi, so I will leave the internet and the link above to fill you in on that.

To use it you will need to download Martin O'Hanlon's [mcpi code here](https://github.com/martinohanlon/mcpi) and save it to your home folder, `/home/pi`.
You can use the built in Pi `Midori` browser to download it or the commandline:

You can also clone the [RF-Rail-Craft-Repo](https://github.com/cheapjack/RF-Rail-Craft) repo and you can run a version of the installation yourself

Open a Terminal on your Pi (it's in accessories) and type

Type `pi$ ls` and it will list your files in your home folder
In the following, just type the text after the `pi$ ` part, thats just the command line prompt and shows you who you are logged in as, in this case, `/home`.

download Martin's [mcpi code](https://github.com/martinohanlon/mcpi) with `git` if you use it or `wget` and save it to your home folder, `/home/pi` and unzip it.

`pi$ wget https://github.com/martinohanlon/mcpi/archive/master.zip`

You might need to install `unzip`
Do that with `pi$ sudo apt-get install unzip`
Once it's installed unzip with `pi$ unzip master.zip`

You should now have a `mcpi-master` or `mcpi-master.zip` folder so unzip it and go inside that folder

`pi$ cd mcpi-master`

Then download the file below with the command line on your Pi with 

`wget http://soundnetwork.org.uk/misc/cheapjack/carriage.py.zip`
or from this link <a href="http://soundnetwork.org.uk/misc/cheapjack/carriage.py.zip">here</a>

unzip `pi$ unzip carriage.py.zip`

Or you can get it straight from git `pi$ wget https://github.com/cheapjack/RF-Rail-Craft/blob/master/carriage.py`

**Make sure the `carriage.py` is in the same folder as mcpi so your programme can find it when it imports the module**

Now open Minecraft in the Pi Main Menu and go to a new world and find where you want to build some carriages, you may want to clear a space 

Now go back to your Terminal and Run your python code with 
`python carriage.py`

If all goes well and the mcpi folder you downloaded is in the same place as your carriage.py code, you will see the message `"Hello Minecraft World!"` followed by some other messages in the game console.

Yay! now try hack the `CarriageTemplate` function or use it to make more carriage chassis and start building some classic rolling stock through the ages! Have a look at <a href="mikes.railhistory.railfan.net/r155.html">Mike's Engineering Wonders Site</a> for some historical tips.

If you get stuck come to MSIMakeFest2016 and we will help try you out!

```
#!/usr/python

# import mcpi, you will need the mcpi directory to be local to the carriage.py ie in the same directory.

from mcpi import minecraft

# connect to the game locally, ie on your pi

mc = minecraft.Minecraft.create()

#Define a Carriage function

def CarriageTemplate(xpos, ypos, zpos, length, width, numberOfCarriages, material, materialType):
    length = length + 1
    # main carriage chassis
    for i in range(1,numberOfCarriages + 1):
        mc.setBlocks(xpos + (i*length) + 1, ypos + 1, zpos, (xpos+(i*length)) + length + 1, ypos + 1, zpos + width, material, materialType)
        #Make gaps
        mc.setBlocks(xpos + (i*length) + length, ypos + 1, zpos, xpos + (i*length) + length, ypos + 1, zpos + width, 0)
        # Make 4 wheels
        mc.setBlock(xpos + (i*length) + 2, ypos, zpos - 1, 57)
        mc.setBlock(xpos + (i*length) + length - 2, ypos, zpos - 1, 57)
        mc.setBlock(xpos + (i*length) + 2, ypos, zpos + (width + 1), 57)
        mc.setBlock(xpos + (i*length) + length - 2, ypos, zpos + (width + 1), 57)

# Send a message to minecraft console
mc.postToChat("Hello Minecraft World!")
mc.postToChat("We need rolling stock!")
mc.postToChat("Lets get building carriages!")
playerTilePos = mc.player.getTilePos()
mc.postToChat("TilePos is " + str(playerTilePos))

# Remember our Carriage function above needs the values Starting xpos, ypos, zpos, length of carriage, width of carriage, numberOfCarriages, blockmaterial, blockmaterialType.

# Call our Carriage Function with all the parameters we want
CarriageTemplate(playerTilePos.x + 1, playerTilePos.y, playerTilePos.z + 1, 6, 2, 4, 42, 0)

#print to minecraft console so we know what we did
mc.postToChat("Building Carriage chassis!")

```

Follow the action at MakeFest on twitter at <a href="https://twitter.com/hashtag/msimakefest">#MSIMakeFest</a>
