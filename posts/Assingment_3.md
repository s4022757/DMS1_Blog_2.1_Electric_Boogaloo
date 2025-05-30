---
title: Assignment 3
published_at: 2025-05-30
snippet: All lumped together context for A3!
---

# Week 7 - Session 1

In today's class we were intoduced to the next medium we will be working on: 3D Environments

First we unpacked the upcoming assignment 3, and there were some key changes to the assignment brief compared to last time I attended the unit.

## In class

So let's get Unity up and running.

Since last I used it, Unity has updated to v6. How exciting.

![Unity Install](week7/Install/Unity6installcomplete.png)

Now that's installed, lets start a new project using the latest 3D core with inbuilt render pipeline.

![New Project](week7/Install/newproject.png)

Now we're in the belly of the beast. Let's start with the basics and create a new 3D GameObject.

![Create Shape](week7/Install/shapesget.png)

*sphericool*

The shape is nice, but it sure ain't pretty. Let's fix that.

Thomas guided us over to the [Solar System Scopes](https://www.solarsystemscope.com/) website, who provide some high quality textures ready to go.

Let's apply one of them to our new sphere. First, we import the image into Unity. This becomes a texture, but to apply it to a GameObject, we'll new to create a material with an albedo set to the new texture file.

![Apply Texture](week7/Install/textureapply.png)

Looks great! Oh, but this is just the begining.

## Homework

### Solar System Scope

Let's expand on the new project we made in class. There were many more textures available on that website so let's download and import them all to get used to Unity.

Even though the shape looks nice with the new texture, the background it sits on is not so much. Let's fix that.

There was a Milky Way texture on the site which will work nicely.

When creating a material, we have the option to change shaders. Let's import the Milky Way texture, create a new material with it, and switch its shader from Default to Skybox.

![skybox](week7/Solar/skybox.png)

That looks much better.

That said, our sun and moon is looking rather lonely. Let's now create a sphere for all of the textures that we downloaded earlier. Then we'll create a material for each of them and apply them to each new sphere.

![All the planets of the solar system](week7/Solar/allplanets.png)

They're all there! [^1]*sorry Pluto*

Now with all the planets, they don't quite represent their real counterpart's actual size. Let's look up the sizes of the real planets and change the scale of our spheres to match a somewhat relative representation of this.

![Planets to scale](week7/Solar/resize1.png)

That's slightly more realistic. Although, the real scale of the planets would make it very difficult to make out the beautiful textures we went to the effort of implementing. Let's adjust the scales down some.

![Planets almost to scale](week7/Solar/resize2.png)

That looks great. Mercury is still tiny, but thems just the breaks. 

That said, the planets are all spaced uniform which is not a very accurate depiction of their counter parts. Let's look up the real planet spacings and squash them to a reasonable scale for our purposes.

![spaced out](week7/Solar/spacedout.png)

Looks great. Now that we're *spaced out*, lets see if we can get the planets moving.

How do we do this? Code!

Luckily Unity allows the creation of scripts easily from a context menu. A simple right click of the project heirarchy and we're off to the races. Once named, the inspector of our new script includes a button taking us straight to editing in Visual Studio Code. 

Let's consult the Unity user manual and forums, and wizard up a movement script.

If my abilities don't decieve that should be the ticket. That said, with some of our small planets and a particularly dark skybox, it'll be hard to make out the movement. Before testing, let's implement a trail renderer effect on all of our planets, and attatch and configure our new script.

![Into orbit](week7/Solar/movement.png)

We've got the planets into orbit. Unfortunately, they're all orbiting around the sun at the same rate. That's not very realistic and looks quite inorganic. Let's look up the length of each real counterpart planet's year and adjust the orbit rate perameter in the script of each planet.

Speaking of orbits, the planets also rotate. Let's quickly do the same process for rotation and implement a script before testing.

![Complete Solar System](week7/Solar/movement2.png)

It's all working and looking great. I'd say we've learnt a bunch about using Unity, so let's get on with the Assignment and have a read of the brief.

It looks like we'll need to publish a WebGL build of our completed assignment. Since we've now completed our solar system, let's try doing this. 

Success! You can play [my Unity Solar System](https://play.unity.com/en/games/9ba9e586-a676-4e46-acc3-13dcbbe233a3/webgl-builds) here.


### Brainstorm

It's time to develop some ideas for my project.

I've been asked to represent "a physical, emotional, intellectual, or geographical transformation that you have undergone."

Many things come to mind. That said, I have remained physically and geographically similar in recent memory. While my intellect has potentially been growing, I'm not so sure how I would represent this. 

Emotional transformation seems to be an interesting one. My emotional growth is certainly at a different state compared to when I last under took this course and has been on my mind due to what has now become a long term relationship.

Let's jump over to an Obsidian Canvas and expand on emotional transformation into a brainstorm.

![Emotional Brainstorm](week7/brainstorm.png)

There is some colour coding here to help decipher. Seen in yellow & purple are potential ideas for the encounters I must design for the assignment brief. In blue are some of the navigational elements to implement. Surrounding are other ideas for elements to include.

### Sketch map

Following the brainstorm session, let's sketch up some rough top down maps with ye olde pen & paper.

![Encounter 1](week7/sketch/Encounter1.png)

![Encounter 2](week7/sketch/Encounter2.png)

![Encounter 3+4](week7/sketch/Encounter3+4.png)

Looks a little *sketchy* but we can develop this further.

### Asset list

With that complete, let's have a think about what assets we will need to make the enviroment. Consulting my brainstorm and my ability to riff, I put this her list together.

#### 3D assets
- Statue of Liberty
- Skyscrapers
- Street lamp
- Male humanoid
- Female humanoid
- Archway
- Park Bench
- Butterfly
- Trees/plants
- Mountains
- Flowers
- Moon

#### Sounds
- Cityscape
- Stage lights switch
- Street lamp buzz
- Swoosh
- Waves crashing
- distorted nostalgic music
- distorted nursery rhymes
- Chaotic noise
- Crowded laughs
- Flapping wings
- Cute laughs
- Chirping insects / birds

#### Textures
- Brick
- Concrete
- Pavement
- Oxidised bronze
- Fire
- Grass
- Rock
- Water
- Wood
- Metal
- Grass with flowers
- Moon surface

Some of these are possible to make in Unity, but others we might have to look elssewhere.


# Week 7 - Session 2

In the next session we looked at designing 3D space. There were some interesting points about how  design choices in this medium affects the audience in different ways. I'll factor this into my draft.

## Character Controller

On Canvas we were supplied with a character controller template prefab. Let's start a new Unity project so we can play around with it.

First, our character will need a surface to walk on. 

Let's create a terrain.

![Terrain](week7/s2/terrain.png)

That's a good start. Let's now bring in the controller prefab.

![Character Controller](week7/s2/charcont.png)

We should run the build and see how it goes. First though, the terrain is a little flat & boring. Let's make it 3 dimensional.

![Mountain](week7/s2/mountain.png)

That gives us something to look at. Let's run the build and see this new world from the perspective our our character.

![Point of View](week7/s2/mountainPOV.png)

There camera asset in the character controler sure works, but let's see if the movement controls are working correctly too.

![Changed POV](week7/s2/mountainPOV2.png)

Alright great. We have now become the god of a livng being! Or an avatar at the very least.

Like Sisyphus, our character's destiny is to climb.

![Summit](week7/s2/terrainpaint.png)

As much as I am a fickle god, the summit was challenging. If I am to empathise with my upcoming audience, they may not like sisyphean condemnation. Let's explore the terrain brush tools to smooth out this here mountain, and create a plateau to serve as a lookout.

![Lookout](week7/s2/lookout.png)

Looks... looks kinda plain from up there. Let's bring in some more life through textures!

![Terrain Textures](week7/s2/texturepaint.png)

Starting to look better.

## Perspective

After this, we continued on with the lecture and learnt about perspective.

We discussed how we may be able to extend the functionality of Unity by playing around with perspective. Reminiscent of Anamorphic art, if we place objects in certain orients, when the player character views these objects from a certain angle, we can represent form more complicated than possible with the basic 3D gameobjects available in the vanilla Unity editor.

Let's create some shapes and play around with scale and rotation to make somethig interesting.

![Playing with perspective](week7/s2/perspective.png)

This is quite finicky, we'll have to continue on after class.

## Homework

Let's continue on with our anamorphic scene in Unity.

First, we'll find a reference image to recreate with 3D forms in unity.

This will work:

![Reference Image](week7/s2/hw/Reference.png)

I'll continue on and recreate the image with cubes of various sizes, rotations and distances from the character controller. Luckily there is a way to have the POV of the character controller displayed in a window alongside the editor.

Here is the completed recreation of the reference image:

![Recreation](week7/s2/hw/recreation.png)

Well its not great, but it's almost there. While this appears this way from the starting perspective, this is the configuration from another angle:

![Alternate angle](week7/s2/hw/wrongangle.png)

This could be a cool way to implement an encounter in my assignment. Have game objects that appear insignificant at first, but as the player progresses, they reveal another configuration which paints another picture.

### Greybox Prototype

Now that we have developed our skills, lets transform our sketches into 3D basic forms.

Starting with the first scene:

![scene 1](week7/greybox/scene1-1.png)
The basic forms

![scene 1](week7/greybox/scene1-2.png)
Painting a road into the texture.

Not sure how much I like that. Let's try an alternative method using EasyRoads3D

![scene 1](week7/greybox/scene1-3.png)
That's better


Alright, now for scene two:

![scene 2](week7/greybox/scene2-1.png)
Starting position

![scene 2](week7/greybox/scene2-2.png)
Starting perspective

![scene 2](week7/greybox/scene2-3.png)
The destination

![scene 2](week7/greybox/scene2-4.png)
Bird's eye view of whole scene

Next, scene 3:

![scene 3](week7/greybox/scene3-1.png)
Starting perspective

![scene 3](week7/greybox/scene3-2.png)
Bird's eye view of whole scene

![scene 3](week7/greybox/scene3-3.png)
Full context of staircase

![scene 3](week7/greybox/scene3-4.png)
Final destination 

![scene 3](week7/greybox/scene3-5.png)
Looming moon

I thought at first the it would be possible to extend this scene further, although it does not seem possible for me to have a tunnel into another area that runs through the staircase. The object meshes available in the vanilla unity editor are somewhat limited in the way.

To solve we will create another scene:

![scene 4](week7/greybox/scene4-1.png)
Bird's eye view of the scene

![scene 4](week7/greybox/scene4-2.png)
Inside the tunnel

![scene 4](week7/greybox/scene4-3.png)
Exiting the tunnel

That's looking pretty good, now to beautify it with assets.

# Week 8 - Session 1

In today's class we looked at guiding navigation. Thomas gave us a lecture about wayfinding and techniques to guide movement through 3D space

## Wayfinding activity

Thomas group us up and gave us a destination.

Without using Google Maps and only using what we observe in the environment, we were asked to navigate to Assembly, a café in Carlton.

None of us had been there before, so we started planning our route before setting out. We decided on our path and noted the road names we should follow, and landmarks to look out for to orient.

We then set out from Building 9 and went to Victoria St. We were looking for the corner of Victoria and Lygon Streets

![Victoria & Lygon](week7/wayfinding/victoriast.jpeg)

Found it. Let's continue towards Lygon.


![way](week7/wayfinding/mapsign.jpeg)

As we went to cross the street, we found this helpful sign - map included. On we go.


![way](week7/wayfinding/icon.jpeg)

To safely cross the street, we had to press the pedestrian crossing signal. What's this? An Icon! How helpful that it is pointing us towards our destination. Onwards!


Along our path we encounter an obstacle.

![way](week7/wayfinding/obstacle.jpeg)

We'll have to use reasoning and problem solving to continue. 

An then we spotted assurance.

![way](week7/wayfinding/park.jpeg)

We knew we were on the correct path, this park was a landmark that we learnt would be along the correct path. Onwards!

Looking around we then spotted the next signifier.

![way](week7/wayfinding/pelhamst.jpeg)

This is the street we needed to find which we were to turn off Lygon. Onwards!

Then, almost missing it but looking to our left, we spotted another good sign.

![way](week7/wayfinding/espressodecal.jpeg)

Mmm coffee, could this be the place?

![way](week7/wayfinding/foundit.jpg)

We found it! 

While we're here we may as well indulge in a taste of caffiene.

# Fin

That's about all the development evidence I got through. Will make sure to work on improving documenting process in future.

# Assignment 3 Notes

## Statement

This 3D environment depicts the emotional transformation I have experienced in my life. There are a number of encounters that I have created which represent the following:

- My early childhood in New York City and tragedy in the family
- Reconnecting with my roots back in Australia saying goodbye 
- Struggling downwards through grief to find inspiration at rock bottom
- Marching on through elongated depression
- Emergence into the rekindling of love into pursuit of dreams


## Credits

### 3D Assets

- Brick wall/fence for park or garden by sketchfab user ironmania2004 under Creative Commons Attribution https://sketchfab.com/3d-models/brick-wallfence-for-park-or-garden-082bd8dff6d540cd816d80a26a29465d

- Butterfly animated butterflies Free 3D model by cgtrader user Amar-P under Royalty Free No Ai License https://www.cgtrader.com/free-3d-models/animals/insect/butterfly-47f7781e-8338-4154-9dd5-3ec1d73accb6

- Man in Suit figure generated using Tencent's HunYuan3D

- Phonograph figure generated using Tencent's HunYuan3D

- Rusty Streetlight by sketchfab user Barbodoji under Creative Commons Attribution https://sketchfab.com/3d-models/rusty-streetlight-d75f8d8a26054e3584f55eb07644801a

- Statue Of Liberty by sketchfab user Gravity Jack under Creative Commons Attribution https://sketchfab.com/3d-models/statue-of-liberty-84094e8d5e724b5c882cf576ca12e44e

- Woman in Suit figure generated using Tencent's HunYuan3D

### Sounds

- Beach - close, waves by FilmCow under FilmCow Royalty Free SFX Library License

- car horn by freesound user keweldog under Creative Commons Zero https://freesound.org/people/keweldog/sounds/182474/

- Ceramic statue breaking 3 by FilmCow under FilmCow Royalty Free SFX Library License

- D2_kidslaughing by freesound user Iamgiorgio under Creative Commons Zero https://freesound.org/people/Iamgiorgio/sounds/371342/

- HeartBeatNormal S08ER.241 from WavFX in Pro Sound Effects - Blastwave FX https://library-prosoundeffects-com.ap1.proxy.openathens.net/track/936140

- Horror Sound: Dark Ambient by pixabay user AlesiaDavina under Pixabay Content License https://pixabay.com/sound-effects/horror-sound-dark-ambient-189961/

- Hymnal ascent by freesound user Bigvegie under Creative Commons 0 https://freesound.org/people/Bigvegie/sounds/554159/

- Lights flicker On by freesound user mmaruska under Creative Commons Zero https://freesound.org/people/mmaruska/sounds/232447/

- London Atmos VST pack recordings via LABS by Spitfire Audio

- nursery rhyme by freesound user arnaud coutancier under Creative Commons Attribution Non-Commerical https://freesound.org/people/arnaud%20coutancier/sounds/369190/

- Ominus machine sound by freesound user tonant under Creative Commons Zero https://freesound.org/people/tonant/sounds/255532/

- spotlight stereo by freesound user reidmangan under Creative Commons Zero https://freesound.org/people/reidmangan/sounds/49023/

- Summer Meadow by freesound user baryy under Creative Commons Zero https://freesound.org/people/baryy/sounds/409143/

- WaHi siren to loop by freesound user chripei under Creative Commons Zero https://freesound.org/people/chripei/sounds/393666/

- Whooshy puff by freesound user spendoza under Creative Commons Attribution Non-Commercial https://freesound.org/people/Speedenza/sounds/168109/
