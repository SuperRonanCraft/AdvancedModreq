## Menu ##
### Learn how to make a valid item! ###

### Summary ###
- [Title](#user-content-title)
- [Name](#user-content-name)
- [Lore](#user-content-lore)
- [Item](#user-content-item)
- [Custom Placeholder](#user-content-custom-placeholder)
- [Deletable Placeholder](#user-content-deletable-placeholder)
- [Placeholders](#user-content-placeholders)

#### Title ####
Info: The title of the inventory an item will be generated in  
Value Type: String

#### Name ####
Info: The name an item will have, with an optional %ticket_id% placeholder in most places  
Value Type: String  

#### Lore ####
Info: A list of strings displaying unique information per ticket and/or menu  
Value Type: String List

#### Item ####
Info: The item that should be generated  
Value Type: ItemID:*Data*:*Amount*   
Extra:
 - Get a list of valid item ids [here](http://minecraft-ids.grahamedgecombe.com)
 - Data and Amount are optional!
 - Data changes the data type, such as orange wool being "wool:1"
 - Amount can be added without altering the data with a "0" in place for data
 - Some sections allow [custom placeholders](#user-content-custom-placeholder), view available section on the [menu](files/menu.yml) file
Examples:
```yaml
Item: 'ink_sack:10:2'
Item: 'tnt:0:64'
Item: 'wool:1'
```

#### Custom Placeholder ####
Info: Placeholders that are based off the [messages.yml](files/messages.yml#user-content-placeholders) file, under the *Placeholders* section

#### Deletable Placeholder ####
Info: A [custom placeholder](#user-content-custom-placeholder) that will delete the line it's on if it returns a null or zero

#### Placeholders ####
Info: Every placeholder available, to view where each are valid, look at the default [menu.yml](files/menu.yml) file!  
Placeholders:
 - %ticket_id%: Displays the ticket id the generated item is displaying
 - %ticket_player%: Displays the owner the ticket belongs to
 - %ticket_msg%: The message the ticket was submitted with
 - %ticket_status%: Show a [custom placeholder](#user-content-custom-placeholder) of the tickets open/closed status
 - %ticket_status_reply%: Shows a [custom placeholder](#user-content-custom-placeholder) if there was a reply made to the ticket
 - %ticket_importance%: Shows a [deletable placeholder](#user-content-deletable-placeholder) of the tickets importance level
 - %ticket_category%: Shows a [deletable placeholder](#user-content-deletable-placeholder) of the tickets category
 - %ticket_time%: Shows a [custom placeholder](#user-content-custom-placeholder) of the tickets creation date
 - %ticket_resolved_msg%: Shows a [deletable placeholder](#user-content-deletable-placeholder) if the ticket was resolved when it was closed
 
