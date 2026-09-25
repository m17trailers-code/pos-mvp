# Shots — The Basement

All shots: **Aspect 9:16**, 1080×1920. Look: handheld phone video, phone-flashlight
lighting only (hard white centre, fast falloff to black), noisy shadows, slight motion
blur, no colour grading. Timestamp and text overlays are added in edit, not generated.

Base image prompt (reuse):
> Vertical smartphone video, handheld, lit only by a phone flashlight, harsh white
> centre and deep black edges, heavy sensor noise, old residential basement, found
> footage, realistic, no text, no watermark

## Shot 1 — top of the stairs (covers 0–3s)
- Image prompt: base + "looking down a wooden basement staircase from the doorway, handrail on the left, cobwebs, the beam does not reach the bottom"
- Motion prompt: slight handheld sway, flashlight beam trembles, camera tilts down slowly
- Duration: 4s
- Avoid: any figure, legible text, clean modern stairs

## Shot 2 — descending (covers 3–10s)
- Image prompt: base + "mid-way down wooden basement stairs, steps close and out of focus at bottom of frame, concrete wall on the right, darkness below"
- Motion prompt: handheld walking motion down the stairs, one step per second, beam bouncing, occasional glance at the handrail
- Duration: 8s
- Avoid: feet in frame, smooth gimbal motion, any figure

## Shot 3 — basement sweep (covers 10–18s)
- Image prompt: base + "unfinished basement, stacked cardboard boxes, old furnace, water heater, exposed pipes, concrete floor, and in the far wall a small wooden door about three feet tall at floor level closed with a chain and padlock"
- Motion prompt: slow handheld pan left to right across the boxes and furnace, then the beam stops and holds on the small door
- Duration: 8s
- Avoid: the door being normal height, any figure, legible labels on boxes

## Shot 4 — the small door, close (covers 18–24s, 30–36s, 42–46s)
- Image prompt: base + "close-up of a small old wooden door about three feet tall at floor level, grey paint peeling, rusted chain through a hasp with a padlock, concrete wall around it, dust on the frame"
- Motion prompt A (18–24): static handheld hold, with each of three knocks a puff of dust falls from the top of the frame
- Motion prompt B (30–36): static handheld hold, four faster dust puffs, slight camera flinch on the last
- Motion prompt C (42–46): the door drifts inward about one inch revealing a thin black line along its edge, very slow
- Duration: 6s each (three generations from the same image)
- Avoid: door opening wide, any hand or arm in these takes, changing padlock state

## Shot 5 — knocking back (covers 24–30s)
- Image prompt: Shot 4 image + "the out-of-focus knuckles of a man's right hand at the edge of frame about to knock on the door"
- Motion prompt: hand knocks three times then withdraws out of frame, camera holds
- Duration: 6s
- Avoid: fingers in focus, wrong finger count, hand covering the door. If hands fail, film the owner's own hand knocking on any dark wood and composite.

## Shot 6 — the open padlock (covers 36–42s)
- Image prompt: base + "extreme close-up of a rusted padlock hanging open on a chain against a small grey wooden door, phone flashlight glare on the metal"
- Motion prompt: beam drops down onto the padlock, slight shake, the chain swings gently
- Duration: 6s
- Avoid: padlock closed, text on the lock

## Shot 7 — the arm (covers 46–48s) — MAIN SCARE
- Image prompt: base + "small wooden door at floor level slammed open, from inside a very long pale grey arm with too many joints reaches out low across the concrete floor toward the camera, fingers spread, skin smooth and dry like clay, no face visible, motion blur"
- Motion prompt: door slams inward in a single frame, arm shoots out toward the lens in under half a second, then camera drops and spins to the floor
- Duration: 3s (use ~1.5s, then cut to Shot 8)
- Avoid: blood, wounds, claws, a visible face, human-normal hand proportions
- Compliance: dry, clay-like, no injury detail. If the model adds blood, regenerate.

## Shot 8 — phone on the floor (covers 48–66s)
- Image prompt: base + "smartphone lying on its side on a concrete basement floor, the flashlight beam pointing along the floor at a small open wooden door with pure darkness inside, dust in the beam, image rotated ninety degrees"
- Motion prompt A (48–56): a low pale humanoid silhouette drags itself out of the small door on its elbows and passes out of the beam to the right, only a shape, no detail
- Motion prompt B (56–66): static, dust drifts in the beam, nothing moves, the beam flickers once
- Duration: 8s + 10s
- Avoid: face or eyes on the silhouette, it standing upright, it looking at the camera

## Shot 9 — black card (covers 66–70s)
- No generation. Black with the closing line in edit.

## Edit notes
- Rotate Shot 8 so the frame is sideways like a dropped phone; do not correct it.
- All knocks are foley; give the four-knock set a slightly different room tone.
- Footsteps on the stairs at 56–62s are only sound; nothing is shown.
- Keep total cut length ≥ 65s after trimming. Target 70s.
