# analogue-clock
A digital analogue clock using device time. 

_I'd like to get this running on mobile devices as a widget or lock screen clock as well as convert it to run on a smart watch with a round display in the future._

This was a fun project; not like I don't have fun working on **ALL** websites ;)

The hour, minute, and second tic markers are colorfully distinct. The second tic markers light up as the seconds tic by but the white second hand marker tic color doesn't overtake the blue or yellow hour and minute hand tic markers while passing over them.

The hour hand is accurate to the exact degree at all times while the minute hand moves once each minute is reached. There is no second hand but instead second hand markers and animations indicating the current second.

## Seconds Indicators
The second hand animations I think are particularly interesting. There are two larger circles that travel the outline of the clock along with two smaller circles that stick with the following large circle and traverse back and forth the length of the hour hand marker at each second tick. The leading inner larger circle moves onto the second that is about to tic, then when over the next second tic marker "lights" the second hand tic up. Once the second hand marker is lit up the following larger circle and two smaller circles move to the newly lit tic.

It can be a metaphor for many things focused on discovery, analysis, etc. or even a family unit where a parent leading the rest of the family. For discovery and analysis it can stand for the discoverer/creator/innovator as the leading large circle who discovers/creates/innovates something new, then those that follow them see, use, analyze, expand, etc. that discovery. Interesting to note is that the larger inner circle and one of the smaller circles that follow it actually touch the minute hand of the clock, giving them reference to the minute hand connected to the the middle circle which connects to the hour hand; in a way giving them all knowledge of the length of the hour marker's length which the smaller circles traverse.

Besides that, each second marker that has passed during the minute time-frame stays lit until the next minute tics, then all are greyed out again for the start of the next minute except the first second as the class for the lit seconds is removed at the strike of the next minute and has a slight transition timing less than a second long while the second marker circles traverse their way back in time to the start of the new minute.

## Background tab JavaScript processing issue and temporary fix

Since this is a web application the JavaScript stops running while the page/tab is not in focus. This led to me coming back to it with the correct locations of the hour and minute hands and the correct minute markers being lit up as they are all based on a new Date().getTime() but led to graphical anomalies concerning the passed second tic markers and the placement of the animated second marker circles so I added a function to check if the page/tab was active (again) and then set the clock to re-initialize when the page/tab was back in focus. Not a huge deal but I'm pretty sure I could figure out a fix for it if it were a priority again. For now, it remains the fun project it was to build and a good example of responsiveness across devices. The clock's size is changed at initialization and at window.onresize to scale relative to the smallest amount of pixel distance be it width or height of the display.
