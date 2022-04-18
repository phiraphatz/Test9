function ChangeName()
    for i,v in pairs(game:GetService("Workspace").Shop.place.blinkep:GetChildren()) do -- GetDescendants
a = 3
if a == i then
    v.Name = "GG"
    end
end
end

function FindLocation()
for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack.Location.Handle.SurfaceGui:GetChildren()) do
    if v.Text == "TECHNIC SHOP" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Inbox.technicshop.Part.CFrame * CFrame.new(0,-4,-5)
        wait(1)
        fireclickdetector(game:GetService("Workspace").Inbox.technicshop.ClickDetector)
    elseif v.Text == "MINE" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Inbox.mine.Part.CFrame * CFrame.new(0,-4,-5)
        wait(1)
        fireclickdetector(game:GetService("Workspace").Inbox.mine.ClickDetector)
    elseif v.Text == "METAL SHOP" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Inbox.metalshop.Part.CFrame * CFrame.new(0,-4,-5)
        wait(1)
        fireclickdetector(game:GetService("Workspace").Inbox.metalshop.ClickDetector)
    elseif v.Text == "SAW MILL" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Inbox.sawmill.Part.CFrame * CFrame.new(0,-4,-5)
        wait(1)
        fireclickdetector(game:GetService("Workspace").Inbox.sawmill.ClickDetector)
    elseif v.Text == "HUNTING STORE" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Inbox.huntingstore.Part.CFrame * CFrame.new(0,-4,-5)
        wait(1)
        fireclickdetector(game:GetService("Workspace").Inbox.huntingstore.ClickDetector)
        wait(1)
    elseif v.Text == "RICE MILL" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Inbox.ricemaill.Part.CFrame * CFrame.new(0,-4,-5)
        wait(1)
        fireclickdetector(game:GetService("Workspace").Inbox.ricemaill.ClickDetector)
    end
    end
end

Section:NewToggle("Auto Farm (Delivery)", "ToggleInfo", function(state)
    if state then
        a1 = true
    else
        a1 = false
    end
end)

spawn(function()
while wait() do
if a1 == true then
pcall(function()
ChangeName()
wait(.25)
fireclickdetector(game:GetService("Workspace").Shop.place.blinkep.GG.click.ClickDetector)
wait(.25)
FindLocation()
end)
end
end
end)
