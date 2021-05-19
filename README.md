### ImGui Documentation
#### Initialization
```lua
function get_library()
    repeat wait() until game:IsLoaded()
    pcall(function()loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/VM-Voxel/vm-scripts/master/UI-Library.lua"))() end)
end
```
#### Library
```lua
local Library = get_library()
```
#### Library Window
```lua
local Window = Library:CreateWindow("Example")
```
#### Library Tab
```lua
local ExampleTab = Window:CreateTab("Example")
```
#### Library Groupbox
```lua
local ExampleGroupbox = ExampleTab:CreateGroupbox("Example", "Left") -- Side: Left or Right
```
#### Library Toggle
```lua
local ExampleToggle = ExampleGroupbox:CreateToggle("Example", function(bool)
    if bool then
        return print("True")
    else
        return print("False")
    end
end)
```
#### Library Button
```lua
local ExampleButton = ExampleGroupbox:CreateButton("Example", function()
    return print("Pressed!")
end)
```
