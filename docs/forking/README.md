# Docs on Forking HiT World

- These docs are for Forking HiT World v0.8 (a **BETA** version *restored* by [V1RU5](https://github.com/jodri-code))
- Everything mentioned is in the [Google Drive Folder](https://drive.google.com/drive/u/0/folders/1ujQ28-in2dxSWqQbJtsk7_WaqBCEzKQ-); these files include:
  - The updated logo (the saved `.zip` files use the old logo)
  - The main `.zip` with the main game files and assets
  - A basic README.md file with some "getting started with your HiT World Fork" help

## Getting Started with Unity and HiT World

It's all in the [README.md](https://docs.google.com/document/d/10z52nBCIjpex67x2xdRJLJLf7UaGJeQ7-KCZ-ve4-v4/) file.

## Some Advanced (Game Dev Env) help

These are some useful tips to help you with developing your fork of HiT World directly from the Google Drive Folder.

- Block Spacing

  Theoretically, the "world" or "landscape" for HiT World should've been made using a tilemap. Instead, it's manually placed tile assets, which we like to call "block"'s.
  
  To help you speed along the process of placing these blocks, it's worth noting that you can place them evenly at an interval of `x+1.12` with `x` being where your previously placed block was. For example, if I place a `path-straight` block at `x = 0; z = 1.6` the next block would be placed above it at `x = 0; y = 2.72`, then `x = 0; y = 3.84`.
  
  For `path-junction` block's, there's a bit more math involved. To attach `path-straight` block to it, you need to do `x*1.7` to get a block above it, or `x/1.7` to get the block below it.
  
  To do the reverse (put a `path-junction` tile around a `path-straight`), simply add or subtract 1.85 on `x`.
  
- Music

  Another theoretical, yet untrue process, is the sounds. HiT World should, like any good game, have a sound engine. Instead, we slapped the music file onto our `player` object. *You are always the player, so you'll always hear the music*
  
  Please, for your own sake, use or create your own sound engine.
