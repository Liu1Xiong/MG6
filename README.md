# MG6

## Devlog
1) The whole loop should complete in the frame before the Update() finishes. It will thus probably make the game lag as Unity must wait for everything inside the Update() finish before rendering the next frame. 
2) I found that one issue while playing is that even if the player does not clear the whole platform during the jump, as long as the player makes contact with the platform they will get stuck in it and can jump over it in the following jump, allowing players to jump to platforms that their character technically didn't clear. This probably stems from the code which defines the player as being in a state of jumping as long as their movement exceeds 0, so once the player gets partially caught in a platform the game no longer considers them jumping and their collider reactivates, causing them to get stuck midway through said platform. 
