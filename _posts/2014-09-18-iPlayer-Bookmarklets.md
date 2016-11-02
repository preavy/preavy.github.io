---
layout: post
category : tech
---
I listen to BBC iPlayer radio in a pinned tab in Chrome.

I am usually scrolled halfway down the playlist on the page. Then the
phone rings or someone talks to me and I want to quickly find the
pause button.

So I came up with these JS snippets to make Play and Pause bookmarklets.

    // paste this into the URL field of a bookmark called Play
    javascript:{document.getElementsByClassName('media-player--playlink')[0].click();}void(0);

    // paste this into the URL field of a bookmark called Pause
    javascript:{document.getElementById('media-player-empjumpMediaPlayerLink').click();}void(0);
