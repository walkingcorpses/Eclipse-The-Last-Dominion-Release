# Development Updates

## 2026-11-25 — Foundation complete (Milestone 1)

The technical foundation is in place:

- The project now runs on its own C++ code (Unreal Engine 5.8).
- **Save system:** versioned saves that also protect against crashes. Every save is checksummed, and if the latest save is damaged, the game falls back to the previous one automatically.
- **Settings:** groundwork for camera and accessibility options, including separate first- and third-person field of view, look sensitivity and inversion, and camera shake and head-bob reduction.
- An automated test suite that checks these systems on every build.
- Modern lighting is switched on (Lumen global illumination and virtual shadow maps).

![First test map — placeholder floor and sky](screenshots/2026-11-25-dev-foundation-map.png)
*First engine test map. Placeholder floor and sky only; used to verify the lighting setup.*

**Next:** the player character and the first-person/third-person camera system. You will be able to switch between the two at any time.

## 2026-11-25 — Project kick-off

- Completed the full design specification and a technical audit of the starting project.
- Locked the engine version: Unreal Engine 5.8.
- Set up source control and the development toolchain.
