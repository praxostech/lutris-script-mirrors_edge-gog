# Lutris Mirror´s Edge (GOG) installation script

A Lutris script for installing Mirror´s Edge (GOG).


## Prerequisites
* NVIDIA PhysX Legacy (9.13.0604)
* NVIDIA PhysX (9.17.0524)
* DirectX 9.0c
* Visual C++ Redist 2005

All prerequisites get installed by the GOG-Installer

## Supported Locales
The language-settings can be configured by changing the registry value "Locale" in:   
"HKEY_LOCAL_MACHINE\SOFTWARE\EA GAMES\Mirror's Edge".   
It defines the language of the menu, audio and subtitles.     
You can retrieve the correct value for your preferred language from the table down below.   
**Note:** Some audio localization may not be available for your language, visit [this page](https://www.pcgamingwiki.com/wiki/Mirror%27s_Edge#Localizations) for further information.


Language | Locale (Language Code) | Displayed language in setup
-|-|-
Hungarian		          | hu-HU   | magyar
French			          | fr_FR   | Francais
Portuguese	              | pt_PT   | Portugues
Spanish			          | es_ES   | Español
Korean			          | ko_KR   | Korean
Chinese (Traditional)	  | zh_TW   | Chinese (Traditional)
Italian			          | it_IT   | Italiano
Russian			          | ru_RU   | Pусский
German			          | de_DE   | Deutsch
Japanese		          | jp_JP   | Japanese
Czech			          | cs      | Cestina
Polish			          | pl_PL   | Polski
English (UK)		      | en_UK   | English




## Mirror´s Edge GOG setup - silent
The required commandline flags are "/VERYSILENT /SUPPRESSMSGBOXES".   
However, you still have to manually click trough Nvidia Physics setup when it launches during the installation.   
The language setting has to be changed afterwards in the registry because the "/LANG" option does not change the game´s language.   
The setup uses a custom function, which does not recognize the "/LANG" option.

## Prerequisites install commands

File | Arguments
-|-
DXSETUP.exe | /silent
PhysX-9.13.0604-SystemSoftware-Legacy.msi | /passive /norestart
PhysX-9.17.0524-SystemSoftware.exe | -s
vcredist_x86.exe | *The flags were not obtainable from the setup*
