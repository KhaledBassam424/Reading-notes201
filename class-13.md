**local storage**

The local storage mechanism is a nice replacement for cookies, and with HTML5, you can write up to 5MB of data to a special file on the client. This file is not executable and cannot hold binary data (only strings), so it’s reasonably safe.

All the pages that come from your domain share the same storage area, so you can use this mechanism to keep data persistent between multiple pages. The data also stays on the client machine (until you remove it), so it can be used to keep track of information over time.

The localStorage attribute is an example of a very simple (but powerful) type of data structure called a dictionary. You’ve already used dictionaries many times as a Web developer. Each piece of data is stored in a key/value pair. The key identifies the name of the information (say ‘firstName’), and the value is the value associated with that key (‘Herbert’).

HTML attributes are dictionaries (in `<a href = “http://www.google.com“>`, href is the key, and http://www.google.com is the value). CSS rules are also dictionaries. (In the style rule color: red;, color is the key, and red is the value.) Some programming languages use different names for dictionaries, including associative arrays and hash tables.

Access to the local storage is through a special built-in object called localStorage(). This class has a relatively small number of methods, but they are extremely powerful and easy to use:

1. localStorage.setItem(key, value): Stores a value associated with a key. Essentially, key is like a variable name, and value is the value associated with that key. You can store any type of value you want, but it will be stored as string data.

2. localStorage.getItem(key): Retrieves the value associated with the key. Again, you can think of the key as a variable name. Note that this method always returns a string value, so you might need to convert the data to another type. If the key does not exist, you will get the special value null.

3. localStorage.removeItem(key): Removes an item from storage. The key and the value will both be removed. This can be useful if you are running out of space. You are allotted only 5MB of space, and once it’s full, you can’t add anything else.

4. localStorage.length: Returns the number of key/value pairs in the database. Usually used in a loop with the key() method to work with every key/value pair.

5. localStorage.key(i): Given an integer i, this method finds the corresponding key. Note that the order of the keys is not guaranteed. Normally, this method is used in a loop to retrieve all the keys in the database. Then each key is used to look up the corresponding value.

6. localStorage.clear(): Clears all key/value pairs from localStorage. This is a potentially destructive command, so think carefully before you use it. By definition, localStorage data is not backed up on the server (or anywhere else). Once it’s gone, it’s really gone.


> Brief history of the storage: 

In the beginning, there was only Internet Explorer. Or at least, that’s what Microsoft wanted the world to think. To that end, as part of the First Great Browser Wars, Microsoft invented a great many things and included them in their browser-to-end-all-browser-wars, Internet Explorer. One of these things was called DHTML Behaviors, and one of these behaviors was called userData.

userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure. (Trusted domains, such as intranet sites, can store 10 times that amount. And hey, 640 KB ought to be enough for anybody.) IE does not present any form of permissions dialog, and there is no allowance for increasing the amount of storage available.

> HTML5 local storage in action 

Let’s see HTML5 Storage in action. Recall the Halma game we constructed in the canvas chapter. There’s a small problem with the game: if you close the browser window mid-game, you’ll lose your progress. But with HTML5 Storage, we can save the progress locally, within the browser itself. Here is a live demonstration. Make a few moves, then close the browser tab, then re-open it. If your browser supports HTML5 Storage, the demonstration page should magically remember your exact position within the game, including the number of moves you’ve made, the position of each of the pieces on the board, and even whether a particular piece is selected.

How does it work? Every time a change occurs within the game, we call this function:
```
function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}```