# Using Timeline in Cinder #


## Introduction ##

Cinder provides a tweening engine called Timeline for creating full featured animations. Timeline has been designed to easily animate variables over time without having to keep track of them. Flash developers familiar with [Tween Lite](http://www.greensock.com/tweenlite/) can use this as a somewhat similar context when working with Timeline. Those familiar with After Effects (AE) can use this as a frame of reference to visualize how Timeline is used.

## Basic Usage ##

The master class called Timeline manages a collection of *Anims*. Anims are variables that can be *tweened* or animated over time. The app <!-- the app class, namespace, project --> always contains a master timeline which is accessed similar to the way you would use console().

Before anything can be done first make sure timeline is included in your project:
<pre class="fragment">
#include "cinder/Timeline.h"
</pre>

After you've included Timeline see below for a very basic example using it:

<pre class="fragment">
	Anim<float> radius;
	radius = 0.0f;
	timeline().apply( &radius, 10.0f, 1.5f, EaseOutCubic() );

	<!-- maybe show how this is represented in the draw function as well -->
	<img src="#" alt="Tween code above in svg and js" width="450" height="250">
</pre>

In the example above the variable *radius* is of Anim type. The value is then initialized to 0.0 as if you <!-- almost -->  you were actually using a float. On the master timeline we use the the apply function to tween the radius to a final value of 10.0 over 1.5 seconds using the EaseOutCubic function.  

It is important to note that the master timeline's apply function is accepting a *reference* to the Anim radius along with the easing function used. The easing function is basically the equation that is applied to your Anim variable over time. This is described in more detail in the following section below.

## Ease Functions ##

In the example

* Will show the basic easing equations and how to use them 
* Display images/svg javascript of each easing equation 
	* take from cinder example using Penner easing equations 

## Callbacks ##

## Cues ##

## Looping ##

### Standard Looping ###

### Looping with cues ###

## Advanced Usage ##

### Using Step or StepTo ###

### Nest Timelines ###

### Create Timeline Items ###

#### Auto Remove ####

### Ping-ponging ###

### Using TweenRef ###

### Using Timeline::applyPtr ###

### Using Timeline::appendToPtr ###

### Creating a timeline on a seperate thread ###

### Creating nonrealtime animations ###