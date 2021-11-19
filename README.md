# phaser-3-snippets
Some essential phaser 3 code

## configuration setting
```javascript
let config = {
    type: Phaser.AUTO,
    width: 800,
    height: 600,
    parent: 'phaser-game',
    scene: [SceneMain]
}

var game = new Phaser.Game(config)
```
