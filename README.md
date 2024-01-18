# The Tesla-GUI
Graphical User Interface for Tesla and Wall Connector to Home Assistant. Frontend with image card and elements.

This GUI is using incredible work of alandtse https://github.com/alandtse/tesla as data source for almost everything. The UX / UI was drawn from Mobile App and most of the usable functions have been added that makes sense to use trough Home Assistant. Also shoutout to ds2000 https://github.com/ds2000/homeassistant-fe-tesla for initial idea. I have White MYP so the initial version will have only these available. I can add new pictures to the GUI if some one provides the screen shots from their car.

![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/MainView1.png)
![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/MainView2.png)

The GUI has buttons below the image and four different menus. Inside the menus there are buttons that will actually make changes to your car. Some features are not working yet and they may be finalized in the future...

![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/MainView3.png)

The Image will change if the charging cable is connected and the charging current and limit can be changed from UI. Scheduling is also visible if it is in use and the charging time will be shown.

![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/ChargerView1.png)

GUI also covers the Wall Connector and it shows the main information with similar look. The individual values have more details by clicking. Wall Connector GUI requires https://www.home-assistant.io/integrations/tesla_wall_connector integration

## Installation

This gives some pain since I have seen so many badly documented instructions, maybe this will be different:

### Prework
To make things easy you should have some addon to gain access to the file system and files. All following steps can be done with https://github.com/hassio-addons/addon-vscode Easiest way to install this is to search it from Home Assistant Addon store!

### Car card
1. Add custom integration from https://github.com/alandtse/tesla
2. Make it work with your vehicle as instructed
3. Add "Stack In Card" by @RomRider from HACS or manually (https://github.com/custom-cards/stack-in-card)
4. Add "slider-entity-row" from HACS or manually (https://github.com/thomasloven/lovelace-slider-entity-row)
5. Add the Gotham font to the Dashboard Resources: https://fonts.cdnfonts.com/css/gotham. Go to Settings/Dashboards and click on the 3-dot menu at the top right.
6. Copy "Tesla GUI" folder https://github.com/H3ikki/Tesla-GUI/tree/main/Tesla-GUI from trunk to Home assistant file system, /config/www/ *here* So the result should be Config/www/Tesla-GUI
7. Add the Tesla GUI to configuration.yaml by adding following lines:<br>
homeassistant:<br>
&nbsp;&nbsp;packages:<br>
&nbsp;&nbsp;&nbsp;&nbsp;tesla_gui: !include www/Tesla-GUI/Tesla GUI.yaml<br>
8. Replace "tessu" with your tesla entity name (nickname by default) at /config/www/Tesla-GUI/Tesla GUI.yaml
9. Check that everything is working by Developer tools --> YAML Settings --> Check Settings
10. If all good, then proceed by quick reboot at developer tools.
11. Go to dashboard and create new "Manual card"
12. Copy-Paste "Car_card.txt" to the manual card code
13. My car is called "Tessu" so and that is also in the entity name so search and replace "tessu" with your own entity name and the "Tessu" with capital for main view
14. Customise the pictures if available by search MYP_White and replace with your model like MS_Blue
15. Enjoy!

### Wall Connector card
1. Add https://www.home-assistant.io/integrations/tesla_wall_connector integration
2. Go to dashboard and create new "Manual card"
3. Copy-Paste "Wall_Connector_card.txt" to the manual card code
4. Enjoy!

## TODO
- Chevrons should be working or they will be removed

## Bugs & Requests
There will surely be some initial bugs and I'll try to handle them asap. Features and pictures will be added in hte furute

If you like the work feel free to byu me a beer!

[![](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/donate/?business=DQCTDKTYT5UFQ&no_recurring=0&currency_code=EUR)
