# Quest Block

![Quest Block](../../images/quest/quest.jpg)

The quest block creates a new quest wrapper and is needed to create a quest.


### Parameters

| Name               | Usage                                                     | Type    | Other |
|--------------------|-----------------------------------------------------------|---------|-------|
| Level Requirement  | The level that is needed to start the quest               | Number  |       |
| QP Requirement     | The amount of quest points needed to start the quest.     | Number  |       |
| Members Only       | If the quest is members only.                             | Boolean |       |
| Quest Name         | The name of the quest                                     | Text    |       |
| Quest ID           | The ID of the quest                                       | Number  |       |
| Start NPC          | The ID of the NPC that starts the quest                   | Number  |       |
| Filename           | The internal name of the quest                            | Text    |       |
| Stages             | The amount of stages the quest has                        | Number  |       |
| Gold Reward        | The amount of gold the user will be rewarded with         | Number  |       |
| XP Reward          | The amount of XP the user will be rewarded with           | Number  |       |
| Quest Point Reward | The amount of quest points the user will be rewarded with | Number  |       |
| Item Rewards       | The items the user gets when the quest is completed       | List    | See [here](#item-list) for more information |

## Item List

The item list is special as it needs a list of lists.

To add an item, drag two [`Create List With`](../blocks/list/create_list.md) blocks into the `Item Rewards` parameter, attaching the second list block to the first list block.

![Quest Block With Lists](../../images/quest/quest-block-with-lists.jpg)

In the second block, add two [`Text`](../blocks/text/text.md) blocks and set the first one to the ID of the item you want to give, and the second one to the amount.

![Quest Block With Items](../../images/quest/quest-block-with-items.jpg)