Get-WinUserLanguageList

https://learn.microsoft.com/en-us/powershell/module/international/set-windefaultinputmethodoverride?view=windowsserver2022-ps
---

PS C:\Users\jose_> Get-WinUserLanguageList

LanguageTag     : en-US
Autonym         : English (United States)
EnglishName     : English
LocalizedName   : English (United States)
ScriptName      : Latin
InputMethodTips : {0409:00020409}
Spellchecking   : True
Handwriting     : False


PS C:\Users\jose_> Get-WinUserLanguageList

LanguageTag     : en-US
Autonym         : English (United States)
EnglishName     : English
LocalizedName   : English (United States)
ScriptName      : Latin
InputMethodTips : {0409:00020409}
Spellchecking   : True
Handwriting     : False


PS C:\Users\jose_> (Get-Culture)

LCID             Name             DisplayName
----             ----             -----------
1033             en-US            English (United States)

PS C:\Users\jose_> (Get-Culture).KeyboardLayoutID
1033
PS C:\Users\jose_> (Get-Culture) | FL

Parent                         : en
LCID                           : 1033
KeyboardLayoutId               : 1033
Name                           : en-US
IetfLanguageTag                : en-US
DisplayName                    : English (United States)
NativeName                     : English (United States)
EnglishName                    : English (United States)
TwoLetterISOLanguageName       : en
ThreeLetterISOLanguageName     : eng
ThreeLetterWindowsLanguageName : ENU
CompareInfo                    : CompareInfo - en-US
TextInfo                       : TextInfo - en-US
IsNeutralCulture               : False
CultureTypes                   : SpecificCultures, InstalledWin32Cultures
NumberFormat                   : System.Globalization.NumberFormatInfo
DateTimeFormat                 : System.Globalization.DateTimeFormatInfo
Calendar                       : System.Globalization.GregorianCalendar
OptionalCalendars              : {System.Globalization.GregorianCalendar}
UseUserOverride                : True
IsReadOnly                     : True

---
### Hide searchbar
`https://jdhitsolutions.com/blog/powershell/8424/hiding-taskbar-search-with-powershell/`
Set-ItemProperty -Path HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Search -Name SearchBoxTaskbarMode -Value 0 -Type DWord -Force




Set-ItemProperty -Path HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Search -Name TaskbarDa -Value 0 -Type DWord -Force

### Disable widget bar

New-ItemProperty "HKLM:\Default\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" -Name "TaskbarDa" -Value "0" -PropertyType Dword -Force

### Useful info
https://github.com/Ccmexec/PowerShell/blob/master/Customize%20TaskBar%20and%20Start%20Windows%2011/CustomizeTaskbar.ps1

### Taskbar hacks
https://www.howto-connect.com/registry-hacks-for-start-menu-and-taskbar-in-windows-10/
https://www.makeuseof.com/windows-taskbar-settings-enable-disable/
