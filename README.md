game:GetService("StarterGui"):SetCore("SendNotification",{
    Title = "quracik",
    Text = "Made By quracik",
    Icon = "rbxassetid://57254792";
Duration = 5;
})
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Level Qura W Phyt", "BloodTheme")
    -- MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")

MainSection:NewLabel("Level Spoofer")

MainSection:NewTextBox("Level", 10044538000, function(arg)
local Targets
	Targets = tonumber(arg)
	wait(0.1)
	local mt = getrawmetatable(game);
setreadonly(mt, false);
local old_index = mt.__index;
mt.__index = function(a, b)
    if tostring(a) == "PPLevel" or tostring(a) == "Level" then
        if tostring(b) == "Value" then
            return Targets;
        end
    end
    return old_index(a, b);
end
end)

MainSection:NewTextBox("XP", 10044538000, function(arg)
local Targetz
	Targetz = tonumber(arg)
	wait(0.1)
	local mt = getrawmetatable(game);
setreadonly(mt, false);
local old_index = mt.__index;
mt.__index = function(a, b)
    if tostring(a) == "XP" then
        if tostring(b) == "Value" then
            return Targetz;
        end
    end
    return old_index(a, b);
end
end)
