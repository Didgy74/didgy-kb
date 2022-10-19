# didgy-kb
A catch-all repo for any keyboards I design.

These designs are all designed with [Ergogen](https://github.com/ergogen/ergogen).

# Mitten

This design has the following properties:
 - 30 keys
 - Split
 - Columnar stagger
 - Column splay on the outer columns
 - Wireless
 - Reversible PCB
 - (Very) Low profile (Choc Mini)
 - Choc spacing in Y direction
 - MX spacing in X direction
 - 1u keys for fingers
 - 1.5u keys for thumbs
 - Includes mountplate
 - Standard ProMicro support (Note that it's wireless only, so use a compatible MCU with Bluetooth connectivity)


In short, this design is heavily inspired by the [Ferris](https://github.com/pierrechevalier83/ferris) (or more specifically, the [Sweep](https://github.com/davidphilipbarr/Sweep)). This keyboard is very similar with a few key design differences:
 - Stagger adjusted for hands that have a short index finger
 - Outer columns are splayed
 - Removed one key from innermost column and outermost column.
 - Choc Mini support
 - Larger thumbkeys (1.5u)
 - Designed for wireless operation **only**
 - Includes mountplate
 
 
### Information

**Main PCB thickness:** 1.6mm
**Mount plate thickness:** 1.6mm
Mount plate is mostly for making the design sturdier and holding keys in place a bit better.
**Connector:** Molex PicoBlade 2-pin horizontal (Often mislabeled as Micro JST in stores)
**Key switches:** Kailh Choc Mini PG1232 (https://www.aliexpress.com/item/4000277394324.html)
Personal note: Try using 35g springs with linear (black) motion.
**MCU sockets:** Mill-Max Interconnect Machined Pin Socket. Pitch 2.54mm. Height above PCB: 7mm. Part no. 801-XX-XXX-10-001000. You need at least 12 pins wide, any more can be broken off.
**Underside material:** Neoprene (need actual testing still)
**Keycaps:** MBK profile Choc (https://splitkb.com/collections/switches-and-keycaps/products/blank-mbk-choc-low-profile-keycaps)
**Power switch:** 7-pin micro SPDT
**MCU:** nice!nano
Xiao Seeed was considered for its smaller size, but since battery is mounted under the MCU, the battery would have to become too small anyways.
**MCU socket pins:** Mill-Max gold pins. Part no. 3320-0-00-15-00-00-03-0. (https://splitkb.com/collections/keyboard-parts/products/mill-max-low-profile-sockets?variant=32170972020813)
These could be thicker / longer, fit is not very good.



### Instructions

The MCU has to be mounted **face down** by default.

By default, all jumpers need to be shorted on the **opposite side** of where components are mounted.




### Future design work
I intend to keep iterating on this design over time, here are a few ideas I would like to eventually realize:
 - Add wired connectivity (but only if I, or a number of users request it)
 - Remove a key from the pinky column
 - **Possiby** try out a very low profile rotary encoder
 - Tighter vertical keyspacing (would require custom keycap work)
 - Choc Mini support
 - Add instructions for automatically routing the PCB

Other than that, I'll probably make adjustments to the stagger and key placement over time.

### Configuration 

While this is currently configured to fit my hands specifically, I am very much interested in creating a very parametric design. I try to keep the .yaml file commented enough to easily understand how to modify it. For instance, you could easily switch to using MX spacing by modifying the lines
```yaml
  keyspacingx: cx
  keyspacingy: cy
```
to
```yaml
  keyspacingx: u
  keyspacingy: u
```
and even switch to MX switch footprints by finding the YAML variable named `key_footprints`. Other configurable values currently include margin around key switches, rotation of the home thumbkey. I plan to add more of configuration in the future.
