# Knowledge Base Article - Sample 3

[Return to Knowledge Base Samples](overview.html)

---

## Using Rivet Killer Network Cards

[Killer](https://www.killernetworking.com) network cards (made by [Rivet Networks](https://www.rivetnetworks.com)) require special configuration to work with High Fidelity. If not configured, the cards can accept data from Interface, but fail to write it to the network for several seconds. This may result in a frozen avatar or loss of audio; in other cases, you may be temporarily disconnected from the domain.

> NOTE: Killer Network cards come with a software that limits bandwidth to some applications, controls priority between applications, and allows some applications to use multiple cards at once.  You MUST be running the latest version of this controlling software, the Killer Control Center.
> 
> If you are running the older version (Killer Network Manager), then you may need help from Rivet to remove and update it. This software is no longer supported and all support pages have been removed. 

To configure a Killer network card:

1. Ensure you have the most current version of the [Killer Control Center](https://support.killernetworking.com). To perform a clean install, go [here](https://support.killernetworking.com/knowledge-base/clean-install-killer-control-center).
2. Open HQ Launcher. 
3. Open the Killer Control Center (search Windows for "killer control center").
4. In the left column, click 'Apps' and locate the row for 'interface.exe'.
5. Change the priority for interface.exe to "1 Highest".
6. If there are other apps set to "1", we recommend changing them to "2".
7. Ensure that there are no limit sliders for 'Download Speed' or 'Upload Speed'.
8. Close Killer Control Center.

