# Desktop Entries
Guide to creating a desktop entries
(Debian/Gnome DE)

## Template
[Desktop Entry]
Name=Your Application
Comment=An amazing application
Exec=your-application
Icon=com.example.YourApplication
Keywords=various;keywords;describing;your;application;
StartupNotify=true
Terminal=false

## Directions
1. Create desktop entry with the desired program in the `Exec=` path
   Desktop entries on default Gnome desktops should be placed in
   `~/.local/share/applications/yourapp.desktop`
2. make sure both the application and the desktop entry are executable
   `chmod +x`
3. After that update the desktop database (or log out/log back in)
   `update-desktop-database`
4. Verify that your launcher appears in the applications menu
5. (optional) you can right click and pin the launcher to your dash

## Troubleshooting
if the launcher is not showing up in your applications menu, make sure
there are no typos in (especially Exec=) the desktop entry. Make sure
your application is able to launch (try running app without .desktop file)
Make sure to run `chmod +x` and `update-desktop-database`
