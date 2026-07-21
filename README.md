# Dark Side of Horror (Unity) — Local Co-op Top-Down Shooter

> A local co-op top-down shooter focused on fast combat, progression, and wave survival.

**Playable build:** https://saulosouza2703.itch.io/darksideofhorror  
**Trailer / gameplay clip:** https://www.youtube.com/watch?v=KaRmbNnXc-o  
**Engine:** Unity (version: 6000.3.4f1)  
**Platforms:** Windows

---

## My role (Gameplay / Engineering)

I was the **Lead Programmer** on the project. My work focused on core gameplay systems, performance, and moment-to-moment feel.

### What I implemented
- **Player controller**: movement + rotation + animation state machine integration
- **Shooting framework** with **5 weapon types** (data-driven where possible)
- **Interaction systems**: weapon purchase, perks, score/economy loop
- **Object pooling** for bullets/projectiles (performance + reduced runtime allocations)
- **Gameplay support for enemies**: ragdoll hit reactions / bullet impact integration
- **Wave gameplay support** (integration / iteration support with the team system)

> Note on repo history: this repository is a **portfolio snapshot/import** of our team project. Earlier commits may reflect the original team repository authorship. The sections above describe **my direct contributions**.

---

## Key systems (high-level overview)

- **Weapons**
  - Multiple weapon behaviors (e.g., projectile patterns / fire rates / reload behaviors)
  - Clear separation between input → weapon logic → projectile spawning
- **Pooling**
  - Central pooling for high-frequency objects (bullets / VFX if applicable)
  - Reuse objects to avoid Instantiate/Destroy spikes
- **Interactions**
  - Generic interactables with player prompts + purchase validation
  - Upgrades/perks applied through centralized player stats/modifiers

---

## How to run (for reviewers)

1. Download the latest build from: https://saulosouza2703.itch.io/darksideofhorror
2. Extract and run: `Dark Side of Horror.exe`
---

## Controls

Controls may vary by build; check the in-game menu if available.

**Keyboard / Mouse (typical default):**
- Move: `WASD`
- Aim: Mouse
- Shoot: `Left Mouse`
- Interact: `E`
- Reload: `R`
- Switch weapon: `1–5`

**Controllers (local co-op):**
- Supports multiple controllers for local co-op (join flow: Press any button when gameplay starts)
- Move: `Left analog stick`
- Aim: `Right analog stick`
- Shoot: `RT/R2`
- Interact: `right d-pad`
- Reload: `X/Square`
- Switch weapon: `Y/Triangle`

---

## Media

<!-- TODO: add gameplay screenshots / a short GIF to docs/media and embed them here:
![Gameplay](docs/media/gameplay-01.png)
-->

Watch the [trailer / gameplay clip](https://www.youtube.com/watch?v=KaRmbNnXc-o) or grab the [playable build on itch.io](https://saulosouza2703.itch.io/darksideofhorror).

---

## Performance notes

- Pooling was introduced to reduce runtime allocations and avoid spikes during combat-heavy moments.
- High-frequency objects (bullets/projectiles) are reused and returned to the pool on lifetime end / impact.

---

## Credits

See: **CREDITS.md**

---

## License / usage

This repository is shared for **portfolio/review purposes**.  
If you want to reuse code or assets, please contact the team first.

---

## Contact

- GitHub: [Ian-WB](https://github.com/Ian-WB)
