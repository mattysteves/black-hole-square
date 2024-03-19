# Improvements / work sheet:

## 1. Scroll-Wheel Support
Added mouse scroll wheel controls. Sroll wheel can be used to "swipe" rather than clicking and dragging with a mouse. While playing the game as a user I found the smooth swiping interface of the game very satisfying, but clicking and dragging it with a mouse is slightly tedious. The mouse scroll wheel was an obvious choice for this function as it is not been bound to any other game function and suits the "swiping" style of the game interface in a mouse (rather than touch) context.

This commit added the functionality to the puzzle logic with a quick code comment to describe the code block's purpose, as it looks similar to existing code but performs a different, specific function.

## 2. Settings Screen
Added a settings page to the game as a framework for adding future functionality, most notably an in-game mute function, control options, and visual theming options. The settings screen is included in a way that is easy to access and stays in line with the game's existing interface and theme. The idea behind this work-in-progress addition is to open an obvious space in the project for other developers.

This commit added the settings page to the game's assets and load order. This should enable future developers to have an easier time adding game configuration functionality without worrying about where to put it.

## 3. Remove Unimplemented Monetisation Logic and Assets
Removed useless monetisation code that was not being used and was clogging up game logic wherever the sequence of levels needed to be checked. Since monetisation was not implemented in the original game and there is no plan for it to be implemented by the original developer or in this fork, it made sense to remove this code before it caused problems later on in development. 

This commit replaced all instances of this conditional "monetisation" logic across the game logic files. The conditionals were replaced with direct references to the needed assets. The "paid" assets were also removed and so cannot be referenced or cause confusion in the future.

