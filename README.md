Create a bookmarklet using the following code:

javascript:(async function(){try{const m=document.body.innerHTML.match(/https:\/\/audio-bible-cdn\.youversionapi\.com\/[\w\/\-]+\.mp3\?version_id=\d+/);if(m&&m[0])await navigator.clipboard.writeText(m[0]);}catch(e){}})();

This will basically extract the link to the audio file on YouVersion.

Example Link:
https://www.bible.com/audio-bible/2692/LUK.4.NASB2020
