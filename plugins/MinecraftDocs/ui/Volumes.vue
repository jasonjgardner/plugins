<template>
<div style="overflow: scroll">
<v-html>
<h1>VOLUMES DOCUMENTATION </br>Version: 1.19.10.20</h1>
This is documentation for a preview release of Minecraft. New features, components, and capabilities in this release are not final and might change without notice before the final release.<br/>Be sure to check the documentation once the release is out of preview if your add-on isn't working properly. Resource and Behavior Packs created for the preview are not guaranteed to work on the final release.<br/>
<h2><p id="Index">Index</p></h2>
<table border="1">
<tr> <th><a href="#Volumes">Volumes</a></th> </tr>
<tr> <td> <a href="#Volume Components"> Volume Components</a> </tr> </td>
<tr> <td> <a href="#Volume Definition Properties"> Volume Definition Properties</a> </tr> </td>
<tr> <td> <a href="#Volume Description Properties"> Volume Description Properties</a> </tr> </td>
</table>
<a href="#Index">Back to top</a>
<h1><p id="Volumes">Volumes</p></h1>

<h1><p id="Volume Components">Volume Components</p></h1>

These are the various possible components for this entity</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:fog</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Displays the given fog whenever a player enters the volume. Each volume can only have one fog attached.</br><table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Default Value</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">fog_identifier</td>
<td style="border-style:solid; border-width:2; padding:8px">String</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">The identifier of a fog definition. Note that you will not receive any feedback if the definition does not exist.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">priority</td>
<td style="border-style:solid; border-width:2; padding:8px">Integer</td>
<td style="border-style:solid; border-width:2; padding:8px">INT_MAX</td>
<td style="border-style:solid; border-width:2; padding:8px">The priority for this fog definition setting. Smaller numbers have higher priority. Fogs with equal priority will be combined together.</br></td>
</tr>
</table>
</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:on_actor_enter</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Component that defines what happens when an actor enters the volume. Can contain multiple json objects.</br><table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Default Value</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">on_enter</td>
<td style="border-style:solid; border-width:2; padding:8px">Array</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">Required array that contains all the triggers.</br><h5><p id="condition">condition</p></h5>

Molang expression to test against the actor. The given event will be triggered if the expression evaluates to true.</br><a href="#Index">Back to top</a><br><br>

<h5><p id="event">event</p></h5>

Name of the event to run.</br><a href="#Index">Back to top</a><br><br>

<h5><p id="target">target</p></h5>

One of "self" or "other". Self means the event is attached to the volume. Other means the event is attached to the actor.</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
</table>
</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:on_actor_leave</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Component that defines what happens when an actor leaves the volume.</br><table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Default Value</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">on_leave</td>
<td style="border-style:solid; border-width:2; padding:8px">Array</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">Required array that contains all the triggers.</br><h5><p id="condition">condition</p></h5>

Molang expression to test against the actor. The given event will be triggered if the expression evaluates to true.</br><a href="#Index">Back to top</a><br><br>

<h5><p id="event">event</p></h5>

Name of the event to run.</br><a href="#Index">Back to top</a><br><br>

<h5><p id="target">target</p></h5>

One of "self" or "other". Self means the event is attached to the volume. Other means the event is attached to the actor.</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
</table>
</td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h1><p id="Volume Definition Properties">Volume Definition Properties</p></h1>

The properties of a minecraft:volume entity. All components are optional.</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">format_version</td>
<td style="border-style:solid; border-width:3; padding:7px">String</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Specifies the version of the game this entity was made in. Minimum supported version is 1.17.0. Current supported version is 1.19.10.</br></td>
</tr>
</table>
<h2>Example</h2>
Example<br / ><textarea readonly="true" cols="58" rows="15">
{
  "format_version": 1.17.0,
  "minecraft:volume": {
    "description": {
      "identifier": "your_custom_namespace:sample_volume"
    },
    "components": {
      "minecraft:fog": {
        "fog_identifier": "minecraft:fog_savanna",
        "priority": 1
      }
    }
  }
}
</textarea> </br>
<a href="#Index">Back to top</a><br><br>

<h1><p id="Volume Description Properties">Volume Description Properties</p></h1>

The description contains a single 'identifier' string</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">identifier</td>
<td style="border-style:solid; border-width:3; padding:7px">String</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The unique identifier for this volume. It must be of the form 'namespace:name', where namespace cannot be 'minecraft'.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

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