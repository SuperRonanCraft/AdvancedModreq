# Config ([View Default Config File](files/config.yml))
***
## Summary ##
- [Disable-Updater](#user-content-disable-updater) 
- [Settings](#user-content-settings)
- [Notifications](#user-content-notifications)
- [Category](#user-content-category)
- [Economy](#user-content-economy)
- [Alias](#user-content-alias)

### Disable-Updater ###
Info: Disable the "update avaiable" if an update is available  
***
Values: 'true' or 'false'  
Default Value: 'false'

### Settings ###
Info: Basic Plugin settings that can be disabled/changed
***
  #### DownloadDBOnReload ####
  Info: Download the database (if [MySQL](files/MySQL.yml) is enabled) on plugin reload  
  Value Type: Boolean  
  Default Value: 'false'  
  #### MinimumWords ####
  Info: The minimum amount of words a ticket must be to allow submitting  
  Value Type: Integer  
  Default Value: 5
  #### MessageCutOff ####
  Info: The maximum characters allowed until a line is cutoff  
  Value Type:
  ```yaml
  Settings:
    MessageCutOff:
      Max: Integer  
      Suffix: String
  ```
  Default Value: 
  ```yaml 
  Settings:
    MessageCutOff:
      Max: 32  
      Suffix: '...'
  ```
  #### Importance ####
  Info: Enable the importance system?  
  Value Type:   
  ```yaml
  Settings:
    Importance:
      Enabled: Boolean 
  ```
  Default Value:  
  ```yaml
  Settings:
    Importance:
      Enabled: true
  ```
  #### Rating ####
  Info: Enable the Ratings system (Rate how well their service was after a ticket is closed with a resolved message)  
  Value Type:  
  ```yaml
  Settings:
    Rating:
      Enabled: Boolean 
  ```
  Default Value:  
  ```yaml
  Settings:
    Rating:
      Enabled: true
  ``` 
  #### Filter ####
  Info: Create a filter system to filter out foul language  
  Value Type:  
  ```yaml
  Settings:
    Filter:
      Enabled: Boolean  
      Submitting:  
        AllowSubmitting: Boolean  
        Substitute: String  
      Blacklist: List
  ```
  Default Value:
  ```yaml
  Settings:
    Filter:
      Enabled: true  
      Submitting:  
        AllowSubmitting: true  
        Substitute: '******'  
      Blacklist:  
      - dumb
      - stupid
      - crap
  ```
### Notifications ###
Info: Enable a notification when the specified ticket event happens, and what sound to play
***
Value Type:
```yaml
Notifications:
  <Type>:
    Enabled: Boolean
    Sound: Sound
```
Default Value:
```yaml
Notifications:
  <Type>:
    Enabled: true
    Sound: 'Any sound at https://www.spigotmc.org/wiki/cc-sounds-list/'
```

### Category ###
Info: Tickets can have a category type to organize situations
***
  #### Enabled ####
  Info: Enable the Categories system  
  Value Type: Boolean  
  Default Value: true
  #### Categories ####
  Info: Create a custom category with it's name as the yaml section  
  Value Type: Section List  
  Example:
  ```yaml
  Category:
    Categories:
      CUSTOMCATEGORYNAME:
        Description: 
        - 'A description of category, viewable with /modreq categories' # Can have multiple lines
        Importance: 5 ## Optional if you don't want players chosing an importance level for this category!
        Item: 'bedrock' # Any item name
      CUSTOMCATEGORYNAME2:
        Description: 
        - '&aCool Category &7- &fMake a report based off coolness'
        Importance: 0 ## If an importance level is zero, players can still chose an importance level!
        Item: 'ice'
  ```

### Economy ###
Info: Make a ticket cost some cash to create a submission
***
  #### Enabled ####
  Info: Enable the Economy system  
  Value Type: Boolean  
  Default Value: false
  #### Price ####
  Info: The price of a ticket submission  
  Value Type: Integer  
  Default Value: 25
  
### Alias ###
Info: Alias the command "/modreq create" to just one command and no arguments
***
  #### Enabled ####
  Info: Enable the Categories system  
  Value Type: Boolean  
  Default Value: true
  #### List ####
  Info: Create a custom category with it's name as the yaml section  
  Value Type: String List
