# Creating Your First World in Isaac Sim 4.5

Welcome! This guide will teach you how to create a simple virtual world in Isaac Sim 4.5. We'll add ground, lights, and objects that follow physics (like gravity). Follow each step, and you'll have your own 3D world in no time!

---

## What You'll Learn

By the end of this tutorial, you'll know how to:
- Create a new empty world
- Add a ground plane
- Add lighting so you can see things
- Add objects (like a cube) that fall with gravity
- Run a simulation and watch physics in action!

---

## Step 1: Open Isaac Sim and Create a New World

1. Launch Isaac Sim 4.5 (if you haven't already, check the [Installation Guide](../../Installation/Workstation_setup.md))
2. Once Isaac Sim is fully loaded, look at the top menu bar
3. Click **File → New**
   - This gives you a clean, empty world to start with
   - You should see an empty 3D viewport (the big window in the middle)

> 💡 **Tip**: If you see a dialog asking to save your current work, click "Don't Save" (since we're starting fresh)

---

## Step 2: Set Up Stage Properties (Important!)

This step makes sure everything looks the right size and orientation.

1. Click **Edit → Preferences** in the top menu
2. In the left sidebar, click on **Stage**
3. You'll see several important settings:

   - **Up Axis**: This should be set to **Z** (this means "up" is the Z direction)
     - If your models look tilted, you might need to change this to **Y**
   
   - **Linear Units**: This should be set to **meters**
     - If your objects look tiny or huge, check this setting!
   
   - **Rotation Order**: Leave this as **XYZ** (the default)

4. Click **OK** or close the Preferences window

> 🎯 **Why This Matters**: If these settings are wrong, your objects might look tiny, huge, or upside down!

---

## Step 3: Add a Physics Scene

Physics makes things fall, bounce, and collide. Let's add physics to your world!

1. Click **Create → Physics → Physics Scene** in the top menu
2. A Physics Scene object will be added to your world
3. Look at the **Properties** panel (usually on the right side of the screen)
4. Find the Physics Scene you just created in the **Stage** panel (left side) and click on it
5. In the Properties panel, you should see:
   - **Gravity**: Should be set to something like `(0, 0, -9.8)` - this makes things fall down
   - **Enable GPU Dynamics**: You can turn this OFF if your computer isn't super powerful
   - **Broadphase Type**: Set this to **MBP** (this makes physics calculations faster)

> ⚙️ **What is Physics Scene?**: It's like the "rules" for how objects move and interact in your world. Without it, objects won't fall or collide!

---

## Step 4: Add a Ground Plane

A ground plane is like the floor of your world. Without it, objects would fall forever!

1. Click **Create → Physics → Ground Plane** in the top menu
2. You should see a flat surface appear in your 3D viewport
3. To make it easier to see, you can turn on the grid:
   - Look at the viewport (the 3D window)
   - Find the grid toggle button (usually at the top of the viewport)
   - Click it to show the grid lines

> 🎨 **Tip**: The ground plane is infinite - it goes on forever in all directions. Perfect for catching falling objects!

---

## Step 5: Add Lighting

Lighting helps you see your objects. Let's add a nice light source!

1. First, let's check the default light:
   - Look in the **Stage** panel (left side)
   - Find an object called "defaultLight" or similar
   - Click on it
   - In the **Properties** panel, you can lower its **Intensity** to something like `1000` (so it's not too bright)

2. Now add a new light:
   - Click **Create → Light → Sphere Light** (or **Distant Light**)
   - A light object will appear in your world

3. Move the light up:
   - Click on the light in the Stage panel
   - Use the **Move** tool (usually a button with arrows at the top)
   - Click and drag the light upward (along the Z axis) so it's above your scene
   - Or manually set its position in the Properties panel to something like `(0, 0, 5)`

4. Adjust the light's properties (click on the light, then look at Properties):
   - **Color**: Choose any color you like! (White is fine for now)
   - **Intensity**: Try `1000000` (that's 1 million - sounds big but it's normal for lights!)
   - **Radius**: Make it smaller, like `0.1` meters
   - **Cone Angle**: If it's a spot light, try `45` degrees
   - **Cone Softness**: Try `0.5` for softer edges

> 💡 **Pro Tip**: You can add multiple lights to make your scene look more interesting!

---

## Step 6: Add a Cube and Make It Physical

Now let's add an object that will fall with gravity!

1. Create a cube:
   - Click **Create → Shape → Cube** in the top menu
   - A cube will appear in your world (probably at the center)

2. Move the cube up:
   - Click on the cube in the **Stage** panel
   - Use the **Move** tool to drag it up, or set its position to something like `(0, 0, 3)` in the Properties panel
   - This puts it 3 meters above the ground

3. Make the cube physical (so it falls and collides):
   - Make sure the cube is selected (clicked on in the Stage panel)
   - In the **Properties** panel, look for an **Add** button or **+** button
   - Click **Add → Physics → Rigid Body with Colliders Preset**
   - This gives the cube:
     - **Mass** (so gravity affects it)
     - **Colliders** (so it can bump into things)

4. Adjust physics properties (optional):
   - **Mass**: Try `1.0` kg (or leave it as default)
   - **Linear Damping**: `0.0` (no air resistance)
   - **Angular Damping**: `0.0` (no spinning resistance)

> 🎲 **What's a Rigid Body?**: It's an object that can move, rotate, and collide with other objects. Perfect for things that should fall and bounce!

---

## Step 7: Run the Simulation!

This is the fun part - watch physics in action!

1. Look at the top of the screen for the **Play** button (usually a triangle icon ▶️)
2. Click the **Play** button
3. Watch your cube fall down and land on the ground plane! 🎉

4. To stop the simulation:
   - Click the **Pause** button (⏸️) or **Stop** button (⏹️)

5. To reset everything:
   - Click **Stop** if it's playing
   - Then click the **Reset** button (usually a circular arrow icon 🔄)

> 🎮 **Try This**: Move the cube to different heights and watch it fall again. The higher it is, the faster it falls!

---

## Step 8: Save Your World

Don't forget to save your work!

1. Click **File → Save** (or **Save As...**)
2. Choose a location to save your file
3. Give it a name like `my_first_world.usd`
   - **USD** is the file format Isaac Sim uses
4. Click **Save**

> 💾 **Remember**: Save your work often! You can always load it later with **File → Open**

---

## Bonus: Add More Objects!

Now that you know the basics, try adding more things:

1. **Add a sphere**:
   - **Create → Shape → Sphere**
   - Move it up
   - Add **Rigid Body with Colliders Preset**
   - Watch it roll when it falls!

2. **Add a cylinder**:
   - **Create → Shape → Cylinder**
   - Move it up
   - Add physics
   - See how it tumbles differently than a cube!

3. **Stack objects**:
   - Place one cube on top of another
   - Make sure both have physics
   - Watch them balance (or fall over)!

---

## Bonus: Create Worlds with Python Code

If you want to learn how to create worlds using code (like a programmer!), Isaac Sim comes with example scripts:

1. Find the example script:
   - Go to your Isaac Sim folder
   - Look for: `standalone_examples/tutorials/getting_started.py`

2. Run it:
   - **On Windows**: Open Command Prompt in the Isaac Sim folder and type:
     ```
     python.bat standalone_examples\tutorials\getting_started.py
     ```
   - **On Linux**: Open Terminal and type:
     ```bash
     ./python.sh standalone_examples/tutorials/getting_started.py
     ```

3. This script does the same things we just did, but with code!

---

## Quick Reference: What Each Step Does

| Step | What You Did | Why It Matters |
|------|--------------|---------------|
| 1 | Created new world | Clean starting point |
| 2 | Set stage properties | Makes objects the right size and orientation |
| 3 | Added Physics Scene | Enables gravity and physics |
| 4 | Added Ground Plane | Gives objects something to land on |
| 5 | Added Lighting | Makes everything visible |
| 6 | Added cube with physics | Creates an object that falls with gravity |
| 7 | Ran simulation | See physics in action! |
| 8 | Saved world | Keep your work for later |

---

## Troubleshooting

### Problem: The cube doesn't fall

- **Solution**: Make sure you added "Rigid Body with Colliders Preset" to the cube. Also check that the Physics Scene has gravity enabled.

### Problem: Everything is too dark or too bright

- **Solution**: Adjust the light intensity in the Properties panel. Try values between 100,000 and 10,000,000.

### Problem: Objects look tiny or huge

- **Solution**: Check the Stage properties (Edit → Preferences → Stage). Make sure "Linear Units" is set to "meters".

### Problem: The cube falls through the ground

- **Solution**: Make sure both the cube AND the ground plane have physics enabled. The ground plane should have "Static" physics.

---

## What's Next?

Congratulations! You've created your first world in Isaac Sim 4.5! 🎉

Now you can:
- Add robots to your world
- Add sensors (like cameras)
- Create more complex scenes
- Learn about single agents and multi-agent systems

Check out the other tutorials:
- [Single Agent Guide](../../Robots/single_agent.md)
- [Multi Agent Guide](../../Robots/Multi_agent.md)

---

> 📝 **Remember**: This guide is ONLY for Isaac Sim version 4.5. If you're using a different version, some menu items or features might be slightly different!

