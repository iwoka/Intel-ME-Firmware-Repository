### Intel ME Firmware Repository

The project is a mirror from [Station-Drivers](https://www.station-drivers.com/index.php?option=com_remository&Itemid=352&func=select&id=105&lang=fr) and [Win-RAID](https://www.win-raid.com/t832f39-Intel-Engine-Firmware-Repositories.html). 


### Why was the project created?

- Intel does not (_often_) releases updates or their updates are difficult to find and they in general prefer to fix problems for OEM's first which means they get fixes first.
- I'm _usually faster in uploading files.
- I prefer _reliable_ hosters like GitHub, GitLab over Mega.nz & Station-Drivers (_sorry ST!_).
- Better versions tracking & control. If there is a changelog I try to provide them and mention them.
- Other people can submit their findings via pull request(s), which makes it easier to stay up-2-date.
- I'm a reliable person, I do not have any intentions to infect someone.


### How can be verify that the files are not manipulated?

You **can not**, because no uploader (incl. myself) has something to compare against, the files are _ripped_ (dumped) from OEM PC's and other places, re-named and re-labeled which makes it impossible to verify or at least pretty hard. Even if you get or rip the pre-installed firmware yourself you couldn't verify it because Intel or the OEM where you took the files don't release any source code or providing up-2-date binaries (_in most cases_).

However, I test every single upload myself and flash them myself (even if I don't use ME, I still have one Intel test PC and one intel test Laptop). You simply have to believe me that these are clean dumps, _I guarantee_ that I did not altered the files and that they are untouched, I do not have any interest, intention or do I make money with this repo, so there is no reason to doubt my words, however you could still inspect the files yourself with any hex editor and report your findings.


### Versions Tag

I follow the same guidelines [plutomaniac](https://www.win-raid.com/t832f39-Intel-Engine-Firmware-Repositories.html) does. 

```
- Every Engine firmware version tag has a Major, Minor, Hotfix & Build number. Example: ME 8.1.40.1416 has Major 8, Minor 1, Hotfix 40 and Build 1416.
- Every PMC firmware version tag has only a Build number. Example: PMC 300.2.11.1011 has Build 1011.
- The SKU of each firmware, when applicable, depends on the platform generation and is usually distinguished based on supported features (Consumer H/LP/1.5MB, Corporate H/LP/5MB etc).
- The Revision is the PCH stepping of a given platform generation and is used to further categorize CSE & PMC firmware (C, D, B etc).
- The Release of each firmware can be Production (PRD), Pre-Production (PRE) or ROM-Bypass (BYP). You could see these as Stable, Debug & Alpha but there's a lot more to it than that. Only Production (PRD) Engine & PMC firmware based on Production PCH Steppings are included in these repositories.
- The Type of each firmware can be Stock Region (RGN), Extracted Region (EXTR) or FWUpdate Image (UPD). RGN are clean/stock/unconfigured images provided by Intel to OEMs. EXTR are dirty/extracted/configured images from various SPI/BIOS. UPD are partial RGN/EXTR firmware regions which contain only ME CODE without any DATA, used only by Intel FWUpdate tool. To learn more, read Section B of the Intel Management Engine: Drivers, Firmware & System Tools.

There is a certain mentality which is followed in order to structure the Engine & PMC firmware repository properly:

- Every Engine firmware filename follows the structure Major.Minor.Hotfix.Build_SKU_Revision_Release_Type and has a .bin extension. CSME 11 PCH-LP additionally has a PDM entry. Example: 11.0.0.1180_CON_LP_C_NPDM_PRD_RGN.
- Every PMC firmware filename follows the structure PCH-Name_PCH-Series.PCH-SKU.PCH-Revision.Build_SKU_Revision_Release_Type and has a .bin extension. Example: CNP_300.2.11.1011_H_B_PRD.
- When it comes to Engine Region images (RGN/EXTR), Stock (RGN) ones are more important that EXTR. ME Analyzer can detect that as well.

```


### License

The project has no license because the files are taken from several places. I see this as a community based effort to provide Intel ME Security fixes by flashing the new firmware's from _trusted persons_.