## Removing the pin icon in Windows Explorer quick access

### <sub><sup>*You should probably backup `C:\Windows\SystemResources\imageres.dll.mun` before continuing*</sub></sup>

1. Install [Resource Hacker](http://www.angusj.com/resourcehacker/)
2. Take control of `C:\Windows\SystemResources\imageres.dll.mun`:
    1. Open `cmd.exe` with administrator
    2. `cd C:\Windows\SystemResources`
    3. `takeown /f "%cd%" /r /d y`
    4. `icacls "%cd%" /grant Everyone:(OI)(CI)F /t /q`
3. Download a [transparent icon](https://raw.githubusercontent.com/st0rmw1ndz/st0rmw1ndz.github.io/guides/assets/blank.ico)
4. Go into Resource Hacker and open `C:\Windows\SystemResources\imageres.dll.mun`
5. Click on **Icon Group**
6. Find **5100:1033**
7. Select the icon and use **Ctrl+R** to replace
8. Select the transparent icon
9. Use **Ctrl+S** to save