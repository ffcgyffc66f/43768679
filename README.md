local OrionLib = loadstring(game:HttpGet("https://pastebin.com/raw/FUEx0f3G"))()
local LBLG = Instance.new("ScreenGui", getParent)
local LBL = Instance.new("TextLabel", getParent)
local player = game.Players.LocalPlayer

LBLG.Name = "LBLG"
LBLG.Parent = game.CoreGui
LBLG.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
LBLG.Enabled = true
LBL.Name = "LBL"
LBL.Parent = LBLG
LBL.BackgroundColor3 = Color3.new(1, 1, 1)
LBL.BackgroundTransparency = 1
LBL.BorderColor3 = Color3.new(0, 0, 0)
LBL.Position = UDim2.new(0.75,0,0.010,0)
LBL.Size = UDim2.new(0, 133, 0, 30)
LBL.Font = Enum.Font.GothamSemibold
LBL.Text = "TextLabel"
LBL.TextColor3 = Color3.new(1, 1, 1)
LBL.TextScaled = true
LBL.TextSize = 14
LBL.TextWrapped = true
LBL.Visible = true

local FpsLabel = LBL
local Heartbeat = game:GetService("RunService").Heartbeat
local LastIteration, Start
local FrameUpdateTable = {}

local function HeartbeatUpdate()
	LastIteration = tick()
	for Index = #FrameUpdateTable, 1, -1 do
		FrameUpdateTable[Index + 1] = (FrameUpdateTable[Index] >= LastIteration - 1) and FrameUpdateTable[Index] or nil
	end
	FrameUpdateTable[1] = LastIteration
	local CurrentFPS = (tick() - Start >= 1 and #FrameUpdateTable) or (#FrameUpdateTable / (tick() - Start))
	CurrentFPS = CurrentFPS - CurrentFPS % 1
	FpsLabel.Text = ("标准时间"..os.date("%H").."时"..os.date("%M").."分"..os.date("%S").."秒")
end
Start = tick()
Heartbeat:Connect(HeartbeatUpdate)
local Window = OrionLib:MakeWindow({Name = "TG中心", HidePremium = false, SaveConfig = true,IntroText = "TG中心", ConfigFolder = "老郭/跳鬼"})
local Tab = Window:MakeTab({
    Name = "用户",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

Tab:AddParagraph("用户名:"," "..game.Players.LocalPlayer.Name.."")
Tab:AddParagraph("你的注入器:"," "..identifyexecutor().."")
Tab:AddParagraph("服务器的ID"," "..game.GameId.."")
local Tab =Window:MakeTab({
	Name = "关于作者",
	Icon = "rbxassetid://17360377302",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "复制作者QQ",
	Callback = function()
     setclipboard("422414119")
  	end
})
Tab:AddButton({
	Name = "复制QQ群",
	Callback = function()
     setclipboard("653221974")
  	end
})
OrionLib:MakeNotification({
	Name = "❌️❌️❌️❌️ ",
	Content = "持续更新",
	Image = "rbxassetid://17360377302",
	Time = 2
})

local Tab = Window:MakeTab({
    Name = "主要",
    Icon = "rbxassetid://17360377302",
    PremiumOnly = false
})

Tab:AddButton({
    Name ="点击传送工具",
    Callback = function()
    mouse = game.Players.LocalPlayer:GetMouse() tool = Instance.new("Tool") tool.RequiresHandle = false tool.Name = "[FE] TELEPORT TOOL" tool.Activated:connect(function() local pos = mouse.Hit+Vector3.new(0,2.5,0) pos = CFrame.new(pos.X,pos.Y,pos.Z) game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos end) tool.Parent = game.Players.LocalPlayer.Backpack
    end
})
Tab:AddButton({
    Name ="铁拳（能打飞人）",
    Callback = function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/0Ben1/fe/main/obf_rf6iQURzu1fqrytcnLBAvW34C9N55kS9g9G3CKz086rC47M6632sEd4ZZYB0AYgV.lua.txt'),true))()
    end
})
Tab:AddButton({
    Name ="飞行v3",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
    end
})
Tab:AddButton({
    Name = "隐身按E",
	Callback = function()
	 loadstring(game:HttpGet('https://pastebin.com/raw/nwGEvkez'))()
	end
})
Tab:AddButton({
    Name ="甩人通用",
    Callback = function()
    loadstring(game:HttpGet("https://pastebin.com/raw/zqyDSUWX"))()
    end
})
Tab:AddButton({
    Name ="最强透视",
    Callback = function()
    loadstring(game:HttpGet("https://pastebin.com/raw/uw2P2fbY"))()
    end
})
Tab:AddButton({
    Name ="人物体积",
    Callback = function()
    loadstring(game:HttpGet("https://shz.al/~KSJXBC62"))()
    end
})
Tab:AddButton({
    Name ="反挂机",
    Callback = function()
    loadstring(game:HttpGet("https://pastebin.com/raw/9fFu43FF"))()
    end
})
Tab:AddButton({
    Name ="吸人",
    Callback = function()
    loadstring(game:HttpGet("https://shz.al/~HHAKS"))()
    end
})
Tab:AddButton({
    Name ="骂人无违规",
    Callback = function()
    loadstring(game:GetObjects("rbxassetid://1262435912")[1].Source)()
    end
})
Tab:AddButton({
    Name ="工具挂",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Bebo-Mods/BeboScripts/main/StandAwekening.lua"))()
    end
})
Tab:AddButton({
    Name ="键盘",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt", true))()
    end
})
Tab:AddButton({
    Name ="动画中心",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Animation-Hub/main/Animation%20Gui", true))()
    end
})
Tab:AddButton({
    Name ="光影v4",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/MZEEN2424/Graphics/main/Graphics.xml"))()
    end
})
Tab:AddButton({
	Name = "替身",
	Callback = function()
loadstring(game:HttpGet(('https://raw.githubusercontent.com/SkrillexMe/SkrillexLoader/main/SkrillexLoadMain')))()
    end
})
Tab:AddButton({
	Name = "爬墙",
	Callback = function()
loadstring(game:HttpGet("https://pastebin.com/raw/zXk4Rq2r"))()
    end
})
Tab:AddButton({
	Name = "转起来",
	Callback = function()
      	loadstring(game:HttpGet('https://pastebin.com/raw/r97d7dS0', true))()
  	end
})
Tab:AddButton({
    Name="立即死亡",
    Callback= function()
        game.Players.LocalPlayer.Character.Humanoid.Health=0
    end
})

local Tab = Window:MakeTab({
    Name = "玩家",
    Icon = "rbxassetid://17360377302",
    PremiumOnly = false
})

Tab:AddSlider({
	Name = "速度!",
	Min = 16,
	Max = 200,
	Default = 16,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "数值",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end
})
Tab:AddSlider({
	Name = "跳跃高度!",
	Min = 50,
	Max = 200,
	Default = 50,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "数值",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end
})
Tab:AddTextbox({
	Name = "跳跃高度设置",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end
})
Tab:AddTextbox({
	Name = "移动速度设置",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end
})
Tab:AddTextbox({
	Name = "重力设置",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
		game.Workspace.Gravity = Value
	end
})
Tab:AddToggle({
	Name = "夜视",
	Default = false,
	Callback = function(Value)
		if Value then
		    game.Lighting.Ambient = Color3.new(1, 1, 1)
		else
		    game.Lighting.Ambient = Color3.new(0, 0, 0)
		end
	end
})
Tab:AddButton({
	Name = "透视",
	Callback = function()
	local Players = game:GetService("Players"):GetChildren()
local RunService = game:GetService("RunService")
local highlight = Instance.new("Highlight")
highlight.Name = "Highlight"

for i, v in pairs(Players) do
    repeat wait() until v.Character
    if not v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
        local highlightClone = highlight:Clone()
        highlightClone.Adornee = v.Character
        highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
        highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
        highlightClone.Name = "Highlight"
    end
end

game.Players.PlayerAdded:Connect(function(player)
    repeat wait() until player.Character
    if not player.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
        local highlightClone = highlight:Clone()
荧光笔克隆。Adornee =玩家。性格；角色；字母
荧光笔克隆。家长=玩家。角色:findfirtschild(" HumanoidRootPart ")
荧光笔克隆。Name = "Highlight "
结束
结束)

游戏。players . player remove:Connect(函数(playerRemoved)
玩家已移除。人物:findfirtschild(" HumanoidRootPart ")。亮点:销毁()
结束)

运行服务。心跳:连接(函数()
对于I，v成对(玩家)做
重复wait()直到第五个字符
如果不是v . Character:findfirst child(" HumanoidRootPart "):findfirst child(" Highlight ")那么
local highlight Clone = highlight:Clone()
荧光笔克隆。Adornee = v .字符
荧光笔克隆。parent = v . Character:findfirst child(" HumanoidRootPart ")
荧光笔克隆。DepthMode = Enum。HighlightDepthMode.AlwaysOnTop
荧光笔克隆。Name = "Highlight "
task.wait()
结束
结束
end)
	end 
})
Tab:AddButton({
  Name = "隐身道具",
  Callback = function()
    loadstring(game:HttpGet("https://gist.githubusercontent.com/skid123skidlol/cd0d2dce51b3f20ad1aac941da06a1a1/raw/f58b98cce7d51e53ade94e7bb460e4f24fb7e0ff/%257BFE%257D%2520Invisible%2520Tool%2520(can%2520hold%2520tools)",true))()
  end
})
Tab:AddToggle({
	Name = "穿墙(可用)",
	Default = false,
	Callback = function(Value)
	local Workspace = game:GetService("Workspace")
local Players = game:GetService("Players")
local Clipon = true
 
Stepped = game:GetService("RunService").Stepped:Connect(function()
	if not Clipon == false then
		for a, b in pairs(Workspace:GetChildren()) do
        if b.Name == Players.LocalPlayer.Name then
        for i, v in pairs(Workspace[Players.LocalPlayer.Name]:GetChildren()) do
        if v:IsA("BasePart") then
        v.CanCollide = false
        end end end end
	else
		Stepped:Disconnect()
	end
end)
    end
})    
Tab:AddButton({
    Name ="飞车",
    Callback = function()
    loadstring(game:HttpGet("https://pastebin.com/raw/G3GnBCyC", true))()
    end
})

local Tab =Window:MakeTab({
	Name = "驾驶帝国",
	Icon = "rbxassetid://17360377302",
	PremiumOnly = false
})

Tab:AddButton({
    Name ="自动刷钱",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Marco8642/science/main/drivingempire"))()
    end
})

local Tab =Window:MakeTab({
	Name = "伐木大亨2",
	Icon = "rbxassetid://17360377302",
	PremiumOnly = false
})

Tab:AddButton({
    Name ="伐木大亨2",
    Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/frencaliber/LuaWareLoader.lw/main/luawareloader.wtf"))()
    end
})

local Tab = Window:MakeTab({
	Name = "鲨口求生2",
	Icon = "rbxassetid://17360377302",
	PremiumOnly = false
})

Tab:AddDropdown({
	Name = "免费船只",
	Default = "1",
	Options = {"DuckyBoatBeta", "DuckyBoat", "BlueCanopyMotorboat", "BlueWoodenMotorboat", "UnicornBoat", "Jetski", "RedMarlin", "Sloop", "TugBoat", "SmallDinghyMotorboat", "JetskiDonut", "Marlin", "TubeBoat", "FishingBoat", "VikingShip", "SmallWoodenSailboat", "RedCanopyMotorboat", "Catamaran", "CombatBoat", "TourBoat", "Duckmarine", "PartyBoat", "MilitarySubmarine",  "GingerbreadSteamBoat", "Sleigh2022", "Snowmobile", "CruiseShip"},
	Callback = function(Value)
local ohString1 = (Value)
game:GetService("ReplicatedStorage").EventsFolder.BoatSelection.UpdateHostBoat:FireServer(ohString1)
	end
})
Tab:AddButton({
	Name = "自动杀鲨鱼🦈",
	Callback = function()
loadstring(game:http get(" https://raw . githubusercontent . com/sw1 ndlerscripts/RobloxScripts/main/Misc % 20 scripts/shark bit 2 . Lua "，true))()
结束
})

local Tab = Window:MakeTab({
Name = "doors "，
Icon = "rbxassetid://17360377302 "，
PremiumOnly = false
})

Tab:AddButton({
    Name = "AND已汉化 推荐配合穿墙",
    Callback = function()
    --[[门黑王和BobHub脚本汉化]]loadstring(game:HttpGet("\104\116\116\112\115\58\47\47\112\97\115\116\101\98\105\110\46\99\111\109\47\114\97\119\47\54\53\84\119\84\56\106\97"))()
    end
})
Tab:AddButton({
	Name = "穿墙(无拉回)",
	Callback = function()
loadstring(game:HttpGet("https://github.com/DXuwu/OK/raw/main/clip"))()
    end
})
Tab:AddButton({
  Name = "手电筒",
  Callback = function()
loadstring(game:HttpGet('https://pastebin.com/raw/9Daqa4hD'))()
  	end
})

local Tab = Window:MakeTab({
    Name = "力量传奇",
    Icon = "rbxassetid://17360377302",
    PremiumOnly = false
})

Tab:AddButton({
    Name = "力量传奇修改力量",
    Callback = function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/jynzl/main/main/Musclas%20Legenos.lua'))()
    end
})
local Section = Tab:AddSection({
	Name = "传送位置"
})
Tab:AddButton({
	Name = "传送到出生点",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(7, 3, 108)
    end
})
Tab:AddButton({
	Name = "传送到冰霜健身房",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2543, 13, -410)
    end
})
Tab:AddButton({
	Name = "传送到神话健身房",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2177, 13, 1070)
    end
})
Tab:AddButton({
	Name = "传送到永恒健身房",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6686, 13, -1284)
    end
})
Tab:AddButton({
	Name = "传送到传说健身房",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4676, 997, -3915)
    end
})
Tab:AddButton({
	Name = "传送到肌肉之王健身房",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-8554, 22, -5642)
    end
})
Tab:AddButton({
	Name = "传送到安全岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-39, 10, 1838)
    end
})
Tab:AddButton({
	Name = "传送到幸运抽奖区域",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2606, -2, 5753)
  	end
})

local Tab = Window:MakeTab({
    Name = "新更",
    Icon = "rbxassetid://17360377302",
    PremiumOnly = false
})

Tab:AddButton({
    Name="自瞄",
    Callback=function()
loadstring(game:HttpGet("https://pastebin.com/raw/1Gp9c57U"))()
    end
})
Tab:AddButton({
  Name = "范围",
  Callback = function ()
loadstring(game:HttpGet("https://pastebin.com/raw/jiNwDbCN"))()
  end
})
Tab:AddButton({
    Name ="iw指令",
    Callback =function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'),true))()
    end
})
Tab:AddButton({
	Name = "操b脚本",
	Callback = function()
	--Variables
local SimpleSexGUI = Instance.new("ScreenGui")
local FGUI = Instance.new("Frame")
local btnNaked = Instance.new("TextButton")
local btnSex = Instance.new("TextButton")
local tbxVictim = Instance.new("TextBox")
local lblFUCKEMALL = Instance.new("TextLabel")
local ImageLabel = Instance.new("ImageLabel")
local lbltitle = Instance.new("TextLabel")
local TextLabel = Instance.new("TextLabel")
--Properties
SimpleSexGUI.Name = "SimpleSexGUI"
SimpleSexGUI.Parent = game.CoreGui

FGUI.Name = "FGUI"
FGUI.Parent = SimpleSexGUI
FGUI.BackgroundColor3 = Color3.new(255,255,255)
FGUI.BorderSizePixel = 1
FGUI.Position = UDim2.new(0,0, 0.667, 0)
FGUI.Size = UDim2.new(0,317, 0,271)
FGUI.Draggable = true

lbltitle.Name = "Title"
lbltitle.Parent = FGUI
lbltitle.BackgroundColor3 = Color3.new(255,255,255)
lbltitle.BorderSizePixel = 1
lbltitle.Position = UDim2.new (0, 0,-0.122, 0)
lbltitle.Size = UDim2.new (0, 317,0, 33)
lbltitle.Visible = true
lbltitle.Active = true
lbltitle.Draggable = false
lbltitle.Selectable = true
lbltitle.Font = Enum.Font.SourceSansBold
lbltitle.Text = "一个简单的操蛋脚本!!"
lbltitle.TextColor3 = Color3.new(0, 0, 0)
lbltitle.TextSize = 20

btnSex.Name = "Sex"
btnSex.Parent = FGUI
btnSex.BackgroundColor3 = Color3.new(255,255,255)
btnSex.BorderSizePixel = 1
btnSex.Position = UDim2.new (0.044, 0,0.229, 0)
btnSex.Size = UDim2.new (0, 99,0, 31)
btnSex.Visible = true
btnSex.Active = true
btnSex.Draggable = false
btnSex.Selectable = true
btnSex.Font = Enum.Font.SourceSansBold
btnSex.Text = "让我们操蛋吧!!"
btnSex.TextColor3 = Color3.new(0, 0, 0)
btnSex.TextSize = 20

tbxVictim.Name = "VictimTEXT"
tbxVictim.Parent = FGUI
tbxVictim.BackgroundColor3 = Color3.new(255,255,255)
tbxVictim.BorderSizePixel = 1
tbxVictim.Position = UDim2.new (0.533, 0,0.229, 0)
tbxVictim.Size = UDim2.new (0, 133,0, 27)
tbxVictim.Visible = true
tbxVictim.Active = true
tbxVictim.Draggable = false
tbxVictim.Selectable = true
tbxVictim.Font = Enum.Font.SourceSansBold
tbxVictim.Text = "名字"
tbxVictim.TextColor3 = Color3.new(0, 0, 0)
tbxVictim.TextSize = 20

lblFUCKEMALL.Name = "FUCKEMALL"
lblFUCKEMALL.Parent = FGUI
lblFUCKEMALL.BackgroundColor3 = Color3.new(255,255,255)
lblFUCKEMALL.BorderSizePixel = 1
lblFUCKEMALL.Position = UDim2.new (0.025, 0,0.856, 0)
lblFUCKEMALL.Size = UDim2.new (0, 301,0, 27)
lblFUCKEMALL.Visible = true
lblFUCKEMALL.Font = Enum.Font.SourceSansBold
lblFUCKEMALL.Text = "操蛋和操蛋"
lblFUCKEMALL.TextColor3 = Color3.new(0, 0, 0)
lblFUCKEMALL.TextSize = 20

ImageLabel.Name = "ImageLabel"
ImageLabel.Parent = FGUI
ImageLabel.Image = "http://www.roblox.com/asset/?id=42837..."
ImageLabel.BorderSizePixel = 1
ImageLabel.Position = UDim2.new (0.274, 0,0.358, 0)
ImageLabel.Size = UDim2.new (0, 106,0, 121)
--Scripts
btnSex.MouseButton1Click:Connect(function()
local player = tbxVictim.Text
local stupid = Instance.new('Animation')
stupid.AnimationId = 'rbxassetid://148840371'
hummy = game:GetService("Players").LocalPlayer.Character.Humanoid
pcall(function()
    hummy.Parent.Pants:Destroy()
end)
pcall(function()
    hummy.Parent.Shirt:Destroy()
end)
local notfunny = hummy:LoadAnimation(stupid)
notfunny:Play()
notfunny:AdjustSpeed(10)
while hummy.Parent.Parent ~= nil do
wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[tbxVictim.Text].Character.HumanoidRootPart.CFrame
end
end)
end
})

local Tab = Window:MakeTab({
    Name = "监狱人生",
    Icon = "rbxassetid://17360377302",
    PremiumOnly = false
})

Tab:AddButton({
	Name = "手里剑（秒杀）",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/PSXhuge/1/114514/jian"))()
  	end
})
local Section = Tab:AddSection({
	Name = "传送位置"
})
Tab:AddButton({
	Name = "警卫室",
	Callback = function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(847.7261352539062, 98.95999908447266, 2267.387451171875)
  	end
})
Tab:AddButton({
	Name = "监狱室内",
	Callback = function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(919.2575073242188, 98.95999908447266, 2379.74169921875)
  	end
})
Tab:AddButton({
	Name = "罪犯复活点",
	Callback = function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-937.5891723632812, 93.09876251220703, 2063.031982421875)
  	end
})
Tab:AddButton({
	Name = "监狱室外",
	Callback = function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(760.6033325195312, 96.96992492675781, 2475.405029296875)
  	end
})

local Tab = Window:MakeTab({
    Name = "战斗勇士",
    Icon = "rbxassetid://17360377302",
    PremiumOnly = false
})

Tab:AddButton({
    Name = "弓箭爆头",
    Callback = function()
    loadstring(game:HttpGet("https://pastebin.com/raw/6RQGbFqD"))()
    end
})

local Tab = Window:MakeTab({
	Name = "忍者传奇",
	Icon = "rbxassetid://17360377302",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "位置传送"
})
Tab:AddButton({
	Name = "传送到出生点",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(25.665502548217773, 3.4228405952453613, 29.919952392578125)
    end
})
Tab:AddButton({
	Name = "传送到附魔岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(51.17238235473633, 766.1807861328125, -138.44842529296875)
    end
})
选项卡:添加按钮({
Name = "传送到神秘岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(171 . 9649902344，42 . 42343434346
结束
})
选项卡:添加按钮({
Name = "传送到太空岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(148，157714844，738653677
结束
})
选项卡:添加按钮({
Name = "传送到冻土岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(139，9285，772344 . 9365237367
结束
})
选项卡:添加按钮({
Name = "传送到永恒岛",
回调=函数()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(149.34817504882812, 13680.037109375, 73.3861312866211)
    end
})
Tab:AddButton({
	Name = "传送到沙暴岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(133.37144470214844, 17686.328125, 72.00334167480469)
    end
})
Tab:AddButton({
	Name = "传送到雷暴岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(143.19349670410156, 24070.021484375, 78.05432891845703)
    end
})
Tab:AddButton({
	Name = "传送到远古炼狱岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(141.27163696289062, 28256.294921875, 69.3790283203125)
    end
})
Tab:AddButton({
	Name = "传送到午夜暗影岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . c frame = c frame . new(132.7467578125366
结束
})
选项卡:添加按钮({
Name = "传送到神秘灵魂岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . c frame = c frame . new(137.6686816406376
结束
})
选项卡:添加按钮({
Name = "传送到冬季奇迹岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(137，184326172，526172，52637 . 5267676777
结束
})
选项卡:添加按钮({
Name = "传送到黄金大师岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(128，539062，52607，562607 . 5636767
    end
})
Tab:AddButton({
	Name = "传送到龙传奇岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(146.35226440429688, 59594.6796875, 77.53300476074219)
    end
})
Tab:AddButton({
	Name = "传送到赛博传奇岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(137.3321075439453, 66669.1640625, 72.21722412109375)
    end
})
Tab:AddButton({
	Name = "传送到天岚超能岛",
	Callback = function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(135.48077392578125, 70271.15625, 57.02311325073242)
    end
})
Tab:AddButton({
	Name = "传送到混沌传奇岛",
	Callback = function()
游戏1000名球员。本地玩家。性格。humanoidrootpart。cframe = cframe。新(148，724，288，624，221，8365
结束
})
选项卡:添加按钮({
Name = "传送到混沌传奇岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(148，7242188，6242218365
    end
})
选项卡:添加按钮({
Name = "传送到灵魂融合岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(136.97734343375，79746，554837
    end
})
选项卡:添加按钮({
Name = "传送到黑暗元素岛",
回调=函数()
游戏1000名球员。本地玩家。性格humanoidrootpart .cframe = cframe .新的(141 .665625 .56363636387
结束
})
选项卡:添加按钮({
Name = "传送到内心和平岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . cframe = cframe . new(135.3222070705657
结束
})
选项卡:添加按钮({
Name = "传送到炽烈漩涡岛",
回调=函数()
游戏。players . local player . character . humanoidrootpart . c frame = c frame . new(135.0866857910156，91246，69)54656 . 5456565667
结束
})
选项卡:添加按钮({
Name = "传送到35倍金币区域",
回调=函数()
游戏。players . local player . character . humanoidrootpart . c frame = c frame . new(86.29382421875，91245，120 . 5487385876
结束
})
选项卡:添加按钮({
Name = "传送到死亡宠物",
回调=函数()
游戏。玩家本地玩家。性格。humanoidrootpart。cframe = cframe。新的(13001 . 486386867675
结束
})
