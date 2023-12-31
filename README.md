# Discord Chess Bot (Version 1.0)

## Description

### Note: This is a self-directed personal project which is optimized for the Linux Ubuntu environment.

This Discord Bot allows users to play chess games, solve tactics, view and analyze previously played games, and check their personal stats. The bot is built using python with the `discord.py` library for interacting with the `Discord API` and the `chess` library for handling chess game logic.

## Video Demo

[Watch the Video Demo Here](https://youtu.be/vSPYnxuu5gE)

## Installation & Setup

To set up the project, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/coolyashas/Discord-Chess-Bot.git
    ```

2. Navigate to the project directory:

    ```bash
    cd Discord-Chess-Bot
    ```

3. Install all necessary libraries:

    ```bash
    pip install -r requirements.txt
    ```

4. Install the CairoSVG library using apt:

    ```bash
    sudo apt-get install cairosvg
    ```

This will set up the Discord Chess Bot codebase and its dependencies for your use.

To run the bot, follow the instructions given in the `.env` file and and then run the `main.py` file.

## Usage

The Discord Chess Bot fully utilizes Discord slash commands for its functionality. Please ensure that the bot has the necessary permissions in your server to ensure full functionality.

- The `/move` and `/solve` commands require an input in the form of "initial square" to "target square".

- Format for `/move` and `/solve` slash commands:

  Correct Format:   g1f3  
  Incorrect Format: Nf3

- `/challenge` and `/move`:  Use these commands to play chess games with other members of the server.

- `/tactics` and `/solve`:  Use these commands to solve chess tactics.

- `/view`:  Use this command to view and analyze previously played games of any member of the server.

- `/stats`:  Use this command to track tactics solved, score, and games played of any member of the server.

The `/tactics` command allows you to choose between three levels of tactics:

- Easy:   1 or 2 moves
- Medium: 2 or 3 moves
- Hard:   3 or 4 moves

Make sure to use the correct format and level when interacting with the bot's slash commands.

## Main Files

1. **main.py**: This file serves as the trigger point for the entire program. It initializes the Discord bot, loads environment variables, and sets up the necessary extensions.

2. **challenge.py**: This file contains the implementation of the `Challenge` cog (Component of a Guild), which handles commands related to playing chess games. It includes commands such as making moves, challenging other players, and handling game logic.

3. **view.py**: This file contains the implementation of the `View` cog, which handles commands related to viewing and analyzing previously played games. It allows users to navigate through moves and visualize the game board.

4. **tactics.py**: This file implements the `Tactics` cog, which is responsible for handling commands related to solving tactics retrieved from an external API connected to the Lichess Tactics database. The cog enables users to make accurate moves and earn higher scores upon successfully solving a tactic.

5. **utility.py**: This file includes utility functions and classes used throughout the project, such as the database session management.

Note: An empty `tactics` folder must be created for the bot to function. It was not pushed to this repo since Git does not track empty directories.

## Database

The project utilizes an `SQLite database` with the `SQLAlchemy ORM` for storing games and viewing data.

## Features

- Play chess games with other users on Discord.
- Solve tactics from the `Lichess Tactics database`.
- View and analyze previously played games.
- Check personal stats and game history.
- Ephemeral messages for privacy.
- Message editing, button interactions, and image rendering.

## Contribution Guidelines

If you would like to contribute to the project, please follow these guidelines:

1. Fork the repository and clone it to your local machine.
2. Create a new branch for your feature or bug fix.
3. Implement your changes and ensure they are properly tested.
4. Commit and push your changes to your forked repository.
5. Submit a pull request to the main repository, clearly explaining the changes you have made.

Your contributions are appreciated!

## Contact

If you have any questions, feedback, or suggestions regarding the Discord Chess Bot, feel free to reach out to me:

Name: Yashas Donthi  
Email: 2yashas2@gmail.com

## Release Notes: Version 1.0

- Initial release of the Discord Chess Bot.
- Implemented basic functionality for playing chess games, solving tactics, and viewing game history.
- Integration with the Lichess Tactics database for challenging tactics.
- Database support for storing and retrieving game data.
- Added features like ephemeral messages, message editing, button interactions, and image rendering.
