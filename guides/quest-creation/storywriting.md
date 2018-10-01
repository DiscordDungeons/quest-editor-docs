# Storywriting

Alright, let's focus on the story.

As I explained at the start of this guide, we need a story for our quest. For this one, we'll be writing a simple gathering quest where the user will need to gather two different items in different stages.

### Let's outline it.

In order to write a quest, I like to put each dialog and action on its own line in the outline.

For dialogs, I also like to have it in the format of `NPC Name - Dialog`.

#### Let's write it.

For this guide, we'll say our NPC is named `Julian` and we'll be giving the user a multiple option choice for the first dialog.

We'll also say that the user needs to firstly gather two oak logs, and then two pine logs, which has the item IDs `375` and `408`.

To specify a certain stage of the quest, we'll use two equals signs, the stage ID and another two equals signs in the format of `== Stage <Stage ID> ==`

To specify what happens when a user selects a certain option, we'll use square brackets (`[]`)

To specify a certain action that doesn't directly relate to the dialog, we'll use curly brackets (`{}`)

To specify that a line is related to the previous ones, we'll use tabs or four spaces to indent the line.

```

== Stage 1 ==

Julian - Hi there, I have an issue and I need some logs, would you mind getting them for me?
* Option 1: Sorry, I'm kind of busy right now.
* Option 2: Sure, I'd love to!

[Option 1]
	Julian - I see, maybe I can find someone else to help me.
[Option 2]
	Julian - Great! I need 5 Oak Logs!
	{Continue Check}
    	{Start Quest}
        {Send Message "Quest Started: ${this.name}.\n[Written by Username]"}
       
== Stage 2 ==

{If User Has 5 Oak Logs}
	Julian - Just what I needed, thank you! I need some pine logs too, do you mind getting those for me too?
    {Continue Check}
    	{Take 5 Oak Logs from User Inventory}
    	{Update Quest with Text "Get 5 pine logs"}
        {Switch to Stage 3}
{Else}
	Julian - Have you gotten the oak logs yet?
    
== Stage 3 ==

{If User Has 5 Pine Logs}
	Julian - Thank you, now I can solve this issue!
    {Continue Check}
        {Take 5 Oak Logs from User Inventory}
    	{End Quest}
        {Send End Quest Dialog}
{Else}
	Julian - Have you gotten the pine logs yet?
```

Now that we have written the quest, let's go ahead and build it.