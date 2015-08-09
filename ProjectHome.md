# PlantUML File Watcher project #

Build for the Windows platform, a quick and dirty tool for giving almost instant visualisations of the changes to your PlantUML diagrams.

Requires a working PlantUML scripting environment to be able to run.

## Installation ##
Installs in a few steps:
  1. Make sure you have a working environment for compiling PlantUML text files into diagrams  using the command line option as described at the PlantUML home page: http://plantuml.sourceforge.net/command_line.html
  1. Download and unzip the latest file from the [Google Drive](https://drive.google.com/folderview?id=0B1d6azjfUdTWVnBFWDU1SU4tTFk&usp=sharing#list). Please notice that the download section has been deprecated, hence the redirection to Google Drive.
  1. Alter the `PlantUMLFileWatcher.exe.config` file, so that `PlantUML` and `JavaExecutable` points to the required files. Standard values are:
```
 <appSettings>
    <add key="PlantUML" value="C:\Program Files\PlantUML\plantuml.jar" />
    <add key="JavaExecutable" value="C:\Program Files (x86)\Java\jre7\bin\java.exe" />
    ...
  </appSettings>
```
  1. Double click that PlantUMLFileWatcher.exe file and you are good to go!

May require that you have .NET framework v3.5 installed.

### A note on installing the PlantUML environment ###
Read the [PlantUML project website](http://plantuml.sourceforge.net) for a full description.

Basically it boils down to:
  1. Do you have java installed? Requires at least java 1.5: http://java.com
  1. Do you have Graphviz installed? Requires the latest version: http://www.graphviz.org/
  1. Have you downloaded the plantuml.jar file? http://plantuml.sourceforge.net/download.html

Then you should be set to go.

## Usage ##
Usage is very simple.
  1. Launch the application (after the initial setup as stated above)
  1. Open a PlantUML text (`*`.uml or `*`.txt) file using the button on the form or clicking the menu item.
  1. Wait while the image is being rendered.
  1. While having the file opened in PlantUML File Watcher, alter the text source using your favorite text file editing tool (for example [Notepad++](http://notepad-plus-plus.org/)).
  1. Whenever you save a new version PlantUML File Watcher automatically detects the changes and refresh the compiled image representation that is presented to you.
  1. When done, save your work as a PNG file via the menu.

## Compile the code ##
If you want to use the code, then a few remarks on the environment it was created on.

The code are in C#, and is developed using Visual Studio 2008. It should be possible  to upgrade the solution file to a later version of Visual Studio.

The code was compiled against .NET framework 3.5.

## Disclaimner ##
The code and binaries are made available for the public 'as is', and with absolutely no warranty at all.

**USE AT YOUR OWN RISK**

The owner or any participants of this project cannot be hold accountable for any damages, or inconveniences what so ever that may follow using this software.

This project have only been tested on a Windows 7 (64-bit) machine, and comes with no guarantee that it will operate on any other configurations.