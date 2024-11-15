# assignment1 All in one

![assignment one](https://github.com/user-attachments/assets/07e2c0f9-d101-4b44-b0b9-484df276c3b8)

<h3>Task one :Using timelines to effect rotation</h3>

![assignment one day night cycle timeline](https://github.com/user-attachments/assets/f3d5e83d-a319-475f-b553-a0676f69673e)

Added the night-day time cycle using two directional lights, and timelines to affect the light's rotation.

Added the control system to the sun, the user can now control the timeline by pausing, playing or reversing the animation liinked to the sun rotation.

These are set up as follows:

Spacebar = Pause 2: Left Arrow = Reverse 3: Right Arrow: Play

![assignment one event graph sunmoon](https://github.com/user-attachments/assets/6efd0d13-0440-49d9-aea3-b34f3207b9fa)

<h4>How to do</h4>

<p> Add a Directional Light: This will act as the sun. 
Duplicate the Directional Light: Name it "MoonLight".


Next, I need a Blueprint that will manage my sun and moon rotation using a Timeline.

Add Variables: Add two variables for the sun and moon:
SunLight (of type Directional Light)
MoonLight (of type Directional Light)

Add a Timeline Component: Click ‘Add Component’ and search for "Timeline". Name it "SunMoonTimeline".
Double-click on the Timeline component
In the Timeline editor, add two float track.

Rename track one SunRotation.
Rename track two MoonRotation.

Set the length of the Timeline: Adjust the total length to synchronize with your desired day-night cycle, I want it to be 15 seconds long a complete cycle.

Add Keyframes: Set keyframes to set rotation angles for the sun and moon over a specified time:

<ul>
  <li>Sun
Time 0s: Value at 0.0 (Sun at its highest point).

Time 15s: Value at 360.0 (Sun completes a full rotation).
</li>

<li> Moon
Time 0s: Value at 360 (Moon would rotate the other way).

Time 15s: Value at 0.</li>
</ul>

Setting Up the Blueprint Logic

Back in the Event Graph: Use the "Event BeginPlay" to start the Timeline.

For Sun: Connect the output from the Timeline - sun rotation to Y axis of Set Actor Rotation.
For Moon: Use a separate Set Actor Rotation connected to Rotation Y + Moon Timeline Output.

</p>

<h3>Task Two: Shot Explosion</h3>

<img width="1383" alt="assignment one event graph bp shot" src="https://github.com/user-attachments/assets/0fe5165c-dc24-423a-9cdc-4bc3bc44604d">  
<img width="1339" alt="assignment one event graph" src="https://github.com/user-attachments/assets/75442fcb-f5e5-4406-b967-a6bc333707b1">

<p>Created a shot explosion effect that activates when the ENTER key is pressed</p>

<h3>Task Four: Collisions

  <img width="1379" alt="assignment one event graph sphere" src="https://github.com/user-attachments/assets/c0c89f93-b1e5-4a49-9b5b-1e7be884a7dc">

<p>Turned on Simulation Generates Hit Event on Sphere. Cubes gets destroyed when the Sphere collides with it</p>

  ![paddlebp](https://github.com/user-attachments/assets/4627f971-4e9a-499b-9295-e93372bd3514)
  
<p>Added a rotating paddle that destroys sphere.

Reference: Collisions and Physics with Blueprints in UE https://www.youtube.com/watch?v=by31O0Vc3cY
</p>


<h3>Glowing material</h3>

![assignment one light material graph](https://github.com/user-attachments/assets/b7ec1f52-eefe-43a8-847f-9c9d3ee9ab19)


<p>Created a glowing sphere
  
  Reference: Emissive Material in Unreal Engine 5 - Glow | Neon Effect Tutorial https://www.youtube.com/watch?v=WCmq4e6vacc
</p>
