This is an attempt to make Intellij products look like they did before they dropped the GTK theme
in 2018.3.  It won't actually get colors from the GTK theme, but uses the same colors I like to use
in my GTK theme.

http://www.jetbrains.org/intellij/sdk/docs/reference_guide/ui_themes/themes_customize.html
is a good place to start for information on how to customize the UI.

Highlights:

To enable internal mode:
Go to Help | Edit Custom Properties.  Add `idea.is.internal=true` to the file that gets opened.
Restart Idea

To open the UI inspector panel:
Tools | Internal Actions | UI | UI Inspector.  Or Ctrl-Alt-Click on an element to open the inspector
on the element that was clicked.

To open the LaF panel:
Tools | Internal Actions | UI | LaF Defaults

To build and install:
1. Ensure that the Plugin DevKit is installed from the plugin marketplace.
2. Build
3. Build | Prepare Plugin Module <module name> for Deployment
4. Go to plugins. Click the gear and choose "Install from file".
5. Choose the file.
6. Restart and choose the theme.
7. If the font is too big, look at the font in the Theme's XML file, then go
  to Settings | Editor | Color Scheme | Color Scheme Font and make sure the 
  font and size are correct.

Todo
----

1. The inlay foreground color doesn't seem to have the effect we want.