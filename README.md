# BindTheEarth
BindTheEarth (BtE) is a sound pack for [Dungeon Crawl](https://crawl.develz.org/download.htm) Stone Soup that leverages [Earthbound](https://en.wikipedia.org/wiki/EarthBound)'s sound effects.

Before you get started, you'll need to obtain a version of DCSS that supports sound. At the VERY LEAST, you'll need to make sure that your version supports sound (Hit '?V' in game). As of this writing, this depends on a feature in [my own fork](https://github.com/Autofire/crawl), but this will hopefully change soon. If you're not okay with that, you could probably get around with with some sed-fu, but I won't help you there.

To use BtE you will first need to get [the Earthbound sound effects](http://starmen.net/mother2/soundfx/), at the bottom of that page. Download the zip and extract it in a sensible place. (i.e. one without a rediculously long path; I think DCSS has a limit of 256 character-long paths.)

Then clone this repo into your DCSS settings folder. Once that is done, add these lines into your init.txt file:

```
sound_file_path = /path/to/earthbound/sounds/
include = BindTheEarth/core.txt
```

Where `/path/to/earthbound/sounds/` is the location of your sound files. If you're on Windows you may have to change the forward slashes to back slashes **Note that you must have a slash at the end!**

Now Crawl should make noises! I'm not done with it yet, and I am aware that certain sound effects can get *really* repetitive after a while, depending on your character's background. Feel free to fiddle with stuff as you wish.
