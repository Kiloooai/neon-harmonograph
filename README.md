# 🌟 Neon Harmonograph

*Virtual pendulum drawing machine. Two perpendicular pendulums with adjustable frequency, amplitude, phase, and damping create mesmerizing geometric Lissajous-like patterns. Neon trails fade slowly. Real-time parameter tweaking. Randomize for infinite variation. Meditative, hypnotic, zero pressure.*

---

## What is this?

A harmonograph is a mechanical device that uses pendulums to draw geometric patterns. This is a software simulation: two virtual pendulums swing perpendicular to each other, and their combined motion draws a curve. Adjust each pendulum's frequency, amplitude, initial phase, and damping (energy loss). Watch the pattern evolve in real time with neon glow. It's part physics toy, part generative art, part mindfulness aid.

---

## Features

- **Dual-pendulum system** — X and Y oscillators with independent parameters
- **Real-time drawing** — neon trails follow the pendulum tip
- **Adjustable parameters (per pendulum):**
  - Frequency (0.1–5 Hz)
  - Amplitude (10–300 px)
  - Phase (0–2π rad)
  - Damping (0–0.1) — how quickly oscillations decay
- **Global controls:**
  - Hue (0–360)
  - Trail fade (0.01–0.2) — lower = longer trails
  - Speed multiplier (0.5–3×)
- **Clear** — wipe canvas and reset time
- **Random** — randomize all parameters for serendipitous patterns
- **Stats** — elapsed time, FPS
- **Single HTML file** — no dependencies

---

## How to Use

1. Open `index.html`
2. Watch the pattern draw itself automatically
3. Tweak sliders to change the pendulum behavior:
   - **Frequency** — higher = more oscillations per second
   - **Amplitude** — how far the pendulum swings
   - **Phase** — starting offset in the swing cycle
   - **Damping** — energy loss; low damping = pattern continues longer, high damping = spiral into center
4. Change **Hue** to cycle colors
5. Adjust **Trail Fade** — lower values keep trails longer, creating dense intricate patterns; higher values fade faster
6. **Speed** — speed up or slow down the simulation
7. **Random** — generate surprising new parameter sets
8. **Clear** — start fresh

---

## The Math

Each pendulum follows damped harmonic motion:

```
displacement(t) = amplitude * exp(-damping * t) * sin(frequency * t + phase)
```

The X pendulum contributes to horizontal position, Y pendulum to vertical. The drawing point is:
```
x = centerX + dispX(t)
y = centerY + dispY(t)
```

As time progresses, the exponential term causes the amplitude to shrink (if damping > 0), making the pattern spiral inward. With zero damping, the pattern continues indefinitely, producing perfect Lissajous figures when frequency ratios are rational.

---

## The Real Story

There's something deeply satisfying about watching mathematical curves appear stroke by stroke. The neon glow gives it that syntheticfuture look. The Random button is genuinely magical — you never know what you'll get. Sometimes you get simple ellipses, sometimes you get intricate snowflake-like structures that take minutes to fully form. It's the perfect thing to leave open on a second monitor while you think or relax.

No goal, no failure, just pretty lines.

---

*Made with ✨ and a couple of virtual pendulums during a heartbeat build cycle.*

**Repo:** https://github.com/Kiloooai/neon-harmonograph
