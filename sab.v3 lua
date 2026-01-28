-- Woke St4rs Hub v.3 | Steal a Brainrot (Anti-Crash | Mobile OK | Jan 2026)
-- Auto Steal | No Knockback | Auto Hit | Speed | Fly | ESP | Space Theme

local Players=game:GetService("Players");local TweenService=game:GetService("TweenService");local RunService=game:GetService("RunService");local UserInputService=game:GetService("UserInputService");local LocalPlayer=Players.LocalPlayer
task.wait(5);local Character=LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait();local Humanoid=Character:WaitForChild("Humanoid");local RootPart=Character:WaitForChild("HumanoidRootPart")
LocalPlayer.CharacterAdded:Connect(function(c)Character=c;Humanoid=c:WaitForChild("Humanoid");RootPart=c:WaitForChild("HumanoidRootPart")end)
local Bases=workspace:WaitForChild("Bases",15)or workspace:FindFirstChild("Bases")

local sg=Instance.new("ScreenGui");sg.Name="WokeSt4rs";sg.Parent=game.CoreGui;sg.ResetOnSpawn=false

-- Loading (minimal)
local lf=Instance.new("Frame");lf.Size=UDim2.new(1,0,1,0);lf.BackgroundColor3=Color3.fromRGB(2,2,6);lf.Parent=sg
local logo=Instance.new("ImageLabel");logo.Size=UDim2.new(0,140,0,140);logo.Position=UDim2.new(0.5,-70,0.4,-70);logo.BackgroundTransparency=1;logo.Image="rbxassetid://7072718362";logo.ImageColor3=Color3.fromRGB(180,220,255);logo.Parent=lf
local lt=Instance.new("TextLabel");lt.Size=UDim2.new(0,300,0,30);lt.Position=UDim2.new(0.5,-150,0.6,0);lt.BackgroundTransparency=1;lt.Text="WOKE ST4RS v.3 LOADING...";lt.TextColor3=Color3.fromRGB(220,240,255);lt.TextSize=20;lt.Font=Enum.Font.GothamBold;lt.Parent=lf
local pb=Instance.new("Frame");pb.Size=UDim2.new(0,250,0,6);pb.Position=UDim2.new(0.5,-125,0.7,0);pb.BackgroundColor3=Color3.fromRGB(20,20,50);pb.Parent=lf;local pc=Instance.new("UICorner",pb);pc.CornerRadius=UDim.new(0,3)
local pf=Instance.new("Frame");pf.Size=UDim2.new(0,0,1,0);pf.BackgroundColor3=Color3.fromRGB(100,160,255);pf.Parent=pb;local pfc=Instance.new("UICorner",pf);pfc.CornerRadius=UDim.new(0,3)
TweenService:Create(pf,TweenInfo.new(2),{Size=UDim2.new(1,0,1,0)}):Play();task.wait(2.5);lf:Destroy()

-- MainFrame
local mf=Instance.new("Frame");mf.Size=UDim2.new(0,460,0,320);mf.Position=UDim2.new(0.5,-230,0.5,-160);mf.BackgroundColor3=Color3.fromRGB(4,4,14);mf.Parent=sg;local mfc=Instance.new("UICorner",mf);mfc.CornerRadius=UDim.new(0,12)

-- Title/Drag
local tb=Instance.new("Frame");tb.Size=UDim2.new(1,0,0,45);tb.BackgroundColor3=Color3.fromRGB(8,8,32);tb.Parent=mf;local tbc=Instance.new("UICorner",tb);tbc.CornerRadius=UDim.new(0,12)
local logotb=Instance.new("ImageLabel");logotb.Size=UDim2.new(0,45,0,45);logotb.Position=UDim2.new(0,10,0,0);logotb.BackgroundTransparency=1;logotb.Image="rbxassetid://7072718362";logotb.ImageColor3=Color3.fromRGB(200,230,255);logotb.Parent=tb
local ttl=Instance.new("TextLabel");ttl.Size=UDim2.new(1,-70,1,0);ttl.Position=UDim2.new(0,60,0,0);ttl.BackgroundTransparency=1;ttl.Text="WOKE ST4RS | BRAINROT";ttl.TextColor3=Color3.fromRGB(230,245,255);ttl.TextSize=20;ttl.Font=Enum.Font.GothamBold;ttl.Parent=tb
local enjoy=Instance.new("TextLabel");enjoy.Size=UDim2.new(0,100,0,18);enjoy.Position=UDim2.new(1,-110,1,-22);enjoy.BackgroundTransparency=1;enjoy.Text="Enjoy 🌌";enjoy.TextColor3=Color3.fromRGB(160,200,255);enjoy.TextSize=14;enjoy.Font=Enum.Font.Gotham;enjoy.Parent=mf

-- Drag
local dragging=false;local dragInput,dragStart,startPos
tb.InputBegan:Connect(function(i)if i.UserInputType==Enum.UserInputType.MouseButton1 then dragging=true;dragStart=i.Position;startPos=mf.Position;i.Changed:Connect(function()if i.UserInputState==Enum.UserInputState.End then dragging=false end end)end end)
tb.InputChanged:Connect(function(i)if i.UserInputType==Enum.UserInputType.MouseMovement then dragInput=i end end)
UserInputService.InputChanged:Connect(function(i)if dragging and i==dragInput then local d=i.Position-dragStart;mf.Position=UDim2.new(startPos.X.Scale,startPos.X.Offset+d.X,startPos.Y.Scale,startPos.Y.Offset+d.Y)end end)

-- Toggles Table
local toggles={autoSteal=false,noKnock=false,autoHit=false,speed=false,fly=false,esp=false}

-- Tabs
local tabs={"Steal","Defense","Attack","Movement"}
local tabContents={};local curTab="Steal"
local tbar=Instance.new("Frame");tbar.Size=UDim2.new(1,-20,0,38);tbar.Position=UDim2.new(0,10,0,55);tbar.BackgroundTransparency=1;tbar.Parent=mf

for i,tn in ipairs(tabs)do
 local btn=Instance.new("TextButton");btn.Size=UDim2.new(0,105,1,0);btn.Position=UDim2.new(0,(i-1)*110,0,0);btn.BackgroundColor3=Color3.fromRGB(25,25,60);btn.Text=tn;btn.TextColor3=Color3.fromRGB(200,220,255);btn.Font=Enum.Font.GothamSemibold;btn.TextSize=16;btn.Parent=tbar;local bnc=Instance.new("UICorner",btn);bnc.CornerRadius=UDim.new(0,8)
 local cont=Instance.new("Frame");cont.Size=UDim2.new(1,-20,1,-105);cont.Position=UDim2.new(0,10,0,103);cont.BackgroundTransparency=1;cont.Visible=(tn=="Steal");cont.Parent=mf;tabContents[tn]=cont
 btn.MouseButton1Click:Connect(function()
  for _tn,_ in pairs(tabContents)do tabContents[_].Visible=false end;cont.Visible=true;curTab=tn
  for _,b in pairs(tbar:GetChildren())do if b:IsA("TextButton")then b.BackgroundColor3=Color3.fromRGB(25,25,60)end end;btn.BackgroundColor3=Color3.fromRGB(70,120,255)
 end)
end

-- STEAL TAB - Auto Steal
local asbtn=Instance.new("TextButton");asbtn.Size=UDim2.new(1,-20,0,55);asbtn.Position=UDim2.new(0,10,0,10);asbtn.BackgroundColor3=Color3.fromRGB(40,80,40);asbtn.Text="Auto Steal: OFF";asbtn.TextColor3=Color3.white;asbtn.Font=Enum.Font.GothamBold;asbtn.TextSize=18;asbtn.Parent=tabContents.Steal;local asc=Instance.new("UICorner",asbtn);asc.CornerRadius=UDim.new(0,10)
asbtn.MouseButton1Click:Connect(function()toggles.autoSteal=not toggles.autoSteal;asbtn.Text="Auto Steal: "..(toggles.autoSteal and "ON"or"OFF");asbtn.BackgroundColor3=toggles.autoSteal and Color3.fromRGB(80,160,80)or Color3.fromRGB(40,80,40)end)

task.spawn(function()while task.wait(0.8)do if toggles.autoSteal and RootPart and Bases do
 local closest=math.huge;local target=nil
 for _,b in pairs(Bases:GetChildren())do if b.Name~=LocalPlayer.Name and b:FindFirstChild("Brainrots")and not b:FindFirstChild("Shield")then
  for _,br in pairs(b.Brainrots:GetChildren())do if br:IsA("Model")and br.PrimaryPart then local dist=(RootPart.Position-br.PrimaryPart.Position).Magnitude;if dist<closest then closest=dist;target=br end end end
 end end
 if target and closest<400 then Humanoid:MoveTo(target.PrimaryPart.Position);if closest<15 then RootPart.CFrame=CFrame.new(target.PrimaryPart.Position+Vector3.new(0,3,-3));local pp=target:FindFirstChild("ProximityPrompt");if pp then pp:InputHoldBegin();task.wait(0.1);pp:InputHoldEnd()end end
end end end end end)

-- DEFENSE TAB - No Knockback
local nkbtn=Instance.new("TextButton");nkbtn.Size=UDim2.new(1,-20,0,55);nkbtn.Position=UDim2.new(0,10,0,10);nkbtn.BackgroundColor3=Color3.fromRGB(80,40,40);nkbtn.Text="No Knockback: OFF";nkbtn.TextColor3=Color3.white;nkbtn.Font=Enum.Font.GothamBold;nkbtn.TextSize=18;nkbtn.Parent=tabContents.Defense;local nkc=Instance.new("UICorner",nkbtn);nkc.CornerRadius=UDim.new(0,10)
nkbtn.MouseButton1Click:Connect(function()toggles.noKnock=not toggles.noKnock;nkbtn.Text="No Knockback: "..(toggles.noKnock and "ON"or"OFF");nkbtn.BackgroundColor3=toggles.noKnock and Color3.fromRGB(200,80,80)or Color3.fromRGB(80,40,40)end)
RunService.Heartbeat:Connect(function()if toggles.noKnock and RootPart then local v=RootPart.AssemblyLinearVelocity;if v.Magnitude>60 then RootPart.AssemblyLinearVelocity=Vector3.new(0,v.Y,0)end end end)

-- ATTACK TAB - Auto Hit
local ahbtn=Instance.new("TextButton");ahbtn.Size=UDim2.new(1,-20,0,55);ahbtn.Position=UDim2.new(0,10,0,10);ahbtn.BackgroundColor3=Color3.fromRGB(120,40,40);ahbtn.Text="Auto Hit: OFF";ahbtn.TextColor3=Color3.white;ahbtn.Font=Enum.Font.GothamBold;ahbtn.TextSize=18;ahbtn.Parent=tabContents.Attack;local ahc=Instance.new("UICorner",ahbtn);ahc.CornerRadius=UDim.new(0,10)
ahbtn.MouseButton1Click:Connect(function()toggles.autoHit=not toggles.autoHit;ahbtn.Text="Auto Hit: "..(toggles.autoHit and "ON"or"OFF");ahbtn.BackgroundColor3=toggles.autoHit and Color3.fromRGB(255,100,100)or Color3.fromRGB(120,40,40)end)
task.spawn(function()while task.wait(0.3)do if toggles.autoHit then local closest=math.huge;local tar=nil
 for _,p in pairs(Players:GetPlayers())do if p~=LocalPlayer and p.Character and p.Character:FindFirstChild("HumanoidRootPart")then local dist=(RootPart.Position-p.Character.HumanoidRootPart.Position).Magnitude;if dist<closest and dist<80 then closest=dist;tar=p.Character.HumanoidRootPart end end end
 if tar then firetouchinterest(RootPart,tar,0);task.wait();firetouchinterest(RootPart,tar,1)end
end end end)

-- MOVEMENT TAB - Speed+Fly
local sbtn=Instance.new("TextButton");sbtn.Size=UDim2.new(1,-20,0,50);sbtn.Position=UDim2.new(0,10,0,10);sbtn.BackgroundColor3=Color3.fromRGB(40,60,120);sbtn.Text="Speed 50: OFF";sbtn.TextColor3=Color3.white;sbtn.Font=Enum.Font.GothamBold;sbtn.TextSize=16;sbtn.Parent=tabContents.Movement;local sc=Instance.new("UICorner",sbtn);sc.CornerRadius=UDim.new(0,10)
sbtn.MouseButton1Click:Connect(function()toggles.speed=not toggles.speed;sbtn.Text="Speed 50: "..(toggles.speed and "ON"or"OFF");sbtn.BackgroundColor3=toggles.speed and Color3.fromRGB(100,150,255)or Color3.fromRGB(40,60,120)end)
RunService.RenderStepped:Connect(function()if Humanoid then Humanoid.WalkSpeed=tonumber((toggles.speed and"50"or"16"))end end)

local fbtn=Instance.new("TextButton");fbtn.Size=UDim2.new(1,-20,0,50);fbtn.Position=UDim2.new(0,10,0,65);fbtn.BackgroundColor3=Color3.fromRGB(60,40,120);fbtn.Text="Fly: OFF";fbtn.TextColor3=Color3.white;fbtn.Font=Enum.Font.GothamBold;fbtn.TextSize=16;fbtn.Parent=tabContents.Movement;local fc=Instance.new("UICorner",fbtn);fc.CornerRadius=UDim.new(0,10)
local bv,bg;fbtn.MouseButton1Click:Connect(function()toggles.fly=not toggles.fly;fbtn.Text="Fly: "..(toggles.fly and "ON"or"OFF");fbtn.BackgroundColor3=toggles.fly and Color3.fromRGB(180,120,255)or Color3.fromRGB(60,40,120)
 if toggles.fly then bv=Instance.new("BodyVelocity");bv.MaxForce=Vector3.new(4e4,4e4,4e4);bv.Velocity=Vector3.new();bv.Parent=RootPart;bg=Instance.new("BodyGyro");bg.MaxTorque=Vector3.new(4e4,4e4,4e4);bg.CFrame=RootPart.CFrame;bg.Parent=RootPart
 else if bv then bv:Destroy()end;if bg then bg:Destroy()end end end)
RunService.Heartbeat:Connect(function()if toggles.fly and bv and bg then local cam=workspace.CurrentCamera;local v=cam.CFrame.LookVector*(Humanoid.MoveDirection.Magnitude*45);bv.Velocity=Vector3.new(v.X,(UserInputService:IsKeyDown(Enum.KeyCode.Space)and 45 or UserInputService:IsKeyDown(Enum.KeyCode.LeftShift)and -45 or 0),v.Z);bg.CFrame=cam.CFrame end end)

print("🌌 WOKE ST4RS v.3 CUSTOM HUB LOADED)
