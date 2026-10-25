--[[
          __      __      __      __      __      __
     ____/  \____/  \____/  \____/  \____/  \____
   /  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  \
  /   Bacon Guard v0.43.0 | FAST Protection | Build 2d8b37a36177
 /    https://baconbossscript.com/
 \  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  ~~~  /
  \____  ____  ____  ____  ____  ____  ____  ____  ____/
       \/    \/    \/    \/    \/    \/    \/
]]
local _s=game:GetService("Players")
local _M=game:GetService("StarterGui")
local _N=game:GetService("TweenService")
local _c=game:GetService("RunService")
local _p=_s.LocalPlayer
local _B=_p.Character or _p.CharacterAdded:Wait()
local _n=_B:WaitForChild("Humanoid")
local _L=_B:WaitForChild("HumanoidRootPart")
_M:SetCore("SendNotification",{Title="xdzn Runtime",Text="Environment initialized successfully",Duration=4})
print("[xdzn Runtime] Environment initialized successfully. Developed by xdzn.")
local _h=false
local _t=false
local _U=nil
local _V=nil
local function _r()local _u,_I=pcall(function()return _n:GetAppliedDescription()
end)
if _u and _I then return _I
end
return nil
end
local function _v(_D)local _e=_r()
if not _e then return
end
if not _U then _U=_e:Clone()
end
_e.HeightScale=_D
_e.WidthScale=_D
_e.DepthScale=_D
_e.HeadScale=_D
_n:ApplyDescription(_e)
end
local function _w()if _U then _n:ApplyDescription(_U)
else _v(1)
end
end
local function _y()if _h then _w()
_h=false
else _v(3.2)
_h=true
end
end
local _z=507771019
local function _q()if _V then _V:Stop()
_V:Destroy()
_V=nil
end
_t=false
end
local function _m()_q()
local _Z=_n:FindFirstChildOfClass("Animator")
if not _Z then _Z=Instance.new("Animator")
_Z.Parent=_n
end
local _F=Instance.new("Animation")
_F.AnimationId="rbxassetid://".._z
local _S,_E=pcall(function()return _Z:LoadAnimation(_F)
end)
if _S and _E then _E.Looped=true
_E.Priority=Enum.AnimationPriority.Action
_E:Play()
_V=_E
_t=true
end
end
local function _P()if _t then _q()
else _m()
end
end
local _o=Instance.new("ScreenGui")
_o.Name="xdznHub"
_o.ResetOnSpawn=false
_o.ZIndexBehavior=Enum.ZIndexBehavior.Sibling
_o.Parent=_p:WaitForChild("PlayerGui")
local _C=Instance.new("Frame")
_C.Name="Main"
_C.Size=UDim2.new(0,320,0,280)
_C.Position=UDim2.new(0.5,-160,0.5,-140)
_C.BackgroundColor3=Color3.fromRGB(18,18,22)
_C.BorderSizePixel=0
_C.Parent=_o
local _f=Instance.new("UICorner")
_f.CornerRadius=UDim.new(0,12)
_f.Parent=_C
local _O=Instance.new("UIStroke")
_O.Color=Color3.fromRGB(40,40,50)
_O.Thickness=1.5
_O.Parent=_C
local _X=Instance.new("Frame")
_X.Name="TitleBar"
_X.Size=UDim2.new(1,0,0,42)
_X.BackgroundColor3=Color3.fromRGB(28,28,34)
_X.BorderSizePixel=0
_X.Parent=_C
local _Q=Instance.new("UICorner")
_Q.CornerRadius=UDim.new(0,12)
_Q.Parent=_X
local _b=Instance.new("Frame")
_b.Size=UDim2.new(1,0,0,12)
_b.Position=UDim2.new(0,0,1,-12)
_b.BackgroundColor3=Color3.fromRGB(28,28,34)
_b.BorderSizePixel=0
_b.Parent=_X
local _W=Instance.new("TextLabel")
_W.Name="Title"
_W.Size=UDim2.new(1,-20,1,0)
_W.Position=UDim2.new(0,10,0,0)
_W.BackgroundTransparency=1
_W.Text="xdzn Hub"
_W.Font=Enum.Font.GothamBold
_W.TextSize=20
_W.TextColor3=Color3.fromRGB(255,255,255)
_W.TextXAlignment=Enum.TextXAlignment.Left
_W.Parent=_X
local _R=Instance.new("TextLabel")
_R.Name="Brand"
_R.Size=UDim2.new(1,-40,0,36)
_R.Position=UDim2.new(0,20,0,60)
_R.BackgroundTransparency=1
_R.Text="xdzn"
_R.Font=Enum.Font.GothamBlack
_R.TextSize=32
_R.TextColor3=Color3.fromRGB(120,180,255)
_R.Parent=_C
local _d=Instance.new("TextLabel")
_d.Name="Sub"
_d.Size=UDim2.new(1,-40,0,20)
_d.Position=UDim2.new(0,20,0,96)
_d.BackgroundTransparency=1
_d.Text="Runtime Tools"
_d.Font=Enum.Font.Gotham
_d.TextSize=13
_d.TextColor3=Color3.fromRGB(140,140,160)
_d.Parent=_C
local _G=Instance.new("Frame")
_G.Name="ButtonHolder"
_G.Size=UDim2.new(1,-40,0,110)
_G.Position=UDim2.new(0,20,0,130)
_G.BackgroundTransparency=1
_G.Parent=_C
local function _g(_J,_k,_T)local _A=Instance.new("TextButton")
_A.Name=_J
_A.Size=UDim2.new(1,0,0,44)
_A.Position=UDim2.new(0,0,0,_T)
_A.BackgroundColor3=Color3.fromRGB(32,32,40)
_A.BorderSizePixel=0
_A.Text=_k
_A.Font=Enum.Font.GothamMedium
_A.TextSize=15
_A.TextColor3=Color3.fromRGB(230,230,240)
_A.AutoButtonColor=false
_A.Parent=_G
local _i=Instance.new("UICorner")
_i.CornerRadius=UDim.new(0,8)
_i.Parent=_A
local _H=Instance.new("UIStroke")
_H.Color=Color3.fromRGB(55,55,70)
_H.Thickness=1
_H.Parent=_A
_A.MouseEnter:Connect(function()_N:Create(_A,TweenInfo.new(0.15),{BackgroundColor3=Color3.fromRGB(45,45,58)}):Play()
end)
_A.MouseLeave:Connect(function()_N:Create(_A,TweenInfo.new(0.15),{BackgroundColor3=Color3.fromRGB(32,32,40)}):Play()
end)
return _A
end
local _j=_g("GiantBtn","Giant Morph",0)
local _l=_g("DanceBtn","Dance Emote",54)
_j.MouseButton1Click:Connect(function()_y()
_j.Text=_h and"Reset Morph"or"Giant Morph"
end)
_l.MouseButton1Click:Connect(function()_P()
_l.Text=_t and"Stop Dance"or"Dance Emote"
end)
_p.CharacterAdded:Connect(function(_a)_B=_a
_n=_a:WaitForChild("Humanoid")
_L=_a:WaitForChild("HumanoidRootPart")
_h=false
_t=false
_U=nil
_V=nil
_j.Text="Giant Morph"
_l.Text="Dance Emote"
end)
local _x=false
local _K,_Y
_X.InputBegan:Connect(function(_sf)if _sf.UserInputType==Enum.UserInputType.MouseButton1 then _x=true
_K=_sf.Position
_Y=_C.Position
end
end)
_X.InputEnded:Connect(function(_Mf)if _Mf.UserInputType==Enum.UserInputType.MouseButton1 then _x=false
end
end)
game:GetService("UserInputService").InputChanged:Connect(function(_Nf)if _x and _Nf.UserInputType==Enum.UserInputType.MouseMovement then local _cf=_Nf.Position-_K
_C.Position=UDim2.new(_Y.X.Scale,_Y.X.Offset+_cf.X,_Y.Y.Scale,_Y.Y.Offset+_cf.Y)
end
end)
