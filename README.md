# LiberationBoard

DISCLAIMER:
This project has no political implications or affiliations, and is not linked to any one party _in any way_. The name of the board is derived from the fact that I'm building a keyboard specifically for Helldivers 2, which is a fictional game.

With that out the way, let's dig in!

## Structure

- QMK Keyboard
- Gamepad
- combined

Yeah that's basically the idea.

Currently, I won't promise anything other than the above. I have a ton of ideas on how this could be implemented, but I'd rather focus on prototyping and figuring things out by _doing_ rather than my previous approaches, which led to demotivation and burnout. So I'll document as I go along instead of document ahead of time and lose interest. Let's see how this goes, I guess!

## Components

- Cherry MX-like mechanical switches (likely Durock or Gateron based on preference)
- MCU (likely RPi Pico w/ RP2040 architecture)
- Diodes (1N4148)
- Joystick (end goal would likely be low profile joycon-like TMR / Hall Effect stick, and concave thumb cap for non-held grip)
  - by default, joysticks have convex caps for better grip when the controller is held. However, this is a keyboard, not a controller, so it's seated on the desk and not held. I need something to cup my thumb more-so than protrude for better grip.
  - found recommendations online of Skull & Co. joystick cap addons, can check that out later
- 

## Layout

- 5x6, 6x6, or 7x7 matrix (12 or 14 pins)
- joystick (X, Y, button click -- 3 pins)
- Optional OLED SPI Display (5-6 pins)
- total: 20-22 pins. Safe side: 24 pins

Probably need an RP2040, easiest to use a Pi Pico.

---

## Other features (scope creep)

- Transparent OLED screen to display stratagem input directions when pressed. https://docs.qmk.fm/features/oled_driver
- Sound effects through a speaker (on the board) when directional arrows are pressed on the board. because that's possible. https://docs.qmk.fm/features/audio
  - with an RP2040 architecture, I'd likely need a DAC, and load game sounds on the board itself
- Haptics
  - feedback on gamepad rumble
  - feedback on... other stuff? I dunno

- Vertical variant
  - basically have the keypad near vertically mounted, and the joystick on the underside, such that my hand is tilted at a >45° angle and my thumb is on the underside to control the joystick
  - This is a very whacky idea, but would be cool to see it just to see it

- Azeron Cyborg II clone layout
  - basically like an Azeron Cyborg II, using extremely small switches, and directionality on _every finger_, instead of just a single press button on a flat layout
  - Specifically needing four-directional button switches on every finger PLUS press-down, which provides 5 potential actuations per finger
  - Ergonomics may suffer for this due to mechanical spacing... further prototyping required.
- Actually on second thought, it might be a lot closer to the DataHand keyboard style
  - resources:
    - https://octopup.org/computer/datahand
    - https://github.com/JesusFreke/lalboard
  - upon some research, I feel like going with a hall-effect switch system per-direction per-finger would likely be the ideal -- and the press-down would be good as hall-effect too, but I could also get away with just a mechanical switch here if I get lazy
  - Regardless, the bottom line is something like this would easily take a significant lot more effort and research and learning to implement than simply "ooh boy, just refactor it a little bit and it's golden!"

---

## Learning

- handwiring keyboards guide: https://www.youtube.com/watch?v=hjml-K-pV4E
  - further resources: https://docs.qmk.fm/hand_wire

