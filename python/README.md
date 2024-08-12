# The original python script.
This is the original "proof-of-concept" script.
I don't recommend this for anything other than testing and playing with.
Once development strategy has been decided, I will be focussing on developing
either micro-python or (more likely at this point) arduino code.

## What's wrong with this code?
Primarily, because I believe that the client should communicate with the LMS-server
with a _single_ command, rather than multiple requests -- with all database
searches happening on the server itself.
I presume at this point that the only way to achieve this is to write a plugin.