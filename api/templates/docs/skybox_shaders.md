# Dragoncraft's Skybox and Model Shader Guide

## Version Note
Core Shaders are not officially supported by Mojang and can change a lot between versions.  
I will try to update this guide for newer versions but can't guarantee that it's always going to be up to date.  
Currently, this guide is for **Minecraft Java 1.21.4**  

This guide also assumes that you already know a bit about ressource packs and how to edit core shaders as going over all of this would be out of scope  
I might add more instructions for that in the future

## Concept and Limitations

These Shaders work by detecting a custom alpha or color value in a model texture and then overriding that with a new color using the shader.  
The use of an item like leather horse armor is recommended as it allows the shader to recieve an additional 3 bytes of input values.   
The core shader responsible for item displays with leather horse armor is `rendertype_item_entity_translucent_cull`, this is also the shader I will be using for the rest of this guide.  


All world shaders are **incompatible with shader mods**, this means that the custom effects will **not** display while a player has enabled a custom shaderpack through the use of mods such as **Iris** or **Optifine**  
It will work fine while the mod is loaded, just not with an active shaderpack

Now with all of that out of the way, we can start to create some cool skyboxes!
## First Steps
First, you need to copy the default minecraft core shader files for the `rendertype_item_entity_translucent_cull` shader into your ressource pack.  
This will make the editing a lot easier.   
A good source for the vanilla files are:  

- [mcmeta by misode](https://github.com/misode/mcmeta/tree/assets/assets/minecraft/shaders/core) 
- [mcasset.cloud by InventivetalenDev](https://mcasset.cloud/1.21.4/assets/minecraft/shaders/core) 