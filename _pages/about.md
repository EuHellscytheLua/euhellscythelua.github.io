---
layout: page
title: Scripts
---
These are all [public] standalone scripts I have made or use.
Updated somewhat frequently, patched scripts are removed.

## AOT: Last Breath Hitbox Expander

```markdown
loadstring(game:HttpGet(('https://raw.githubusercontent.com/EuHellscytheLua/Lua-Script/master/LastBreathHitBox')))()
```

## Untitled Door Game Auto Complete [Requires Level 100+] 

```markdown
local player = game.Players.LocalPlayer
local counter = 0
while true do wait(2)

if workspace.Checkpoints:FindFirstChild(tostring(counter)) then

counter = counter +  1
game.workspace[player.Name].HumanoidRootPart.CFrame = workspace.Checkpoints:FindFirstChild(tostring(counter)).CFrame
end
end
```

## Script Webhook - See who executes script, this one aint mine but is very useful.
```
local webhookcheck =
   is_sirhurt_closure and "Sirhurt" or pebc_execute and "ProtoSmasher" or syn and "Synapse X" or
   secure_load and "Sentinel" or
   KRNL_LOADED and "Krnl" or
   SONA_LOADED and "Sona" or
   "the fuck?"

local url =
   "Insert Webhook"
local data = {
   ["content"] = "_____",
   ["embeds"] = {
       {
           ["title"] = "**_____**",
           ["description"] = "Username: " .. game.Players.LocalPlayer.Name.." with **"..webhookcheck.."**",
           ["type"] = "rich",
           ["color"] = tonumber(0x7269da),
           ["image"] = {
               ["url"] = "http://www.roblox.com/Thumbs/Avatar.ashx?x=150&y=150&Format=Png&username=" ..
                   tostring(game:GetService("Players").LocalPlayer.Name)
           }
       }
   }
}
local newdata = game:GetService("HttpService"):JSONEncode(data)

local headers = {
   ["content-type"] = "application/json"
}
request = http_request or request or HttpPost or syn.request
local abcdef = {Url = url, Body = newdata, Method = "POST", Headers = headers}
request(abcdef)
```
