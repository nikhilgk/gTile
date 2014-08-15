gTile
-----
for cinnamon 2.0 and 2.2

---------------------------------------------------------------
             This extension has been developped by
                            vibou
                                
           With the help of the gnome-shell community
                           
                  cinnamon-fork by shuairan

                 With the help of some coffee
---------------------------------------------------------------
http://cinnamon-spices.linuxmint.com/extensions/view/21

**Usage**:

  [Super]+[Space] opens gTile
  
  you can change this on extension-settings.



**Changelog:**

forked from V12 [vibou.gTile](https://github.com/vibou/vibou.gTile) (for original changelog look there)

* v0.6{wip}
    + merge upstream changes from vibou.gTile (V21)
    + exclude some apps by detecting wm_class. This is a wild guess to find apps which should not be tiled.
    +

* v0.5 
    + support for latest cinnamon >1.8
    + settings-system is used (configure keyboard shortcut via extension settings)

* v0.3 thx to [dalcde](https://github.com/dalcde)
    + fixed conky-bug
    + changed compatiblity to match all 1.6 releases
    + changed grid color to blue
    + removed panel icon (use applet instead: https://github.com/shuairan/gTile-applet )

* v0.2
    + added support for different panel positions of cinnamon (top,bottom,both)
    + panel icon is now displayed

* v0.1
    + added support for cinnamon
    + fixed small offset

-----

**Additional Settings:**

To configure gTile open the file extension.js  
go down to SETTINGS comments  
and edit this part of code:
    

    /*****************************************************************
                            SETTINGS
    *****************************************************************/
    /*INIT SETTINGS HERE TO ADD OR REMOVE SETTINGS BUTTON*/
    /*new GridSettingsButton(LABEL, NBCOL, NBROW) */
    function initSettings()
    {
        //Here is where you add new grid size button
        gridSettings[SETTINGS_GRID_SIZE] = [
            new GridSettingsButton('2x2',2,2),
            new GridSettingsButton('4x4',4,4),
            new GridSettingsButton('6x6',6,6)
        ];
        
        //example for new GridSettingsButton:
        myCustomButton = new GridSettingsButton('Custom',8,8); //Going to be a 8x8 GridSettings 
        gridSettings[SETTINGS_GRID_SIZE].push(myCustomButton);
        
        
        /*NEW SETTINGS*/    
         //You can change those settings to set whatever you want by default
         //Afterward you can change those parameters using the gTile interface
         gridSettings[SETTINGS_AUTO_CLOSE] = true;
         gridSettings[SETTINGS_ANIMATION] = true;
    }
