#### 

###### This will Take you from Start to End of Getting Started with Hex Editing!!!

(GameCube DAMM intended)



1. Extract iso.
2. Extract files from bundles.
3. Set up Hex Editor and how to look at values.
4. Examples of Offset Locations.
5. Rebuilding Files.
6. How to load in-game.

#### 

#### **============= EXTRACT ISO =============**



**(You may ignore this part if already done)**



1\) In dolphin right click the game --> Properties

~~------------------------------------------------------------------~~

2\) Go to file system and right click on the disc --> Extract entire disc

~~------------------------------------------------------------------~~

3\) Location --> I recommend the Dolphin Game directory for step 4   *(Same place you load your Roms)*





**4) In Config go to paths and check "Search Subfolders", You can now run the extracted game like normal!!**





##### ============ GETTING STARTED (EXTRACTION) ==============



(In the Extracted Disc Bundles are found in **files/Bundles** ...Yeah I'm Mr. "no shit sherlock" I guess)



1\) Open a character's bundle after extracting the iso in **GZBuildr**



&#x20;       **- Load Bundle directory, and select the Character bundle from the drop down**



~~------------------------------------------------------------------~~

2\) Extract **MONSTERDATA** (Should be around the top of the list)

~~------------------------------------------------------------------~~

3\) Open in Hex Editor (HxD is fine, RxD is more beginner friendly and has some analysis tools)





##### **============== SET UP ================**



\- Drag or open the file you extracted into chosen Hex Editor!



\- In the bottom right change the data inspector to **BE (Big Endian)**



&#x20;      - This ensures it'll display the segments at the correct values!



~~------------------------------------------------------------------~~



\- Each Value is in a set of 4: \[ 0x0-0x3 | 0x4-0x7 | 0x8-0xA | 0xB-0xF ]  Column Segments.

&#x20;

&#x20;             (RxD has an option to put Column lines under View!)



Majority if not all of these values sit in the data inspector under **"FLOAT32"**





##### **=============== OFFSET LOCATIONS ==============**





0x3C = Health Value

~~------------------------------------------------------------------~~

0x120, 0x124, 0x128, 0x12C = Resistances (Edged, Blunt, Energy, Not sure what the 4th does)





##### **================ Rebuild ======================**



**1)** Using GZBuildr, load the directory of the bundle:

~~------------------------------------------------------------------~~

**2)** Load it in the drop down and hit rebuild

~~------------------------------------------------------------------~~

**3)** Select the replacement file where you saved the changes, and select output and name it the same file and extension.

&#x20;

&#x20;                               ***(Anguirus\_3.cmg --> Anguirus\_3.cmg). GZBuildr should rezip the zipped bundles for you!***



~~------------------------------------------------------------------~~

**4)** It'll make an entirely new character bundle with the changes inside!!



##### **============== LOAD INGAME ===================**



Option 1: Put the file back in the extracted disc from above



Option 2: Use Riivolution, But it requires some setup... My mod Godzilla: DAM - Domination! Comes with loading custom files



Either of these options and it'll load in-game!



Remember: \_0 = Player 1, \_1 = Player 2, etc   (Characters also have micro files that need to be edited separately, since their collision box and size values are different)





#### **=============================================================================**

#### 

\*\*This is mainly to get started, you can do more than just do stuff in Monster Data...

## Look around! Change things, Import them, Play and find out!!\*\*

