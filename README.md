noogai03 branch of X-flixel

Instructions:
1) Folder setup
Copy "flixel" folder in "Content" into the Content folder of an XNA game.
Copy "flixel" folder in base directory into main project folder of XNA game.

2) Code setup
Create a partial class of FlxGame, and define the initGame method in the constructor. initGame is then as in any Flixel game (define an FlxState, etc)
eg:

using System;
using Microsoft.Xna.Framework;
using Microsoft.Xna.Framework.Graphics;
using Microsoft.Xna.Framework.Input;

namespace org.flixel
{
    //this is where you should kick off your game by specifying some basic stuff
    partial class FlxGame : DrawableGameComponent
    {
        public FlxGame()
            : base(FlxG.Game)
        {
            initGame(320, 240, new PlayState(), new Color(0x13, 0x1c, 0x1b), false, new Color(0x3a, 0x5c, 0x39));
        }
    }
}

Make a PlayState class extending FlxState, let the fun begin.
