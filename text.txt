local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(0, 350, 0, 100)
Frame.Position = UDim2.new(0.5, -175, 0.1, 0)
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.BackgroundTransparency = 0.3
Frame.BorderSizePixel = 0
Frame.Parent = ScreenGui
Frame.Visible = true

local UICorner = Instance.new("UICorner")
UICorner.CornerRadius = UDim.new(0, 12)
UICorner.Parent = Frame

local TextLabel = Instance.new("TextLabel")
TextLabel.Size = UDim2.new(1, -40, 1, -20)
TextLabel.Position = UDim2.new(0, 10, 0, 10)
TextLabel.BackgroundTransparency = 1
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.Font = Enum.Font.SourceSansBold
TextLabel.TextWrapped = true
TextLabel.Text = "⚠️ Temporarily closed for unexpected reasons!"
TextLabel.Parent = Frame

local CloseButton = Instance.new("TextButton")
CloseButton.Size = UDim2.new(0, 30, 0, 30)
CloseButton.Position = UDim2.new(1, -35, 0, 5)
CloseButton.BackgroundColor3 = Color3.fromRGB(200, 0, 0)
CloseButton.TextColor3 = Color3.fromRGB(255, 255, 255)
CloseButton.TextScaled = true
CloseButton.Font = Enum.Font.SourceSansBold
CloseButton.Text = "X"
CloseButton.Parent = Frame

local CloseCorner = Instance.new("UICorner")
CloseCorner.CornerRadius = UDim.new(0, 8)
CloseCorner.Parent = CloseButton

CloseButton.MouseButton1Click:Connect(function()
	Frame.Visible = false
end)
