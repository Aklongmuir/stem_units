# Build a Town Map

## Create a Tilemap

Let's build the world for our game.

Open the **Scene** category and drag out the ``set tilemap to`` block.

Set the map size to **50 × 50** tiles.

Use different tiles to create:
* Grass
* Roads
* Buildings
* Water

~hint

You can change the map size using the size button at the bottom of the Tilemap Editor.

~

## Create a Player

Now add a sprite for the player.

Open the **Sprites** category and create a new sprite of kind ``Player``.

Draw a character that will represent you in the town.

```blocks
let player = sprites.create(img`
`, SpriteKind.Player)
```

## Add Movement

Allow the player to move around the map.

Add the ``move mySprite with buttons`` block and connect it to your player sprite.

```blocks
controller.moveSprite(player)
```

Run your game.

Can your character move?

## Follow the Player

The map is much larger than the screen.

Make the camera follow your player.

```blocks
scene.cameraFollowSprite(player)
```

Run the game again.

The camera should move as your character explores the town.

## Create an NPC

NPC stands for **Non-Player Character**.

Create another sprite to represent someone living in your town.

```blocks
let npc = sprites.create(img`
`, SpriteKind.Food)
```

Possible ideas:
* Teacher
* Shopkeeper
* Friend
* Mayor
* Bus driver

## Place the Characters

Use the ``place on top of tile`` block to position each character on the map.

```blocks
tiles.placeOnTile(player, tiles.getTileLocation(5, 5))
tiles.placeOnTile(npc, tiles.getTileLocation(10, 10))
```

Place them somewhere that makes sense in your town.

~hint

A player might start outside their house while an NPC could be placed near a shop or school.

~

## Add Walls

Buildings should be solid.

Open the Tilemap Editor and mark building tiles as **Walls**.

Test your game.

Can the player walk around the buildings without passing through them?

## Your Turn

Improve your town by adding:

* More buildings
* A park
* A school
* A river
* Extra roads
* More decorations

## Check Your Work

You should now have:

* A 50 × 50 tilemap
* A player character
* An NPC
* Working movement
* A camera that follows the player
* Solid buildings
* A town to explore

Congratulations! You have built the starting map for your town simulation game.
