# LibreOffice-dictionaries
Ready-to-install dictionary extensions from https://github.com/LibreOffice/dictionaries

## To recreate:
- Install [7-Zip](https://www.7-zip.org/)
- Run the following as a batch script
```
for /d %%X in (*) do "c:\Program Files\7-Zip\7z.exe" a "%%X.zip" ".\%%X\*"
```
- Open a PowerShell window in the same directory and run
```
get-childitem *.* |  foreach {rename-item $_ $_.name.replace("zip","oxt")}
```
