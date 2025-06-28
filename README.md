# Raven UI

Simple UI library for Roblox with tabs and smooth animations.

## How to use

Load the UI library in your Roblox game with this snippet:

```lua
local UILibraryURL = "https://raw.githubusercontent.com/WinzeTim/Raven/refs/heads/main/ui.lua"

local success, UILibraryCode = pcall(function()
    return game:HttpGet(UILibraryURL)
end)

if success then
    local UILibrary = loadstring(UILibraryCode)()
    
    -- Create the UI instance
    local ui = UILibrary.new()
    
    -- Create tabs
    ui:CreateTab("Home")
    ui:CreateTab("Settings")
    
    ui:Show()
else
    warn("Failed to load UI library")
end
