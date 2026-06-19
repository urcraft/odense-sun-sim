# Odense Sun & Heat Simulator

An interactive sun-path and heat simulator for a top-floor flat in **Odense, Denmark**
(55.40°N, 10.39°E). Built to plan passive, non-AC summer cooling: it shows the sun's
position through the day and which rooms catch direct sunlight (and therefore heat up).

**Live page:** https://urcraft.github.io/odense-sun-sim/

## What it does

- Computes the real solar position (elevation + azimuth) for Odense at any time of day
  using standard solar-geometry math (declination, equation of time, hour angle).
- Renders the flat's floor plan on an HTML5 canvas and washes warm light over the rooms
  the sun can actually reach.
- Models the building correctly: only the **north** (bedrooms) and **south**
  (living room / balcony) walls are exterior facades. The **east and west walls are
  shared party walls** to neighbouring flats — no glazing, no solar gain there.

## How to use

Open the live page, or run it locally:

```bash
# any static server works, e.g.
python -m http.server 8765
# then open http://localhost:8765/index.html
```

Drag the time control to move through the day and watch which rooms light up. Hot side
= south (living/balcony) from mid-morning to evening; bedrooms (north) only catch weak
early-morning grazing light.

## Tech

Single self-contained `index.html` — vanilla JavaScript + Canvas 2D, no dependencies,
no build step.

## License

MIT — do whatever you like with it.
