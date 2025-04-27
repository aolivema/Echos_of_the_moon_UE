# 🧤 VR Gloves Controller Project

A custom VR experience built in **Unreal Engine 5.5.3** where players use custom astronaut gloves instead of standard hand models. Players can move around using controller inputs, trigger particle effects (like firing bullets).

## 🚀 Features

### 🧤 Custom Astronaut Gloves
- Replace default hands/controllers with realistic glove models.

### 🎮 Controller-Based Movement
- Move the player forward, sideways using thumbstick inputs.

### 🔥 Particle Effects on Trigger Press
- Spawn bullets or fire particles when pulling the right controller trigger.

### 🖐️ Finger Movement Animations
- Animate gloves' thumb and index fingers based on controller input for natural interaction.

### 🌌 Custom VR Environment
- Explore a custom-made 3D house or cave environment designed for immersive VR interaction.

### 🎥 Scene One: Intro Video
- Players start in a "black box" theater environment and watch a short intro video.
- After the video ends, players are seamlessly transitioned into the gameplay environment to explore and interact.

### 🛠 Collision-Enabled Particles
- Projectiles interact properly with the environment's surfaces.

## 📦 Project Setup

**Engine Version:**  
Unreal Engine 5.5.3

**Hardware Required:**  
- VR Headset (Meta Quest 3 tested)  
- Motion Controllers

**VR Template:**  
- Started from Unreal VR Template or Custom VR Pawn.

## 🛠 How to Run

1. Clone the repository and open the project in **Unreal Engine 5.5.3**.
2. Set the default map to the intro video environment.
3. After the intro video plays, you will automatically enter the custom environment (house/cave).
4. Ensure the **VRPawn Blueprint** is assigned as your **GameMode default Pawn**.
5. Connect your VR headset and run in **VR Preview** mode.

## 🎮 Controls

| Action                | Controller Input            |
|------------------------|------------------------------|
| Move Forward/Backward  | Thumbstick (Y-Axis)          |
| Strafe Left/Right      | Thumbstick (X-Axis)          |
| Fire Bullet/Particle   | Right Trigger Button         |
| Finger Animation       | Thumb & Index Finger Inputs  |

## 📋 Technical Details

**Intro Video Implementation:**  
- Uses a Media Player asset to stream or play a preloaded video inside a black box VR scene.
- Video auto-plays on game start and triggers level change after completion.

**Character Type:**  
- Custom Character Blueprint (not Pawn) for gravity and collision.

**Hand Models:**  
- FBX imported gloves attached to `MotionController (Left)` and `MotionController (Right)`.

**Particle Firing:**  
- Spawn Emitter at Location triggered on right trigger press.

**Movement Blueprint:**
- `Event MoveForward → GetActorForwardVector → Add Movement Input`
- `Event MoveRight → GetActorRightVector → Add Movement Input`

**Collision Setup:**
- Particle Systems have Collision Enabled to stick to cave walls and objects.

## 📸 VR Preview

*(Add a few in-game screenshots or VR preview shots here!)*
