# VBA Curve Tracer

Note:
When you order boards, make sure you select the black color for the Face Plate and the Back plate, otherwise you will get the default color and that may be green.
Read the important item below about ordering PCB's.

IMPORTANT:
Read the installation instructions for the Front board and the Main board carefully before installing parts.
 
As some of you may know already, designing something is bliss, manufacturing is hell. Especially after some time because things have a habit of changing.
Keep an eye out to newer revision numbers of the BOM's. I have added the partnumbers other users recommended because we either made a mistake in the ordernumber, or the part is no longer available. These alternatives are listed as suggestions. We cannot keep track of this ourselves but appreciate it if you can point out where there are partnumber issues so others can benefit.

Maker Matt Web and maker Cory Lytle have spend a lot of time correcting BOM partnumber errors and installation instructions. Thank you Matt & Cory!

Based on a suggestion from Cory, we have made a small change to the silkscreen of the Front Panel to make the Y-amplifier gain setting more obvious. The is reflected in file FrontPanelRev2b-Display.png.
It replaces the original one, bit since it's only this small change, I left all the other information intact. When you use the Gerber information, it has the change.

---------------------------------------------------------------------------------------------------

This is a repository to hold all files related to the VBA Curve Tracer project. With this information you can build one yourself.
Note that newer versions of files will overwrite the existing ones, there will be no version control. Look at the upload dates for more information.

---------------------------------------------------------------------------------------------------
Here is a note about issues that may come up when you're ordering boards.
Note that we have not heard about unresolved issues when you order through PCBWay. (look at the shared projects on their site and search for VBA to get access to all four boards)
The response below was a result of questions by the engineers of JLCPCB: (more info can be found in the Comment section of the Blog)

Mark, who was the EDA specialist in our team, designed the schematics and the PCB layouts. He used Altium, because his University has a full license.
He is the sole keeper of the EDA information.

This is what Mark replied to the issue:
I went back to look at the gerber files as they were distributed. At that time I was putting the board outline on every gerber plot. The Keepout layer was used for the cutouts in the inner parts of the board not the board outline or to keep copper out of certain areas of the board which is the intended use of this layer. This never has a use as a gerber file unless you are faking the keepout layer as a board outline layer. There is a keepout layer for the front panel PCB since it has the two rectangular connectors on it for holding the DUTs. Some manufacturers use the keepout layer to indicate internal holes. This is not the intended use of the layer either. I have encountered several different uses of the various gerber layers. You have to decide with the board manufacturer what they want to use as the board outline correctly or incorrectly. At the time when I made 10 systems, PCBWAY was allowing the board outline to be on all layers and not the keepout layer. I have had discussions more recently with PCBWAY. Among other things I got complaints about line thickness used for the lines depicting the board outline. So I decided to use the more industry standard of the .GM board outline gerber file. It uses 0 thickness lines for the board outline. Altium has this built into the design package so it was fairly easy to do. I no longer give a keepout layer unless there are internal "holes" on the PCB and that is how they want it indicated. In the description file I send with every PCB order I tell them exactly what the keepout layer is showing. I don't give it when there are no holes. The GM layer could also show the internal holes but I haven't needed to have any newer PCBs manufactured with them. Unfortunately I also get asked about the keepout layer when it is included on a board where the copper is supposed to be kept out. (This is the correct use of this layer). So no more keepout layer to the board manufacturer. The keepout layer is used by the PCB program to keep copper off a layer in a certain region. The gerber files never need to know this as the copper layer file will not have the copper in those regions already. So after all that verbal diarrhea can you tell me what they really want to indicate what the PCB outlines are. If they insist on using the incorrect keepout layer than I can send you some. If they will use the correct GM layer than I will send you some. The gerber layers JLPCB has, all have board outlines on every gerber layer. If you want to come up with a scheme that works for them, you need to let me know what it is and I will make that layer for you. I assume since the keepout layer was included on the front panel you don't need that one as long as JLPCB knows it isn't a board outline but the outline plus internal cutouts. You can create an issue on this Github site, add it as a comment on the Blog, or send the info directly via email if you prefer that. allie@wisc.edu.

--------------------------------------------------------------------------------------------------
There are four different Blogs that I created for this project.
The original posting with a description of the Theory of Operation for the CT and the building of my first version, a working prototype.

http://www.paulvdiyblogs.net/2017/12/building-curve-tracer.html

A few years later, a PCB layout has been developed using mostly SMD parts by Mark Allie. The Blog that covers the Version 2 can be found here:

http://www.paulvdiyblogs.net/2021/03/building-curve-tracer-v2.html

Some of the development process of the VBA Curve Tracer (Version 3) with the help from Mark Allie and Bud Bennet can be found here:

http://www.paulvdiyblogs.net/2021/03/building-curve-tracer-version-3.html

The information about the final instrument for a DIY build can be found here:

https://www.paulvdiyblogs.net/2022/06/the-vba-curve-tracer.html

I also created a blog post with several measurements that were made with the VBA Curve Tracer.

https://www.paulvdiyblogs.net/2021/11/making-meassurements-with-v3-curve.html

Enjoy!
