# IntelliJ IDEA

**IntelliJ IDEA shortcuts ([IntelliJIDEA_ReferenceCard](https://resources.jetbrains.com/storage/products/intellij-idea/docs/IntelliJIDEA_ReferenceCard.pdf))**

## Learn shortcuts as you work
IntelliJ IDEA provides several possibilities to learn shortcuts:

Find Action lets you search for commands and settings across all menus and tools.

Press `Ctrl+Shift+A` and start typing to get a list of suggested actions. Then select the necessary action and press `Enter` to execute it.

Find Action
To add or change the shortcut for any action, press `Alt+Enter` when it is selected in the list.


If you are using one of the predefined keymaps, you can print the default keymap reference card  and keep it on your desk to consult it if necessary. This cheat sheet is also available under Help | Keyboard Shortcuts PDF.


The following table lists some of the most useful shortcuts to learn:

| Shortcut | Action |
|----------|----------|
| ==Double `Shift`== | *__Search Everywhere:__* <br/> Quickly find any file, action, symbol, tool window, or setting in IntelliJ IDEA, in your project, and in the current Git repository.|
| ==`Ctrl+Shift+A`== | *_Find Action:_* <br/> Find a command and execute it, open a tool window, or search for a setting.|
| ==`Alt+Enter`== | *_Show Context Actions:_* <br/> Quick-fixes for highlighted errors and warnings, intention actions for improving and optimizing your code.|
| ==`F2`== <br/> `Shift+F2` | Navigate between code issues <br /> Jump to the next or previous highlighted error.|
| ==`Ctrl+E`== | *_View recent files:_* <br/> Select a recently opened file from the list.|
| ==`Ctrl+Shift+Enter`== | *_Complete Current Statement:_* <br/> Insert any necessary trailing symbols and put the caret where you can start typing the next statement.|
| ==`Ctrl+Alt+L`== | *_Reformat Code:_* <br/> Reformat the whole file or the selected fragment according to the current code style settings. |
| `Ctrl+Alt+O` | *_Optimise Imports:_* <br/> Remove irrelevant Java imports. |
| `Ctrl+Alt+I` | *_Auto Ident:_* <br/> Fix line idents. |
| ==`Ctrl+Alt+Shift+T`== | *_Invoke refactoring (show refactor menu):_* <br/> Refactor the element under the caret, for example, safe delete, copy, move, rename, and so on.|
| ==`Ctrl+W` <br/> `Ctrl+Shift+W`== | Extend or shrink selection <br /> Increase or decrease the scope of selection according to specific code constructs.|
| ==`Ctrl+/`== <br/> `Ctrl+Shift+/` | Add/remove line or block comment <br/> Comment out a line or block of code.|
| ==`Ctrl+B`== | *_Go To Declaration:_* <br/> Navigate to the initial declaration of the instantiated class, called method, or field.|
| `Ctrl+Alt+B ` | _Navigate to implementation:_ <br/> To navigate to the implementations of an abstract method, position the caret at its usage or its name in the declaration and press   Ctrl   Alt   B  . |
| ==`Alt+F7`== | *_Find Usages:_* <br/> Show all places where a code element is used across your project.|
| ==`Alt+1`== | Focus the Project tool window |
| `Escape` | Focus the editor |
| `Ctrl+Space` | Code completion|
| ==`Ctrl+Ctrl`== | _Run anything anywhere:_ <br/> No matter where we are in the IDE or which file is open, if we double tap Ctrl the Run Anything window opens.  By default, this shows a list of recently run configurations.  But we can also type the name of something to run to search for other run configurations.|
| `Alt+Insert` | _Code generation:_ <br/> IntelliJ IDEA can generate getter and setter methods for fields in your class. With the caret inside the class, press   Alt   Insert   (Code | Generate). | 
| `Ctrl+Q` | _Quick code documentation:_ <br/> To quickly see the documentation for a class or method at the caret, press   Ctrl   Q   (View | Quick Documentation). |



## Show usages
You can view the list of all usages of a class, method or variable across the whole project, and quickly navigate to the selected item. Place the caret at a symbol and press   `Ctrl + Alt + F7`   (Edit | Find Usages | Show Usages).
To jump to a usage, select it from the list and press   ↩ Enter  .


## The Rename refactoring
You can easily rename your classes, methods, and variables with automatic correction of all places where they are used.
Position the caret at the symbol you want to rename, and press   `Shift + F6`   (Refactor | Rename). Type the new name and press   ↩ Enter  .


Access VCS-related options
Press  `Alt + Back Quote` to access all VCS-related commands available in the current context.
 

Show usages
You can view the list of all usages of a class, method or variable across the whole project, and quickly navigate to the selected item. Place the caret at a symbol and press   Ctrl   Alt   F7   (Edit | Find Usages | Show Usages).
To jump to a usage, select it from the list and press   ↩ Enter  .


Navigate to implementation
To navigate to the implementations of an abstract method, position the caret at its usage or its name in the declaration and press   Ctrl   Alt   B  .


Smart Line Joins
   Ctrl   Shift   J  .

Extract Variable refactoring
The Extract Variable refactoring wraps a selected expression into a variable. It adds a new variable declaration and uses the expression as an initializer. Select an expression and press   Ctrl   Alt   V   (Refactor | Extract/Introduce | Variable).
 
Create code constructs with completion
You can create code constructs using statement completion. Start typing a method declaration, a method call or a statement such as   if  ,   do -while  ,   try -catch  , or   return  . Press   Ctrl   Shift   Enter   to complete the statement into a syntactically correct construct.
 

View recent files
Press   Ctrl   E   (View | Recent Files) to view the list of recently opened files.

Surround code fragments
You can quickly wrap a code block in useful constructs. Select it in the editor and press   Ctrl   Alt   T   (Code | Surround With).
The list of available options or wrappers is context-sensitive and depends on the language. 

Switch scheme
You can apply a different code style, coloring scheme, or keymap with a single keystroke right from the editor. Press   Ctrl   Back Quote   (View | Quick Switch Scheme) to specify the scheme you want to switch to.

Show file structure
You can quickly navigate within the current file with   Ctrl   F12   (Navigate | File Structure).
File structure shows the list of members of the current class. To navigate to an element, select it and press   Enter   or   F4  .
To easily locate an item in the list, start typing its name.

### Top Underrated Shortcuts

| Shortcut | Action |
|----------|----------|
| `Alt+X` | *_Close all inactive tabs_*: <br /> If your editor looks overloaded with open tabs, you can take care of this with just one key and a click. All you have to do is press _⌥_ (macOS) or _Alt_ (Windows/Linux) and click the _“x”_ on the active tab. The IDE will then close all inactive tabs at once, and the tab you are currently working on will stay open. |
| `Shift+Ctrl+V` | *_Choose content to paste_*: <br /> IntelliJ IDEA allows you to keep several recently copied items in the clipboard and paste any of them with the help of _⇧⌘V_ (macOS) or _Shift+Ctrl+V_ (Windows/Linux). This means you don’t have to worry about losing any pieces of code you’ve copied recently.|
| `Alt+/` | *_Use hippie completion_*: <br /> You are probably used to IntelliJ IDEA’s code completion mechanism, which offers suitable suggestions depending on the context. However, there may be cases when you simply want to reuse words that have been used earlier in the current file or even the project, regardless of their context.<br /><br />[_Hippie completion_](https://www.jetbrains.com/help/idea/auto-completing-code.html#hippie_completion) works in such situations. You can use this feature by putting the caret at the desired position and pressing _⌥/_ (macOS) or _Alt+/_ (Windows/Linux). |
| `Ctrl+Alt+L` | *_Reformat code_*: <br /> When working in a team, you usually share a unified code format. So, if the formatting in a project doesn’t correspond to the conventions you are using, select a piece of code you want to reformat according to your settings and press _⌥⌘L_ (macOS) or _Ctrl+Alt+L_ (Windows/Linux).|
| `Ctrl+F12` | *_Navigate along file structure_*: <br /> This shortcut is for you if you are searching for an alternative way to quickly access methods used in your file. Instead of text search, you can open your file structure by pressing _⌘F12_ (macOS) or _Ctrl+F12_ (Windows/Linux). Then, in the structure window that pops up, start typing the method name, navigate to the correct variant with the up and down arrows, and press Enter. That’s it!|
| `Alt+J` | *_Select multiple occurrences_*: <br /> If you need to select and edit identical pieces of code quickly, then this shortcut is your best option. To use it, put the caret on the necessary symbol and press _⌃G_ (macOS) or _Alt+J_ (Windows/Linux). Then, once the code element is highlighted, keep pressing this shortcut to move through the file. You will notice that the caret is being multiplied and appears next to every instance of the highlighted code element. If you start editing the highlighted code, this code will be changed automatically in every other instance.|
| `Alt+Shift+↑/↓` | *_Move lines_*: <br />  This shortcut is simple, yet very effective. Press _⌘⇧_ (macOS) or _Alt+Shift_ (Windows/Linux), and then use the up and down arrow keys to move the line where the caret is currently positioned into the desired position.<br /><br />However, be careful when using this shortcut, as it can move lines out of scope.<br /><br />If you are worried about moving lines outside of statements accidentally, use the shortcut that moves statements – _⇧⌘↑/↓_ (macOS) or _Ctrl+Shift+↑/↓_ (Windows/Linux).|
| `Ctrl+D` | *_Duplicate line_*: <br /> This shortcut is useful for when you need to add several similar lines but with different parameters. To try it out, place the caret at the line that needs duplicating and then press _⌘D_ (macOS) or _Ctrl+D_ (Windows/Linux). |
| `Ctrl+F11` | *_Add mnemonic bookmarks_*: <br /> To quickly access folders, files, project items, and code lines, you can bookmark them with numbers (0 –9) or letters (A–Z). Once assigned, the IDE will show mnemonics in the gutter.<br /><br />To add this kind of bookmark to a code line, place the caret on this line and press _⌥ F3_ (MacOs) or _Ctrl+F11_ (Windows). To bookmark a file, package, folder, or module, select the necessary item in the _Project_ list, and press the same shortcut.<br /><br />Then, select the number or letter you want to use as an identifier for this bookmark in the popup. All done!<br /><br />To jump to the bookmark, hold _^_ (MacOs) or _Ctrl_ (Windows) and then press the predefined digit or letter on your keyboard. |
| `` Ctrl+` `` | *_Change view mode_*: <br /> IntelliJ IDEA offers a variety of view modes to meet your personal needs while coding. They include _Presentation Mode_, _Distraction Free Mode,_ _Full Screen_, and _Zen Mode_. To activate them: <ul><li> Press _^`_ (macOS), or _Ctrl+`_ (Windows/Linux). </li><li> In the _Switch_ dialog that appears, press 5. </li><li> Use the up/down arrow keys to select the desired mode or press the corresponding number.</li></ul> To go back to the default view, repeat the same steps.<br /><br />One of our favorites is _Distraction Free Mode_. It keeps you 100% focused on the task by hiding all UI elements and keeping the source code centered. Check it out! |
| `Ctrl+G` | *_Go to line:column_*: <br /> This shortcut works perfectly when you know the exact place in the code where you need to navigate to quickly. Press _⌘L_ (macOS) or _Ctrl+G_ (Windows/Linux) to open the _Go to Line:Column_ dialog and enter the desired line or column number. You can also enter both, separating them with a colon (:). Click OK, and you are at the desired position. |
| `Ctrl+ -/+` | *_Collapse and expand code blocks_*: <br /> Use this shortcut to see the file structure more clearly or quickly navigate to specific parts of a class. You can collapse all the expandable code blocks by pressing _⌘-_ (macOS) or _Ctrl +_ – (Windows/Linux). To expand them back, press _+_ in combination with _⌘_ or _Ctrl_. |
| `Ctrl+Shift+A` | *_Find action to add photo as background_*: <br /> This shortcut evokes various actions in the IDE that can be useful in many situations. However, today we want to share just one of these actions – one that you can use to give your IDE a cute and personalized touch.<br /><br />Would you like to have a view of your favorite people, animals, things, or landscapes while coding? That’s easy – you just have to set a background photo.<br /><br />To do so, press _⌘⇧A_ (macOS) or _Ctrl+Shift+A_ (Windows and Linux) to conjure the _Find Actions_ dialog and then type “background image”. Then, in the dialog that appears, select the path to the photo and configure other available settings however you like. For example, you can change the opacity of your image.<br /><br />To return to your standard editor background, click the _Clear and Close_ button in the previous dialog. |
[The IntelliJ IDEA Blog: Top Underrated Shortcuts](https://blog.jetbrains.com/idea/2022/10/top-underrated-shortcuts/)


#ide #shortcuts