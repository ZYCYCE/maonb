local WindUI = loadstring(game:HttpGet("https://raw.githubusercontent.com/Footagesus/WindUI/main/dist/main.lua"))()

WindUI.TransparencyValue = 0.2
WindUI:SetTheme("Dark")
local function gradient(text, startColor, endColor)
    local result = ""
    for i = 1, #text do
        local t = (#text == 1) and 0 or (i - 1) / (#text - 1)
        local r = math.floor((startColor.R + (endColor.R - startColor.R) * t) * 255)
        local g = math.floor((startColor.G + (endColor.G - startColor.G) * t) * 255)
        local b = math.floor((startColor.B + (endColor.B - startColor.B) * t) * 255)
        result = result .. string.format('<font color="rgb(%d,%d,%d)">%s</font>', r, g, b, text:sub(i, i))
    end
    return result
end

local Window = WindUI:CreateWindow({
    Title = "猫帝脚本",
    Icon = "zap",
    Folder = "LinUI",
    Size = UDim2.fromOffset(550, 350),
    Background = WindUI:Gradient({
        ["0"] = { Color = Color3.fromHex("#1a1a2e"), Transparency = 1 },
        ["100"] = { Color = Color3.fromHex("#16213e"), Transparency = 0.9 },
    }, {
        Rotation = 135,
    })
})

Window:Tag({
    Title = "猫帝大王",
    Color = Color3.fromHex("#FF6B9D")
})

local section = Window:Section({ 
    Title = "通用",
    Opened = true 
})

local tab = section:Tab({ 
    Title = "功能"
})

tab:Slider({
    Title = "移动速度",
    Value = {
        Min = 16,
        Max = 10000000,
        Default = game.Players.LocalPlayer.Character.Humanoid.WalkSpeed
    },
    Step = 1,
    Callback = function(Value)
        spawn(function() 
            while task.wait() do 
                game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value 
            end 
        end)
    end
})

tab:Slider({
    Title = "跳跃高度",
    Value = {
        Min = 50,
        Max = 10000,
        Default = 50
    },
    Step = 1,
    Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
    end
})

tab:Slider({
    Title = "重力",
    Value = {
        Min = 198,
        Max = 999999999,
        Default = 198
    },
    Step = 1,
    Callback = function(Value)
        game.Workspace.Gravity = Value
    end
})

tab:Toggle({
    Title = "夜视",
    Value = false,
    Callback = function(Light)
        spawn(function() 
            while task.wait() do 
                if Light then 
                    game.Lighting.Ambient = Color3.new(1, 1, 1) 
                else 
                    game.Lighting.Ambient = Color3.new(0, 0, 0) 
                end 
            end 
        end)
    end
})

tab:Toggle({
    Title = "穿墙",
    Value = false,
    Callback = function(NC)
        local Workspace = game:GetService("Workspace")
        local Players = game:GetService("Players")
        local RunService = game:GetService("RunService")
        
        if Stepped then
            Stepped:Disconnect()
            Stepped = nil
        end
        
        if NC then
            Clipon = true
            Stepped = RunService.Stepped:Connect(function()
                local character = Players.LocalPlayer.Character
                if character and Clipon then
                    for _, v in ipairs(character:GetDescendants()) do
                        if v:IsA("BasePart") then
                            v.CanCollide = false
                        end
                    end
                end
            end)
        else
            Clipon = false
            local character = Players.LocalPlayer.Character
            if character then
                for _, v in ipairs(character:GetDescendants()) do
                    if v:IsA("BasePart") then
                        v.CanCollide = true
                    end
                end
            end
        end
    end
})

tab:Toggle({
    Title = "无限跳",
    Value = false,
    Callback = function(Value)
        Jump = Value
        game.UserInputService.JumpRequest:Connect(function()
            if Jump then
                game.Players.LocalPlayer.Character.Humanoid:ChangeState("Jumping")
            end
        end)
    end
})

tab:Button({
    Title = "r6撸管",
    Callback = function()
loadstring(game:HttpGet("https://pastefy.app/wa3v2Vgm/raw"))()
   end
})

tab:Button({
    Title = "r15撸管",
    Callback = function()
loadstring(game:HttpGet("https://pastefy.app/YZoglOyJ/raw"))()
  end
})


tab:Button({
    Title = "无敌少侠",
    Callback = function()
loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Invinicible-Flight-R15-45414"))()
  end
})

tab:Button({
    Title = "隐身",
    Callback = function()
loadstring(game:HttpGet('https://pastebin.com/raw/3Rnd9rHf'))()
  end
})

tab:Input({
    Title = "头部范围",
    Value = "",
    Callback = function(v)
        _G.HeadSize = v
        _G.Disabled = true
        game:GetService('RunService').RenderStepped:connect(function()
            if _G.Disabled then
                for i,v in next, game:GetService('Players'):GetPlayers() do
                    if v.Name ~= game:GetService('Players').LocalPlayer.Name then
                        pcall(function()
                            v.Character.Head.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
                            v.Character.Head.Transparency = 1
                            v.Character.Head.BrickColor = BrickColor.new("red")
                            v.Character.Head.Material = "Neon"
                            v.Character.Head.CanCollide = false
                            v.Character.Head.Massless = true
                        end)
                    end
                end
            end
        end)
    end
})

tab:Input({
    Title = "攻击范围修改",
    Value = "",
    Callback = function(value)
        _G.HeadSize = value
        _G.Disabled = true
        game:GetService('RunService').RenderStepped:connect(function()
            if _G.Disabled then
                for i,v in next, game:GetService('Players'):GetPlayers() do
                    if v.Name ~= game:GetService('Players').LocalPlayer.Name then
                        pcall(function()
                            v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
                            v.Character.HumanoidRootPart.Transparency = 0.7
                            v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really red")
                            v.Character.HumanoidRootPart.Material = "Neon"
                            v.Character.HumanoidRootPart.CanCollide = false
                        end)
                    end
                end
            end
        end)
    end
})

tab:Button({
    Title = "关闭攻击范围",
    Callback = function()
        _G.HeadSize = 1
        _G.Disabled = true
        game:GetService('RunService').RenderStepped:connect(function()
            if _G.Disabled then
                for i,v in next, game:GetService('Players'):GetPlayers() do
                    if v.Name ~= game:GetService('Players').LocalPlayer.Name then
                        pcall(function()
                            v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
                            v.Character.HumanoidRootPart.Transparency = 0.7
                            v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really red")
                            v.Character.HumanoidRootPart.Material = "Neon"
                            v.Character.HumanoidRootPart.CanCollide = false
                        end)
                    end
                end
            end
        end)
    end
})


local section = Window:Section({ 
    Title = "服务器",
    Opened = true 
})

local tab = section:Tab({ 
    Title = "力量传奇"
})

tab:Button({
    Title = "安脚本",
    Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Anscripterato/QQ2134702438/refs/heads/main/byato/AnScript/atoscript"))()
    end
})

tab:Toggle({
    Title = "自动抽奖",
    Value = false,
    Callback = function(state)
        while state do
            game:GetService("ReplicatedStorage").rEvents.openFortuneWheelRemote:InvokeServer("openFortuneWheel", game:GetService("ReplicatedStorage").fortuneWheelChances:FindFirstChild("Fortune Wheel"))
            wait(0.1)
        end
    end
})

tab:Toggle({
    Title = "自动购买暗星猎人",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Darkstar Hunter"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买以太仙灵兔子",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Aether Spirit Bunny"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买肌肉王光环",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Muscle King"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买赛博对决龙",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Cybernetic Showdown Dragon"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买霓虹守护者",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Neon Guardian"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买熵爆 光环",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Entropic Blast"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买肌肉老师",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Muscle Sensei"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买地狱火龙",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Inferno Dragon"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买黑暗闪电 光环",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Black Lightning"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "自动购买黑暗风暴 光环",
    Value = false,
    Callback = function(state)
        Interstellar.Main = state
        if Interstellar.Main then
            while Interstellar.Main do
                game:GetService("ReplicatedStorage").cPetShopRemote:InvokeServer(game:GetService("ReplicatedStorage").cPetShopFolder:FindFirstChild("Black Storm"))
                wait()
            end
        end
    end
})

tab:Toggle({
    Title = "打石头100万",
    Value = false,
    Callback = function(RK1M)
        if game.Players.LocalPlayer.Durability.Value >= 1000000 then 
            getgenv().RK1M = RK1M 
            while getgenv().RK1M do 
                wait() 
                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                    if v:IsA("Tool") and v.Name == "Punch" then 
                        game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):EquipTool(v) 
                    end 
                end 
                for i,h in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                    if h:IsA("Tool") and h.Name == "Punch" then 
                        h:Activate() 
                    end 
                end 
                game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").CFrame = CFrame.new(4160.87109, 987.829102, -4136.64502, -0.893115997, 1.25481356e-05, 0.44982639, 5.02490684e-06, 1, -1.79187136e-05, -0.44982639, -1.37431543e-05, -0.893115997) 
            end 
            if not getgenv().RK1M then 
                game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):UnequipTools() 
            end 
        end
    end
})

tab:Toggle({
    Title = "打石头500万",
    Value = false,
    Callback = function(RK5M)
        if game.Players.LocalPlayer.Durability.Value >= 5000000 then 
            getgenv().RK5M = RK5M 
            while getgenv().RK5M do 
                wait() 
                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                    if v:IsA("Tool") and v.Name == "Punch" then 
                        game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):EquipTool(v) 
                    end 
                end 
                for i,h in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
                    if h:IsA("Tool") and h.Name == "Punch" then 
                        h:Activate() 
                    end 
                end 
                game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").CFrame = CFrame.new(-9035.8037109375, 45.52519226074219, -6066.02197265625) 
            end 
            if not getgenv().RK5M then 
                game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):UnequipTools() 
            end 
        end
    end
})

local tab = section:Tab({ 
    Title = "其他脚本"
})

tab:Button({
    Title = "龙脚本破解",
    Callback = function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/nahida-cn/Roblox/main/long"))()
  end
})

tab:Button({
    Title = "俄亥俄州",
    Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/rbxluau/Roblox/main/ScriptHub.lua"))()
  end
})

tab:Button({
    Title = "俄亥俄州自动印钞机",
    Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/PUSCRIPTS/MONEY-PRINTER-YAY/main/MONEY"))()
  end
})

tab:Button({
    Title = "极速传奇（一般般）",
    Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/TtmScripter/GoodScript/main/LegendOfSpeed(Chinese)"))()
  end
})

tab:Button({
    Title = "皮脚本",
    Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/xiaopi77/xiaopi77/main/QQ1002100032-Roblox-Pi-script.lua"))()
  end
})
