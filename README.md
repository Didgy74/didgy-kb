# didgy-kb
A catch-all repo for any keyboards I design.

These designs are all designed with [Ergogen](https://github.com/ergogen/ergogen).

# Mitten
**Proper real-life image coming soon**

**Note: This design has not been tested yet**
![Mitten layout](https://user-images.githubusercontent.com/25203601/156046583-952bedf7-c728-4c2f-b3b5-7066d6396dc0.png)

**Note: The following PCB is slightly outdated**
![image](https://user-images.githubusercontent.com/25203601/156047663-6b54d818-8cf3-40c7-9c49-15d928bcadfc.png)


This design has the following properties:
 - 32 keys (5 columns, 3 rows with one row missing 1 key, plus 2 thumbkeys, per hand)
 - Split
 - Columnar stagger
 - Column splay on the outer columns
 - Wireless
 - Hot-swappable
 - Reversible PCB
 - Low profile (Choc V1)
 - Choc spacing
 - Uses primarily 1u keys, with a 1.5u home thumbkey.
 - Includes mountplate
 - Standard ProMicro support (Note that it's wireless only, so use a compatible MCU with Bluetooth connectivity)


In short, this design is heavily inspired by the [Ferris](https://github.com/pierrechevalier83/ferris) (or more specifically, the [Sweep](https://github.com/davidphilipbarr/Sweep). This keyboard is very similar with a few key design differences:
 - Stagger adjusted for hands that have a short index finger
 - Outer columns are splayed
 - Removed one key from innermost column, and heavily increased columnar stagger of that column
 - Choc V1 hotswap sockets
 - Larger home thumbkey (1.5u)
 - Designed for wireless operation **only**
 - Includes mountplate

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
