# BindTheEarth
BindTheEarth (BtE) is a sound pack for [Dungeon Crawl](https://crawl.develz.org/download.htm) Stone Soup that leverages [Earthbound](https://en.wikipedia.org/wiki/EarthBound)'s sound effects.

Before you get started, you'll need to obtain a version of DCSS that supports sound. Most new version support it, but not out of the box. You may check whether sound is upported by hitting '?v', which will take you to the version information. If it says something like "Sound Support," then you're good to go! Skip the next paragraph!

If you need to compile Crawl with sound support, you'll first have to be able to compile Crawl (check the Crawl github for that). Once you have the sournce code and you're able to do this, you'll need to edit the sound.h file. Then, with the line that says `//#define SOUND_PLAY_COMMAND "/usr/bin/play -v .5 \"%s\" 2>/dev/null &"`, you'll need to delete the double slashes at the start. Then, on your command line, do `make SOUND=y`, and it should all work fine. Repeat the steps in the paragraph above. It should have worked. (This is all assuming you're not using Tiles. If you are...it ought to support sound out of the box? Maybe do `make TILES=y SOUND=y`?)

To use BtE you will first need to get [the Earthbound sound effects](http://starmen.net/mother2/soundfx/), at the bottom of that page. Download the zip and extract it in a sensible place. (i.e. one without a rediculously long path; I think DCSS has a limit of 256 character-long paths.)

Then clone this repo into your DCSS settings folder. Once that is done, add these lines into your init.txt file:

```
sound_file_path = /path/to/earthbound/sounds/
include = BindTheEarth/core.txt
```

Where `/path/to/earthbound/sounds/` is the **absolute** path of your sound files. If you're on Windows you may have to change the forward slashes to back slashes. **Note that you must have a slash at the end!**

Now Crawl should make noises! I'm not done with it yet, and I am aware that certain sound effects can get *really* repetitive after a while, depending on your character's background. Feel free to fiddle with stuff as you wish.

(I'm aware that these steps are pretty darn complex for something that's still pretty experimental and may not agree with everyone. I'll have to figure out how to simpilfy things...)
