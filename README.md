if game.PlaceId == 77152986671070 then

local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "WBlack script farm",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Ari´s HUB",
   LoadingSubtitle = "by ARI",
   Theme = "Default", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = false,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "GG Ari"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "https://discord.gg/xasXErJwxR", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "WBlack script Key",
      Subtitle = "WBlack system key",
      Note = "copy the link", -- Use this to tell the user how to get a key
      FileName = "arihub", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"https://link-target.net/1288464/wblack-keyhub"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

    local WBlackTabTab = Window:CreateTab("Home", nil) -- Title, Image
    local WBlackSection = WBlackTab:CreateSection("WBlack")

Rayfield:Notify({
   Title = "You executed AriHub",
   Content = "AriHub",
   Duration = 3.2,
   Image = nil,
})

local Button = WBlackTab:CreateButton({
   Name = "WalkSpeed",
   Callback = function()
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 60
   end,
})
