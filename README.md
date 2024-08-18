# Introducing _the Duke_

Music is a uniquely evocative thing, and whilst technology has brought a huge
improvement in sound quality, radically changed the means of distribution, yet
I can't help feeling that it has lost a little bit of the magic. I vividly
remember buying my first 45rpm single, just as I remember my first real album,
and my first CD -- and most of them mI still have. The joy of removing the disc
from the sleeve, and carefully placing it on the player to listen to, perhaps
whilst reading the sleeve notes...

Even going out to the pub brought music magic -- punching in the track numbers
into the jukebox. Where is all that now? Instead, I stare at a screen, trying to
scroll through endless lists of tracks, not really knowing what I want to listen
to, and getting frustrated beccause everything is too darned slow. I need a new
approach.

## the _Solution_

_the Duke_ brings back the tangible, tactile, music experience -- and makes playing
audio a lot simpler and quicker. Whilst it has been planned for years, and intended
to be used by everyone in the family, the credit for finally motivating me to get off
my lazy arse has to go to the sternest and most ruthless critics of all -- my two
children -- who really couldn't manage using Lyrion as it currently stands. So, I
move away from anything which requires a display, to something that is cheap and
simple to create and use -- but powerful enough to adapt to every circumstance: the
humble barcode.

## the _Audio Library_

The concept is simple: Audio is brought back to a physical object, upon which is
affixed a barcode. The object, of course, can be anything -- but in our family we print
a jpeg of the album cover onto a piece of card, stick a barcode on the reverse, and
then lamitate it just for good measure. This provides enough protection for general
use.

## the _Barcode_

We have tried to optimise the barcode design to deliver maximum flexibility within the
minimum search-string length. The printed barcode size should be relatively compact,
and yet should have a high-resistance to false readings (_ie_: error correction should
be as high as is practically possible).

Whilst the end-user is free to choose any barcode symbology they feel works best for
their own needs, we have gone for the QR-Code. The contents of the code is as follows:

1) The URL.
This is _OPTIONAL_, but including it enables the QR-Code to be read by any
modern smartphone. Of course, you will need to ensure that the server is actually
accessible over the network -- but *please* don't open up LMS to the public internet!
2) The Query.
To save space, this is **an array**, consisting of **three** fields:
   1) **Object Type:** A **single digit**, which determines whether we are wanting to play
   a single, an album, a playlist, a classical work, an episode, or to issue a
   command to the controller or to the server.
   2) **Search String:** A simple **array**
   3) **Artist Criteria:** A complex **array**, consisting of either one or two arrays.
   The first holds the artist name(s), with the second (optional) containing their
   respective role.

The power of this system lies in the simplicity of the query, and of the tolerance to
variations of file-tagging within the library. If you have inconsistent tagging, it won't
matter if the work that you are searching for is by "Mozart, WA", "Mozart, Wolfgang",
"WA-Mozart", or any other possible permutation thereof. Just searching for "Mozart"
is good enough. And, if you have works by _Leopold Mozart_ in your library as well, just
ensure that the rest of the search string is sufficient to narrow the results returned...

... unless you actually _want_ ambiguity. Yep, we can manage that too. `[1, ["Abba"]]` will
give you a track from Abba, chosen entirely at random!

## the _Result_
Some examples of fully-functioning labels in our home.


