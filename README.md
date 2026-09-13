# 🎨 ModernUI Library

> A lightweight, modern Roblox UI library for script hubs — with a draggable floating hexagon button, safe CoreGui parenting, and full mobile support.

[![Version](https://img.shields.io/badge/Version-2.0.0-green.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Roblox](https://img.shields.io/badge/Roblox-Executor-red.svg)]()

---

## 📖 About

**ModernUI** is a clean, executor-friendly UI library for building Roblox script hubs. It ships with:

- ⚡ **Fast performance** — minimal overhead, tween-based animations
- 📱 **Mobile support** — sliders and buttons work on touch devices
- 🎯 **Floating hexagon button** — restore minimized/hidden UI instantly
- 🛡️ **Safe CoreGui fallback** — works on executors that restrict CoreGui
- 🎨 **Accent color system** — fully themeable
- 🔔 **Notification system** — stackable, auto-fading toasts

---

## 🚀 Quick Start

```lua
-- 1. Load the library
local Library = loadstring(game:HttpGet("YOUR_RAW_LINK_HERE"))()

-- 2. Create the window
local Window = Library:CreateWindow({
    Name           = "My Script",
    Keybind        = Enum.KeyCode.RightControl,
    Accent         = Color3.fromRGB(90, 70, 220),
    FloatingButton = true
})

-- 3. Create a tab
local Tab = Window:CreateTab("Main")

-- 4. Create a section
local Section = Tab:CreateSection("Example")

-- 5. Add elements
Section:CreateParagraph("This is a paragraph.")
Section:CreateToggle("Enable Feature", false, function(state)
    print("Toggle:", state)
end)
Section:CreateButton("Click Me", function()
    Window:Notify({
        Title = "Success",
        Content = "Button clicked!",
        Duration = 3
    })
end)
