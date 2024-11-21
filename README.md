# Pulse-Magnetizer
For research involving magnets, it is often required to magnetize unmagnetized permanent magnets by exposing them to a strong field. For neodymium (NdFeB) magnets, this can pose quite a challenge because the fields required to permanently magnetize them are very strong. Commercial magnetizers exist but are large and expensive and not well suited for occasional lab use.

Fortunately, Yuri Skvortsov published his design of a [pulse magnetizer](https://medium.com/@yuriy.skvortsov/pulse-re-magnetizer-for-neodymium-magnets-e5c42aefbf78) using a capacitor bank and coil to remagnetize hard drive magnets which was an excellent starting point for this project. This repository contains a modifed version of Yuri's that aims to improve safety and functionality with a basic control panel, laser cut wooden case, and build instructions.

## Contents
- Complete KiCAD schematic for use with 120VAC mains
- CSV bill of materials for all electrical components
- SVG for laser cut 3mm and 6mm plywood to construct housing
- Shop drawings of machined bus bars etc.
- STEP file CAD assembly

## Performance
A simple test to verify the functionality of the pulse magnetizer was conducted by measuring and recording the pull force of a 0.75" diameter, 0.1875" thick NdFeB disc magnet acting on a steel disk placed on a gram scale. The magnet was then heated using a heat gun to above its curie point to remove any magnetic properties. After cooling, the magnet was exposed to a full pulse from the magnetizer and measured using the gram scale again. The scale indicated the field was 98.5% of the original strength. This is not a perfect test because the grade of the magnet was not known (likely a lower grade e.g. N40), and could struggle to remagnetize higher grades like N55. Based on SPICE simulations and theoretical calculations for a 30mm diameter, 30mm long, 30 turn coil using 1mm diameter copper wire, the field strength generated was 3.5T. This could be further improved using the same dimension coil but with 1.5mm diameter wire (by reducing inductance and resistance allowing more current flow), to generate a 4.3T field. This is plenty strong for even N55 magnets.

## Safety
This device deals with lethally high voltages, and capacitors that can maintain these voltages even after the device is unplugged. Any use of this project is at your own risk.
