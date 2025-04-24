# TaskFire
A todo tool which let's you create multiple boards. Each board can have child boards with its own todos and categories. If a todo is triggered it fires up to the master board. All on your local disk.

## The Main Screen
Complete view
![grafik](https://github.com/user-attachments/assets/499ae332-4547-44e6-af34-65b1a16c9b42)


### Boards
![grafik](https://github.com/user-attachments/assets/01d2432c-43ce-4522-a0f6-20f9335ee7f9)

#### Menu
Here you see at the top a menu which let you choose between
- Board View
- Search View (Comeing)
- Tag View (Comeing)
- Settings

#### Board Panel
Right below the boards are listed. In this case from two different databases stored local.
Task which get on fire on a sub board bubble all the way up to the board which can extinguish.
If a Task fires up the board shows a blue number to indicate the amount of new on fire tasks.

#### Board menu
The left button opens the board editor where you can add categories and some other stuff.
Under the board panel you can add a board to a database of your choice.
Each button has a tooltip if you move the mouse over it.

### Tag Editor
![grafik](https://github.com/user-attachments/assets/f3ce61a9-bd75-4a86-9d64-107d27bb0545)

#### Subtasks
Right below the title you can add subtasks. Subtasks which are marked as done are hidden automatically.
If you write #rd/#bu/#ye/#gn at the beginning of the subtask it is getting colored accordingly.

#### Tags
Tag categories can be defined in the tag editor. The tag category defines the color of the tag.
![grafik](https://github.com/user-attachments/assets/01bd8b69-7aa2-46ca-873f-5b09c1d8e90c)
Tags are also suggested which have been used in other tasks.
If no task uses this tag anymore it is not shown anymore.

#### Priority
The priority defines the position in the tasks list and also the color of the border.

#### Alert Date
![grafik](https://github.com/user-attachments/assets/983560c0-832b-4520-9f38-8ff7091ab022)
Here you can set a time when the task fires up.
If this happens and it comes up on your master board you can easily add more time and throw it back to the origin board.
You will also see a notify icon in the task bar which tells you how many new tasks got on fire since your last check.

#### Notes
A simple note box and below a link section.
If you do a screenshot, copy a url or file - just enter a name and press enter. It saves it automatically.
I use a macro in outlook to generate a link to a mail for example.

#### Links
Below the note section is a list of links. Just copy any url or even a screenshot, write a name and voila you got a link.

### Task list
![grafik](https://github.com/user-attachments/assets/9a7a189c-f7a0-40d7-a343-296147a35909)
Here you can see the tasks which are owned by the board or came up from a child board.
- The canceled alarm tells you that no alarm is set and it will not come up some day to remind you.
- The flame tells you whether it got on fire. In that case it is red.
- There can also be a blue siren which is visible when the task just came up and you haven't clicked on it.

## Other cool things
- Your data stays your data - no server, no risk
- It has an auto update function
- It is possible to sync between multiple devices through your favourite file sharing software like Dropbox, SharePoint or my favourite Syncthing.
- It is created with the power of AvaloniaUI. So it is only a question of time when the mobile app comes

# Thanks to
- [AvaloniaUI](https://avaloniaui.net/)
- [ReactiveUI](https://www.reactiveui.net/)
- [Projektanker/Icons](https://github.com/Projektanker/Icons.Avalonia)
- [LiteDB](https://www.litedb.org/)
- [Velopack](https://velopack.io/)
