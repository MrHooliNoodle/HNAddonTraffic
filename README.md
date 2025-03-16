# hn_addontraffic
This is a simple resource where you can edit the NPCs and Vehicle traffic models for FiveM with OpenIV.
THIS IS A FREE AND OPEN SOURCE, IF YOU PAID FOR THIS, YOU WERE SCAMMED.

# How do I edit this file?
To change a spawn, you need to change the name of the item in popgroups.ymt, and you will need OpenIV to view the code and edit it,
The fastest way to do this is to add the popgroups.ymt anywhere easily accessible in your GTA 5 mods folder, turn on edit mode in OpenIV, Right-click popgroups.ymt and select edit,
Copy the code into Visual Studio Code or whatever you use for easier browsing.

# What should I edit?
For vehicles, there are many groups based on where they are located in the city.
Low end cars typically spawn in the south side of the city.
Let's change these for an example.
We will start with low end cars.

Search for <Name>VEH_POOR</Name>

Under "models" you will see each car in that group. This is the Asea.
```
<Item>
          <Name>asea</Name>
          <Variations type="NULL"/>
        </Item>
```
Simply type the model name of the car you wish to replace this with.
Say we want this to be the Cheburek, we'll change it to this:
```
<Item>
          <Name>cheburek</Name>
          <Variations type="NULL"/>
        </Item>
```

Do this for all of the following models until you see the line "models" again, you'll know it is the bottom when you see this:   <flags>"POPGROUP_SCENARIO POPGROUP_AMBIENT"</flags>
This means you are done with that section. 

EACH GROUP WILL HAVE THIS LINE SO BE CAREFUL THAT YOU AREN'T REPLACING THE WRONG GROUPS.
                                                                                                                               </Item> 


You will notice after this, there is an identical line, but the title has MP in it. (<Name>VEH_POOR_MP</Name>) for example.

Simply copy the above lines that you just edited, from the first "models" under the groupname (in this example, it is <Name>"VEH_POOR"</Name>) all the way down to "models" just before the POPGROUP_SCENARIO mentioned in the line above.

Do this for all groups with whatever vehicles you'd like, except for <Name>VEH_YANKTON</Name> and <Name>VEH_YANKTON_MP</Name>, unless you use north yankton and want traffic there i guess? 

If something doesn't work, simply remove the resource to return the traffic models to default.

# This is very simple and I will not provide much support for this.




