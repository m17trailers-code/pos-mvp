# Shots — Doorbell, 3:12 AM

All shots: **Aspect 9:16**, 1080×1920. Look: doorbell camera, wide fisheye, infrared
night vision monochrome, slight vignette, mild compression noise. Higgsfield generates
the porch scenes; the app UI overlay (timestamps, "Motion detected") is added in edit,
not in the model, because generated text is unreliable.

Base image prompt (reuse for every porch shot):
> Doorbell camera view, ultra-wide fisheye lens, infrared night vision, monochrome
> grey-green, suburban front porch at night, concrete walkway leading to a mailbox at
> the street, one streetlight across the road, hanging plant top-left, faint IR
> vignette, compression artifacts, security footage, no text, no UI

## Shot 1 — empty porch (covers 0–7s)
- Image prompt: base prompt + "completely empty, still night"
- Motion prompt: static camera, a small moth flutters across the lens at 4s, hanging plant sways slightly in wind, nothing else moves
- Duration: 7s (generate 8s, trim)
- Avoid: any figure, any legible text, camera movement

## Shot 2 — figure at the streetlight (covers 7–12s)
- Image prompt: base prompt + "at the far edge of the streetlight across the road a very tall pale thin humanoid figure stands perfectly still, indistinct, featureless face, arms hanging too long, barely visible, small in frame"
- Motion prompt: static camera, figure does not move at all, subtle IR flicker, plant sways once
- Duration: 5s
- Avoid: figure walking, figure facing away, any recognisable facial features, more than one figure

## Shot 3 — figure at the mailbox (covers 12–17s)
- Image prompt: base prompt + "the same tall pale featureless humanoid figure now stands at the mailbox at the end of the walkway, head tilted slightly to its left, arms hanging past its knees, perfectly still, facing the camera"
- Motion prompt: static camera, figure completely motionless, very slow IR exposure pulse, a single leaf moves on the walkway
- Duration: 5s
- Avoid: motion in the figure, blinking, hands in detail, clothing detail

## Shot 4 — empty porch again (covers 17–19s)
- Reuse Shot 1 footage, a different 2s slice. No new generation.

## Shot 5 — the face (covers 19–20s)
- Image prompt: "Extreme close-up doorbell camera fisheye, infrared night vision monochrome, a pale wet humanoid face rising from the bottom edge of frame filling the lens, eyes reflecting bright white IR glare, mouth slightly open, skin smooth and featureless like a mannequin, heavy fisheye distortion, security footage, no text"
- Motion prompt: face lunges upward into frame in under half a second and stops inches from the lens, slight IR bloom on the eyes
- Duration: 2s (use ~0.6s)
- Avoid: blood, wounds, teeth detail, resemblance to any real person, hands
- Compliance: no gore. Face must read as uncanny, not injured.

## Shot 6 — signal lost (covers 20–30s)
- No generation. Black frame + UI built in edit. Add breathing SFX and the "Door opened" notification at 25s.

## Edit notes
- Alerts are separate clips with a hard cut and a UI banner slide-in; do not crossfade.
- Timestamps in UI: 3:12:04 · 3:12:41 · 3:13:20 · 3:13:58 · door opened 3:14:22.
- Keep crickets bed under alerts 1–2; kill it hard at 7s when the figure appears.
- Scare audio peaks once; do not layer a music sting.
