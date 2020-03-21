# Voice on Time Problems and Solutions

### No skill at styling elements

The obvious and most time-effective solution would be to use bootstrap.  
But I've opted to use tailwind which allows me to very easily copy styles from the tailwind docs page. Went into it knowing nothing and in a few hours I'm profficient enough. The docs pages are also really good. Would recommend.

### Auto-expanding textarea

This is normally solved by a jquery plugin. But since I used Vue with its 2 way data binding I've opted for the "div behind the textarea method". You use a parent div which contains a div and a `position: absolute` textarea. Both are children are styled the same but the div also has `white-space: pre-line` applied. Using Vue, put the text from the textarea into the div and append an extra letter to the end of the text so that newlines are rendered in the dev. And done. An auto-expanding textarea without adding extra dependencies.

### Mobile devices won't stay awake (which pauses the timers)

There is an API comming soon: wakeLock, but it's not here yet. Instead I used a video, because mobile browsers will wake lock the device if there is a video playing. So I've added a video that starts playing when there's a timer and pauses when the timer ends. Also it seems that the video can be hidden by setting its opacity to 0.
