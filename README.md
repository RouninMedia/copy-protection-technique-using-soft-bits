# Copy Protection Technique using Soft Bits
*A JavaScript simulation of **soft bits**, which can then be used as part of a specific copy-protection technique.*

### More of an experimental working model than a final approach
On **WebmasterWorld**, on Oct 9th, 2022, poster *lucy24* wrote:

> I’m reminded of “soft bits”. Remember those? Back when everything came on a floppy disk, one form of copy protection was to include sectors whose bits 
> couldn’t quite decide if they were off or on. If the program read the relevant sector more than once, and got the identical content each time, that was a dead 
> giveaway that it was dealing with an unauthorized copy.
>
> **Source:** *https://www.webmasterworld.com/foo/5074152.htm*

This represents an intriguing approach to copy protection:

1) a **dynamic** series of 1s and 0s which, in its original form, changes every time it's read.

But when that dynamic series is *copied*:

2) the resulting copy is a **static** series of 1s and 0s which is identical every time it's read.  

I wanted to see if it might be possible, in JavaScript, to take a single obfuscated file and simulate within it the equivalent of a *floppy disk sector with soft bits*, such that if the obfuscated file were copied without authorisation, the copy would contain the same *floppy disk sector* but this time with *resolved hard bits* which had lost their dynamic state.
