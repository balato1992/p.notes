
[[SOLVED] - Changing Windows boot manager drive | Tom's Hardware Forum (tomshardware.com)](https://forums.tomshardware.com/threads/changing-windows-boot-manager-drive.3571420/)

**diskpart**​
**list disk**​
**select disk 1**​
**list partition**​
**select partition x**​
**shrink desired=500**​
**create partition efi**​
**format fs=fat32 quick**​
**assign letter=H**​
**exit**​
**bcdboot C:\\windows /s H:**
