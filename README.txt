audio_ssdt_enabler
============
OS X Realtek ALC885 through ALC150 Onboard Audio

hdae/ssdt installed with a Patched AppleHDA.kext enables OS X Realtek ALC onboard audio on Intel based motherboards with a bootable clean install of OS X. ssdt-hdae-1 injects Audio_ID = 1,  ssdt-hdae-2 injects Audio_ID = 2 and ssdt-hdae-12 injects Audio_ID = 12 for native DSDT systems with HDEF.  For native DSDT systems without HDEF, use audio_ssdt-no_hdef-hdae-1 or audio_ssdt-no_hdef-hdae-2.

Verify IOReg/Search: @1B: two choices, 1. With HDEF or 2. Without HDEF 

For dsdts with HDEF (IOReg/HDEF@1B)

ssdt-hdae-1 supports 
1. Audio_ID: 1 for 3,  5 and 6 port Realtek ALC onboard audio
2. Realtek audio codecs: ALC885, ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

ssdt-hdae-2 supports 
1. Audio_ID: 2 for 3 port (5.1) Realtek ALC onboard audio
2. Realtek audio codecs: ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

ssdt-hdae-12 supports 
1. Audio_ID: 12 for other IM AppleHDA.kext solutions using layout12

For dsdts without HDEF (IOReg/pci8068,xxxx@1B, ex, xxxx=3b56)

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
Copy Download/audio_ssdt.../SSDT-1.aml to Extra
1. If Extra/SSDT.aml is present, install Downloads/audio_ssdt.../SSDT-1.aml  as Extra/SSDT-1.aml
2. If no Extra/SSDT.aml, rename Downloads/audio_ssdt..../SSDT-1.aml to SSDT.aml and install as Extra/SSDT.aml
3. The 1st SSDT is SSDT.aml, 2nd is SSDT-1.aml, 3rd is SSDT-2.aml, etc.; no gaps

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