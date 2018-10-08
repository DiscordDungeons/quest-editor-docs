# Travel Data Block

![Travel Data Block](../../images/locations/travel-data.jpg)

The travel data block returns a new travel data object.

| Name        | Usage                                                              | Type   | Extra                                                             |
|-------------|--------------------------------------------------------------------|--------|-------------------------------------------------------------------|
| Travel To   | The ID of the location the travel applies to                       | Text   |                                                                   |
| Travel Time | The amount of time it takes for the user to travel to the location | Number | Defined in seconds                                                |
| Travel Type | The type of travel it takes to get to the location                 | Text   |                                                                   |
| Travel Fee  | The cost of travelling to the location                             | Number | Requires the `Travel Type` to not be set as `Default` to function |