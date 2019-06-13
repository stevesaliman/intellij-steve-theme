Some elements I've discovered:

- ActionButton: buttons in the toolbar.  hover* is when you hover over them, 
  pressed* is when you press them.
- Button.*: The rest of the buttons on the screen.  There are several properties
  in use.  In general, the button has a color, then a 1 pixel "halo" if it is 
  the default button, then a 2 or 3 pixel border.  The startBackground and 
  endBackground define the color of the button itself.  The halo comes from
  default.StartBorderColor and defaultEndBorderColor.  The background defines 
  the border when the button is not selected.  I haven't figured out where the
  border for a selected button comes from yet.
- Button.default.*: The default button in a group of buttons.
- ComboBox.background: the color of the drop down part of the combo box.
- ComboBox.nonEditableBackground: The color of the drop down part of the combo
- ComboBox.ArrowButton.nonEditableBackground: The color of the arrow in the 
  preference pane drop downs.
  box in certain preferences panes.
- ComboBoxButton.*: Attributes of a combo box that looks like a button, like
  the run configuration drop down on the toolbar.
- Component.borderColor: The outline of drop down menus and search fields.
- Component.focusColor: The outline of the currently selected button or input
  field.  This should probably match Component.focusedBorderColor and 
  Button.focusedBorderColor
- FileColor.*: The actual color to render when a color is selected in the 
  Preferences -> Appearance -> File Colors.  They effect the backgrounds of the
  editor tabs and file tree for the types of files mapped to the color.
- Group.separatorColor: The lines that divide sections of a panel like the 
  Preferences -> Appearance -> Appearance screen.
- Menu.separatorColor: The horizontal lines between menu items.
- MenuBar.borderColor: The bottom separator of the menu.
- NavBar.borderColor: The top separator of the NavBar (file breadcrumb), or the
  bottom of the toolbar.
- Popup.separatorColor: Appears to be the separator of the drop down lists.
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

To change the Editor Scheme in the UI Theme, edit the scheme's XML file.  However
Locally imported schemes will override whatever is in the theme.  To fix this,
Go to Preferences -> Editor -> Color Scheme.  If the theme name shows up, and 
it is not in bold, you will need to delete the scheme and re-apply the theme
plugin to get the colors to take.

TODO
====

- The background of the checkbox in the exit menu that asks "Do not show again"
- Checkboxes in preferences - Got the background, not the box itself, which may
  be fine.
- Tooltip slider background in preferences
- Radio buttons in preferences -> system settings.
