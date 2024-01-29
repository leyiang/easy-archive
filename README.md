Sometimes, we might need to copy a file from within a zip archive without actually extracting it. Ideally, an app should extract the file into a temporary folder and then place it in my clipboard. While this feature is readily available and easy to use in Windows, it's not as straightforward in Linux. To meet this need, I developed a short script.

## How to use?

1. Create a desktop file
```shell
# inside ~/.local/share/application/test.desktop

[Desktop Entry]
Exec={path_of_the_script}
Name=Easy Archive
Terminal=true
Type=Application
```

2. Determine mime type for .zip files
```
mimetype {ur_zip_file}

application/zip
```

3. Set default application for .zip files
```
xdg-mime default test.desktop application/zip
```

## Known issues

Copy file to clipboard does not have a universal solution.
