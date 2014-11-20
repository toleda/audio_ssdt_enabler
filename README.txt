audio_ssdt_enabler
============
OS X Realtek ALC885 through ALC150 Onboard Audio

Update v2 - Added AZAL to HDEF ssdt, revised installation instructions

hdae/ssdt installed with a patched AppleHDA.kext enables OS X Realtek ALC onboard audio. Native DSDT systems with HDEF,  ssdt-hdae-1 injects Audio_ID = 1,  ssdt-hdae-2 injects Audio_ID = 2 and ssdt-hdae-12 injects Audio_ID = 12. For native DSDT systems with AZAL, use ssdt-azal2hdef-hdae-1. Native DSDT systems without HDEF, use audio_ssdt-no_hdef-hdae-1 or audio_ssdt-no_hdef-hdae-2.

DSDT not required, use IOReg (Download/View Raw and install)
IOReg/Search: @1B
https://github.com/toleda/audio_ALCInjection/blob/master/IORegistryExplorer_v2.1.zip

Verify IOReg/Search: @1B (three choices, select one)
A. With AZAL (IOReg/AZAL@1B)
B. With HDEF (IOReg/HDEF@1B)
C. Without HDEF or AZAL (IOReg/pci8068,xxxx@1B, ex, xxxx=3b56)

A. For dsdts with AZAL (IOReg/AZAL@1B)

ssdt-azal2hdef-hdae-1 supports 
1. Audio_ID: 1 for 3, 5 and 6 port Realtek ALC onboard audio
2. Realtek audio codecs: ALC885, ALC887, ALC888, ALC889, ALC892, ALC898, ALC11

B. For dsdts with HDEF (IOReg/HDEF@1B)

ssdt-hdae-1 supports 
1. Audio_ID: 1 for 3, 5 and 6 port Realtek ALC onboard audio
2. Realtek audio codecs: ALC885, ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

ssdt-hdae-2 supports 
1. Audio_ID: 2 for 3 port (5.1) Realtek ALC onboard audio
2. Realtek audio codecs: ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

ssdt-hdae-12 supports 
1. Audio_ID: 12 for other IM AppleHDA.kext solutions using layout12

C. For dsdts without HDEF (IOReg/pci8068,xxxx@1B, ex, xxxx=3b56)

audio_ssdt-no_hdef-hdae-1 supports 
1. Audio_ID: 1 for 3,  5 and 6 port Realtek ALC onboard audio
2. Realtek audio codecs: ALC885, ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

audio_ssdt-no_hdef-hdae-2 supports 
1. Audio_ID: 2 for 3 port (5.1) Realtek ALC onboard audio
2. Realtek audio codecs: ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

Download
1. https://github.com/toleda/audio_ssdt_enabler
2. Select: audio_ssdt-.....zip
3. Select: Raw Data
4. Select: Save
5. Select: Use .zip (to Save, not .aml)

Installation
1. See [Guide]-audio_ssdt_hdef-installation_v2.pdf (included with ssdt download)

Troubleshooting/Problem Reporting
1. See https://github.com/toleda/audio_ALCInjection/README.txt

Credit
bcc9

toleda
https://github.com/toleda/audio_ssdt_enabler
audio_ssdt-hdae-1.zip
audio_ssdt-hdae-2.zip
audio_ssdt-hdae-12.zip
audio_ssdt-no_hdef-hdae-1.zip
audio_ssdt-no_hdef-hdae-2.zip
README.txt