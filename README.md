local DrRayLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/AZYsGithub/DrRay-UI-Library/main/DrRay.lua"))()
local window = DrRayLibrary:Load("Supportsema", "Default")

local tab = DrRayLibrary.newTab("esp", "ImageIdHere")

tab.newButton("esp", "bestuniversal", function()
  loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Exunys-ESP-7126"))()
end)

tab.newButton("OP esp", "use esp", function()
  loadstring(game:HttpGet(('https://raw.githubusercontent.com/cool83birdcarfly02six/UNIVERSALESPLTX/main/README.md'),true))()
end)

tab.newButton("toolesp", "don't workoryes", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/ZTixsB3N'))()
end)

tab.newButton("chams", "don't workoryes", function()
  local FillColor = Color3.fromRGB(175,25,255)
local DepthMode = "AlwaysOnTop"
local FillTransparency = 0.5
local OutlineColor = Color3.fromRGB(255,255,255)
local OutlineTransparency = 0

local CoreGui = game:FindService("CoreGui")
local Players = game:FindService("Players")
local lp = Players.LocalPlayer
local connections = {}

local Storage = Instance.new("Folder")
Storage.Parent = CoreGui
Storage.Name = "Highlight_Storage"

local function Highlight(plr)
    local Highlight = Instance.new("Highlight")
    Highlight.Name = plr.Name
    Highlight.FillColor = FillColor
    Highlight.DepthMode = DepthMode
    Highlight.FillTransparency = FillTransparency
    Highlight.OutlineColor = OutlineColor
    Highlight.OutlineTransparency = 0
    Highlight.Parent = Storage
    
    local plrchar = plr.Character
    if plrchar then
        Highlight.Adornee = plrchar
    end

    connections[plr] = plr.CharacterAdded:Connect(function(char)
        Highlight.Adornee = char
    end)
end

Players.PlayerAdded:Connect(Highlight)
for i,v in next, Players:GetPlayers() do
    Highlight(v)
end

Players.PlayerRemoving:Connect(function(plr)
    local plrname = plr.Name
    if Storage[plrname] then
        Storage[plrname]:Destroy()
    end
    if connections[plr] then
        connections[plr]:Disconnect()
    end
end)
end)

tab.newButton("aimbot", "bestuniversal", function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/Avtor1zaTion/AimBot-Fov/main/Aimbot%20Fov", true))()
end)

tab.newButton("hitboxhead", "bestuniversal", function()
  loadstring(game:HttpGet("https://github.com/RectangularObject/UniversalHBE/releases/latest/download/main.lua", true))()
end)

local tab = DrRayLibrary.newTab("miscellaneous", "ImageIdHere")

tab.newButton("infjump", "bestuniversal", function()
  loadstring(game:HttpGet("https://pastefy.app/o3x1u9ZN/raw"))()
end)

tab.newButton("chinahat", "bestuniversal", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/TePYk91W'))()
end)

tab.newButton("fov 120", "bestuniversal", function()
 local FovNumber = 120 --Enter your FOV number here
local Camera = workspace.CurrentCamera
Camera.FieldOfView = FovNumber
end)

tab.newButton("4:3", "bestuniversal", function()
  local camera = workspace.CurrentCamera
local settings = {
    ["Aspect Ratio"] = true, --// leave it like this if i don't know what You're doing
    ["Ratio Value"] = 0.6 --// leave it like this if i don't know what You're doing
}

local oldNewindex

oldNewindex = hookmetamethod(game, "__newindex", function(object, propertyName, propertyValue)
    if object == camera and propertyName == "CFrame" then
        if settings["Aspect Ratio"] then
            propertyValue = propertyValue * CFrame.new(0, 0, 0, 1, 0, 0, 0, settings["Ratio Value"], 0, 0, 0, 1)
        end
    end
    return oldNewindex(object, propertyName, propertyValue)
end)
end)

tab.newToggle("fullbright", "Toggle! (Work)", true, function(toggleState)
  loadstring(game:HttpGet('https://pastebin.com/raw/K6LifFtr'))()   
end)

tab.newButton("rtxgui", "bestuniversal", function()
  loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/RTX%20Gui%20Hub%20Obfuscator'))()

-- rtx wit no lag
end)

tab.newButton("noclip", "bestuniversal", function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/FransizALWAYS/NoClip/refs/heads/main/V1"))()
end)

tab.newButton("teleporttoplayer", "bestuniversal", function()
  local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui")
gui.Name = "TeleportGui"
gui.Parent = player.PlayerGui

local frame = Instance.new("Frame")
frame.Name = "TeleportFrame"
frame.Size = UDim2.new(0, 200, 0, 150)
frame.Position = UDim2.new(0.5, -100, 0.5, -75)
frame.BackgroundColor3 = Color3.new(1, 1, 1)
frame.Parent = gui

local textBox = Instance.new("TextBox")
textBox.Name = "TeleportTextBox"
textBox.Size = UDim2.new(0, 180, 0, 30)
textBox.Position = UDim2.new(0.5, -90, 0, 10)
textBox.Text = "Enter player name"
textBox.Parent = frame

local teleportButton = Instance.new("TextButton")
teleportButton.Name = "TeleportButton"
teleportButton.Text = "Teleport"
teleportButton.Size = UDim2.new(0, 150, 0, 50)
teleportButton.Position = UDim2.new(0.5, -75, 1, -60)
teleportButton.Parent = frame

frame.Active = true
frame.Draggable = true

local function teleportAndJump()

    local targetPlayerName = textBox.Text

    local targetPlayer = game.Players:FindFirstChild(targetPlayerName)
    if targetPlayer then

        player.Character.HumanoidRootPart.CFrame = targetPlayer.Character.HumanoidRootPart.CFrame

        wait(0.3)
        player.Character.Humanoid.Jump = true
    end
end

teleportButton.MouseButton1Click:Connect(function()
    teleportAndJump()
end)
end)

local tab = DrRayLibrary.newTab("espitem", "ImageIdHere")

tab.newButton("bearEsp", "bestuniversal", function()
  -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.Animals, { -- Object Path, For example: Workspace.ThisFolder
    Name = "Bear", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "Bear", -- Name you want to be displayed
    Color = Color3.fromRGB(200, 100, 200), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
})
ESP.whatever = true
end)



tab.newButton("antikick", "use", function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/Exunys/Anti-Kick/main/Anti-Kick.lua"))()
end)

tab.newButton("copterEsp", "bestuniversal", function()
   -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.Minicopter, { -- Object Path, For example: Workspace.ThisFolder
    Name = "Base", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "copter", -- Name you want to be displayed
    Color = Color3.fromRGB(140, 0, 10), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
})
ESP.whatever = true
end)

tab.newButton("wardrobe", "esp", function()
  -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.Builds, { -- Object Path, For example: Workspace.ThisFolder
    Name = "ToolCupboardModel", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "Wardrobe", -- Name you want to be displayed
    Color = Color3.fromRGB(0, 200, 150), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
})
ESP.whatever = true
end)

tab.newButton("Hemp", "esp", function()
  -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.Hemp, { -- Object Path, For example: Workspace.ThisFolder
    Name = "Hemp", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "Hemp", -- Name you want to be displayed
    Color = Color3.fromRGB(0, 200, 150), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
})
ESP.whatever = true
end)

tab.newButton("sulfur", "esp", function()
  -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.ores, { -- Object Path, For example: Workspace.ThisFolder
    Name = "Sulfur", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "Sulfur", -- Name you want to be displayed
    Color = Color3.fromRGB(0, 200, 150), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
})
ESP.whatever = true
end)

tab.newButton("stone", "esp", function()
  -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.ores, { -- Object Path, For example: Workspace.ThisFolder
    Name = "stone", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "stone", -- Name you want to be displayed
    Color = Color3.fromRGB(0, 200, 150), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
 })
ESP.whatever = true
end)

tab.newButton("iron", "esp", function()
  -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = false
ESP.Names = true
ESP:Toggle(true)

-- object
ESP:AddObjectListener(Workspace.ores, { -- Object Path, For example: Workspace.ThisFolder
    Name = "iron", --Object name inside of the path, for example: Workspace.ThisFolder.Item_1
    CustomName = "iron", -- Name you want to be displayed
    Color = Color3.fromRGB(0, 200, 150), -- Color
    IsEnabled = "whatever" -- Any name, has to be the same as the last line: ESP.TheNameYouWant
})
ESP.whatever = true
end)

tab.newButton("military crate", "esp LAG!", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/txZYECdu'))()
end)

tab.newButton("loot crate", "esp LAG!", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/U12AvQcB'))()
end)

local tab = DrRayLibrary.newTab("anticheatbypass", "ImageIdHere")

tab.newButton("Walkspeed", "BYPASS ANTICHEAT", function()
  game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 25
end)

tab.newButton("unwalkspeed", "BYPASS ANTICHEAT", function()
  game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
end)

tab.newButton("Spinbot", "BYPASS ANTICHEAT", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/Pqve0wi8'))()
end)

tab.newButton("unSpinbot", "BYPASS ANTICHEAT", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/Ne2FCBAD'))()
end)
