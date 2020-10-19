---
layout: page
title: About
---
These are all [public] standalone scripts, either ones i use, scrapped, to be put into a UI, or WIP.

## AOT: Last Breath Hitbox Expander

```markdown
loadstring(game:HttpGet(('https://raw.githubusercontent.com/EuHellscytheLua/Lua-Script/master/LastBreathHitBox')))()
```

## [SCP] Area 52 - Open All Doors

```markdown
for i,v in pairs(workspace.Doors:GetDescendants()) do
if v.Name == "Open" then
v:FireServer(true)
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
