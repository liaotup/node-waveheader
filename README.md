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

No one has published a solution to [Issue 1](https://github.com/TooTallNate/node-wav/issues/1) in which
the Writer constructor goes sideways,
so [@karlwestin](https://github.com/karlwestin) adapted this module from @tooTallNate's
[node-wav/lib/writer.js](https://github.com/TooTallNate/node-wav/blob/master/lib/writer.js)
