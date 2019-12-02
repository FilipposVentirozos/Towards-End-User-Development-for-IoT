
## Annotation Guidelines

#### Practises to follow during annotation

- In selecting an event type, only slot values contained within the same sentence should be considered.
- The slots “Where”, “What”,“Why” and “How” should describe one of the events listed in the table below.
- The value of “Where” should be in our compiled dictionary (i.e. `kitchen_appliance_dictionary.json`) regarding the `wordlist`s inside the main class and subclass of the device.
- In cases where one or more of the “Where”, “What”,“Why” and “How” slots are missing but the event type is implicit, an event type should still be selected.
- Of interest  are  events  directly related to the kitchen device rather than  the  dish  being  prepared. For instance, in the instruction “After 10 minutes, take out the dish from the oven, stir, and then set it back inside”, the events of interest are those pertaining to setting the oven timer and the (implicit) opening of the oven, rather than the stirring of the dish.
- Only events where the device is used to cook or produce the dish are annotated. For example, in the instruction “Take out eggs from the fridge”, the fridge is used for storage and not as a device for producing the dish; hence no event is annotated in this instruction.

#### Events table

|  Event No | Where       | What            | Why                       | How                 | About                                                                    | Example                                    |
|-----------|-------------|-----------------|---------------------------|---------------------|--------------------------------------------------------------------------|--------------------------------------------|
| 1         | device      | time            | switch off                | unit of measurement | Setting the  timer to switch off the oven or  take out from fridge       | bake for  10 minutes                       |
| 2         | device      | state           | switch on                 | description/boolean | Turn on the oven or set  in the fridge                                   | switch on  the microwave                   |
| 3         | device      | temperature     | increase or decrease heat | unit of measurement | Set the  temperature in the oven                                         | preheat  your oven to 225 F                |
| 4         | device      | cooking  style  | style parameter           | description         | Set the style  in the oven                                               | set the oven on grill                      |
| 5         | device door | opening         | set extent                | description         | Open-close  the oven door                                                | open the oven                              |
| 6         | device      | visual state    | switch off                | description         | Switch off after  a visual state  has been me                            | switch off oven when crust is golden brown |
| 7         | device      | material  state | switch off                | description         | Switch off after a  material state has  been met or take out from fridge | microwave until melted                     |
| 8         | device      | oven rack       | position  parameter       | description         | Set the position  (e.g., racks) inside the oven or the fridge            | insert in the  middle rack of the oven     |