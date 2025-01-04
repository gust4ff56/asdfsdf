local UILib = loadstring(game:HttpGet(''))()
local Window = UILib.new(gameName, userID, rank)

-- Available functions: Window:Notification({Title = Title, Description = Description}) & prompt, same parameters

-- Other useful functions:
-- Window:ChangeCategory(string new)
-- Window:ChangeCategorySelection(string name) -- no fucking idea what this does

local Category = Window:Category("Main", "https://imgur.com/JbruMQn")
local SubButton = Category:Button("Options", "")
local Section = SubButton:Section("Selection", "Left")

--[[
  Section functions:
  - Section:Button(dictionary Settings (Title, Description & ButtonName are needed), function Callback)
  - Section:Checkbox(dictionary Settings (Title, Description & default (boolean) are needed.), function Callback - fired with boolean)
  - Section:Toggle (same as checkbox)
  - Section:Textbox(dictionary Settings (Title, Description & string default are needed), function Callback - fired with string)
  - Section:Keybind (dictionary Settings (Title, Description & Enum.KeyCode default is needed), function Callback - fired with nothing.)
  - Section:ColorPicker (dictionary settings (Title, Description & Color3 default is needed), function Callback - fired with color.)
  - Section:Slider(dictionary settings (Title, Description, number Min, number Max, number Default), function Callback - fired with number)
  - Section:Dropdown - this one is vague as fuck - just look into the code for it.
]]
