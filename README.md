# TwitGrid: Because TweetDeck is a mess at times.

TwitGrid is a simple, broadsheet layout for reading Twitter feeds that shows a
dense, instant overview of the latest posts from only the users you care about.
It doesn't mix multiple feeds up into an infinite-scrolling jumble.

It's easy to use:

1. Save a copy of [`twitgrid.html`](https://raw.githubusercontent.com/nuket/TwitGrid/master/twitgrid.html) anywhere.

2. Edit the lists of Twitter handles you want to see:

   ```
   const handlesTopInterests = 'vilimpoc checklyhq dspillere GreatDismal tim_nolet';
   const handlesFunStuff     = 'BVG_Kampagne fryuppolice KoreanTravel thingiverse NI_News steak_umm ConanOBrien taylorswift13 jimmykimmel';
   ```

3. Call the `render()` method, with optional alphabetical sorting:

   ```
   render(handlesTopInterests);
   render(handlesFunStuff, true);
   ```

4. Reload the page and enjoy.
5. Page Up / Down will smooth scroll the whole viewport, snapping to the next set of feeds.
   Or you can drill down into individual user feeds.

## The View

You will see feeds from only the specified handles, like so:

![](twitgrid.apng)

Because most people have usable long-term memory, you'll know what you have read
and haven't, somewhat in the vein of RSS (though less automatic).

There will not be an algorithm intermediating what you want to see and what you
actually see or surfacing things it thinks you might be interested in.

## Technology

It's a single page, no dependencies, pure ES6 Javascript. Not even `lodash`.

## Styling: Changing the Column Count

Edit this:

```
.twit  { flex: 0 0 20%; }
```

And this:

```
// Change this to suit the width of your monitor.
const columnCount = 5;
```
