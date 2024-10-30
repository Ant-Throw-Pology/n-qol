# n-qol
Quality-of-life mod for landgreen/n-gon.

## Usage

You have some options here, depending on the settings your administrators (if any) have set.

### Option 1 - Bookmarklet

Create a bookmark with the following as the URL:

```js
javascript:(function(){const r=new XMLHttpRequest;r.open("GET", "https://raw.githubusercontent.com/Ant-Throw-Pology/n-qol/main/index.js");r.onloadend=function(){new Function(r.responseText)();};r.send();})();
```

Then, go to n-gon and click the bookmark.

### Option 2 - Console

Paste the following into the console of your browser's Developer Tools.

```js
(function(){const r=new XMLHttpRequest;r.open("GET", "https://raw.githubusercontent.com/Ant-Throw-Pology/n-qol/main/index.js");r.onloadend=function(){new Function(r.responseText)();};r.send();})();
```

(If it doesn't let you paste, follow its instructions for it to let you paste.)

Then, hit Enter to run the code.

### Option 3 - Edit index.html

1. Go to [the GitHub page for n-gon](https://github.com/landgreen/n-gon).
2. Click the green button in the upper right that says "Code".
3. Click "Download ZIP".
4. Extract the contents of the downloaded zip file into a location on your computer, preferably one you can find easily later.
5. Open that location in your computer's file explorer, then open the "n-gon-master" folder inside that.
6. Open the "index.html" file inside that folder in your favorite text editor. If you don't have one, you can use (the online version of VSCode)[https://vscode.dev].
7. At the bottom, between the `</script>` and the `</body>`, add:

```diff
      <script src="js/engine.js"></script>
      <script src="js/index.js"></script>
+     <script>(function(){const r=new XMLHttpRequest;r.open("GET", "https://raw.githubusercontent.com/Ant-Throw-Pology/n-qol/main/index.js");r.onloadend=function(){new Function(r.responseText)();};r.send();})();</script>
  </body>
  
  </html>
```

8. Save the file, and open index.html in your browser.

## Features

- Improved `powerUps.spawnDelay` - It doesn't take as long
   * Set `powerUps.spawnRate` to set how many powerups of each type are spawned per tick (default 10)
- Improved powerup collecting - You can collect multiple powerups at once
- Removed powerup recoil - so you don't fly into the stratosphere from late-game interest
