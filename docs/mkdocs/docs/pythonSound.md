#Sound
---

Sound is only supported in Windows, using the Winsound API.  
Therefore, only ```.WAV``` files will work.

###Playing Sound Files
---

* `.playSound(sound, wait=False)`  
    Play the named sound file.  
    By default, the sound is played asynchronously, meaning the function will return immediately, even though the sound hasn't finished playing.  
    It is possible to override this, by setting wait to True. This is not recommended though, as the GUI will become unresponsive.

* `.stopSound()`  
    This will stop whatever sound is currently being played.

* `.loopSound(sound)`  
    This will play the named sound in a loop.

* `.setSoundLocation(location)`  
    Set a folder for the sound files.  
    This will be put before the names of any sound files used.  

---
<div style='text-align: center;'>
*Advertisement&nbsp;<sup><a href="/advertising">why?</a></sup>*
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
    style="display:block"
    data-ad-format="fluid"
    data-ad-layout-key="-gw-13-4l+6+pt"
    data-ad-client="ca-pub-6185596049817878"
    data-ad-slot="5627392164"></ins>
<script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
</div>
---

###Playing Built-In Sounds
---

* `.bell()`  
    This will work on all platforms, playing a bell sound.  

* `.soundError()`  
    This will sound a simple error beep.

* `.soundWarning()`  
    This will sound a simple warning beep.

###Playing Musical Notes
---

* `.playNote(note, duration=200)`

    Support is built in for playing musical notes, using winsound.
    The note can be a numeric frequency, or a String note.
    The duration can be a number in milliseconds, or a String duration.

    Over 50 String notes are available, such as:

    * f#1 = 46
    * b7 = 3951
    * g9 = 12543  
    
    The following String durations are supported:

    * BREVE = 2000
    * SEMIBREVE = 1000
    * MINIM = 500
    * CROTCHET = 250
    * QUAVER = 125
    * SEMIQUAVER = 63
    * DEMISEMIQUAVER = 32
    * HEMIDEMISEMIQUAVER = 16

    These can be accessed through the variables `gui.NOTES` and `gui.DURATIONS`
