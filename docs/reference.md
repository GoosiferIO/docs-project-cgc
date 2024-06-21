# Reference Guides

This section intends to include information about miscellaneous topics that might help developers understand the Unreal Engine better. 

## List of Important Unreal Engine Objects

Unreal has several default objects that it must create in order to function, such as the game instance object. These objects have built-in functionality and it is often advantageous to create your own. Defaults can be modified in the edit -> project settings -> Project:Maps&Modes menu. Defaults can also be modified in the world settings menu (docked in the editor by default).

Below is a table of the most important objects in Unreal Engine:

| Object | Description |
| --- | --- |
| Game Instance | There is only one game instance per game. It's automatically created as the game is being initialized and isn't destroyed until the game ends. It is ideal for handling functionality that needs to be available at all times, such as save & load functionality. |
| Game Mode | The game mode handles various rules about the game. Uncertain: It seems only one game mode object can be active per map. In a networked game the game mode is non-replicable (e.g. server side only). |
| Game State | The game state generally handles data about the game. In a networked game this generally means holding things like team scores. Game states are replicated from the server to all clients. |
| Player State | The player state object generally handles data about the player such as player name and score. Player states are replicated from the server to all clients. This allows for things like displaying every player's score in an online FPS game. |
| Player Controller | The player controller handles setup of the controls for the player. This is generally where you would place functionality for changing controls based on context e.g. quicktime events, controlling a car vs. a character, etc. |
| Player Pawn | The player pawn is 'possessed' by the player who is, as the name implies, a disembodied concept unless possessing a pawn. Pawns can be characters with a visually displayed mesh, a car, plane, whatever. Pawns generally have a camera component and a mesh. Individual pawns handle the implementation of the control scheme as defined in the player controller. This way you can allow a player to swap from one pawn to another and have many or all of the same controls shared but with differing implementations as needed. |