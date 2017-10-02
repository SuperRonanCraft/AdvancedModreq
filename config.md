# Config #

### Summary ###
- [Disable-Updater](#user-content-disable-updater)
- [Settings](#user-content-settings)

#### Disable-Updater ####
  Info: Disable the "update avaiable" if an update is available  
  Values: 'true' or 'false'  
  Default Value: 'false'

#### Settings ####
  #### Settings Summary ####
  - [DownloadBDOnReload](#user-content-downloaddbonreload)
  - [MinimumWords](#user-content-minimumwords)
  - [MessageCutOff](#user-content-messagecutoff)
  - [Importance](#user-content-importance)
  - [Rating](#user-content-rating)
  - [Filter](#user-content-filter)
  
  #### DownloadDBOnReload ####
  Info: Download the database (if MySQL is enabled) on plugin reload  
  Value Type: Boolean  
  Default Value: 'false'
  
  #### MinimumWords ####
  Info: The minimum amount of words a ticket must be to allow submitting  
  Value Type: Integer  
  Default Value: 5
  
  #### MessageCutOff ####
  Info: The maximum characters allowed until a line is cutoff  
  Value Type:  
  \- Max: Integer  
  \- Suffix: String  
  Default Value:  
  \- Max: 32  
  \- Suffix: '...'  
  
  #### Importance ####
  Info: Enable the importance system?  
  Value Type:   
  \- Enabled: Boolean  
  Default Value:  
  \- Enabled: true
  
  #### Rating ####
  Info: Enable the   
  Value Type:  
  \- Enabled: Boolean  
  Default Value:  
  \- Enabled: true  
  
  #### Filter ####
  Info: Create a filter system to filter any foul language  
  Value Type:  
  \- Enabled: Boolean  
  \- Submitting:  
    \-- AllowSubmitting: Boolean  
    \-- Substitute: String  
  \- Blacklist: List
  Default Value:  
  \- Enabled: true  
  \- Submitting:  
    \-- AllowSubmitting: true  
    \-- Substitute: '******'  
  \- Blacklist:  
    \-- dumb  
    \-- stupid  
    \-- crap  
