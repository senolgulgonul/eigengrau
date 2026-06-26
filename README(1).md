# eigengrau

A single-file, dependency-free WebGL toy that mimics **closed-eye visual noise** — the dim *eigengrau* ("intrinsic grey") field and the slow, cloud-like orange tones you see with your eyes shut. It runs entirely client-side.

Live: https://senolgulgonul.github.io/eigengrau

## What it is (and isn't)

This is a **contemplative visual**, not a psychological test. There is no scoring, no interpretation, and no claim that what you see "means" anything. It simply renders a soft, in-place boiling field in a narrow near-black orange band, the way a closed-eye field looks in daylight.

The underlying phenomena it gestures at are real: *eigengrau* / intrinsic grey, *phosphenes*, and *closed-eye visualizations* (entoptic phenomena). The motion is deliberately slow because, in practice, the field changes mostly with eye movement rather than on its own.

## Controls

- **Intensity** — overall brightness of the field (kept inside a dark, narrow band).
- **Flow speed** — rate at which the field evolves. At `0` the field is fully frozen.
- **Run / Stop** — freeze the current frame to hold a random shape.
- **Pointer** — click or drag on the field to gather a little light at that point.

## Implementation

A full-screen fragment shader. The field is 3D value-noise `fbm` whose third axis is time, so it evolves **in place** with no net drift. A slow large-scale "swell" makes regions brighten and fade like clouds. Colour is a narrow ramp from a warm near-black to a dim orange. No external libraries.

## License

Code and content © 2026 Şenol Gülgönül, released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
