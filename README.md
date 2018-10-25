# halite3-bot

A bot for Halite III competition written in Rust.

## Halite III starter kit components

* MyBot.{extension}, a starter bot outline
* /hlt directory, which contains modifiable helper functions for your bot
* A Halite executable that enables local playtesting of your bot
* The scripts run_game.bat (Windows) and run_game.sh (MacOS, Linux)

## Testing your bot locally

Run run_game.bat (Windows) and run_game.sh (MacOS, Linux) to run a game of
Halite III. By default, these scripts run a game of your MyBot.py bot vs.
itself.  You can modify the board size, map seed, and the opponents of test
games using the CLI.

## CLI

The Halite executable comes with a command line interface (CLI). 
Run `$ ./halite --help` to see a full listing of available flags.

## Submitting your bot

* Zip your MyBot.{extension} file and /hlt directory together.
* Submit your zipped file here: https://halite.io/play-programming-challenge

## Compiling your bot on our game servers

* Your bot has `10 minutes` to install dependencies and compile on the game 
  server.
* You can run custom commands to set up your bot by including an `install.sh`
  file alongside `MyBot.{ext}`. This file will be executed and should be a
  Bash shell script. You must include the shebang line at the top: `#!/bin/bash`.
  * For Python, you may install packages using pip, but you may not install
    to the global package directory. Instead, install packages as follows:
    `python3.6 -m pip install --system --target . numpy`
* Some languages don't use the `MyBot.{ext}` convention. Exceptions include:
  * Rust: a Cargo.toml in the root will be detected as Rust. Your bot will
    compile with `cargo rustc`.
