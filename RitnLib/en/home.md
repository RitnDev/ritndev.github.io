# Presentation
This mod is a library of functions, and since version 0.7 it mainly adds classes used in most RitnMods.
You can obviously use this library for your mods by adding it as a dependency.

## Settings stage
RitnLib currently does not add any function for this game loading stage.

## Data stage
There are functions and classes for this game loading stage.
To access them, you can include the definition file to then load only the modules you need.

```
-- INITIALIZE
---------------
if not ritnlib then require("__RitnLib__/defines") end
```

Then, for example, if you need the "RitnProtoRecipe" class to use its methods, you just have to add the following after the definition declaration :
```
local RitnProtoRecipe = require(ritnlib.defines.class.prototype.recipe)
```

The **ritnlib** variable is global to the entire Data stage, which means you can access it from "data-updates.lua" if you have declared it in the "data.lua" file.

However, the **RitnProtoRecipe** variable (class) is local to the file where it is declared. It is also preferable to always use local variables as much as possible. Local variables occupy less memory and are faster.