WaveHeader
====

Just generates a WAVE-file header, with the specified length as argument.

    javascript
    var waveheader = require("waveheader");
    //write to a normal fs.createWriteStream
    myFileStream.write(waveheader(44100 * 8)); // 44100 khz * 8 seconds


    // using options (all available options listed)
    myOtherFileStream.write(waveheader(0,
    { format     : 1 // or 3 for IEEE floating point
    , channels   : 2
    , sampleRate : 22050
    , bitDepth   : 8
    })); 

@karlwestin adapted this module from @tooTallNate's node-wav/lib/writer.js -
in which there appears to be an incompatibility with the stream-parser package.
Independently, neither of us have been able to figure out what's going sideways with that.
