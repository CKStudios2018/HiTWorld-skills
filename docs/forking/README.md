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
  
  To help you speed along the process of placing these blocks, it's worth noting that you can place them evenly at an interval of `x+1.12` (or `y+1.12` for placing the block next to another one) with `x` (or `y`) being where your previously placed block was. For example, if I place a `path-straight` block at `x = 0; y = 1.61` the next block would be placed above it at `x = 0; y = 2.73`, then `x = 0; y = 3.85`.
  
  For `path-junction` block's, it's just as simple, with a slightly different formula. To attach `path-straight` block to it, you need to do `x*1.7` to get a block above it, or `x/1.7` to get the block below it (same applies for `y` values). i.e `path_junction` at `x = 0; y = 0;` goes to `x = 1.7; y = 0;`.
  
  To do the reverse (put a `path_junction` tile around a `path_straight`), simply add or subtract 1.85 on `x` or `y`.
  
  **We recommend that all** `paths` **have a** `z` **value of** `1`**.**
  
- Music

  Another theoretical, yet untrue process, is the sounds. HiT World should, like any good game, have a sound engine. Instead, we slapped the music file onto our `player` object. *You are always the player, so you'll always hear the music*
  
  Please, for your own sake, use or create your own sound engine.

## The updated patch

HiT World has been patched to use a tilemap in v0.9.2 - A newer version of the files to download will be available to download soon!
