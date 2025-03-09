# VR Interact

This project is consists the following:
- **Interactive Button**: A responsive button that triggers actions when pressed.
- **Toggle Visibility**: A button to show or hide an object in the scene.
- **Two Animations**: Simple animations with objects (like a sphere, cube, or cylinder).
- **Animation Manager**: A smart system ensuring only one animation plays at a time, triggered by button presses.

## How I Built It
I started with Unreal Engine’s starter scene and created custom Blueprints, stored in Content/Blueprints. Here’s a breakdown of my work:

- **Button Logic (*BP_Button*)**:
When the user’s hand (left or right) collides with the button and presses it, the button updates its state to ButtonPressed and triggers the OnButtonPressed event.
- **Toggle Button (*BP_ToggleButton*)**:
I built this by extending BP_Button with an editable Actor variable, letting users choose which object to toggle. The show/hide actions are seamlessly triggered by listening to button events and dispatching the right functions.
- **Animation Manager (*BP_AnimManager*)**:
This system uses an editable array of Actor objects to manage animations. Users can add as many animations as they like, and the manager dynamically creates a button for each one. Pressing a button plays its animation—but only if no other animation is active. Press it again to stop the animation, keeping everything exclusive and intuitive.

To run the application:

1. Clone the repo:
```sh
git clone https://github.com/pankajkaushik12/VRInteract
```
2. Open the project in *Unreal Engine 5*.
3. Connect your VR headset, then click VR Preview to start.

## What You’ll See
Once launched, you’ll find three buttons in front of you:

- **Leftmost Button**: Toggles the visibility of a object (ConeOnCylinder).
- **Other Buttons**: Trigger animations on their respective objects. Only one animation plays at a time—stop the current one by pressing its button again before starting another.

Outputs

Buttons:
![](/Output/Buttons.png)

Animation 1:
![](/Output/Animation%201.gif)

Animation 2:
![](/Output/Animation%202.gif)