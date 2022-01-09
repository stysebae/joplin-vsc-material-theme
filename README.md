# VSCode [Community Material Themes](https://github.com/material-theme/vsc-material-theme) for Joplin

![screenshots](/screenshots.gif)

These themes are **flat material themes** for newer version (>= 2.x) of Joplin  desktop application. They are **heavily inspired by the color schemes [Community Material Themes](https://github.com/material-theme/vsc-material-theme) for Visual Studio Code**. It's not 100% identical and there are rooms for improvement. Mostly background colors are changed. You can see [Screenshots](#screenshots) section to make your choice among the different themes.

These themes are modified versions of [Joplin Light Theme](https://github.com/LongBay/Joplin-Light-Theme) by [LongBay](https://github.com/LongBay), which is itself originally inspired by [Joplin Clear UI theme](https://github.com/marcteys/joplin-theme-clearUI) by [Marc Teyssier](https://github.com/marcteys). Some tweaks are also coming from the topic (Share your CSS)[https://discourse.joplinapp.org/t/share-your-css/1730] on Joplin's forum.

## Installation

Launch Joplin desktop application: 
- Make sure that **Joplin is using the dark mode** in `Tools > Options > Appearance`
- Go to `Tools > Options > Appearance > Show Advanced Settings`. **Paste the content of `userstyle.css` in** the file opened by clicking on the button **"Custom stylesheet for rendered Markdown"**; **paste the content of `userchrome.css` in** the file opened by clicking on the button "Custom stylesheet for Joplin wide-app styles". Alternatively, you can also clone this repository and create symbolic links to `userchrome.css` and `userstyle.css` inside Joplin configuration folder (e.g. in `~/.config/joplin-desktop` on Linux). `userchrome.css` and `userstyle.css` files can be found in one of the folders of this repository, depending on the theme you would like to install.

## Customization

Notes: 
- Please visit the topic (Share your CSS)[https://discourse.joplinapp.org/t/share-your-css/1730] on Joplin's forum. There are some tweaks you might be interested in.
- For enhanced customization, you can also download and install the plugin (Joplin Rich Markdown)[https://github.com/CalebJohn/joplin-rich-markdown]. Then, enable "Add additional CSS classes for enhanced customization" in the plugin settings (`Tools > Options > Rich Markdown`).

### Changing Colors or Police Fonts

You can easily change the colors or the police fonts by editing the `:root` pseudo-class in both files `userchrome.css` and `userstyle.css`. `:root` defines all color schemes variables used along the CSS files. 

The themes also use by default the following police fonts: `Fira Sans` and `Roboto Mono`. Be sure that these are installed on your computer or change them by modifying `--font-face` and `--font-mono` in `:root` pseudo-class. 

### Show/Hide Joplin's UI Elements

Some buttons are shown or hidden by default. You can browse `userchrome.css` to identify these elements and to hide/show them, by adding `display: none !important;` or by removing it respectively. Here are some examples of such tweaks.

#### Show "All notes" Icon (Sidebar)

By default, this icon is hidden. You can show it by comment or remove the following lines in `userchrome.css`:

```css
/* Hide "All notes" icon */
i.icon-notes {
  display: none !important;
}
```

#### Hide Synchronization Area (Sidebar)

Add `display: none;` to `.sidebar > div:last-of-type` in `userchrome.css`, e.g.:

```css
.sidebar > div:last-of-type {
  display: none; /* Hide the synchronization area */
  background-color: none !important;
}
```

#### Hide the button "New Todo" (Notes List)

If you do not use any todo's with Joplin, you can hide this button by adding the following lines in `userchrome.css`:

```css
div[height="50"] .new-todo-button {
  display: none; /* Hide the button "New todo" */
}
```

## Screenshots

### Community Material Theme

### Community Material Theme High Contrast

### Community Material Theme Darker

### Community Material Theme Darker High Contrast

### Community Material Theme Ocean

### Community Material Theme Ocean High Contrast

### Community Material Theme Palenight

### Community Material Theme Palenight High Contrast