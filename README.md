# Ultimate Car & Aircraft Simulator — Unity project (Stage 1–4)

## What works now (all offline)
- Open-world city (8x8 blocks, roads, junctions, parks), highway, race track, airport area (runway/terminal/hangars, no aircraft yet), gas station, parking lot, cone/ramp challenge area, traffic.
- 14 fully drivable cars (WheelCollider physics, 6-speed auto/manual gearbox, handbrake, reverse, 3 camera views, procedural engine sound + exhaust pops on sports/luxury/super).
- Touch controls: steering wheel, gas, brake, handbrake, gear +/-, AUTO/MANUAL, camera, flip-car. Keyboard in editor: WASD/arrows, Space, Q/E, C, R, Esc.
- Main Garage (far outside the map): switch owned cars, paint (12 colours), upgrades (engine/turbo/tires, paid with green coins), select car.
- Showroom (separate building, 7 sections): specs, price + required currency, BUY, TEST DRIVE on its own pad.
- Two currencies: Economy/Sedan/SUV/Classic = GREEN; Sports/Luxury/Super = YELLOW (enforced in code by category). Purchase blocked if not enough coins.
- Earn coins: collect coins in the world (they respawn), drive 1 km = +40 green (+1 yellow every 3 km).
- Local JSON save (coins, cars, paint, upgrades, language, graphics, gear mode). English + Arabic (with letter shaping). Graphics Low/Medium/High/Ultra.

## Not built yet (next stages): damage + repair, aircraft/hangar/aircraft showroom/workshop, missions.

## Open and run
1. Unity Hub -> Add project -> this folder. Use Unity 2022.3 LTS (Built-in Render Pipeline, 3D template settings).
2. Open any scene (even empty) and press Play. The game builds itself at runtime (GameFlow.cs).
   If the console asks, set Project Settings > Player > Active Input Handling = "Input Manager (Old)".

## Build the APK
1. File > Build Settings > Android > Switch Platform. Add the open scene to "Scenes In Build" (save the scene first).
2. Player Settings: Company/Product name; Package Name e.g. com.yourname.carsim; Minimum API 24; Scripting Backend IL2CPP; ARM64 ticked (also ARMv7 for old phones); Default Orientation Landscape Left/Right.
3. Other Settings: Graphics API = OpenGLES3 (remove Vulkan for low-end phones); Color Space = Gamma (faster).
4. Build (APK) and copy to the phone, or Build And Run with USB debugging.
