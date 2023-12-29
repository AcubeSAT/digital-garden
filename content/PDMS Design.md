
---
title: PDMS Design Iterations
draft: false
tags:
  - su
  - pdms
---

## Summary

There are three designs for the on-board microfluidic chip that will host the in-orbit experiments. These three designs are currently being reviewed and tested to select the one that will eventually be used. They are named biodisplay chip, MITOMI-yeast chip and microchemostat-yeast chip, respectively. They are all fabricated using a silicone elastomer (PDMS). The silicon wafers - molds are created using a technique called soft lithography. The silicone is poured in the wafers. Protocols for the fabrication of the chips can be found here. All chip designs contain chambers where the cells are placed and channels through which fluids (water and growth medium) and transferred in and out of the chip.

The functionality of all designs relies on diffusion for nutrient supply to the cells. However, each design differs on how cross-contamination (cells escaping from their chamber and entering a different one downstream) is avoided. There are 2 stages during chip operation:

- First, the chip is empty, and the cells have been spotted (commonly repurposing a DNA microarray spotter) in the chambers. During this phase their volume is minimal and there is empty space in the chambers. To begin, the chip is primed with growth medium (and water, in dual layer designs), which differs as the type of chip that is used changes. More information about the design and functionality of each design is provided below. 
- Then, the chip is filled with liquid, the cells are grown to confluency and nutrients are consistently supplied when needed.

During priming cross-contamination is much more probable. There is empty space inside the chambers, meaning that the cells can diffuse freely inside and outside their chambers, contrasted to the second stage. During this stage there is no flow of medium inside the channels for several hours since cells must firstly grow. On the other hand, during the second phase, cells are fully grown as a result their volume increased to accommodate the chambers fully. Their bigger size has a result to significally limit their movements. At the same time the flow of medium inside the channels is more frequent as a result a strong flow in the channel. Also refreshing the medium much more frequently has a result a strong flow that drifts away dead cells or cells that escaped the chambers. The three designs have different mechanism and functionalities to avoid cross-contamination, that are described to the subsection of each design.

## First design: Biodisplay 

Our current microfluidic design is based on the following paper: [Volpetti et al. A microfluidic biodisplay. (2017). ACS synthetic biology](https://pubs.acs.org/doi/abs/10.1021/acssynbio.7b00088).

### First Modifications Round

- Reduction of the number of flow lines to a singular one per sub-experiment
- Reduction of the number of control lines to two, one for the chamber and one for the sandwich valves
- Chamber number (referred as resolution) changed to 8 x 48 for a total of 384 chambers per sub-experiment
- Re-centering the chip and keeping the same dimensions for the frame

The above are summarized on the single sub-experiment design layout, to also be used as a basis for all designs that follow below.

### Iterations

- Moved the control line managing the chamber valves to the top
- Moved inlets closer to avoid extensive pressure drops
- Introduced vacuum line as an alternative to plasma bonding, inspired from [Chawla et al. 
- Integrating impedance-based growth-rate monitoring into a microfluidic cell culture platform for live-cell microscopy. (2018). Microsystems & nanoengineering](https://www.nature.com/articles/s41378-018-0006-5). Specifically, the proposed layouts include:
1. One with the vacuum line on the separate vacuum layer  
2. One with the vacuum line on the preexisting flow layer  
- Increased the distance between the chamber's control line and the chambers from 7.553 to 21, since the distance between the two was prohibitively small

### Modifications for testing

In order to be able to perform functional testing on a satellite-level, we want to be able to actuate the flow (and preferably, control) channels. However, doing so will leave either growth medium (flow channel) or water (control channel) sitting inside, which could lead to potential damage. To circumvent this, we introduce the following modifications:
- Added a single extra 1x48 chambers row with a single flow channel
- Added a single extra 1x48 chambers row with a single flow channel, with 2 additional control lines (for both sandwich and chamber valves). This is done by extending the original control lines. In both modified layouts, there is an isolated inlet and outlet for the flow channel.  
- Adding additional independent control lines was considered but rejected due to the power cost for extra off-chip solenoid valves.
- In line with the changes to distances outlined above, there are two additional designs with an added flow line for testing purposes:
  - One with the inlets now closer.
  - And one with the inlets closer and the distance between the chamber's control line and the chambers larger.

The biodisplay design is heavily based on published ones from the [Laboratory of Biological Network Characterization](http://lbnc.epfl.ch/index.html) (LBNC) in EPFL. The LBNC designs can be found [here](http://lbnc.epfl.ch/microfluidic_designs.html). 

The final PDMS chip layout is segmented into three identical arrays. In each, a distinct sub-experiment will take place, for a total of three. Each sub-experiment array is comprised of:

- 8 rows, with 48 chambers in each, for a total of 8 × 48 = 384 chambers
- two control channels, the chambers and the sandwich one
- two control inlets, respectively
- a flow channel
- a flow inlet and outlet, respectively

Additionally, a single array was added to facilitate testing procedures. This test array
is comprised of:

- a single row, with 48 chambers
- a flow channel
- a flow inlet and outlet, respectively

To avoid cross contamination the biodisplay design has a control valve which closes the flow channel.

The final layout, with all three sub-experiment arrays and the test array stacked vertically and the sub-experiment array design, together with the test array, can be found in [DDJF_PL](https://gitlab.com/acubesat/documentation/cdr-public/-/blob/master/DDJF/DDJF_PL.pdf?expanded=true&viewer=rich).

## Second Design: MITOMI-Yeast

The final PDMS chip layout is segmented into three identical arrays. In each, a distinct sub-experiment will take place, for a total of three. Each sub-experiment array is comprised of:

- 8 rows, with 48 chambers in each, for a total of 8 × 48 = 384 chambers
- one control channel, the sandwich one
- one control inlets
- a flow channel
- a flow inlet and outlet, respectively

Additionally, a single array was added to facilitate testing procedures. This test array
is comprised of:

- a single row, with 48 chambers
- a flow channel
- a flow inlet and outlet, respectively

This design is taken to consideration as theoretically it can operate with only the flow layer. As described, during the second stage of chip operation the cells inside the chambers are fully grown, accommodating the whole chamber. During priming, medium flows downwards and the force field expands outward. The pressure difference that is created has a result of not allowing the cells to escape. This is how cross contamination is avoided in this design.

1. MITOMI FLOW LAYER

Additionally, a control layer was design for troubleshooting and error prevention. As described, during the first phase (priming), cross contamination is much more easier to happen. There is much more space inside the chambers and cells move around more freely inside and outside their chambers, compared to the second stage. During this stage there is no flow of medium inside the channels for several hours since cells must firstly grow. During this face the control layer when filled will act as a barrier, closing the entrance of the chambers, preventing the cells to escape.

2. MITOMI CONTROL LAYER
3. MITOMI CONTROL(BLUE) AND FLOW(YELLOW) LAYER
4. MITOMI CHAMBERS WITHOUT CONTROL LAYER
5. MITOMI CHAMBERS WITH CONTROL LAYER

## Third Design: Microchemostat

The final PDMS chip layout is segmented into three identical arrays. In each, a distinct sub-experiment will take place, for a total of three. Each sub-experiment array is comprised of:

- 8 rows, with 48 chambers in each, for a total of 8 × 48 = 384 chambers
- a flow channel
- a flow inlet and outlet, respectively

Additionally, a single array was added to facilitate testing procedures. This test array
is comprised of:

- a single row, with 48 chambers
- a flow channel
- a flow inlet and outlet, respectively

This design does not require a control layer and can operate with only the flow layer. This design has blockers inside the channels and the channel is like a chimney to increase the resistance (due to height differences). The growth-medium enters the chambers from smaller entrances, which they do not allow the cells to go through them. The chambers when they are not fully filled with cells do not allow the cells to escape due to the blockers they have on the upper side and the small entrances for the growth-medium to the lower side.

1. MICHROCHEMOSTAT DESIGN
2.  MICHROCHEMOSTAT CHAMBERS
3.  MICHROCHEMOSTAT CHAMBERS - BLOCKERS (1)
4.  MICHROCHEMOSTAT CHAMBERS - BLOCKERS (2)
