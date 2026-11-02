# Callbot now reads your Mac in a tenth of a second

*2 November 2026*

An assistant that works on your computer is only as good as its hands. It has to see the window, find the button and type.
Until today, Callbot's hands were slow: reading one Finder window took 1–2 seconds, because every look went through
a scripting layer that asked macOS about each button and label one at a time.

**We wrote Callbot its own hands.** A small native helper stays running next to the assistant and talks to macOS directly.
It reads a whole window in one pass, the same way screen readers for blind people do. Clicks and keys go in as ordinary
system events, like a real mouse and keyboard.

**Measured on a real MacBook**

| | Before | Now |
|---|---|---|
| Read a Finder window | 1.1–2.3 s | **0.11 s** |
| Read a Cursor window | ~0.2 s, saw 4 elements | **0.013 s**, sees 78 |
| Which app is in front | 0.64 s | **0.005 s** |
| Type 30 characters | ~0.5 s | **0.055 s** |
| Unread badges on the Dock | 7.5 s | **under 0.1 s** |

**Why it is cheaper, not only faster**

Many computer-use agents take a screenshot at every step and send the picture to a vision model. Callbot reads the window
as text instead: names, buttons and fields with their positions. A step costs a short piece of text, not an image, so the
same task runs on fast, inexpensive models. A screenshot remains the fallback for the rare window that has no readable text.

**Small things we fixed on the way**

- WhatsApp on the Mac puts an invisible direction mark in front of its own name and every label. The helper now drops all
  invisible characters, so a contact called «Nikita Savin» is found as «Nikita Savin».
- A new message gets an answer after a minute or two, the way a person would reply, instead of in the same second.
  If you read it on your phone first, the assistant leaves it to you.
- A task you delete is gone for good. It no longer comes back to the queue when it finishes in the background.
- Your direct order is your yes: «write to Anna in WhatsApp: …» sends it without asking again. A recipient you never named still
  waits for your approval.

Every Mac with Callbot received this update over the air in about a minute, with no reinstall.

Try it at [callbot.wecomax.com](https://callbot.wecomax.com).

— Nikita, founder of Wecomax
