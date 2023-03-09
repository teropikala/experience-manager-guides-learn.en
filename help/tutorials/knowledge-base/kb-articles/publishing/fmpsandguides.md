---
title: FMPS and AEM Guides 
description: Publishing with FMPS using AEM Guides

---

# FrameMaker Publishing Server (FMPS) and AEM Guides

**AEM Guides integration with FrameMaker Publishing Server could be your solution if you are looking for high-quality automated publishing.  
Below article will help you in setting up and running FMPS with AEM Guides.**

## Compatibility of FMPS with AEM Guides:

-   Compatibility with 4.1 AEM Guides: [Link](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
-   Compatibility with 4.0 AEM Guides: [Link](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
-   Future Release: [Link](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Installation:

### AEM Guides:

Installation and configuration refer: [Link](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS:

For FMPS installation you can refer given [Video link](https://www.youtube.com/watch?v=2deelyM5VA8&t) or [Documentation](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&rhtocid=_2)

## Required Configurations:

Your DITA content can be output using FrameMaker Publishing Server (FMPS). You can create output in any of the many formats that FMPS supports. In the Web Console, modify the following properties of the com.adobe.fmdita.config.ConfigManager bundle to set up AEM Guides to use FMPS.

To open the Web Console, go to the URL Access http://\<server name\>:\<port\>/system/console/configMgr.

**Configuration properties and their description:** [Link](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Running Test:

Using FMPS, you may automatically publish **PDF, Responsive HTML5**, and **Epub** for your DITA and FM Assets.

From the "Generate PDF using" menu, choose FrameMaker Publishing Server.

The user can provide "settings File(.sts)" and "ditaval. Filtering will be done using ditaval based on the conditions you supply.

-   **setting file**: FrameMaker /FMPS Publish setting which contains all those settings which you want FMPS to honor while publishing For example: Generating output with the customized template, Generating Marks and Bleeds(PDF), Generating PDF with TOC, index, etc.
-   **FMPS present:** Pre-defined combination of ditaval and settings file, Instead of giving separate ditaval and settings files, the User can pre-create FMPS preset which can be re-used for publishing needs.

**Note:** If you don’t select any of the settings or FMPS preset then FMPS will publish with the default system setting.

If you have selected FMPS preset and also provided settings/ditaval file from AEM then this will conflict and FMPS preset will be given precedence over custom settings/ditaval file.

### Baseline Publishing using FMPS:

You can Publish your already created baselines with FMPS2020.0.2 or higher version.

**Sample FMPS settings file(.sts file) to get started:** [Link](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (unzip this file)

## FAQ and Troubleshooting:

-   FMPS publishing fails with “Timeout Exception”.

Check and increase the value of “FMPS timeout” (Seconds) in /system/console/configMgr/com.adobe.fmdita.config.ConfigManager”

-   Unable to get FMPS preset in the dropdown.

Make Sure you have a pre-defined FMPS preset created on Server and that your connection settings are correct.

-   I am getting Blank PDFs when publishing.

If you are using UUID then make sure you have checked “Use UUID based referencing” in FrameMaker Edit Preferences and vice versa for non-UUID AEM guides.

-   My settings/ditaval are not getting applied in the final published output.

Make sure you are not selecting both setting/ditaval file and FMPS preset parallelly. Verify output manually using FrameMaker.

-   The baseline not getting published from FMPS.

Baseline publishing is compatible with FMPS2020.0.2 or higher version.  
Make sure your Baseline is created properly, to verify go to Map Dashboard Topic Download Map and select “Use Baseline “.

-   Publish Tasks from FMPS takes more time than other Engines.

There will be an ideal fixed header of approx. 3-4 min only while publishing from FMPS than other Engines, if you think it is more than that then check with your FMPS administrator or Contact Adobe Support.

## Other Resources:

[FMPS Learn and Support](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[AEM Learn and Support](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[FrameMaker and FMPS community](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&sort=latest_replies&lang=all&tabid=all)

[AEM Guides Community](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)