The primary goal of this localization mod is to completely remove ambiguity from all vehicle names in all cases while at the same time keeping names as close to Gaijin's default names as possible. In most cases, the only name that has been changed is the one that appears at long range (>1.2km) which now matches the close and medium range name. The majority of the name changes are mostly minor syntax changes for the sake of consistency. Early and Late have been stylized as [E] and [L]. NATO names have been added to the statcards of aircraft that had them. Taiwanese vehicles have been given a sun icon. This mod works with any language selected, however the names of vehicles will always be in English. Yak-141 has been renamed to Yak-41M as this name is more accurate to the version we have in War Thunder.

There are three versions. The standard version uses default French/Italian roundels. The "New Icons" version replaces the default roundel icon on French and Italian vehicles with alternative symbols. If you don't like the symbols I used, you can easily change them for all vehicles of a given nation at the same time by using the "replace all" tool in a software like Notepad++. The "Dechinafied" version gives soviet names to chinese copy-paste vehicles in addition to the new French/Italian roundels.

There are two ways to save the contents from github. Start by selecting the version you want and then clicking on units.csv. The first and most convenient method is to use the "copy raw contents" button (two overlapping squares icon near "Raw") which will copy the contents of the entire file to your clipboard. The second method is to click "Raw" and then right click → save as. Make sure it saves as a .csv file and remember where you saved it to.

IMPORTANT NOTE: when using custom localization, your lang folder is frozen and no longer auto-updates. When Gaijin adds new texts, they will appear broken until you update the lang folder manually. Once you are familiar with the process of updating your lang folder it only takes about a minute to do. 

The version of the commit reflects the version of the game at the time I last updated the mod. I try to keep this repository as up to date as possible. If you need to nudge me to update it or if you have any other problems/concerns, feel free to reach out to me  with a DM on discord: Jæk#5326

## Instructions

### To install

- Navigate to your War Thunder files. The easiest way to do this is to look for aces.exe in task manager while the game is running, right click it and go to file location, and then go back one level to see your root files

- Open config.blk with any text editing software such as Notepad or Notepad++. Scroll down to the debug section. Add a new line `testLocalization:b=yes`, checking to make sure spelling and spacing are correct. It should look like this:
```
debug{
  enableNvHighlights:t="auto"
  screenshotAsJpeg:b=yes
  512mboughttobeenoughforanybody:b=yes
  testLocalization:b=yes
}
```
- Save the file
- Launch the game
- A new folder called "lang" should have appeared. Open the folder, inside it there should be multiple CSV files.
- units.csv is the file responsible for vehicle names. Your goal is to replace the default units.csv with the custom one from this GitHub.
  - The easiest way to do this is to use the "Copy raw contents" button as described in the third paragraph. Open units.csv with a text editor like notepad or notepad++, use ctrl+A to select all, delete everything, then paste in what you just copied. If it pasted successfully, save the file and close it. 
  - If for whatever reason that method didn't work, try using the other method where you save the units.csv file from github. Drag it into your lang folder. Choose to replace if prompted. 
- Restart the game

### To update

When you start seeing broken texts, you will need to update your lang folder manually. This is particularly importnat when Gaijin releases a major update as major updates bring lots of new vehicles and lots of new texts.
- With the game running, go to your War Thunder files and delete the lang folder entirely
- In the hangar, go to options, and change your language to Russian. Apply the setting and make sure your language actually changes. Hit esc if a popup comes up prompting you to download additional content.
- A fresh lang folder should have generated. Refresh file explorer if you do not see it. Replace units.csv with the new one in the same way you did before. 
- Tab back into War Thunder and switch the language back to English (or whatever language you were using). 

Switching languages is faster and more convenient than restarting the game. It also updates/fixes the hidden langRegional folder, so if you see broken texts for titles or challenges, cycling your language will usually fix it. 

### To Uninstall

- Delete the lang folder entirely
- Remove the `testLocalization:b=yes` line from config.blk

### Troubleshooting

> Vehicle names are broken and show up as codes (for example, mig-17p_lim_5p instead of Lim-5P)

If this only happens to recently added vehicles, update your localization.
If this happens to all vehicles, the game is not reading units.csv correctly. Make sure units.csv is in the lang folder, that there is only one, and the contents look correct.

> Vehicle names are loading properly, but the national symbols are not

War Thunder uses some interesting unicode characters which it "converts" to the national symbols you see in game. If these symbols are not loading correctly, it is likely that the file did not save correctly from github. Try saving the contents using a different method. 

> Lang folder is not appearing

Check to make sure you put `testLocalization:b=yes` in the correct section, spacing and formatting is correct, you saved the file, you restarted the game, and you're looking in the right directory.

> Text for titles or challenges is broken

Cycle to any other language (make sure the language in the hangar actually changes) and then back to the language you were using. 