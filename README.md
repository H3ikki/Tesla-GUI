# Tesla-GUI
Graphical User Interface for Tesla and Wall Connector to Home Assistant.

This GUI is using incredible work of alandtse https://github.com/alandtse/tesla as data source for almost everything. The inspiration was drawn from Mobile App and most of the usable functions have been added that makes sense to use trough Home Assistant. I have White MYP so the initial version will have only these available. I can add new pictures to the GUI if some one provides the screen shots from their car.

![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/MainView1.png)
![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/MainView2.png)

The GUI has buttons below the image and four different menus. Inside the menus there are buttons that will actually make changes to your car. Some features are not working yet and they may be finalized in the future...

![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/MainView3.png)

The Image will change if the charging cable is connected and the charging current and limit can be changed from UI. Scheduling is also visible if it is in use and the charging time will be shown.

![alt text](https://github.com/H3ikki/Tesla-GUI/blob/main/Images/ChargerView1.png)

GUI also covers the Wall Connector and it shows the main information with similar look. The individual values have more details by clicking. Wall Connector GUI requires https://www.home-assistant.io/integrations/tesla_wall_connector integration
