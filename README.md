Hello I'm this module developer.
This module is still in the testing phase and may contain errors. If you find any

please contact us by email. - blizzard2035@gmail.com

thx for using this module.

You are welcome to use or remake this module for game development. However, you must show me the results of your remake. Please be sure to read the README before using this module.

# functions

1. Data
- There are many simple data types available, including Colors, GUI Components, and TweenInfos.
2. Animation
- You can use AnimationTrack, LoopTween, and Tween more easily.
3. RunCode
- This will be quite useful, as it allows you to make the code a bit shorter and create more variety with the RepeatForSecond function.
4. DataProfile
- Similar to the profile service, but with more features and requires init function to use.
5. State
- Similar to Fusion's Scope, but with more features.
6. Instances
- You can easily manage instance attributes and distances,
and extract specific IDs using the GetInstanceId function.
It's also similar to Fusion's New function. It has a Children key and a separate OnEvent field.

example Code
```lua
local Light = require(Game:GetService("ReplicatedStorage").Light)

local scope = {}

local Part = Light.NewInstance:New(scope, "Part")({
  Size = Vector3.new(3, 3 ,3),
  Parent = workspace,
  Position = Vector3.new(0, 5 ,0),
  Name = "Part",

  [Light.Children] = {
    -- pass
  }
})

Light.OnEvent(Part, "Touched", function(this)
  Light.OutPut:print("Touched")
end)
```
