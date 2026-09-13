# 🎨 Edu UI Library

> A lightweight, modern Roblox UI library for building script hubs — clean API, fast performance, and easy to use.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Roblox](https://img.shields.io/badge/Roblox-Script-red.svg)](https://www.roblox.com/)
[![Version](https://img.shields.io/badge/Version-1.0.0-green.svg)]()

---

## 📖 About

**Edu UI** is a rebuilt and optimized UI library designed for Roblox script hubs. It focuses on:

- ⚡ **Fast performance** — minimal overhead, low memory footprint
- 🎨 **Modern design** — clean squircle elements, smooth tweens
- 🔧 **Simple API** — intuitive method names, easy to learn
- 🌓 **Themeable** — dark/light themes out of the box
- 📱 **Mobile support** — works on touch devices

---

## 🚀 Quick Start

```lua
-- 1. Load the library
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/nfcbadal-cyber/Edu-Scripts-hub/refs/heads/main/Edu%20UI"))()

-- 2. Create the main window
local Window = Library:CreateWindow({
    Name    = "My Script",
    Keybind = Enum.KeyCode.RightControl -- toggle UI with this key
})

-- 3. Create a tab
local Tab = Window:CreateTab("Main")

-- 4. Create a section inside the tab
local Section = Tab:CreateSection("Example")

-- 5. Add elements
Section:CreateParagraph("This is a paragraph / description text.")

Section:CreateToggle("Enable Something", function(value)
    print("Toggle:", value)
end)

Section:CreateSlider("WalkSpeed", 16, 200, 16, function(value)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
end)

Section:CreateDropdown("Choose Mode", {"Normal", "Fast", "Insane"}, function(option)
    print("Selected:", option)
end)

Section:CreateTextbox("Enter username...", function(text)
    print("Textbox:", text)
end)

Section:CreateButton("Kill All", function()
    print("Button clicked!")
end)

Section:CreateLabel("This is a small label")
