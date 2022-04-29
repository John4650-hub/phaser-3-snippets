### Creating a scene in phaser
- **with classes**
We can create scenes in phaser using es6 classes as below. I prefer arcade physics and rarely use matter:
```js
class mainScene extends Phaser.Scene{
	constructor(){
		super({key:'mainscene'});
	}
	preload(){}
	create(){}
	update(){}
}

const config = {
	type: Phaser.AUTO,
	parent: 'div_id',
	scale: {
	mode: Phaser.Scale.FIT
	},
	width:800,
	height:600,
	physics: {
		default:'arcade',
		arcade:
			{
			gravity:{y:200}
			debug:false
			}
	},
	scene:[mainScene]
}
const game = Phaser.Game(config):
```

- **The other way**:
I use this way when am only working in one scene

```js
const config = {
	type: Phaser.AUTO,
	parent: 'div_id',
	scale: {
	mode: Phaser.Scale.FIT
	},
	width:800,
	height:600,
	physics: {
		default:'arcade',
		arcade:
			{
			gravity:{y:200}
			debug:false
			}
	},
	scene:{
		preload,
		create,
		update
	}
}
const game = Phaser.Game(config):

function preload(){}
function create(){}
function update(){}
```

## Loading in things
We do this either in the config or the preload
#### images
```Js
this.load.image('imgKey','imageSrc');
```
#### spritesheet
```js
this.load.spritesheet('key','spritesheetSrc'{frameWidth:'widthOfTheImage/numOfColumns',frameHeight:'heightOfTheImage/numOfRows'});
```
#### audio
```js
this.load.audio('audioKey','audioSrc');
```
