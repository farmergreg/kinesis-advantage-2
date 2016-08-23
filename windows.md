#Windows 8/10

There are a couple of potential “gotchas” with creating and direct editing hotkey layouts on 
Windows 8 and 10. Hopefully these issues will be addressed in future firmware versions but
for now, here are some guidelines when sharing custom layouts and macros:

1. You *CANNOT* just drag and drop a “foreign" .txt file on to the v-drive and rename it either
Qwerty.txt, Dvorak.txt, or an appropriate hotkey layout name. The keyboard has to initially
create all .txt layout files via the onboard programming shortcut (Program + F2).
2. Once the keyboard has created a new hotkey layout, that .txt file must be "conditioned" via
any onboard programming command **before it can be direct edited** by accessing the v-drive. The
simplest way to condition a new layout file is to just toggle thumb key modes immediately
after creating it (the layout file to be condition must be active). Then you can access the
v-drive and direct-edit the hotkey layout file or cut and paste another person's remaps/macros
as normal.
