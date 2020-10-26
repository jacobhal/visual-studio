# Visual Studio 2019 Tips and Keyboard Shortcuts
This README contains the most useful keyboard shortcuts, extensions and some general/debugging tips in Visual Studio.

Table of Contents
=================

   * [Visual Studio 2019 Tips and Keyboard Shortcuts](#visual-studio-2019-tips-and-keyboard-shortcuts)
   * [Table of Contents](#table-of-contents)
      * [My favourite extensions](#my-favourite-extensions)
         * [Codemaid](#codemaid)
         * [ReSharper](#resharper)
         * [Image optimizer](#image-optimizer)
         * [File icons](#file-icons)
         * [File nesting](#file-nesting)
         * [VSColorOutput/Output enhancer](#vscoloroutputoutput-enhancer)
         * [Viasfora](#viasfora)
         * [Object Exporter](#object-exporter)
      * [How to setup ReSharper](#how-to-setup-resharper)
        * [My way of setting up ReSharper](#my-way-of-setting-up-resharper)
      * [My favourite keyboard shortcuts](#my-favourite-keyboard-shortcuts)
         * [Basic global shortcuts](#basic-global-shortcuts)
         * [Default Visual Studio](#default-visual-studio)
         * [Codemaid](#codemaid-1)
         * [ReSharper](#resharper-1)
      * [My favourite code snippets](#my-favourite-code-snippets)
      * [ReSharper Live Templates](#resharper-live-templates)
         * [Create Live Template](#create-live-template)
         * [Edit Live Template](#edit-live-template)
      * [Running &amp; Debugging](#running--debugging)
         * [Running &amp; Debugging keyboard shortcuts](#running--debugging-keyboard-shortcuts)
         * [Debugging windows](#debugging-windows)
            * [Watch window](#watch-window)
            * [Call stack](#call-stack)
            * [Autos](#autos)
            * [Locals](#locals)
         * [Debugging useful tips](#debugging-useful-tips)
            * [Create JSON From Object During Debugging](#create-json-from-object-during-debugging)
            * [Unhelpful exception message](#unhelpful-exception-message)
            * [Debugging tests](#debugging-tests)
      * [Common issues](#common-issues)
         * [Restart Visual Studio](#restart-visual-studio)
         * [Clear cache and restart resharper](#clear-cache-and-restart-resharper)
         * [Delete .vs folder](#delete-vs-folder)

Created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc)

## My favourite extensions

### Codemaid
Code cleanup, restructuring as well as a range of other helpful tools is what you will receive after installing CodeMaid. The nice thing about CodeMaid is, that it works on multiple file types and not only C#.

### ReSharper
Everyone's favourite Visual Studio extension. It is not free but if you are at your workplace, chances are that they have Resharper subscriptions for everyone to use. Resharper provides on-the-fly code inspection, code generation, refactoring, lots of keyboard shortcuts to either use in conjunction with the default Visual Studio keymappings or overriding them and much more.

Resharper allows you to:  
* Write more code with less typing
* Improve code quality
* Easily find files, classes, methods, properties etc.

### Image optimizer
Right click an image inside Visual Studio and heavily reduce image size using a single click.

### File icons
Showing correct file icons in the solution explorer doesn't sound that important. You will quickly realize, after installing this extension, that it means the world when navigating project files.

### File nesting
You know how web.release.config files nest nicely beneath web.config? The File Nesting extension adds this behavior for all types of files. The perfect way to clean up the solution explorer.

### VSColorOutput/Output enhancer
The Output window in Visual Studio shows a lot of useful information, but the window is pretty useless without color highlighting. This extension adds just that.

### Viasfora
Viasfora adds alot of different features, different highlightings, bracket highlightings etc. with the ability to modify the colors to your liking.

### Object Exporter
Object Exporter lets you export out an object while debugging in Visual Studio, the object can be serialized in either C#, JSON or XML.

## How to setup ReSharper
When you first get ReSharper, you are asked to setup your keyboard shortcuts scheme.  
If you are most common to .NET you should select the "Visual Studio" scheme.

If you want to change it later you can go to ReSharper -> Options -> Environment -> Keyboard & Menus

Another thing you need to know is that some of the ReSharper shortcuts are in conflict with the default Visual Studio shortcuts. The recommended thing to do whenever you get a conflicting shortcut popup is to apply the ReSharper shortcuts everywhere.

### My way of setting up ReSharper
1. Go to Tools --> Options --> Environment --> Keyboard and click *Reset* to reset keyboard shortcuts.
2. In the dropdown of the same window, select *ReSharper (Visual Studio)* instead of *default*.
3. Go to Extensions --> ReSharper --> Options --> Environment --> Keyboard & Menus and make sure "Override Visual Studio refactorings", "Hide overriden Visual Studio menu items" and "Use Alt+R shortcut to open ReSharper menu in Visual Studio 2019 is checked. Then select the Visual Studio keyboard scheme and click *Apply Scheme*.
4. Go back into Tools --> Options --> Environment --> Keyboard
    * Assign *Window.CloseDocumentWindow* to Ctrl + W and remove the Ctrl + W shortcut for *Edit.SelectCurrentWord*. Assign Alt + S as the new shortcut for *Edit.SelectCurrentWord* and Alt + Shift + S to *ReSharper.ReSharper_ShrinkSelection*.
    * Remove the shortcut for *ReSharper.ReSharper_LineComment* in order to do curly brackets with Ctrl + Alt + 7.
5. Whenever the popup of conflicting keyboard shortcuts appear, select the ReSharper shortcuts as preference and check "Apply for all".

## My favourite keyboard shortcuts

### Basic global shortcuts
* Move selection one tab stop to the right: **Tab**
* Move selection one tab stop to the left: **Shift + Tab**
* Copy/Cut selection or current line: **Ctrl + C AND Ctrl + X**
* Select text from cursor position to the end of the line: **Shift + End**
* Select text from cursor position to the beginning of the line: **Shift + Home**
* Jump to beginning of line: **Ctrl + Home**
* Jump to end of line: **Ctrl + End**
* Take a screenshot and save to clipboard: **Windows key + Shift + S**

### Default Visual Studio
* Code navigation
    * Go to definition of variable/method: **F12**
    * Go to implementation/declaration: **F12**
    * Show all references: **Shift + F12**
    * Go to the last place of the cursor: **Ctrl + -**
    * Go to the last place of the cursor (reverse): **Ctrl + Shift + -**
    * Go to Line: **Ctrl + G**
    * Properties (with cursor on project/solution): **Alt + Enter**
    * Clipboard history **Ctrl + Shift + V**
* Searching
    * Search everywhere/Go to all: **Ctrl + T**
    * Go to file: **Ctrl + Shift + T**
    * Search current file: **Ctrl + F**
    * Search entire solution: **Ctrl + Shift + F**
* Editing
    * Move lines up or down: **Alt + Up/Down arrow** (Will be move to prev/next method if you use ReSharper shortcuts)
    * Replace in current file: **Ctrl + H**
    * Replace in entire solution: **Ctrl + Shift + H**
    * Surround marked code with code block: **Ctrl + K, Ctrl + S**
* Commenting
    * Comment block: **Ctrl + K, Ctrl + C**
    * Uncomment block: **Ctrl + K, Ctrl + U**
* Formatting
    * Format document: **Ctrl + K + D**
* Expanding/Collapsing
    * Expand/Collapse a code block: **Ctrl + M, Ctrl + M**

### Codemaid
* Go to the current file in solution explorer: **Ctrl + M, F**
* Cleanup & Format the currrent file: **Ctrl + M, Space**
* Start Codemaid Spade (tree view of project with drag and drop): **Ctrl + M, .**
* Reorganize methods/fields to follow Microsoft's convention: **Ctrl + M, Z**

### ReSharper
* The golden shortcut (for private field initialization and much more): **Alt + Enter** 
* Fast name typing: Type the upper case letters of a class/method. For instance ANE for ArgumentNullException.
* Activate autocompletion: **Ctrl + Space**.
* Go to file in solution explorer (if you do not have Codemaid): **Shift + Alt + L**.
* Search everywhere/Go to all (same as default): **Ctrl + T**
* Go to file (same as default): **Ctrl + Shift + T**
* Activate the File Member window: **Alt + \\**
* Expand/shrink code selection: **Ctrl + W AND Ctrl + Shift + W** (I recommend switching these out)
* Move code block up/down: **Ctrl + Shift + Alt + Up/Down arrow**
* Refactor: **Ctrl + Shift + R**
* Reformat code: **Ctrl + Alt + Enter**

## My favourite code snippets
* **class**: Create a class
* **ctor**: Create a constructor
* **interface**: Create an interface
* **cw**: Create a Console.WriteLine() line
* Properties/methods within a class:
    * **prop**: Create an auto-implemented property
    * **propfull**: Create a property with a private field
    * **equals**: Override the Equals method of the base class
* Loops:
    * **for**: Create a for loop
    * **forr**: Create a for loop with a decrementing loop variable
    * **foreach**: Create a foreach loop
    * **while**: Create a while loop
    * **do**: Create a do loop
* Exceptions:
    * **try**: Create a try/catch block
    * **tryf**: Create a try/finally block

> Note: If the code snippet has dynamic variables to fill in, press Tab to move to the next one.

## ReSharper Live Templates
Sometimes you have blocks of code that you constantly have to type over and over. If you want to defined your own code blocks that can be generated using keywords you can use ReSharper live templates.

### Create Live Template
1. Select the code block/snippet
2. ReSharper --> Tools --> Create Live Template from Selection
3. Create and edit
4. Type in a shortcut name and description
5. Optional: Surround the parts you want to be dynamic with a dollar sign "$"
5. Ctrl + S to save

### Edit Live Template
1. ReSharper --> Tools --> Templates Explorer
2. Select the template --> Edit Template
3. Ctrl + S to save

## Running & Debugging
### Running & Debugging keyboard shortcuts
* Breakpoint: **F9**
* Show all breakpoints: **Ctrl + Alt + B**
* Run in debug mode/continue until next breakpoint: **F5**
* Run without debug/stop debug mode: **Ctrl + F5**
* Restart: **Ctrl + Shift + F5**
* Step over: **F10**
* Step into: **F11**
* Step out: **Shift + F11**
* Go to row: **Ctrl + F10**

### Debugging windows
#### Watch window
DEBUG —> Windows —> Watch —> Watch 1 (Choose variables by typing their name into the window)

#### Call stack
Use the call stack to show how you got to a place: DEBUG → Windows → Call stack

#### Autos
Like watch but with an automatic list of variables. Visual studio detects which variables you might be interested in based on where you are in the code.

#### Locals
Like Autos but with a local scope.

### Debugging useful tips

#### Create JSON From Object During Debugging
Type the following in the Immediate window to get a JSON string:

`Newtonsoft.Json.JsonConvert.SerializeObject(obj)`

#### Unhelpful exception message
##### Option 1
Whenever you are facing hard bugs and get exceptions that don't really make sense or relate to your actual problem you can modify the exception sensitivity and get more exceptions:

Debug --> Window --> Exception Settings

Under "Common Language Runtime Exceptions", enable all exceptions.

##### Option 2
Search in Windows for "Event Viewer" -> Windows Logs -> Application.

Sometimes you can find extra information there if you cannot find any logs or crashes when debugging.

#### Debugging tests
Set a breakpoint in the test, then go into Test Explorer and rightclick and select ”Debug Selected Tests”.

## Common issues

### Resharper not working properly
Sometimes Resharper complains even if there are no errors, try these things to solve it:

#### Restart Visual Studio
Restarting Visual Studio does the trick most of the time.

#### Clear cache and restart resharper
In menu, ReSharper > Options > Environment > General > Clear Caches 

and disabling and re-enabling ReSharper:

In menu, Tools > Options > ReSharper > General > Suspend / Restore

#### Delete .vs folder
Try to delete the .vs folder and then run Clean + Rebuild.

### Tests not running
This could depend on a few different things, one could be that the app.config contains dependentassemblies with multiple definitions.

## General tips

### Upgrading .NET version
1. Go into your projects' properties and change target framework version to whatever you want.

2. Run `Update-Package` or `Update-Package -reinstall` to update/reinstall all packages in all the projects of the solution. You can also do this process for only certain projects or choose to only reinstall the packages with the *requireReinstallation="true"* attribute by going over them one by one.

