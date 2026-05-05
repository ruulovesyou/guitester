========================================
CK_UIO Modules Index
Last Refresh: from LABS/CK_UIO/d.txt extracts
========================================

Folders
- containers/
- elements/
- framework/
- helpers/

Module Files

containers
- containers/Category.txt
- containers/ConfigTab.txt
- containers/Section.txt
- containers/Tab.txt
- containers/UserSettings.txt
- containers/Window.txt

elements
- elements/Button.txt
- elements/ColorPicker.txt
- elements/Dropdown.txt
- elements/Keybind.txt
- elements/Paragraph.txt
- elements/Slider.txt
- elements/TextBox.txt
- elements/Toggle.txt

framework
- framework/ColorPickerPanel.txt
- framework/ConfigManager.txt
- framework/KeybindHandler.txt
- framework/KeybindHUD.txt
- framework/LoadDropdown.txt
- framework/LoadElement.txt
- framework/Loader.txt
- framework/MiniElements.txt
- framework/Notify.txt
- framework/Theme.txt
- framework/Watermark.txt

helpers
- helpers/BlurEffect.txt
- helpers/FileSystemPolyfill.txt
- helpers/Globals.txt
- helpers/Helpers.txt
- helpers/LucideIcons.txt
- helpers/Types.txt

Dependency Map (high-level)

- helpers/Types.txt
  - Used by: helpers/Globals.txt, framework/*, containers/*, elements/*

- helpers/Globals.txt
  - Provides: service refs, base `Compkiller`, color table, element registries
  - Used by: all framework/container/element modules

- helpers/FileSystemPolyfill.txt
  - Provides: studio-safe `readfile`, `writefile`, `listfiles`, `makefolder`, `delfile`
  - Used by: framework/ConfigManager.txt

- helpers/BlurEffect.txt
  - Provides: blur/acrylic effect updater tied to window visibility
  - Used by: containers/Window.txt (window visual behavior)

- framework/Theme.txt
  - Provides: theme presets + color refresh/update API
  - Used by: UI drawing modules in framework/containers/elements

- framework/Notify.txt
  - Provides: notification GUI constructor/cache and notification instances
  - Used by: framework/ConfigManager.txt and any action modules that notify

- framework/Loader.txt
  - Provides: intro/loading animation sequence
  - Used by: startup/bootstrap flow

- framework/ConfigManager.txt
  - Depends on: helpers/FileSystemPolyfill.txt, helpers/Globals.txt, framework/Notify.txt
  - Used by: containers/ConfigTab.txt

- framework/ColorPickerPanel.txt
  - Used by: elements/ColorPicker.txt

- framework/LoadElement.txt, framework/LoadDropdown.txt, framework/MiniElements.txt
  - Provide element construction helpers
  - Used by: elements/* and containers/*

- framework/KeybindHandler.txt, framework/KeybindHUD.txt
  - Provide keybind logic + HUD rendering
  - Used by: elements/Keybind.txt and runtime input handling

- framework/Watermark.txt
  - Provides watermark UI helper
  - Used by: containers/Window.txt / startup UI
