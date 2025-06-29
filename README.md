Create a bookmarklet using the following code:

~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~
Audio Link Copy
javascript:(async function(){try{const m=document.body.innerHTML.match(/https:\/\/audio-bible-cdn\.youversionapi\.com\/[\w\/\-]+\.mp3\?version_id=\d+/);if(m&&m[0])await navigator.clipboard.writeText(m[0]);}catch(e){}})();
~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~

This will basically extract the link to the audio file on YouVersion.

There is a silent version of the bookmarklet (which directly copies the mp3 link onto the clipboard for you to paste directly onto Gsheets or the URL bar.

~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~
Audio Link Copy (Silent)
javascript:(async function(){try{const bodyHTML=document.body.innerHTML;const match=bodyHTML.match(/https:\/\/audio-bible-cdn\.youversionapi\.com\/[\w\/\-]+\.mp3\?version_id=\d+/);if(match&&match[0]){await navigator.clipboard.writeText(match[0]);}}catch(e){console.error("Error copying audio link:",e);}})();
~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~

Example Link:
https://www.bible.com/audio-bible/2692/LUK.4.NASB2020

