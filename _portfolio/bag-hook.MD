---
title: "Desktop Multipurpose Purse Hook"
excerpt: "A desktop purse, headphone, and key hook set created through generative design."
header:
  image: /assets/img/side-view.JPG
  teaser: /assets/img/bag-hook.JPG
gallery1:
  - image_path: assets/img/top-view.JPG
  - image_path: assets/img/backpack-hook.JPG
  - image_path: assets/img/realworld-ex.jpg
gallery2:
  - image_path: assets/img/gd1.png
  - image_path: assets/img/gd2.png
  - image_path: assets/img/gd3.png
  - image_path: assets/img/gd4.png
  - image_path: assets/img/gd5.png
  - image_path: assets/img/gd6.png
gallery3:
  - image_path: assets/img/preserve-geom.png
  - image_path: assets/img/obstacle-geom.png
---

# Discussion: 

### Part Overview & Application 

I decided to design a desktop bag hook that allows for docking of a purse, over-ear headphones, and a set of keys. It is designed with an office setting in mind with a maximum table thickness of 25 mm (~1”). 
While a small problem, this saves me a bit of real estate on my desk that is typically taken up by my headphones and bag while keeping them readily available to me, as well as allows me to keep my keys at a good reach if there is an emergency. As someone going into a corporate job next year and seeing how many things my coworkers had on their desks, I came to the realization that my bag really couldn’t stay up next to me long term. Between two to three monitors, a handful of medical devices for referencing, and paperwork organizers I knew I’d have to come up with a solution to keep my desk clear. This allows me to prioritize the things I actually need on my desk while making sure that I don’t ruin my bag or misplace my things.

### Preserve and Obstacle Geometry 

The preserve geometries in my design were the desktop mount and the three hooks: keys, headphones, and purse. The goal of this was to ensure that the hooks remained the right size and all connected through the tree made by generative design. The fixed preserve geometry was the face of the mounting plate that rested on the table. 
Obstacle geometry was iterated throughout the process. At first, I created three obstacles where the items would sit on their hooks. After my first iteration, I realized that there needed to be an obstacle of where the table would be underneath the mount, which I decided to make 25 mm thick. As I continued iterating the design, I added obstacles around the curve of the hook to ensure that the design left space for things like the keys to slide on and off of the hook. Since these parts created a lot of force on the hooks, the design was attempting to add supports extending from the mounting plate to the hooks, but the extra obstacle geometries ensured that these did not interfere with the use cases.
{% include gallery3 caption="Final Preserve and Obstacle Geometries" %}

### Load Case Application and Structural Constraints 

Firstly, I applied loads onto all the top faces of the hooks to represent the maximum weight that the hook would be expected to endure for each item. To determine the magnitude, I picked the maximum weight I thought each item would have on the hook based on some general research and converting it into Newtons. For the purse, I imagined on my busiest day what would be in it? Likely a laptop, iPad, water bottle, and snacks. For headphones, I added the weight of my headphones plus their charging case. Lastly for my keys, I found the average weight of a key fob and then added the weight of my wallet as well since I have them on the same keychain.
Then, based on the length of the hook I applied a moment to the top face that represented the load being applied at the center of the hook. This represents the downwards bending that the hook will be undergoing since the load is not applied directly at the joint. This was in N m. 
Lastly, I applied shear forces to the top face that represented the force of someone pulling the item up and off of the hook. I assumed that the person was pulling with a force of 5 N on smaller items and 10 N on the purse at an angle of 30° upwards to get it off the hook.
Another I considered applying was someone bumping into the hook, but since I intend to have it hanging in the inside corner of a desk I don’t imagine that as a likely scenario. 
I applied a fixed constraint on the desktop mount in order to ensure that under these loads, the mount would not rotate or slide. Since the face on the table was fixed, no forces were applied. 
In order to test this prototype, all of the items should be placed on it to make sure that it actually holds the proper weight. This would test both the compression forces and the bending moment. Next, the items should be taken off the hook at different speeds and forces to ensure that the safety factor accounted for any anomalies.

| Force Type  | Magnitude | Location                       | Rationale                                                                                                                                                                      |
|-------------|-----------|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compression | 12 N      | Top face of the key hook       | Based on a maximum weight of 2.5 pounds, this is a representation of the normal force of the keys on the hook.                                                                 |
| Compression | 10 N      | Top face of the headphone hook | Based on a maximum weight of 2.2 pounds, this is a representation of the normal force of the keys on the hook.                                                                 |
| Compression | 115 N     | Top face of the purse hook     | Based on a maximum weight of 25 pounds, this is a representation of the normal force of the keys on the hook.                                                                  |
| Moment      | 0.10 N m  | Top face of the key hook       | Based on the maximum weight and distance of 5 mm from the COM to the hook’s stem, this is how much bending the hook would undergo.                                             |
| Moment      | 0.25 N m  | Top face of the headphone hook | Based on the maximum weight and distance of 20 mm from the COM to the hook’s stem, this is how much bending the hook would undergo.                                            |
| Moment      | 1.75 N m  | Top face of the purse hook     | Based on the maximum weight and distance of 15 mm from the COM to the hook’s stem, this is how much bending the hook would undergo.                                            |
| Shear       | 1.50 N    | Top face of the key hook       | Based on someone pulling the keys off of the hook at 30° angle and a force of 5 N, this is the shear it will undergo at the contact points before it is off of the hook.       |
| Shear       | 2.50 N    | Top face of the headphone hook | Based on someone pulling the headphones off of the hook at 30° angle and a force of 5 N, this is the shear it will undergo at the contact points before it is off of the hook. |
| Shear       | 40 N      | Top face of the purse hook     | Based on someone pulling the purse off of the hook at 30° angle and a force of 10 N, this is the shear it will undergo at the contact points before it is off of the hook.     |


### Critique of Generative Design 

I think that generative design can definitely be useful during prototyping. With the general idea of a design and what constraints you have, you could easily come up with many different design options that are likely to fit your needs. This also allows you to be more creative and efficient with how you support a structure. 
A large limitation is that you cannot tell generative design what the part is going to be used for, just the load cases. While this gives a good idea, sometimes I found that the generative design process would build geometry right up until an obstacle geometry that interfered with the use case ever so slightly. While this can usually be rectified by more or larger obstacle geometry, it was a long and iterative process to get it exactly right.
I think that this could be quite useful in mechanical and civil fields, as you can set up all the possible load cases and ways that an object should and should not move. This would also help you to optimize any parts for your purposes and reduce costs and material used. However, in things like chemical processes this may be an added layer of complexity that generative design cannot help with. You can choose the materials you want to build with but since it cannot simulate any long-term processing effects it may not totally understand the needs for working with chemical materials.

# CAD Models:

### Base Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4229bcfc2385b32e8?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

### Generated Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a41fab5114fe1b8b58?mode=embed" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
 
# Supplemental Images:
{% include gallery3 caption="Iterations of the Generative Designs" %}
{% include gallery1 caption="Final Prototype" %}
