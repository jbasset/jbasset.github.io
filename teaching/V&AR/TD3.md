---

layout: course
title: A&VR TD3
---

# TD3 Leap Motion

## Step 0 - Ultraleap Tracking



## Step 1 - Installing Leap Motion in Unity

Open the Roll-a-ball project you developped in the previous practical works.

## Step 2 - Roll-a-ball by hand

The goal of this section is to control the ball by pointing at the position you want the ball to go.

TODO gif

### Setting up Leap Motion in Roll-a-ball

Follow the instruction at <a href="https://docs.ultraleap.com/xr-and-tabletop/xr/unity/getting-started/index.html#set-up-hand-tracking-in-unity" target="_blank">this adress</a> (from Set up hand tracking in Unity) to add ultraleap to your project.

Add the example content and open the Capsule Hands scene to test that hand tracking works.

Open the Physical hands Object Interaction scene and play it. Have each member of the group try the scene for a short time to familiarize yourselves with the leap motion.

### Adding hands to Roll-a-ball

Go back to the Roll-a-ball scene.

Add a desktop XR Leap Motion Service Provider to the scene. You can find it in ```Ultraleap > Tracking > Service Provider (desktop)```. From the same toolbar, add hands model as a child to the service provider. Ultraleap proposes several hand types, choose whichever you prefer.

Depending on the scale of your Roll-a-ball scene, the hands might be much too small or much too big. We thus need to scale the hands in order to be able to move the hand confortably on the whole size of your arena. You can either:
- scale the hands by changing uniformely the scale of the Service Provider's transform. However, some hand models will not react well to being scaled up or down and will be distorted.
- to avoid that, you can instead create an empty object, add all elements of your Roll-a-ball but the Service Provider as children, and scale up or down this empty to scale your scene.

![](TD3/hand_scale.gif)

### Getting the position of a finger

### Moving the ball

## Step 3 - Let's cheat! Grabbing the ball

## Step 4 - To go further

Think of new interactions methods using the leap motion, and try to implement it! For example, you could:
- make the ball jump when you close a hand