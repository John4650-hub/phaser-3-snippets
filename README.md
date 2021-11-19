# phaser-3-snippets
Some essential phaser 3 code

## configuration setting
```javascript
import Phaser from './scenes/phamport.js'
import {SceneMain} from './scenes/gameScene.js'

let config = {
  type: Phaser.AUTO,
  width: 800,
  height: 600,
  parent: 'phaser-game',
  scene: [SceneMain]
};

var game = new Phaser.Game(config);
```
For scenes we will store them in another file.Let it be called "gameScenes.js"
and the following code inhabits it

```javascript
import Phaser from './phamport.js'
// here we import phaser

class SceneMain extends Phaser.Scene {
  constructor() {
    super('SceneMain');

  }

  preload()
  {
    this.load.image("theId/name","the_path")
    // some photos to load either sprites
  }
  create() {
this.add.image("x","y","theId/name");

  }
  update()
  {
    //this code is executed everytime the game runs  
  }
}
export { SceneMain };
```
