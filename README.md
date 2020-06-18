# Devigetmw

## Description
Welcome to the Minesweeper game, in this repository you will find the APIs necessaries to be able to render a fully functional minesweeper game.

----

## Technology

+ Java 11
+ Spring Boot
+ Maven
+ Junit
+ Hibernate


---
## Rest APIs
### /markCell
### /revealCell
### /startGame
### /pauseGame


---
## Class Diagram

### Player
	- id

### PlayerGames
	- playerId
	- gameId
### Cell
	- isMined
	- isMarked
	- isRevealed
### Game
	- List<List<Cell>> gameMap
	- id
	- score
	- status
	- startDateStime
	- time

---
## Design Document
### Start button
	
	Ability to select the game parameters: number of rows, columns, and mines
	/starGame?x=10,y=10,mines=?
		Assign a unique id to the game
		This start the time
		Initialize the game	
		Place random mines

### Click one of the Cell
	
	This will call the revealCell service on this one will be the majority of the logic releated to the game, it will return the updated map 
	/revealCell?x=7,y=6,gameId=123
	When a cell with no adjacent mines is revealed, all adjacent squares will be revealed (and repeat)
	return gameMap

### Mark a cell
	will mark the cell with a flag
	/markCell?x=7,y=6,gameId=123

### Pause Game
	will handle the logic of the time used to play
	/pauseGame?gameId=123
		Time logic





-----
