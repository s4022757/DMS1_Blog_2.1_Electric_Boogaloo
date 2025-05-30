---
title: Assignment 3
published_at: 2025-05-25
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

New we're in the belly of the beast. Let's start with the basics and create a new 3D GameObject.

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

![Into orbit](week7/Solar/movement1.png)

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

