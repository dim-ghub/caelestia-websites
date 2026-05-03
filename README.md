# Firefox Caelestia Setup

## Step 1: Find Your Firefox Profile Directory

In Firefox, go to `about:support` and locate the directory next to **Profile Directory** under the **Application Basics** header.

## Step 2: Copy the Template

Copy `material/websites.css` into `~/.config/caelestia/templates`.

## Step 3: Enable User CSS

Go to `about:config` and enable `toolkit.legacyUserProfileCustomizations.stylesheets`.

## Step 4: Create the Chrome Folder

Inside your Firefox profile directory, create a folder named `chrome`.

## Step 5: Copy the Websites Folder

Copy the `websites` folder into the `chrome` folder you just created.

## Step 6: Create userContent.css

Create a `userContent.css` file inside the `chrome` folder.

### Add the Colors Import

Add this as the first line:

```css
@import url("./colors.css");
```

### Add Website Theme Imports

Add an import line for each website CSS theme you want to have applied. For example:

```css
@import url("./websites/github.css");
```

## Step 7: Refresh Your Wallpaper

Refresh your wallpaper by pressing the super key, then typing >wallpapers. You may either switch to a new wallpaper or reselect the wallpaper youre already using.

Then symlink `~/.local/state/caelestia/theme/websites.css` to `[YOURPROFILEFOLDER]/chrome/colors.css`.

You must also set up a post hook to execute the websites.sh script.

## Step 8: Relaunch Firefox

Relaunch Firefox to apply the changes.
