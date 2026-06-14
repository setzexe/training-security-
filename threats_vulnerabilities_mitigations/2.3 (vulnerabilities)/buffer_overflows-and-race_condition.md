# Buffer Overflows

Buffer overflow is just the concept of memory with a fixed size spilling information into another memory. This happens when that fixed memory gets too much information added to it.

Developers perform bounds checks alot. Making sure inputs on byte-size is fine, sanitizing input, seeing what happens if buffer overflow happens, so on and so forth.

The main objective of buffer overflow is to be able to repeat a function (or a set of them) consistently. A good buffer overflow will do the same thing over and over with consistent results and inputs. If this does something that gives the attacker advantage, buffer overflow becomes dangerous here. It is not necessarily something that is done at random or inconsistently; adding too much info may crash the system or just provide completely unwanted results.

# Race Condition

Race condition is when two events occur at the same time and the application does not really know what to do based on this.

A real world example of this (and quite a notable one) is the *Spirit* Mars Rover in 2004. The race condition worked like this:
- The rover had an automatic safe mode reboot sequence if it thought that something was going wrong.
- At the same time, the rover has to naturally save data in its buffer / flash memory.
- The OS was running these two at the same time and it got out of order. 
  - The reboot sequence check would see the file system as a threat and would reboot; this would happen everytime it did reboot.
  - Thus, the rover was stuck in a reboot loop.