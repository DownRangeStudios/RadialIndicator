 # RadialIndicator
 Module that places positional markers in a radius on your screen
 
 Basic usage of this module consists of how to use it to apply the default indicator to a target.
 
 Advanced usage of this module consists of creating custom styles and the specific properties of individual indicators.
 
**Basic Usage**:<br/>
1. Require the RadialIndicator module in your code, i.e.: require(game.ReplicatedStorage.RadialIndicator)<br/> 
2. Call `RadialIndicator.Indicate(Target, Style, Properties)`<br/>
*    `Target` must be either a position (Vector3 value) or a part. It is where your indicator will aim. It is a required parameter.<br/>
*    `Style` must either be `nil` or a string with the name of a Style in the Style library, which is described below. This parameter is optional.<br/>
*    `Properties` must either be `nil` or a table with properties for how the indicator should behave. This parameter is optional.<br/>
**While `Properties` is indeed optional, it is recommended that you supply it with an `IgnoreList` value if your Target is a part. Failure to do so may result in unintended behavior because the module checks if your view of the target is obstructed.**

Example:<br/>
```
local RadialIndicator = require(game.ReplicatedStorage.RadialIndicator)

local ThisPart = Instance.new("Part")
ThisPart.Size = Vector3.new(5, 5, 5)
ThisPart.Parent = workspace

RadialIndicator.Indicate(ThisPart, nil, {
 IgnoreList = {ThisPart}
})
```

**Advanced Usage**:
