---
title: Midified
description: A Mac app in the menu bar turning your MIDI controllers into the keyboard.
url_en: /midified/
url_ja: /midified/ja/
---

# Midified

A Mac app in the menu bar turning your MIDI controllers into the keyboard. Put a complex shortcut on a key or a pad, seek through the timeline of a video editor by turning a knob, and more, in any app, by a config you write in Ruby.

## How to Use

- Allow Midified in System Settings > Privacy & Security > Accessibility, when asked the first time, for it to send the keys.
- Choose "Open Config" from the menu in the menu bar, and map the notes and the controllers to the keys:

```ruby
note 36 => :space                 # holds Space while the note is on
note 37 => command(:b)            # Command+B
note 38 => shift(command(:z))     # Shift+Command+Z

cc 20 do |value|                  # each change of a knob, 0..127
  key(value < 64 ? :left : :right)
end
```

- Save the config, and it is loaded again by itself.
- Choose "Show MIDI Monitor" to see the names of your devices, the numbers of the pads and the knobs you touch, and the keys sent.

## FAQ

### The keys are not sent.

If the icon in the menu bar is dimmed under an exclamation mark, the menu tells why at its top: choose the item to allow Midified in the settings, or to see the error of the config in the MIDI Monitor.

### I allowed Midified, but the keys are not sent yet.

The version of the Mac App Store finds the permission only when launched again: choose "Relaunch Midified" from the menu.

### Where is my config kept?

On your Mac, in the app's own data folder. "Open Config" opens it. See the [Privacy Policy](/midified/privacy_policy.html).

## Support

For questions, problems or suggestions, write to [support@xord.org](mailto:support@xord.org).
Including the versions of Midified and macOS, and the name of your MIDI device, helps.

- [Privacy Policy](/midified/privacy_policy.html)

----

&copy; 2026 xord.org
