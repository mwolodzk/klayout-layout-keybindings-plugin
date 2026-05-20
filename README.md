# KLayout Layout Keybindings Plugin

`Layout Keybindings Plugin` adds a Help entry that opens a graphical keyboard map for layout editing shortcuts in KLayout.

The current macro is tuned for the IHP SG13G2 environment and highlights both built-in KLayout actions and advanced Salt-based tools such as Align, Center Ruler, Selection Dim, Instance Freeze, and Snap Mode switching. The plain `M` binding is kept on KLayout's interactive built-in Move mode.

## Features

- Adds `Help -> Show Layout Keybindings`
- Opens a floating, non-modal shortcut guide window
- Presents a visual keyboard layout instead of a plain text list
- Documents advanced bindings layered on top of KLayout defaults
- Documents `Ctrl+H` for Search and Replace and Instance Freeze shortcuts
- Includes modifier combinations and a legend for action categories

## Installation

### From Salt.Mine

Install `Layout Keybindings Plugin` from Salt once the package is published.

### Manual install

Copy this repository into your KLayout Salt directory so that `grain.xml` sits at the package root:

```text
~/.klayout/salt/LayoutKeybindingsPlugin/
```

KLayout will discover the package automatically on next start.

## Files

- `grain.xml`: Salt package metadata
- `pymacros/show_layout_keybindings.lym`: Help macro implementation

## Notes

- The plugin was written by OpenAI Codex, GPT-5.4 default, in a live coding session for Michał Wołodźko.
- Functional behavior was verified in vivo by Michał Wołodźko in his KLayout environment.
- The window is intentionally non-modal so the guide can stay open while editing the layout.

## License

MIT
