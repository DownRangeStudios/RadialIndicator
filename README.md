# RadialIndicator
 Module that places positional markers in a radius on your screen

Basic Usage:
1. Require the RadialIndicator module in your code
2. Call `RadialIndicator.Indicate(Target, Style, Properties)`
    `Target` must be either a Position or a Part. It is where your indicator will aim. It is a required parameter.
    `Style` must either be `nil` or a string with the name of a Style in the Style library, which is described below. This parameter is optional.
    `Properties` must either be `nil` or a table with properties for how the indicator should behave. This parameter is optional.
* While `Properties` is indeed optional, it is recommended that you supply it with an IgnoreList value if your Target is a part. Failure to do so may result in unintended behavior from the ray that checks if your view is obscured.