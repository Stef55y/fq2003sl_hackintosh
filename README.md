# fq2003sl_hackintosh

I always wanted to use macOS, but unfortunately, some Windows apps aren't available on macOS. So why not have both on the same laptop? We'll do something called Hackintoshing, basically installing macOS on unsupported hardware.
(WARNING: This violates Apple’s EULA)


REQUIREMENTS:​

-At least 16GB of RAM (minimum supported is 8GB).

-A USB stick with at least 32GB of storage.

-At least 5GB of SSD space and 1GB free on disk.

-A macOS virtual machine (VMware is recommended — you can get it from their website and follow the setup process).

-A macOS ISO (Mojave 10.13 / Big Sur recommended — download it from the provided link).

-A bit of patience.

WARNING:
There will be no graphics acceleration with the Iris XE; performance will not be optimal.

ACTUAL GUIDE:​
Download the provided EFI folder (already configured with the kexts for our hardware — HP-15sfq2003sl) and place it on the desktop of your main OS.
Insert the USB stick and connect it to the host (the macOS virtual machine).
Open Disk Utility, format the USB stick as Mac OS Extended (Journaled) or APFSdepending on the macOS version you’re installing.
If you chose a version newer than Mojave, use APFS.
Scheme: GUID Partition Map.
Open Terminal and paste the following command:
sudo /Applications/Install\ macOS\ [macOS_version].app/Contents/Resources/createinstallmedia --volume /Volumes/USB Examples:
Mojave → Install\ macOS\ Mojave.app
Catalina → Install\ macOS\ Catalina.app
Big Sur → Install\ macOS\ Big\ Sur.app
Monterey → Install\ macOS\ Monterey.app (reccomended)
Ventura → Install\ macOS\ Ventura.app
(Replace /Volumes/USB with your USB stick name if different.)

Now the installer is ready. Try booting from your USB on your laptop and report what doesn’t work.
