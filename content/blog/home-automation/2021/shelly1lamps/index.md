---
title: "Shelly 1 Lamps"
date: 2021-01-05T09:10:57+02:00
draft: false
tags: ["shelly1", "zwave"]
author: "Fletcher Kelly"

---

## Use Case  

I had been using a WiFi bulb with the lamps to control the lighting, this was working very well. The lights would come at set times and this was great. I even have automation around presence detection and the lights would NOT come on if the house was NOT oocupied. However, them it comes to actual sleep, my wife was unable to switch off the lamp with causing the WiFi bulb to be dropped from the network and then breaking the automation. This was NO good.

### Solution 1

I also use ZWave around the house and decided to use a WallMote with Node-Red to map buttons to control the above lights, this solution was better but still lacked the local control. My wife was happier but not yet happy.  

{{< figure src="/images/2021/shelly1Lamps/wallmote.jpg" alt="Wallmote" >}}

### Solution 2

So I just recently finished building my Shelly1 based lamps. I simply added the Shelly into the wiring of the lamp. I use the term "simply" loosely. This was an actually a bit of a process as the lamp needed to modified in order for this to work. I added an electrical junction box to the bottom of the lamp and then added the required wiring into the box and added a nice simple external switch.

I followed this video - [shelly 1 how to wire it](https://www.youtube.com/watch?v=CtHo1lIo4_Q)  

<!-- {{< figure src="/images/2021/shelly1Lamps/shellyLamp.jpg" title="Shelly in Lamp" class="left" >}} -->
{{< figure src="/images/2021/shelly1Lamps/shellyLamp.jpg" alt="Shelly in Lamp" >}}

## Takeaway

Always be focused on what you are trying to achieve, home automation should enhance your life, not add challenges.