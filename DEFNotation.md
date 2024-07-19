this is just for my own enjoyment but theres a few ways to write this in DEF notation.

DEF Notation - Commands

Audicle

Tree

Fountain

Sunbird

Braid

Node

Truss

Ribbon

Beux

these werent in the readme i sent but they are parts of the notation. the notation system is a bit weird compared to normal notation systems because it assumes you have a transformer llm able to use these commands lol.

so for this 

`C:   C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |

Am:  D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |

G:   E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |

Cm:  A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - |

G6:  C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |

Am:  D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |

C:   E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |

Cm:  A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - |`

we would probably actually use a ribbon and a beux like this

Audicle{Ribbon#00FF00}~+Node{Voice}>> >>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . | D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . | E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 | A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||=Braid{Beux#00FF00}&>> >>Cmaj || Amin || Gmaj || Cmin || G6maj || Amin || Cmaj || Cmin

Explanation: ribbon tells us were working with a stream of monophonic notes and we're going to do something with them that isnt just playing them alone. in this case we're playing them with our chords. #00FF00 is a hex code identifier that links the melody with our chords. theres no significance to the fact that i choose a lime code, its just a ID. =Braid tells us that we are linking the previous ribbon with something, in this case its a Beux (bow) which signifies that its going to be a chord progression. the reason we write chords like Amaj Amin and not A Am is just to be clear that were not talking about single notes. the double bars || just tell us to adopt the metering of the ribbon. we didnt technically clarify that Cmaj  goes with C4 - D4 B3 - B3 - - D4 - D4 - E4 - . .  but the information is still there because both come before a meter pipe |

ZF
id like to explain the main reason for this 

Audicle{Ribbon#00FF00}~+Node{Voice}>> >>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . | D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . | E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 | A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||=Braid{Beux#00FF00}&>> >>Cmaj || Amin || Gmaj || Cmin || G6maj || Amin || Cmaj || Cmin

instead of this

C: C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . | Am: D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . | G: E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 | Cm: A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - | G6: C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . | Am: D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . | C: E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 | Cm: A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - |

among other things, like style and transformer use, is literally just so its easy to copy and paste the melody seperate from the chords while stile having them together in a cohesive notation

You can also use Truss to write this instead of using Ribbons Braids and Beuxs

Truss' can only hold four channels at a time

so we will need to use 2 Truss' for these 8 chords

we can do it like this

Truss#FF0000{Z: z: N: n:}===={
Z>>Cmaj>>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |
z>>Amin>>D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |
N>>Gmaj>>E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |
Z>>Cmin>>A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||}
Truss#FF0000====FF00FF{Z: z: N: n:}===={
Z>>G6maj>>
z>>Amin>>
N>>Cmaj>>
Z>>Cmin>>}

truss can be useful in some scenerios and less useful in others. in this case its nice becuase when we link both the truss' with the #FF0000 ID it allows us to inherit the melody information and we dont have to rewrite it. We can use two ID's for a truss to signal that its inheriting some info but not all (in this case it has differant chords). if we didnt use two ID's for the second truss we'd have to write it like this

Truss#FF0000{Z: z: N: n:}===={
Z>>Cmaj>>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |
z>>Amin>>D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |
N>>Gmaj>>E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |
Z>>Cmin>>A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||}
Truss#FF00FF{Z: z: N: n:}===={
Z>>G6maj>>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |
z>>Amin>>D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |
N>>Cmaj>>E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |
Z>>Cmin>>A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||}

this is perfectly legal its just more writing. heres an example of something illegal

Truss#FF0000{Z: z: N: n:}===={
Z>>Cmaj>>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |
z>>Amin>>D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |
N>>Gmaj>>E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |
Z>>Cmin>>A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||}
Truss#FF0000{Z: z: N: n:}===={
Z>>G6maj>>C4 - D4 B3 - B3 - - D4 - D4 - E4 - . . |
z>>Amin>>D4 - E4 C4 - - C4 - E4 - E4 - F4 - . . |
N>>Cmaj>>E4 - F4 D4 - - D4 - F4 - F4 - G4 - . F4 |
Z>>Cmin>>A4 - G4 F#4 - D4 E4 - E4 - C#4 - B3 - A#3 - :||}

we cant have two truss' with the same ID. they will try to write over each other recursively. 
In conclusion Truss' are like four channel DEFNotation tracks with some unique properties like being able to have a chord and a melody on one line, and being able to be linked.
