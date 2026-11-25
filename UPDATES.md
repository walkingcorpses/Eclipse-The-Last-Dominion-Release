# Development Updates

## 2026-11-25 — First playable combat (Milestone 3)

The first complete fight is in. You can pick up a weapon, fight an enemy that warns you before it strikes, block, parry, dodge, cast a spell, win or die, and save and load. All of it plays the same in first person and third person.

- **Health, stamina and mana.** Attacks, blocks and dodges cost stamina, spells cost mana, and both refill over time.
- **Pick things up** by looking at them and pressing E (Square on controller). You have to be close: the third-person camera can't grab things your character couldn't reach.
- **Iron Sword:** a three-hit light combo, plus a heavy attack when you hold the button that knocks the enemy off balance.
- **Ember Bolt:** an aimed fire spell that flies to the centre of the screen in both views, with a short cooldown.
- **Defence:** block to take a quarter of the damage, block at the last moment to **parry** (no damage, enemy staggered), or dodge out of the way.
- **The Hollow Thrall,** the first enemy. It chases you, glows red while it winds up an attack so you can react, and can be staggered and killed.
- **Same fight, either view.** An automated test plays the whole fight in third person and again in first person and checks that every number comes out the same.
- **Quick save and load** (F5 / F9, for testing) keep your position, health, equipment and what you've already picked up.
- If you die, you come back at the start with your gear.

![The Hollow Thrall winding up an attack](screenshots/2026-11-25-combat-telegraph.png)
*The Hollow Thrall glows red while winding up its attack: the moment to block, parry or dodge.*

![First person with the Iron Sword](screenshots/2026-11-25-combat-first-person.png)
*First person: the sword in hand and the enemy's health bar after a few hits.*

![Picking up the Iron Sword](screenshots/2026-11-25-pickup-prompt.png)
*Looking at an item shows what you can do with it.*

Everything you see is a temporary placeholder: the box "sword", the mannequin characters, the unarmed punch animations and the simple on-screen bars. Real art, animation and interface come later. This milestone was about making the fight work.

**Next:** the first story slice: character creation, the opening cinematic, a hub in the Ashen Kingdom, and the first main and side quests.

## 2026-11-25 — Player character and dual camera (Milestone 2)

The player can now walk, run, sprint, crouch and jump, and switch between first-person and third-person at any moment.

- **One character, two views.** Switching only changes the camera. Your speed, direction, aim, crouch and jump carry straight through, even mid-air.
- **Smooth switch:** a quarter-second blend, no loading. If a switch can't happen right then (in future, during a cutscene or a climb), it waits and happens as soon as it can, instead of being ignored.
- **First person** uses Unreal Engine 5.8's first-person rendering, so arms and weapons won't clip into walls.
- **Third person** has an over-the-shoulder camera that stays out of walls and ceilings.
- **Controls:** V on keyboard or D-pad Up on controller to switch views, and the bindings can be changed.
- **Ultrawide:** 21:9 screens see more of the world, not less.
- Head bob can be turned down to zero for players sensitive to camera motion.

![Third person](screenshots/2026-11-25-third-person.png)
*Third person in the camera test area. The character is Epic's standard mannequin, a temporary placeholder.*

![First person](screenshots/2026-11-25-first-person.png)
*The same spot in first person.*

![Ultrawide](screenshots/2026-11-25-third-person-ultrawide.png)
*21:9 ultrawide: same vertical framing, wider view.*

**Next:** core gameplay, covering interaction, health and stamina, a first melee and ranged/magic weapon, and a first enemy, all playable in both views.

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
