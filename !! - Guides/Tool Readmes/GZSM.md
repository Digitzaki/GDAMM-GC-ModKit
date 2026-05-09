# DSP Audio Manager



A tool for extracting and managing Nintendo DSP audio files from UBER container files (commonly found in GameCube/Wii games).



### Working with UBER and SAMP Files



**UBER files** are container files that hold multiple DSP audio samples. Think of them like a ZIP file full of audio.

1. Browse or Drag and Drop the .samp and .uber files to the top 2 boxes.
2. The program will scan the file and list all the sounds it finds
3. You'll see each sound listed with its index number, sample rate, and length.



### Browsing Sounds



Once loaded, you'll see a scrollable list of all sounds in the container:

* Each entry shows: `<filename>\_# - sample rate: #####, Length (seconds)`
* Simply scroll through to see what's available.
* All sounds are selected by default.



### Previewing Audio



1. Select a sound from the list
2. Click **"Preview"**
3. The audio will be played through the default media player.
4. Use this to test sounds before exporting



**Tip:** Preview is great for finding specific sound effects without having to export everything.



### Extracting Audio Files



You have two extraction options:



#### Extract (WAV) - Universal Format

1. Select sounds from the `Loaded Sounds` list
2. Click **"Extract (WAV)"**
3. Files appear in the location of the .samp and .uber files
4. The DSP is decoded and saved as a standard WAV file you can use anywhere



#### Extract (DSP) - Original Format

1. Select sounds from the `Loaded Sounds` list
2. Click **"Extract (DSP)"**
3. Files appear in the location of the .samp and .uber files
4. The filename will automatically follow the pattern `filename\_##.dsp` (e.g., `Gigan\_05.dsp`)



### Batch Extract



Want everything at once?



1. Leave everything checked
2. Click **"Extract (WAV)"** or **"Extract (DSP)"**





**Example:** If you extract all from `Gigan.uber` and `Gigan.samp`, you'll get:


~~-----------------~~
Gigan\_01.wav  (or .dsp depending on which Extract button you clicked)
Gigan\_02.wav
Gigan\_03.wav
Gigan\_04.wav
~~-----------------~~


### Rebuilding Game Audio



Want to put your edited audio back into the game? The Rebuild function takes your modified files and repackages them:



1. Click **"Rebuild"**
2. The program automatically finds all WAV files and any DSP files without corresponding WAVs in the directory
3. WAV files are converted to mono DSP with the correct sample rates and specifications
4. New `.uber` and `.samp` files are created ready to inject back into your game



**What Rebuild Does:**

* Converts stereo WAV files to mono (required for GameCube/Wii audio)
* Re-encodes audio to Nintendo DSP format with proper ADPCM compression
* Preserves original sample rates and specifications from the source files
* Generates matching `.uber` and `.samp` files that the game can read



**Old Method Support:**
Already have edited DSP files from previous tools? No problem! Rebuild also accepts DSP files directly, so you can use your existing workflow if you prefer editing DSPs manually instead of WAVs.

**Tip:** Import troubles? Name your edited files using the same pattern. (`filename\_##.wav` or `filename\_##.dsp`).



## Tips

* **Preview before extracting** - Save time by listening first
* **Extract All for archival** - Grab everything at once, .wav makes it easily accessible!
* **WAV for editing** - Extract as WAV to use in audio editing software
* **Keep DSP for authenticity** - Extract as DSP to preserve the original game format, or if you prefer the old editing method



## Supported Games

This tool works with any game that uses UBER containers and Nintendo DSP audio, including:

* Many GameCube titles
* Various Wii games
* Any game using the WiiMusyx or similar sound engines



~~-----------------~~

**Note:** The program automatically handles DSP decoding, sample rates, and loop points. Just load, preview, and export!







