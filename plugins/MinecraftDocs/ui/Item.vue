<template>
<div style="overflow: scroll">
<v-html>
<h1>ITEM DOCUMENTATION </br>Version: 1.19.10.20</h1>
This is documentation for a preview release of Minecraft. New features, components, and capabilities in this release are not final and might change without notice before the final release.<br/>Be sure to check the documentation once the release is out of preview if your add-on isn't working properly. Resource and Behavior Packs created for the preview are not guaranteed to work on the final release.<br/>
<h2><p id="Index">Index</p></h2>
<table border="1">
<tr> <th><a href="#Items">Items</a></th> </tr>
<tr> <td> <a href="#Item Components"> Item Components</a> </tr> </td>
<tr> <td> <a href="#Item Definition Properties"> Item Definition Properties</a> </tr> </td>
<tr> <td> <a href="#Item Description Properties"> Item Description Properties</a> </tr> </td>
</table>
<a href="#Index">Back to top</a>
<h1><p id="Items">Items</p></h1>

To define an item, the item definition must be defined in the behavior pack in a JSON file.</br>All attributes, including item names, must be defined using item components.</br><h1><p id="Item Components">Item Components</p></h1>

Below are the various components for item functionality.</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:armor</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The armor item component determines the amount of protection you have in your armor item.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="protection">protection</p></h3>

How much protection does the armor item have.</br>Minimum value: 0</br>Type: integer</br><a href="#Index">Back to top</a><br><br>

<h3><p id="texture_type">texture_type</p></h3>

Texture Type to apply for the armor. Note that Horse armor is restricted to leather, iron, gold, or diamond.</br>Accepted values: "leather", "none", "chain", "iron", "diamond", "gold", "elytra", "turtle", "netherite"</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:block_placer</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Planter item component. planter items are items that can be planted.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="block">block</p></h3>

block:  Set the placement block name for the planter item.</br>Type: block</br><a href="#Index">Back to top</a><br><br>

<h3><p id="use_on">use_on</p></h3>

List of block descriptors that contain blocks that this item can be used on. If left empty, all blocks will be allowed.</br>Type: array of use_on</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:chargeable</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Allows an item to be used over a duration.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="movement_modifier">movement_modifier</p></h3>

Modifier value to scale the players movement speed when item is in use.</br>Minimum value: 0.00</br>Maximum value: 5.00</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="on_complete">on_complete</p></h3>

Event trigger for when the item has completed its use duration.</br>Type: on_complete</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:cooldown</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Cool down time for a component. After you use an item it becomes unusable for the duration specified by the 'cool down time' setting in this component.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="category">category</p></h3>

The type of cool down for this item.</br>Type: category</br><a href="#Index">Back to top</a><br><br>

<h3><p id="duration">duration</p></h3>

The duration of time this item will spend cooling down before becoming usable again.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:digger</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Digger item. Component put on items that dig.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="destroy_speeds">destroy_speeds</p></h3>

Destroy speed per block.</br>Type: array of destroy_speeds</br><a href="#Index">Back to top</a><br><br>

<h3><p id="on_dig">on_dig</p></h3>

Trigger for when you dig a block that isn't listed in destroy_speeds</br>Type: on_dig</br><a href="#Index">Back to top</a><br><br>

<h3><p id="use_efficiency">use_efficiency</p></h3>

Use efficiency? Default is set to false.</br>Type: boolean</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:display_name</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Display Name item component. Display Names set the name to display when an item is in use or hovered over.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="value">value</p></h3>

The display name for an item.</br>Type: string</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:durability</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">A property that determines when an item will break from use. The durability of an item is potentially depleted upon use based on the damage chance.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="damage_chance">damage_chance</p></h3>

Damage chance is the percentage chance of this item losing durability. Default is set to 100. Defined as an int range with min and max value.</br>Type: damage_chance</br><a href="#Index">Back to top</a><br><br>

<h3><p id="max_durability">max_durability</p></h3>

Max durability is the amount of damage that this item can take before breaking.</br>Minimum value: 0</br>Type: integer</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:dye_powder</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Dye powder, there are 16 kinds of dye.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="color">color</p></h3>

Defines what color the dye is.</br>Accepted values: "black", "red", "green", "brown", "blue", "purple", "cyan", "silver", "gray", "pink", "lime", "yellow", "lightblue", "magenta", "orange", "white"</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:entity_placer</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Entity placer item component. You can specifiy allowed blocks that the item is restricted to.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="dispense_on">dispense_on</p></h3>

List of block descriptors that contain blocks that this item can be dispensed on. If left empty, all blocks will be allowed.</br>Type: array of dispense_on</br><a href="#Index">Back to top</a><br><br>

<h3><p id="entity">entity</p></h3>

The entity to be placed in the world.</br>Type: entity</br><a href="#Index">Back to top</a><br><br>

<h3><p id="use_on">use_on</p></h3>

List of block descriptors that contain blocks that this item can be used on. If left empty, all blocks will be allowed.</br>Type: array of use_on</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:food</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">When an item has a food component, it becomes edible to the player.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="can_always_eat">can_always_eat</p></h3>

If true you can always eat this item (even when not hungry). Default is set to false.</br>Type: boolean</br><a href="#Index">Back to top</a><br><br>

<h3><p id="nutrition">nutrition</p></h3>

The value that is added to the actor's nutrition when the item is used. Default is set to 0.</br>Type: integer</br><a href="#Index">Back to top</a><br><br>

<h3><p id="on_consume">on_consume</p></h3>

Event trigger for when the item is consumed.</br>Type: on_consume</br><a href="#Index">Back to top</a><br><br>

<h3><p id="saturation_modifier">saturation_modifier</p></h3>

Saturation Modifier is used in this formula: (nutrition * saturation_modifier * 2) when applying the saturation buff. Default is set to 0.6.</br>Minimum value: 0.00</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="using_converts_to">using_converts_to</p></h3>

When used, converts to the item specified by the string in this field. Default does not convert item.</br>Type: using_converts_to</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:fuel</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Allows this item to be used as fuel in a furnace to 'cook' other items.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="duration">duration</p></h3>

How long in seconds will this fuel cook items for.</br>Minimum value: 0.05</br>Type: float</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:icon</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The icon item component determines the icon to represent the item.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="legacy_id">legacy_id</p></h3>

Legacy texture string id for older item icons. Legacy ID list can be found here under 'Namespaced ID': https://minecraft.fandom.com/wiki/Bedrock_Edition_data_values</br>Type: string</br><a href="#Index">Back to top</a><br><br>

<h3><p id="texture">texture</p></h3>

The key for the object contain the expected textures, from file 'resource_pack/textures/item_texture.json'.</br>Type: string</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:item_storage</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The Storage Item Component is used for storing Items within an Item's User Data</br>Experimental toggles required: Holiday Creator Features or </br><h3><p id="capacity">capacity</p></h3>

The max capacity of the item, default is 64</br>Type: integer</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:knockback_resistance</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Knockback Resistance Item. Component put on items that provide knockback resistance.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="protection">protection</p></h3>

Amount of knockback resistance provided with the total maximum protection being 1.0</br>Type: float</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:on_use</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The on_use item component allows you to receive an event when the item is used.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="on_use">on_use</p></h3>

Event trigger for when the item is used.</br>Type: on_use</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:on_use_on</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The on_use_on item component allows you to receive an event when the item is used on a block in the world.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="on_use_on">on_use_on</p></h3>

Event trigger for when the item is used.</br>Type: on_use_on</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:projectile</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Projectile item component. projectile items shoot out, like an arrow.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="minimum_critical_power">minimum_critical_power</p></h3>

How long you must charge a projectile for it to critically hit.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="projectile_entity">projectile_entity</p></h3>

The entity to be fired as a projectile.</br>Type: projectile_entity</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:record</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Record Item Component.  Used by record items to play music. </br>Experimental toggles required: Holiday Creator Features</br><h3><p id="comparator_signal">comparator_signal</p></h3>

Signal strength for comparator blocks to use, from 1 - 13.</br>Type: integer</br><a href="#Index">Back to top</a><br><br>

<h3><p id="duration">duration</p></h3>

Duration of sound event in seconds, float value.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="sound_event">sound_event</p></h3>

Sound event type: 13, cat, blocks, chirp, far, mall, mellohi, stal, strad, ward, 11, wait, pigstep, otherside, 5.</br>Accepted values: "death.to.zombie", "jump.prevent", "item.use.on", "hit", "step", "break", "swim", "mob.player.hurt_drown", "step.baby", "fly", "horn_call4", "jump", "place", "heavy.step", "gallop", "fall", "hurt", "fizz", "ambient.screamer", "hurt.baby", "hurt.in.water", "death", "flap", "death.baby", "death.in.water", "ambient", "ambient.baby", "ambient.in.water", "undefined", "ignite", "ambient.tame", "thunder", "random.anvil_use", "ambient.pollinate", "breathe", "mad", "boost", "bow", "squish.big", "squish.small", "fall.big", "fall.small", "splash", "drink", "shear", "block.end_portal_frame.fill", "drink.honey", "pick_berries.cave_vines", "born", "eat", "reappeared", "takeoff", "shake", "plop", "land", "saddle", "armor", "item_taken", "mob.armor_stand.place", "add.chest", "record.5", "throw", "attack", "block.frog_spawn.hatch", "attack.nodamage", "attack.strong", "listening_angry", "warn", "sonic_charge", "milk", "explode", "fire", "fuse", "block.frog_spawn.break", "stare", "spawn", "shoot", "break.block", "launch", "blast", "horn_call2", "large.blast", "twinkle", "remedy", "unfect", "copper.wax.off", "convert_to_drowned", "horn_call6", "levelup", "bow.hit", "bullet.hit", "extinguish.fire", "item.fizz", "chest.open", "chest.closed", "shulkerbox.open", "shulkerbox.closed", "enderchest.open", "enderchest.closed", "power.on", "power.off", "attach", "detach", "deny", "tripod", "pop", "drop.slot", "note", "thorns", "piston.in", "piston.out", "portal", "water", "lava.pop", "lava", "celebrate", "beacon.activate", "beacon.ambient", "block.smithing_table.use", "beacon.deactivate", "beacon.power", "pre_ram.screamer", "conduit.activate", "conduit.ambient", "block.click.fail", "conduit.attack", "conduit.deactivate", "glow_squid.ink_squirt", "conduit.short", "bubble.pop", "bubble.up", "tilt_up.big_dripleaf", "bubble.upinside", "power.on.sculk_sensor", "bubble.down", "bubble.downinside", "burp", "bucket.fill.water", "bucket.empty.water", "bucket.fill.lava", "bucket.empty.lava", "bucket.fill.fish", "drip.water.pointed_dripstone", "bucket.empty.fish", "armor.equip_chain", "armor.equip_diamond", "armor.equip_elytra", "armor.equip_generic", "armor.equip_gold", "armor.equip_iron", "armor.equip_leather", "armor.equip_netherite", "record.13", "record.cat", "record.blocks", "record.chirp", "record.far", "record.mall", "record.mellohi", "record.stal", "record.strad", "record.ward", "record.11", "record.wait", "cast.spell", "record.pigstep", "record.otherside", "flop", "elderguardian.curse", "teleport", "shulker.open", "shulker.close", "mob.warning", "mob.warning.baby", "haggle", "haggle.yes", "haggle.no", "haggle.idle", "disappeared", "chorusgrow", "chorusdeath", "glass", "potion.brewed", "prepare.attack", "roar", "prepare.summon", "prepare.wololo", "ambient.warped_forest.loop", "fang", "charge", "particle.soul_escape.quiet", "camera.take_picture", "block.bell.hit", "leashknot.break", "leashknot.place", "growl", "block.composter.fill_success", "whine", "pant", "block.sweet_berry_bush.hurt", "purr", "purreow", "item.book.put", "death.min.volume", "death.mid.volume", "block.composter.empty", "imitate.blaze", "imitate.cave_spider", "ui.stonecutter.take_result", "imitate.creeper", "imitate.elder_guardian", "block.barrel.open", "imitate.ender_dragon", "imitate.enderman", "imitate.evocation_illager", "ambient.in.raid", "imitate.ghast", "imitate.husk", "convert_mooshroom", "imitate.illusion_illager", "imitate.magma_cube", "block.smoker.smoke", "imitate.polar_bear", "imitate.shulker", "raid.horn", "imitate.silverfish", "imitate.skeleton", "imitate.slime", "imitate.spider", "block.beehive.work", "imitate.stray", "imitate.vex", "imitate.vindication_illager", "imitate.witch", "imitate.wither", "imitate.wither_skeleton", "block.beehive.enter", "imitate.wolf", "imitate.zombie", "tempt", "imitate.zombie_pigman", "imitate.zombie_villager", "block.end_portal.spawn", "bottle.dragonbreath", "balloonpop", "sparkler.active", "item.trident.hit", "respawn_anchor.basalt_deltas.mood", "item.trident.hit_ground", "respawn_anchor.charge", "item.trident.return", "item.trident.riptide_1", "angry", "item.trident.riptide_2", "item.trident.riptide_3", "retreat", "item.trident.throw", "item.trident.thunder", "smithing_table.use", "block.fletching_table.use", "elemconstruct.open", "respawn_anchor.set_spawn", "icebomb.hit", "ambient.soulsand_valley.mood", "lt.reaction.icebomb", "lt.reaction.bleach", "lt.reaction.epaste", "lt.reaction.epaste2", "heartbeat", "lt.reaction.fertilizer", "lt.reaction.fireball", "ambient.crimson_forest.loop", "lt.reaction.mgsalt", "lt.reaction.miscfire", "cauldron_drip.water.pointed_dripstone", "lt.reaction.fire", "lt.reaction.miscexplosion", "ambient.basalt_deltas.additions", "lt.reaction.miscmystical", "lt.reaction.miscmystical2", "ambient.nether_wastes.loop", "lt.reaction.product", "sparkler.use", "bucket.fill.powder_snow", "glowstick.use", "block.turtle_egg.break", "sleep", "block.turtle_egg.crack", "block.turtle_egg.hatch", "block.turtle_egg.attack", "swoop", "presneeze", "ambient.candle", "sneeze", "tongue", "scared", "ambient.aggressive", "irongolem.repair", "ambient.worried", "cant_breed", "block.scaffolding.climb", "jump_to_block", "block.bamboo_sapling.place", "block.sculk_shrieker.shriek", "crossbow.loading.start", "crossbow.loading.middle", "cake.add_candle", "crossbow.loading.end", "crossbow.shoot", "agitated", "crossbow.quick_charge.start", "crossbow.quick_charge.middle", "charge.sculk", "crossbow.quick_charge.end", "nearby_closer", "item.shield.block", "admire", "portal.travel", "block.grindstone.use", "block.campfire.crackle", "block.sweet_berry_bush.pick", "block.stonecutter.use", "block.cartography_table.use", "block.composter.fill", "block.composter.ready", "stun", "block.barrel.close", "ui.cartography_table.take_result", "ui.loom.take_result", "block.blastfurnace.fire_crackle", "block.loom.use", "screech", "block.furnace.lit", "milk_suspiciously", "block.beehive.exit", "block.beehive.shear", "block.beehive.drip", "ambient.cave", "converted_to_zombified", "step_lava", "panic", "particle.soul_escape.loud", "respawn_anchor.deplete", "respawn_anchor.ambient", "ambient.crimson_forest.mood", "ambient.warped_forest.mood", "ambient.nether_wastes.mood", "ambient.crimson_forest.additions", "ambient.warped_forest.additions", "ambient.soulsand_valley.additions", "ambient.nether_wastes.additions", "ambient.soulsand_valley.loop", "ambient.basalt_deltas.loop", "lodestone_compass.link_compass_to_lodestone", "power.off.sculk_sensor", "default", "ram_impact.screamer", "lay_egg", "lay_spawn", "bucket.empty.powder_snow", "cauldron_drip.lava.pointed_dripstone", "tilt_down.big_dripleaf", "drip.lava.pointed_dripstone", "copper.wax.on", "scrape", "item.spyglass.use", "item.spyglass.stop_using", "chime.amethyst_block", "mob.player.hurt_on_fire", "mob.player.hurt_freeze", "hurt.screamer", "death.screamer", "milk.screamer", "pre_ram", "ram_impact", "squid.ink_squirt", "convert_to_stray", "extinguish.candle", "block.click", "bloom.sculk_catalyst", "nearby_close", "nearby_closest", "listening", "item_given", "item_thrown", "irongolem.crack", "horn_break", "horn_call0", "horn_call1", "horn_call3", "horn_call5", "horn_call7", "imitate.warden", "sonic_boom", "convert_to_frog", "block.sculk.spread", "block.sculk_sensor.place", "block.sculk_shrieker.place"</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:render_offsets</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Render offsets component: optional values can be given to offset the way the item is rendered.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="main_hand">main_hand</p></h3>

Main hand transform data.</br>Type: main_hand</br><a href="#Index">Back to top</a><br><br>

<h3><p id="off_hand">off_hand</p></h3>

Offhand hand transform data.</br>Type: off_hand</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:repairable</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Repairable item component: how much damage can this item repair, what items can repair it.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="on_repaired">on_repaired</p></h3>

Event that is called when this item has been repaired.</br>Type: on_repaired</br><a href="#Index">Back to top</a><br><br>

<h3><p id="repair_items">repair_items</p></h3>

Repair item entries.</br>Type: array of repair_items</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:shooter</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Shooter Item Component.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="ammunition">ammunition</p></h3>

Ammunition.</br>Type: array of ammunition</br><a href="#Index">Back to top</a><br><br>

<h3><p id="charge_on_draw">charge_on_draw</p></h3>

Charge on draw? Default is set to false.</br>Type: boolean</br><a href="#Index">Back to top</a><br><br>

<h3><p id="launch_power_scale">launch_power_scale</p></h3>

Launch power scale. Default is set to 1.0.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="max_draw_duration">max_draw_duration</p></h3>

Draw Duration. Default is set to 0.</br>Type: max_draw_duration</br><a href="#Index">Back to top</a><br><br>

<h3><p id="max_launch_power">max_launch_power</p></h3>

Launch power. Default is set to 1.0.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="scale_power_by_draw_duration">scale_power_by_draw_duration</p></h3>

Scale power by draw duration? Default is set to false.</br>Type: boolean</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:throwable</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Throwable item component. Throwable items, such as a snowball.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="do_swing_animation">do_swing_animation</p></h3>

Whether the item should use the swing animation when thrown. Default is set to false.</br>Type: boolean</br><a href="#Index">Back to top</a><br><br>

<h3><p id="launch_power_scale">launch_power_scale</p></h3>

The scale at which the power of the throw increases. Default is set to 1.0.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="max_draw_duration">max_draw_duration</p></h3>

The maximum duration to draw a throwable item. Default is set to 0.0.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="max_launch_power">max_launch_power</p></h3>

The maximum power to launch the throwable item. Default is set to 1.0.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="min_draw_duration">min_draw_duration</p></h3>

The minimum duration to draw a throwable item. Default is set to 0.0.</br>Type: float</br><a href="#Index">Back to top</a><br><br>

<h3><p id="scale_power_by_draw_duration">scale_power_by_draw_duration</p></h3>

Whether or not the power of the throw increases with duration charged. Default is set to false.</br>Type: boolean</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:weapon</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Weapon Item Component. Added to every weapon item such as axe, sword, trident, bow, crossbow.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="on_hit_block">on_hit_block</p></h3>

Trigger for letting you know when this item is used to hit a block</br>Type: on_hit_block</br><a href="#Index">Back to top</a><br><br>

<h3><p id="on_hurt_entity">on_hurt_entity</p></h3>

Trigger for letting you know when this item is used to hurt another mob</br>Type: on_hurt_entity</br><a href="#Index">Back to top</a><br><br>

<h3><p id="on_not_hurt_entity">on_not_hurt_entity</p></h3>

Trigger for letting you know when this item hit another actor, but didn't do damage</br>Type: on_not_hurt_entity</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:wearable</td>
<td style="border-style:solid; border-width:3; padding:7px">JSON Object</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Wearable item component.</br>Experimental toggles required: Holiday Creator Features</br><h3><p id="slot">slot</p></h3>

equipment_slot: slot.weapon.mainhand, slot.weapon.offhand, slot.armor.head, slot.armor.chest, slot.armor.legs, slot.armor.feet, slot.hotbar, slot.inventory, slot.enderchest, slot.saddle, slot.armor, slot.chest, slot.equippable</br>Accepted values: "slot.weapon.mainhand", "none", "slot.weapon.offhand", "slot.armor.head", "slot.armor.chest", "slot.armor.legs", "slot.armor.feet", "slot.hotbar", "slot.inventory", "slot.enderchest", "slot.saddle", "slot.armor", "slot.chest", "slot.equippable"</br><a href="#Index">Back to top</a><br><br>

</td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h1><p id="Item Definition Properties">Item Definition Properties</p></h1>

The properties are part of the Item Definition. This helps the system determine how to parse and initialize this item.</br><h2></h2>

<h2><p id="format_version">format_version</p></h2>

Specifies the version of the game this entity was made in. If the version is lower than the current version, any changes made to the entity in the vanilla version will be applied to it.</br><a href="#Index">Back to top</a><br><br>

<h2>Code Example</h2>
Example<br / ><textarea readonly="true" cols="42" rows="22">
{
  "format_version": "1.16.1",
  "minecraft:item": {
    "description": {
      "identifier": "minecraft:blaze_rod"
    },
    "components": {
      "minecraft:fuel": {
        "duration": 120.0
      },
      "minecraft:max_stack_size": 64,
      "minecraft:icon": {
        "texture": "blaze_rod"
      },
      "minecraft:hand_equipped": true,
      "minecraft:display_name": {
        "value": "Blaze Rod"
      }
    }
  }
}
</textarea> </br>
<br><br>

<h1><p id="Item Description Properties">Item Description Properties</p></h1>

<h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">category</td>
<td style="border-style:solid; border-width:3; padding:7px">String</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The category for this item. Categories are used to control high level properties of how the item is integrated into the bedrock engine, such as whether it can be used in slash commands.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">identifier</td>
<td style="border-style:solid; border-width:3; padding:7px">String</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The identifier for this item. The name must include a namespace and must not use the Minecraft namespace unless overriding a Vanilla item.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">is_experimental</td>
<td style="border-style:solid; border-width:3; padding:7px">Boolean</td>
<td style="border-style:solid; border-width:3; padding:7px">false</td>
<td style="border-style:solid; border-width:3; padding:7px">If this item is experimental, it will only be registered if the world is marked as experimental.</br></td>
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