# Config ([View Default Config File](files/config.yml))
***
## Summary ##
- [Disable-Updater](#user-content-disable-updater) 
- [Settings](#user-content-settings)

### Disable-Updater ###
***
Info: Disable the "update avaiable" if an update is available  
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
  
