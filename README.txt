audio_ssdt_enabler
============
OS X Realtek ALC885 through ALC1150 Onboard Audio

hdae/ssdt installed with a Patched AppleHDA.kext enables OS X Realtek ALC onboard audio on Intel based motherboards with a bootable clean install of OS X. ssdt-hdae-1 injects Audio_ID = 1,  ssdt-hdae-2 injects Audio_ID = 2 and ssdt-hdae-12 injects Audio_ID = 12 for non-DSDT systems

In ML, ssdt-hdae-1 supports 
1. Audio_ID: 1 for 3,  5 and 6 port Realtek ALC onboard audio
2. Realtek audio codecs: ALC885, ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

In ML, ssdt-hdae-2 supports 
1. Audio_ID: 2 for 3 port (5.1) Realtek ALC onboard audio
2. Realtek audio codecs: ALC887, ALC888, ALC889, ALC892, ALC898, ALC1150

In ML, ssdt-hdae-12 supports 
1. Audio_ID: 12 for other IM AppleHDA.kext solutions using layout12

Download
1. https://github.com/toleda/audio_ssdt_enabler
2. Select: audio_ssdt-hdae-1.zip, audio_ssdt-hdae-2.zip or audio_ssdt-hdae-12.zip
3. Select: View Raw
4. Select: Save as .zip

Installation
1. Copy Downloads/audio_ssdt-hdmi.. . ./SSDT-1.aml to Extra
1a. If Extra/SSDT.aml is present, install SSDT-1.aml as is: Extra/SSDT-1.aml
1b. If no Extra/SSDT.aml, rename SSDT-1.aml to SSDT.aml and install as: Extra/SSDT.aml
1c. The 1st SSDT is SSDT, 2nd is SSDT-1, 3rd is SSDT-2, etc.; no gaps
2. Enable SSDT (Chameleon/Chimera - DropSSDT, Clover - DropOem)
3. Rebuild kernel cache
4. Restart

Troubleshooting
1. ML-Patched ALC AppleHDA Capabilities.pdf https://github.com/toleda/audio_ALCInjection
2. Post to http://www.insanelymac.com/forum/topic/290796-realtek-alc-applehda-audio-injection/
3. Post to http://www.tonymacx86.com/audio/76309-mountain-lion-multibeast-no-audio-solutions-problem-reporting.html

Credit
bcc9 http://www.insanelymac.com/forum/topic/290783-intel-hd-graphics-4600-haswell-working-displayport/?p=1934889
PikeRAlpha https://pikeralpha.wordpress.com/2013/06/16/intel-hd4600-with-full-resolution/

toleda
https://github.com/toleda/audio_ssdt_enabler
audio_ssdt-hdae-1.zip
audio_ssdt-hdae-2.zip
audio_ssdt-hdae-12.zip
README.txt