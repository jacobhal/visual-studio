# Visual Studio 2019 Tips and Keyboard Shortcuts

Table of Contents
=================

   * [Visual Studio 2019 Tips and Keyboard Shortcuts](#visual-studio-2019-tips-and-keyboard-shortcuts)
      * [My favourite extensions](#my-favourite-extensions)
         * [Codemaid](#codemaid)
         * [Resharper](#resharper)
         * [Image optimizer](#image-optimizer)
         * [File icons](#file-icons)
         * [File nesting](#file-nesting)
         * [VSColorOutput/Output enhancer](#vscoloroutputoutput-enhancer)
         * [Viasfora](#viasfora)
         * [Object Exporter](#object-exporter)
      * [My favourite keyboard shortcuts](#my-favourite-keyboard-shortcuts)
         * [Basic global shortcuts](#basic-global-shortcuts)
         * [Default Visual Studio](#default-visual-studio)
         * [Codemaid](#codemaid-1)
         * [Resharper](#resharper-1)
      * [My favourite code snippets](#my-favourite-code-snippets)
      * [Running &amp; Debugging](#running--debugging)
         * [Running &amp; Debugging keyboard shortcuts](#running--debugging-keyboard-shortcuts)
         * [Debugging windows](#debugging-windows)
            * [Watch window](#watch-window)
            * [Call stack](#call-stack)
            * [Autos](#autos)
            * [Locals](#locals)
         * [Debugging useful tips](#debugging-useful-tips)
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

### Resharper
Everyone's favourite Visual Studio extension. It is not free but if you are at your workplace, chances are that they have Resharper subscriptions for everyone to use. Resharper provides on-the-fly code inspection, code generation, refactoring, lots of keyboard shortcuts to either use in conjunction with the default Visual Studio keymappings or overriding them and much more.

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

## My favourite keyboard shortcuts

### Basic global shortcuts
* Move selection one tab stop to the right: **Tab**
* Move selection one tab stop to the left: **Shift + Tab**
* Copy/Cut selection or current line: **Ctrl + C / Ctrl + X**
* Select text from cursor position to the end of the line: **Shift + End**
* Select text from cursor position to the beginning of the line: **Shift + Home**
* Jump to beginning of line: **Ctrl + Home**
* Jump to end of line: **Ctrl + End**

### Default Visual Studio
* Code navigation
    * Go to definition of variable/method: **F12**
    * Go to implementation/declaration: **F12**
    * Show all references: **Shift + F12**
    * Go to the last place of the cursor: **Ctrl + -**
    * Go to the last place of the cursor (reverse): **Ctrl + Shift + -**
* Searching
    * Search everywhere/Go to all: **Ctrl T**
    * Go to file: **Ctrl + Shift + T**
    * Search current file: **Ctrl + F**
    * Search entire solution: **Ctrl + Shift + F**
* Editing
    * Move lines up or down: **Alt + Up/Down arrow**
    * Replace in current file: **Ctrl + H**
    * Replace in entire solution: **Ctrl + Shift + H**
* Commenting
    * Comment block: **Ctrl + K, Ctrl + C**
    * Uncomment block: **Ctrl + K, Ctrl + U**
* Formatting
    * Format document: **Ctrl + K + D**
* Expanding/Collapsing
    * Expand/Collapse a code block: **Ctrl + M, Ctrl + M**

### Codemaid
* Go to the current file in project structure: **Ctrl + M, F**
* Cleanup & Format the currrent file: **Ctrl + M, Space**
* Start Codemain Spade (tree view of project with drag and drop): **Ctrl + M, .**
* Reorgnaize methods/fields to follow Microsoft's convention: **Ctrl + M, Z**

### Resharper

## My favourite code snippets
TODO

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

#### Unhelpful exception message
Whenever you are facing hard bugs and get exceptions that don't really make sense or relate to your actual problem you can modify the exception sensitivity and get more exceptions:

Debug --> Window --> Exception Settings

Under "Common Language Runtime Exceptions", enable all exceptions.

#### Debugging tests
Set a breakpoint in the test, then go into Test Explorer and rightclick and select ”Debug Selected Tests”.

## Common issues
Sometimes Resharper complains even if there are no errors, try these things to solve it:

### Restart Visual Studio
Restarting Visual Studio does the trick most of the time.

### Clear cache and restart resharper
In menu, ReSharper > Options > Environment > General > Clear Caches 

and disabling and re-enabling ReSharper:

In menu, Tools > Options > ReSharper > General > Suspend / Restore

### Delete .vs folder
Try to delete the .vs folder and then run Clean + Rebuild.
