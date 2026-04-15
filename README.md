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

## Layout

- 5x6, 6x6, or 7x7 matrix (12 or 14 pins)
- joystick (X, Y, button click -- 3 pins)
- Optional OLED SPI Display (5-6 pins)
- total: 20-22 pins. Safe side: 24 pins

Probably need an RP2040, easiest to use a Pi Pico.

---

## Other features

- Transparent OLED screen to display stratagem input directions when pressed
- Sound effects through a speaker (on the board) when directional arrows are pressed on the board

---

## Learning

- handwiring keyboards guide: https://www.youtube.com/watch?v=hjml-K-pV4E
