Install Drivers for I211 on Windows Server
#VEN_8086-DEV_1539

Source Guide: https://blog.citrix24.com/install-windows-server-2016-core-intel-nuc/

bcdedit /set LOADOPTIONS DISABLE_INTEGRITY_CHECKS

bcdedit /set TESTSIGNING ON

bcdedit /set NOINTEGRITYCHECKS ON


reboot

pnputil -i -a "path\*.inf"

#accept prompt

#revert

bcdedit /set LOADOPTIONS ENABLE_INTEGRITY_CHECKS
bcdedit /set TESTSIGNING OFF
bcdedit /set NOINTEGRITYCHECKS OFF

reboot
