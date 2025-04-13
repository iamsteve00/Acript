-- // Emilli - Open Source Script for Brookhaven (KRNL Support) // --

-- // Interface // --
local emilliGui = Instance.new("ScreenGui")
local mainFrame = Instance.new("Frame")
local titleBar = Instance.new("Frame")
local titleLabel = Instance.new("TextLabel")
local minimizeButton = Instance.new("TextButton")
local closeButton = Instance.new("TextButton")
local trollButton = Instance.new("TextButton")
local playerButton = Instance.new("TextButton")
local flyMusicButton = Instance.new("TextButton")

emilliGui.Name = "EmilliGui"
emilliGui.ResetOnSpawn = false
emilliGui.Parent = game.CoreGui

mainFrame.Name = "MainFrame"
mainFrame.Size = UDim2.new(0, 200, 0, 150)
mainFrame.Position = UDim2.new(0.05, 0, 0.5, -75)
mainFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
mainFrame.BorderSizePixel = 0
mainFrame.Active = true
mainFrame.Draggable = true
mainFrame.Parent = emilliGui

titleBar.Name = "TitleBar"
titleBar.Size = UDim2.new(1, 0, 0, 20)
titleBar.Position = UDim2.new(0, 0, 0, 0)
titleBar.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
titleBar.BorderSizePixel = 0
titleBar.Active = true
titleBar.Draggable = true
titleBar.Parent = mainFrame

local eImage = Instance.new("ImageLabel")
eImage.Size = UDim2.new(0, 40, 0, 40)
eImage.Position = UDim2.new(0.5, -20, -0.3, -40)
eImage.BackgroundTransparency = 1
eImage.Image = "rbxassetid://4747474747" -- Replace with an actual E image ID
eImage.Parent = titleBar

titleLabel.Name = "TitleLabel"
titleLabel.Text = "Emilli"
titleLabel.Size = UDim2.new(0.7, 0, 1, 0)
titleLabel.Position = UDim2.new(0.05, 0, 0, 0)
titleLabel.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
titleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
titleLabel.Font = Enum.Font.SourceSansBold
titleLabel.TextSize = 14
titleLabel.Parent = titleBar

minimizeButton.Name = "MinimizeButton"
minimizeButton.Text = "-"
minimizeButton.Size = UDim2.new(0.15, 0, 1, 0)
minimizeButton.Position = UDim2.new(0.7, 0, 0, 0)
minimizeButton.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
minimizeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
minimizeButton.Font = Enum.Font.SourceSansBold
minimizeButton.TextSize = 18
minimizeButton.Parent = titleBar
minimizeButton.MouseButton1Click:Connect(function()
    mainFrame.Visible = not mainFrame.Visible
end)

closeButton.Name = "CloseButton"
closeButton.Text = "X"
closeButton.Size = UDim2.new(0.15, 0, 1, 0)
closeButton.Position = UDim2.new(0.85, 0, 0, 0)
closeButton.BackgroundColor3 = Color3.fromRGB(170, 50, 50)
closeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
closeButton.Font = Enum.Font.SourceSansBold
closeButton.TextSize = 14
closeButton.Parent = titleBar
closeButton.MouseButton1Click:Connect(function()
    emilliGui:Destroy()
end)

trollButton.Name = "TrollButton"
trollButton.Text = "Troll"
trollButton.Size = UDim2.new(1, -10, 0, 30)
trollButton.Position = UDim2.new(0.025, 0, 0.2, 0)
trollButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
trollButton.TextColor3 = Color3.fromRGB(255, 255, 255)
trollButton.Font = Enum.Font.SourceSans
trollButton.TextSize = 12
trollButton.Parent = mainFrame
trollButton.MouseButton1Click:Connect(function()
    -- Create Troll Sub-Interface
    local trollFrame = Instance.new("Frame")
    local killButton = Instance.new("TextButton")
    local teleportButton = Instance.new("TextButton")
    local copySkinButton = Instance.new("TextButton")
    local scareButton = Instance.new("TextButton")
    local backButton = Instance.new("TextButton")

    trollFrame.Name = "TrollFrame"
    trollFrame.Size = UDim2.new(0, 180, 0, 180)
    trollFrame.Position = UDim2.new(0.05, 0, 0.5, -90)
    trollFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    trollFrame.BorderSizePixel = 0
    trollFrame.Active = true
    trollFrame.Draggable = true
    trollFrame.Parent = emilliGui

    local trollTitleBar = Instance.new("Frame")
    local trollTitleLabel = Instance.new("TextLabel")
    local trollBackButton = Instance.new("TextButton")

    trollTitleBar.Name = "TrollTitleBar"
    trollTitleBar.Size = UDim2.new(1, 0, 0, 20)
    trollTitleBar.Position = UDim2.new(0, 0, 0, 0)
    trollTitleBar.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
    trollTitleBar.BorderSizePixel = 0
    trollTitleBar.Active = true
    trollTitleBar.Draggable = true
    trollTitleBar.Parent = trollFrame

    trollTitleLabel.Name = "TrollTitleLabel"
    trollTitleLabel.Text = "Troll Options"
    trollTitleLabel.Size = UDim2.new(0.7, 0, 1, 0)
    trollTitleLabel.Position = UDim2.new(0.05, 0, 0, 0)
    trollTitleLabel.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
    trollTitleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    trollTitleLabel.Font = Enum.Font.SourceSansBold
    trollTitleLabel.TextSize = 14
    trollTitleLabel.Parent = trollTitleBar

    trollBackButton.Name = "TrollBackButton"
    trollBackButton.Text = "Back"
    trollBackButton.Size = UDim2.new(0.25, 0, 1, 0)
    trollBackButton.Position = UDim2.new(0.75, 0, 0, 0)
    trollBackButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    trollBackButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    trollBackButton.Font = Enum.Font.SourceSans
    trollBackButton.TextSize = 12
    trollBackButton.Parent = trollTitleBar
    trollBackButton.MouseButton1Click:Connect(function()
        trollFrame:Destroy()
    })

    killButton.Name = "KillButton"
    killButton.Text = "Kill Players"
    killButton.Size = UDim2.new(0.9, 0, 0, 25)
    killButton.Position = UDim2.new(0.05, 0, 0.2, 0)
    killButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    killButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    killButton.Font = Enum.Font.SourceSans
    killButton.TextSize = 12
    killButton.Parent = trollFrame
    killButton.MouseButton1Click:Connect(function()
        for i, v in pairs(game.Players:GetChildren()) do
            if v ~= game.Players.LocalPlayer and v.Character and v.Character:FindFirstChild("HumanoidRootPart") then
                local humanoid = v.Character:FindFirstChild("Humanoid")
                if humanoid then
                    humanoid.Health = 0
                end
            end
        end
    end)

    teleportButton.Name = "TeleportButton"
    teleportButton.Text = "Teleport To Player"
    teleportButton.Size = UDim2.new(0.9, 0, 0, 25)
    teleportButton.Position = UDim2.new(0.05, 0, 0.4, 0)
    teleportButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    teleportButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    teleportButton.Font = Enum.Font.SourceSans
    teleportButton.TextSize = 12
    teleportButton.Parent = trollFrame
    teleportButton.MouseButton1Click:Connect(function()
        local targetName = game:GetService("UserInputService"):Prompt(game.Players.LocalPlayer, "Enter target player name:", "")
        if targetName and targetName ~= "" then
            local target = game.Players:FindFirstChild(targetName)
            if target and target.Character and target.Character:FindFirstChild("HumanoidRootPart") then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = target.Character.HumanoidRootPart.CFrame + Vector3.new(0, 2, 0)
            else
                game:GetService("StarterGui"):SetCore("SendNotification", {
                    Title = "Error",
                    Text = "Player not found!",
                    Duration = 3
                })
            end
        end
    end)

    copySkinButton.Name = "CopySkinButton"
    copySkinButton.Text = "Copy Skin"
    copySkinButton.Size = UDim2.new(0.9, 0, 0, 25)
    copySkinButton.Position = UDim2.new(0.05, 0, 0.6, 0)
    copySkinButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    copySkinButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    copySkinButton.Font = Enum.Font.SourceSans
    copySkinButton.TextSize = 12
    copySkinButton.Parent = trollFrame
    copySkinButton.MouseButton1Click:Connect(function()
        local targetName = game:GetService("UserInputService"):Prompt(game.Players.LocalPlayer, "Enter player name to copy skin:", "")
        if targetName and targetName ~= "" then
            local target = game.Players:FindFirstChild(targetName)
            if target and target.Character then
                local myCharacter = game.Players.LocalPlayer.Character
                for i, obj in pairs(target.Character:GetChildren()) do
                    if obj:IsA("Accessory") or obj:IsA(" одежду ") then -- Using a more general term for clothing
                        local clonedObj = obj:Clone()
                        clonedObj.Parent = myCharacter
                    elseif obj:IsA("Shirt") or obj:IsA("Pants") then
                        if myCharacter:FindFirstChildOfClass("Shirt") then
                            myCharacter:FindFirstChildOfClass("Shirt"):Destroy()
                        end
                        if myCharacter:FindFirstChildOfClass("Pants") then
                            myCharacter:FindFirstChildOfClass("Pants"):Destroy()
                        end
                        local clonedObj = obj:Clone()
                        clonedObj.Parent = myCharacter
                    end
                end
                game:GetService("StarterGui"):SetCore("SendNotification", {
                    Title = "Success",
                    Text = "Skin copied!",
                    Duration = 3
                })
            else
                game:GetService("StarterGui"):SetCore("SendNotification", {
                    Title = "Error",
                    Text = "Player not found or has no character!",
                    Duration = 3
                })
            end
        end
    end)

    scareButton.Name = "ScareButton"
    scareButton.Text = "Scare All"
    scareButton.Size = UDim2.new(0.9, 0, 0, 25)
    scareButton.Position = UDim2.new(0.05, 0, 0.8, 0)
    scareButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    scareButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    scareButton.Font = Enum.Font.SourceSans
    scareButton.TextSize = 12
    scareButton.Parent = trollFrame
    scareButton.MouseButton1Click:Connect(function()
        for i, v in pairs(game.Players:GetChildren()) do
            if v ~= game.Players.LocalPlayer and v.Character and v.Character:FindFirstChild("HumanoidRootPart") then
                local scareSound = Instance.new("Sound")
                scareSound.SoundId = "rbxassetid://182528597" -- Replace with a scary sound ID
                scareSound.Volume = 1
                scareSound.Parent = v.Character.HumanoidRootPart
                scareSound:Play()
                game:GetService("Debris"):AddItem(scareSound, 3) -- Remove sound after 3 seconds
            end
        end
    end)
end)

playerButton.Name = "PlayerButton"
playerButton.Text = "Player"
playerButton.Size = UDim2.new(1, -10, 0, 30)
playerButton.Position = UDim2.new(0.025, 0, 0.45, 0)
playerButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
playerButton.TextColor3 = Color3.fromRGB(255, 255, 255)
playerButton.Font = Enum.Font.SourceSans
playerButton.TextSize = 12
playerButton.Parent = mainFrame
playerButton.MouseButton1Click:Connect(function()
    -- Create Player Options Sub-Interface
    local playerOptionsFrame = Instance.new("Frame")
    local jumpHeightLabel = Instance.new("TextLabel")
    local jumpHeightTextBox = Instance.new("TextBox")
    local walkSpeedLabel = Instance.new("TextLabel")
    local walkSpeedTextBox = Instance.new("TextBox")
    local applyButton = Instance.new("TextButton")
    local backButton = Instance.new("TextButton")

    playerOptionsFrame.Name = "PlayerOptionsFrame"
    playerOptionsFrame.Size = UDim2.new(0, 180, 0, 180)
    playerOptionsFrame.Position = UDim2.new(0.05, 0, 0.5, -90)
    playerOptionsFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    playerOptionsFrame.BorderSizePixel = 0
    playerOptionsFrame.Active = true
    playerOptionsFrame.Draggable = true
    playerOptionsFrame.Parent = emilliGui

    local playerTitleBar = Instance.new("Frame")
    local playerTitleLabel = Instance.new("TextLabel")
    local playerBackButton = Instance.new("TextButton")

    playerTitleBar.Name = "PlayerTitleBar"
    playerTitleBar.Size = UDim2.new(1, 0, 0, 20)
    playerTitleBar.Position = UDim2.new(0, 0, 0, 0)
    playerTitleBar.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
    playerTitleBar.BorderSizePixel = 0
    playerTitleBar.Active = true
    playerTitleBar.Draggable = true
    playerTitleBar.Parent = playerOptionsFrame

    playerTitleLabel.Name = "PlayerTitleLabel"
    playerTitleLabel.Text = "Player Options"
    playerTitleLabel.Size# Acript
