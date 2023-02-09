# Haskell Tiny Game Jam

Inspired by the [BASIC 10Liner contest](https://www.homeputerium.de) (see their english rules at the bottom):
the first Haskell tiny games contest runs through February 2023!
The prize.. glory! <!-- and advancing the Haskell game dev craft -->

[Matrix]: https://matrix.to/#/#haskell-game:matrix.org
[IRC]:    https://web.libera.chat/#haskell-game

Submit your entries now (as many as you like) to this repo
(push if you have access, or send a PR),
or paste in the #haskell-game chat ([Matrix] or [IRC]) and we'll commit for you.
sm and f-a are your judges, informed by #haskell-game.
Here are the general rules for February:

1. Make a playable game in one haskell file of up to 10 lines of up to 80 characters each.
2. This can be a [runghc], [stack] or [cabal] script, or a small haskell program, but not a multi-file project.
   Some templates are provided to give ideas.
   Our ideal is a self-contained 10 line program that just works, like BASIC programs.
3. Unlimited comments and notes are permitted after line 11.
   The game's "category/name (author)" info should appear here.
4. The script or program must either be executable and run reliably (eg like a stack script),
   or it must contain reliable build instructions (eg a ghc command line with all needed package options).
   Entries which aren't straightforward to run are incomplete.
5. The game must be accompanied by a small square static screenshot for the main README.
   (Animated gifs get obscured by Github's player overlay - but are great at larger size in your game's readme.)
6. The game should run on all major platforms, ideally.
7. Contest entries will be collected in this repo.

[runghc]: https://downloads.haskell.org/ghc/latest/docs/users_guide/runghc.html
[stack]:  https://docs.haskellstack.org/en/stable/script_command
[cabal]:  https://cabal.readthedocs.io/en/3.6/cabal-commands.html#cabal-v2-run

Compete in any or all of these categories:

## prelude (gam-10-80-hs-prelude)

- Only the standard prelude may be used (no imports). ([template1](prelude/template1.hs))

<table><tr>
<td><a href="prelude/guess1.hs"><img src="prelude/guess1.png" width=100 height=100><br>guess1</a><br>(sm)</td>
<td><a href="prelude/pure-doors.hs"><img src="prelude/pure-doors.png" width=100 height=100><br>pure-doors</a><br>(tristanC)</td>
</tr></table>

## base (gam-10-80-hs-base)

- Imports from the base package may be used. ([template1](base/template1.hs))

<table><tr>
<td><a href="base/timing"><img src="base/timing/timing.png" width=100 height=100><br>timing</a><br>(TravisCardwell)</td>
<td><a href="base/shoot"><img src="base/shoot/shoot.png" width=100 height=100><br>shoot</a><br>(migmit)</td>
<td><img src="base/log2048/log2048.gif" width=100 height=100><a href="base/log2048"><br>log2048</a><br>(Lysxia)</td>
</tr></table>

## default (gam-10-80-hs-default)

- All packages installed by default with the tested ghc version may be used. ([template1](default/template1.hs))
- A second file named Import.hs may be used, to gather imports and re-exports (only).

## hackage (gam-10-80-hs-hackage)

- As above, but all packages released on Hackage may be used. ([template1](hackage/template1.hs))

<table>
<tr>
<td><a href="hackage/guess2.hs"><img src="hackage/guess2.png" width=100 height=100><br>guess2</a><br>(sm)</td>
<td><a href="hackage/wordle.hs"><img src="hackage/wordle.png" width=100 height=100><br>wordle</a><br>(halogenandtoast)</td>
<td><a href="hackage/ski/ski.hs"><img src="hackage/ski/ski.png" width=100 height=100><br>ski</a><br>(sm)</td>
<td><a href="hackage/guesscolor"><img src="hackage/guesscolor/guesscolor.png" width=100 height=100><br>guesscolor</a><br>(TravisCardwell)</td>
</tr>
<tr>
<td><a href="hackage/bulls-n-cows.hs"><img src="hackage/bulls-n-cows.png" width=100 height=100><br>bulls-n-cows</a><br>(akadude)</td>
<td><img src="hackage/hallway-to-hell/hallway-to-hell.gif" width=100 height=100><br><a href="hackage/hallway-to-hell">hallway-to-hell</a><br>(juliendehos)</td>
<td><a href="hackage/1234-hero.hs"><img src="hackage/1234-hero/1234-hero.png" width=100 height=100><br>1234-hero</a> (gelisam)</td>
</tr>
</table>

## Let's play!

You will need a suitable version of GHC (8.10.7+, 9.2.5+, or 9.4.4+ are good bets), and stack (or cabal).
See <https://www.haskell.org/get-started/>.
Once Haskell is installed, and if you have bash, you can run `./play` in this repo:
```
--------------------------------------------------------
                 ___         __                          
|__| _  _|  _||   | . _     / _  _  _  _    | _  _    /| 
|  |(_|_)|((-||   | || )\/  \__)(_||||(-  __)(_||||    | 

--------------------------------------------------------
Here are the entries from HTGJ1, Feb 2023 !
This script can run each game for you, using ghc or stack
(if you don't have these yet, see https://www.haskell.org/get-started).
Most games will return here on exit (others will require CTRL-c).

1) prelude/pure-doors.hs			 7) hackage/bulls-n-cows.hs
2) base/shoot/shoot.hs				 8) hackage/wordle.hs
3) base/timing/timing.hs			 9) hackage/guesscolor/guesscolor.hs
4) prelude/guess1.hs				10) hackage/hallway-to-hell/hallway-to-hell.hs
5) hackage/guess2.hs				11) Quit
6) hackage/ski/ski.hs
** Enter a number to play or quit, or press enter to see the list again: 
```
If you don't have bash, cd into each game's directory and try running the game's .hs file.
If that fails, look for run/build instructions in that file or a nearby readme.
