<template>
<div style="overflow: scroll">
<v-html>
<h1>RECIPES DOCUMENTATION </br>Version: 1.19.10.20</h1>
This is documentation for a preview release of Minecraft. New features, components, and capabilities in this release are not final and might change without notice before the final release.<br/>Be sure to check the documentation once the release is out of preview if your add-on isn't working properly. Resource and Behavior Packs created for the preview are not guaranteed to work on the final release.<br/>
<h2><p id="Index">Index</p></h2>
<table border="1">
<tr> <th><a href="#Recipes">Recipes</a></th> </tr>
<tr> <td> <a href="#Furnace Recipe"> Furnace Recipe</a> </tr> </td>
<tr> <td> <a href="#Potion Brewing Container Recipe"> Potion Brewing Container Recipe</a> </tr> </td>
<tr> <td> <a href="#Potion Brewing Mix"> Potion Brewing Mix</a> </tr> </td>
<tr> <td> <a href="#Shaped Recipe"> Shaped Recipe</a> </tr> </td>
<tr> <td> <a href="#Shapeless Recipe"> Shapeless Recipe</a> </tr> </td>
</table>
<a href="#Index">Back to top</a>
<h1><p id="Recipes">Recipes</p></h1>

Recipes are setup in Json files under the behavior_packs /'name of pack'/ recipes directory.</br>Recipe JSON files have different structures dependent on their type.</br>There are 3 types of recipes, Furnace, Shaped and Shapeless.</br><h1><p id="Furnace Recipe">Furnace Recipe</p></h1>

Represents a furnace recipe for a furnace.'Input' items will burn and transform into items specified in 'output'..</br><h2></h2>

<h2><p id="Parameters">Parameters</p></h2>

<h3></h3>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">input</td>
<td style="border-style:solid; border-width:2; padding:8px">item names</td>
<td style="border-style:solid; border-width:2; padding:8px">Items used as input for the furnace recipe.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">output</td>
<td style="border-style:solid; border-width:2; padding:8px">item names</td>
<td style="border-style:solid; border-width:2; padding:8px">Items used as output for the furnace recipe.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h2>Furnace Recipe Example:</h2>
<br / ><textarea readonly="true" cols="60" rows="16">
{
"format_version": "1.12",
"minecraft:recipe_furnace": {
"description": {
"identifier": "minecraft:furnace_beef"
},
"tags": ["furnace", "smoker", "campfire", "soul_campfire"],
"input": {
"item": "minecraft:beef",
"data": 0,
"count": 4
},
"output ": "minecraft:cooked_beef"
}
}
</textarea> </br>
<br><br>

<h1><p id="Potion Brewing Container Recipe">Potion Brewing Container Recipe</p></h1>

Represents a Potion Brewing Container Recipe..</br><h2></h2>

<h2><p id="Parameters">Parameters</p></h2>

<h3></h3>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">input</td>
<td style="border-style:solid; border-width:2; padding:8px">potion</td>
<td style="border-style:solid; border-width:2; padding:8px">input potion used in the brewing container recipe.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">output</td>
<td style="border-style:solid; border-width:2; padding:8px">potion</td>
<td style="border-style:solid; border-width:2; padding:8px">output potion from the brewing container recipe.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">reagent</td>
<td style="border-style:solid; border-width:2; padding:8px">item</td>
<td style="border-style:solid; border-width:2; padding:8px">item used in the brewing container recipe with the input potion.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">tags</td>
<td style="border-style:solid; border-width:2; padding:8px">array of strings</td>
<td style="border-style:solid; border-width:2; padding:8px">Item used in a Brewing Container Recipe.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h2>Potion Brewing Container Recipe Example:</h2>
<br / ><textarea readonly="true" cols="48" rows="16">
{
"format_version": "1.12",
"minecraft:recipe_brewing_container": {
"description": {
  "identifier": "minecraft:brew_potion_sulphur"
  },
 
 "tags": [ "brewing_stand" ],
 
  "input": "minecraft:potion",
  "reagent": "minecraft:gunpowder",
  "output": "minecraft:splash_potion",
 
  }
}
</textarea> </br>
<br><br>

<h1><p id="Potion Brewing Mix">Potion Brewing Mix</p></h1>

Represents a Potion Brewing Mix..</br><h2></h2>

<h2><p id="Parameters">Parameters</p></h2>

<h3></h3>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">input</td>
<td style="border-style:solid; border-width:2; padding:8px">potion</td>
<td style="border-style:solid; border-width:2; padding:8px">input potion used on the brewing stand.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">output</td>
<td style="border-style:solid; border-width:2; padding:8px">potion</td>
<td style="border-style:solid; border-width:2; padding:8px">output potion from mixing the input potion with the reagent on the brewing stand.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">reagent</td>
<td style="border-style:solid; border-width:2; padding:8px">item</td>
<td style="border-style:solid; border-width:2; padding:8px">item used to mix with the input potion.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">tags</td>
<td style="border-style:solid; border-width:2; padding:8px">array of strings</td>
<td style="border-style:solid; border-width:2; padding:8px">Item used to make a brewing mix.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h2>Potion Brewing Mix Example:</h2>
<br / ><textarea readonly="true" cols="54" rows="16">
{
"format_version": "1.12",
"minecraft:recipe_brewing_mix": {
"description": {
  "identifier": "minecraft:brew_awkward_blaze_powder"
  },
 
 "tags": [ "brewing_stand" ],
 
  "input": "minecraft:potion_type:awkward",
  "reagent": "minecraft:blaze_powder",
  "output": "minecraft:potion_type:strength",
 
  }
}
</textarea> </br>
<br><br>

<h1><p id="Shaped Recipe">Shaped Recipe</p></h1>

Represents a shaped crafting recipe for a crafting table.</br>The key used in the pattern may be any single character except the 'space' character, which is reserved for empty slots in a recipe..</br><h2></h2>

<h2><p id="Parameters">Parameters</p></h2>

<h3></h3>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">key</td>
<td style="border-style:solid; border-width:2; padding:8px">array of key and item pairs</td>
<td style="border-style:solid; border-width:2; padding:8px">patten key character mapped to item names.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">pattern</td>
<td style="border-style:solid; border-width:2; padding:8px">array of strings</td>
<td style="border-style:solid; border-width:2; padding:8px">characters that represent a pattern to be defined by keys.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">priority</td>
<td style="border-style:solid; border-width:2; padding:8px">integer</td>
<td style="border-style:solid; border-width:2; padding:8px">Item used as output for the furnace recipe.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">result</td>
<td style="border-style:solid; border-width:2; padding:8px">array of item names</td>
<td style="border-style:solid; border-width:2; padding:8px">when input items match the pattern then these items are the result.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">tags</td>
<td style="border-style:solid; border-width:2; padding:8px">array of strings</td>
<td style="border-style:solid; border-width:2; padding:8px">Item used as input for the furnace recipe.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h2>Shaped Recipe Example:</h2>
<br / ><textarea readonly="true" cols="40" rows="27">
{
"format_version": "1.12",
"minecraft:recipe_shaped": {
"description": {
  "identifier": "minecraft:acacia_boat"
  },
"tags": [ "crafting_table" ],
"pattern": [
        "#P#",
        "###"
        ],
  "key": {
    "P": {
      "item": "minecraft:wooden_shovel"
    },
    "#": {
      "item": "minecraft:planks",
      "data": 4
      }
    },
"result": {
    "item": "minecraft:boat",
    "data": 4
    }
  }
}
</textarea> </br>
<br><br>

<h1><p id="Shapeless Recipe">Shapeless Recipe</p></h1>

Represents a shapeless crafting recipe..</br><h2></h2>

<h2><p id="Parameters">Parameters</p></h2>

<h3></h3>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">ingredients</td>
<td style="border-style:solid; border-width:2; padding:8px">array of item names</td>
<td style="border-style:solid; border-width:2; padding:8px">items used as input (without a shape) for the recipe.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">priority</td>
<td style="border-style:solid; border-width:2; padding:8px">integer</td>
<td style="border-style:solid; border-width:2; padding:8px">Item used as output for the furnace recipe.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">result</td>
<td style="border-style:solid; border-width:2; padding:8px">array of item names</td>
<td style="border-style:solid; border-width:2; padding:8px">these items are the result.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">tags</td>
<td style="border-style:solid; border-width:2; padding:8px">array of strings</td>
<td style="border-style:solid; border-width:2; padding:8px">Item used as input for the furnace recipe.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h2>Shapeless Recipe Example:</h2>
<br / ><textarea readonly="true" cols="52" rows="19">
{
"format_version": "1.12",
"minecraft:recipe_shapeless": {
"description": {
  "identifier": "minecraft:firecharge_coal_sulphur"
  },
 "priority": 0,
 "ingredients": {
      "item": "minecraft:fireball",
      "data": 0,
      "count": 4
 },
"result": {
      "item": "minecraft:blaze_powder",
      "data": 4
      }
  }
}
</textarea> </br>
<br><br>

<br><br>
</v-html>
</div>
</template>

<style scoped>
textarea{
  color: white;
}

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: white;
}

::-webkit-scrollbar-track {
  background: grey;
}
</style>