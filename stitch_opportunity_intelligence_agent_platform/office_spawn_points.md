# Office Spawn-Point & Navigation Map

Background size: **1310 × 1200px**  
Origin: **top-left (0,0)**

## Agent spawn points

| ID | Agent | Standing/walking spawn | Desk/seated anchor |
|---:|---|---:|---:|
| 1 | Planner | (195, 721) | (195, 642) |
| 2 | Discovery | (495, 721) | (495, 642) |
| 3 | Investigator | (795, 721) | (795, 642) |
| 4 | Verifier | (1092, 721) | (1092, 642) |
| 5 | Match | (195, 965) | (195, 884) |
| 6 | Application | (495, 965) | (495, 884) |
| 7 | Outreach | (795, 965) | (795, 884) |
| 8 | Monitor | (1092, 965) | (1092, 884) |

## Manager / scanner

- Manager stand: **(640, 326)**
- Manager desk anchor: **(640, 274)**
- Manager office door: **(867, 409)**
- Scanner approach: **(245, 426)**
- Scanner: **(232, 321)**

## Navigation routes

- Planner → Discovery: `(195,721) → (195,756) → (495,756) → (495,721)`
- Discovery → Investigator: `(495,721) → (495,756) → (795,756) → (795,721)`
- Investigator → Verifier: `(795,721) → (795,756) → (1092,756) → (1092,721)`
- Verifier → Match: `(1092,721) → (1160,721) → (1160,810) → (195,810) → (195,965)`
- Match → Application: `(195,965) → (195,1000) → (495,1000) → (495,965)`
- Application → Outreach: `(495,965) → (495,1000) → (795,1000) → (795,965)`
- Outreach → Monitor: `(795,965) → (795,1000) → (1092,1000) → (1092,965)`
- Monitor → Manager: `(1092,965) → (1165,965) → (1165,475) → (900,475) → (900,409) → (867,409) → (867,390) → (640,390) → (640,326)`
- Manager → Scanner: `(640,326) → (867,326) → (867,409) → (900,409) → (900,455) → (245,455) → (245,426) → (232,321)`

## Stitch rules

1. Background remains static.
2. Agents are independent layers.
3. Use the provided sprite-sheet frames only.
4. Spawn = character feet/base anchor.
5. Seated agent uses desk anchor.
6. Completed agent swaps to standing sprite, walks along route, performs handoff, then returns and swaps back to seated.
7. Never teleport agents.
8. Keep speech bubbles attached to the moving agent.
