This is an attempt to make Intellij products look like they did before they
dropped the GTK theme in 2018.3.  It won't actually get colors from the GTK
theme, but uses the same colors I like to use in my GTK theme.

http://www.jetbrains.org/intellij/sdk/docs/reference_guide/ui_themes/themes_customize.html
is a good place to start for information on how to customize the UI.

Highlights:

To enable internal mode:
Go to Help | Edit Custom Properties.  Add `idea.is.internal=true` to the file
that gets opened.  Restart Idea

To open the UI inspector panel:
Tools | Internal Actions | UI | UI Inspector.  Then Ctrl-Alt-Click to open.
To open the LaF panel:
Tools | Internal Actions | UI | LaF Defaults

To build and install:
1. Build
2. Build | Prepare Plugin Module <module name> for Deployment
3. Go to plugins. Click the gear and choose "Install from file".
4. Choose the file.
5. Restart and choose the theme.
6. If the font is too big, look at the font in the Theme's XML file, then go
  to Settings | Editor | Color Scheme | Color Scheme Font and make sure the 
  font and size are correct.