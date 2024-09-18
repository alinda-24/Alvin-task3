# 🎮 Building a Simple Game in Java

The following assignment involves creating a fun and interactive game application using Java! You will enhance your programming skills by designing classes, handling player actions, managing scores, and implementing enemy interactions in a simulated environment.

### 👨🏽‍🏫 Instructions
For detailed instructions on how to complete and submit this assignment, please refer to the [assignments section of the course instructions](https://example.com/assignments).

### 📝 Preparation
- Review Module 4: [Object-Oriented Programming in Java](https://example.com/module4).
- Ensure you understand key concepts about classes and objects in Java.
- Familiarize yourself with Java documentation for [standard libraries](https://docs.oracle.com/en/java/).

### ✅ Learning Goals

* Designing Java classes
* Adding instance fields
* Creating and using constructor methods
* Incorporating getters and setters
* Understanding variable scope and shadowing
* Practicing interaction through the terminal
* Using the `main` method

### 🎯 Assignment

#### Exercise 4.0 -- Setting Up the Basics
Create a new class called `Game.java` in the `src` directory. This class should house the infrastructure for your game environment.

1. **Class Design & Fields**: 
    - Create a `Player` class with fields for `playerName` (String), `positionX` (int), `positionY` (int), and `score` (int).
    - Initialize default values for position to be `(0,0)` and score as `0`.
2. **Constructor**:
    - Add a constructor in the `Player` class that takes `playerName` as a parameter and initializes the other fields. 
    - Add a constructor in the `Game` class to initialize game setup if needed.

<details>
<summary> 🛠 Example Main Method </summary>

```java
public static void main(String[] args) {
    Game newGame = new Game();
    Player player = new Player("Adventurer");
    System.out.println("Welcome " + player.getPlayerName() + "!");
}
```
</details>

#### Exercise 4.1 -- Moving the Player and Score System
Expand the `Player` class to include:

1. **Methods**:
    - `move(int deltaX, int deltaY)`: Update the player's position.
    - `addScore(int points)`: Increase the score by a given number of points.
  
2. **Getters and Setters**:
    - Implement getters and setters for `positionX`, `positionY`, and `score` to manage these fields.

3. **Scope and Variable Shadowing**: Ensure that variable shadowing does not occur within your methods and understand why maintaining clarity is important.

<details>
<summary> 🛠 Example Usage </summary>

```java
public static void main(String[] args) {
    Player player = new Player("Hero");
    player.move(5, 3);
    player.addScore(10);
    System.out.println("Position: (" + player.getPositionX() + ", " + player.getPositionY() + ")");
    System.out.println("Score: " + player.getScore());
}
```
</details>

#### Exercise 4.2 -- Enemy Interactions
Introduce an `Enemy` class to simulate interactions:

1. **Fields**:
    - Define fields such as `enemyName` (String), `positionX` (int), and `positionY` (int).
    
2. **Interaction Method**:
    - Create a method in `Game` class `checkCollision(Player player, Enemy enemy)` that calculates if the player and enemy occupy the same coordinates, producing a terminal message if they do.

<details>
<summary> 📚 Collision Example </summary>

```java
public static void main(String[] args) {
    Player player = new Player("Warrior");
    Enemy goblin = new Enemy("Goblin", 5, 3);
    player.move(5, 3);

    Game game = new Game();
    game.checkCollision(player, goblin);
}
```
</details>

### 🎮 Further Development Ideas
- Create multiple enemies with varying behavior or movement.
- Implement a timer or round system.
- Develop a graphical interface using a UI library.

### ❎ Checklist

- [ ] Set up basic class structure for the game.
- [ ] Implement player movement and scoring system.
- [ ] Handle enemy interactions.
- [ ] Utilize getters and setters appropriately.
- [ ] Demonstrate understanding of scope and variable shadowing.

Now, unleash your creativity and get programming! Happy coding! 🎉