Some elements I've discovered:

- Button.*: The rest of the buttons on the screen.
- Button.default.*: The default button in a group of buttons.
- ComboBox.background: the color of the drop down part of the combo box.
- ComboBoxButton.*: Attributes of a combo box that looks like a button, like
  the run configuration drop down on the toolbar.
- Component.borderColor: The outline of drop down menus and search fields.
- Menu.separatorColor: The horizontal lines between menu items.
- MenuBar.borderColor: The bottom separator of the menu.
- NavBar.borderColor: The top separator of the NavBar (file breadcrumb), or the
  bottom of the toolbar.
- Separator.separatorColor: The vertical separators between icon groups in the
  toolbar.

To Change the editor pane's scrollbar:
1. Go to Preferences, then Editor -> Color Scheme.
2. Export the scheme as an icls file.
3. Edit the file.  Look for the "Scrollbar" options and change the following
  colors to what you want.  Note the last 2 digits indicate transparency:
```
    <option name="ScrollBar.Transparent.thumbColor" value="535353BE"/>
    <option name="ScrollBar.Transparent.hoverThumbColor" value="636363BE"/>
```
4. Go back to Preferences, Editor -> Color Scheme and import the modified file.

http://www.jetbrains.org/intellij/sdk/docs/reference_guide/ui_themes/themes_extras.html#customizing-editor-scroll-bar-colors

To change the Editor Scheme in the UI Theme, edit the sceme's XML file.  However
Locally imported schemes will override whatever is in the theme.  To fix this,
Go to Preferences -> Editor -> Color Scheme.  If the theme name shows up, and 
it is not in bold, you will need to delete the scheme and re-apply the theme
plugin to get the colors to take.

TODO
====

- The color of the background in the preference pane.