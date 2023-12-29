---
title: PDMS Fabrication - Single Layer
draft: false
tags:
  - su
  - pdms
---

## Parameters

The spotting loop is defined by the following parameters:

1. `Inking time = 1 s`. Inking time is defined as the time when the pin remains in the liquid (e.g. cell sample) for the uptake.
2. `Stamping time = 1 s`. Stamping time is defined as the time when the pin touches the spotting surface (e.g. glass)
3. Cleaning: `Water, 2 s`.
4. Drying: `Air, 2 s`. Typically performed via a negative pressure after placing the pin in a small hole with vacuum. Air "spraying" does work. Way to dry the pin inbetween spots, in the same sequence, is left to be decided.
5. `Humidity = 75%`. This is for avoiding drying of the spots. Since we don't currently have humidity control, this remains optional.

## Pin Handling

It is of absolute importance to handle the pin with care as it is very fragile. If the pin tip is bent, capillary action in the small gap of the needle may be disturbed, and thus miss its spotting ability. 

- **While using the tip:**
  1. _(optional)_ You can make sure pin is clean by checking it under the stereoscope. You should see an unobstructed gap in the middle of the pin tip. If anything is blocking it perform a wash-air clean (described below). 
  2. Be very careful while mounting the pin to the 3d printer head as to not accidentally "bump" it in the head.
- **Wash-air clean**
  1. When spotting sequence is done, carefully `unmount the tip` off the printer. 
  2. Put it inside a `petri dish` containing distilled water + ethanol 70% solution (just a few sprays of ethanol 70% along with some water - enough to cover the pin is ok).
  3. `Sonic bath`: place the dish on top of the small air pump in lab2. Turn on the pump and let it vibrate for a few seconds (~30sec) while holding the dish in place. 
  4. Turn off the pump, take pin out of the solution and blow it using the `air gun` (preferably highly pressurized) to air-dry. Try to aim the small gap in the pin in order to blow out any remaining debris. Blow till pin is dry.
  5. Put pin back in the `storage box`, and inside the DIY fumehood. 

## Pin cleaning

The best cleaning procedure according to the supplier is the following:

1. Use a sonicator with SDS solution (or any other detergent such as "AQUANOX") for 10 min
2. Use a sonicator with distilled H<sub>2</sub>O for 5 min

The above should remove all residues of buffers.

The usual cleaning procedure (used by the supplier) is the following:

1. Clean the printhead hole with a tooth gap brush and “Sidol” (common brass cleaning solution which you can get in a DIY store)

## Notes

1. Although you can do multiple spots (uptake volume >> delivery volume), prefer to do `1 stamp per spot`.
2. The pin is *very easy* to break, especially if it touches a hard surface with force. For this reason, the pin **should not be strongly fixated** on the mount.
3. Spores should tolerate spotting much better than cells. However, surprisingly (?) cells have better recovery rate (\~90%) if the cell solution is basically a 2 day-old YPD pre-culture. 
