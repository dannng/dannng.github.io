---
layout: page
title: Disk Imaging Decision Factors DRAFT
---
This document was written in tandem with the [DANNNG Glossary](../glossary.html). Bolded text indicates that this term is defined (or identified as a synonym of a term) in the glossary.

## Disclaimer
Participation in the development of this document is not intended to imply a recommendation or endorsement by any of the authors or their employers, nor is it intended to imply that any specific software or toolkit is necessarily the best available for the purpose.

## Overview
The purpose of this document is to explore the role of disk imaging in digital archives by addressing assumptions and identifying potential factors that impact decision-making. The digital archives community often focuses on disk images, but that does not mean that all storage devices[1] must be imaged. In fact, while creating and retaining a disk image was once presented as a default action to be taken on most storage devices, organizations now base their processing decisions on a number of factors, many of which we explore in this document.

Disk imaging is seen as more time-consuming and resource-intensive than logical acquisition, but these assumptions do not necessarily hold: there are many factors to consider that implicate post-imaging actions one may wish to take. Likewise, disk imaging can also seem difficult or esoteric. One aim of this document and other outputs of DANNNG (Digital Archival traNsfer, iNgest, and packagiNg Group) is to demystify disk imaging and the decisions that factor into format selection, creation, handling, and retention. We recognize that the technological expertise to work with disk images is not consistently available across organizations collecting digital materials, and we want to create a community-supported resource for those who wish to increase their knowledge and experience.

The document is structured in the following sections:
1. A definition of "disk image."
2. A set of assumptions that we recognized as we were working through these issues, and wanted to make explicit to readers.
3. Factors that, when present, suggest that the creation of a disk image is appropriate or desirable.[2]
4. Factors that, when present, suggest creating a disk image may or may not be appropriate.
5. Factors that, when present, suggest creating a disk image may not be appropriate or desirable.

In our document we have tried to provide guidance on the factors that go into the decision to image or not. The factors involved in deciding to image are often exceptional, so we have provided additional detail in our explanations of them. This is not intended to imply a preference for disk imaging over logical acquisition as a strategy.

## Definition of Disk Image
A disk image (sometimes just "image") is a digital file that is a copy of the readable area of a storage device (or media object), (e.g., hard drive, optical disc, floppy disk). An image replicates the content and structure of the original media object. Content, especially relevant to working hard drives, includes visible files, but also system files, hidden files, and even deleted files; it can include things the user may not realize are saved on their hard drives, such as downloaded email and web browsing history. It may also include unused, empty, or slack space.3 A disk image will be about the same size as the storage device being imaged. There are proprietary and open source tools that can be used to create an image; there are also proprietary and open disk image file formats. A disk image can be "raw," "forensically-packaged," compressed, and/or split up into several files.

## Assumptions
- You are familiar with the concept and uses of a disk image.
- The factors in this document will be applied as document users see fit for their institutions.
- There is a storage device, (e.g., hard drive, optical disc, floppy disk) that can be imaged.
- Not all storage devices need to be imaged, but there are often compelling reasons to do so. The field has been moving away from imaging by default toward doing analysis of storage devices to determine the most appropriate transfer mechanism.
- A storage device may look empty but may not be depending on the system you’re inspecting it on; alternately, you may not be able to see all files present on a storage device.
- Creating a disk image does not imply permanent retention of the disk image.
- The factors in this document are not the only determinants when deciding whether to image a media object. Other determinants that are more specific to the storage device or the repository or local context should be considered and may influence the decision one way or another.
- This document does not recommend specific disk image file formats, (e.g. raw, forensically packaged, compressed). An institution may choose to use different disk image formats for different use cases: for example, a compressed image format may be appropriate where there are concerns over storage availability; an uncompressed image format may be appropriate when emulation is a key access strategy; a forensically-packaged disk image may be appropriate in cases where provenance metadata is important to retain within the disk image file itself.
- There are no “best practices,” just considerations to be evaluated, which may lead to local and accepted practices.
- When choosing not to create a disk image, be aware that you may lose data. Data loss is a reality that archives need to acknowledge and accept, and each institution needs to define its own level of comfort with the risk of irretrievable data loss.
- When choosing to create a disk image, be aware that you may retain sensitive data. Each institution has to define its own level of comfort with the risk of retaining unknown sensitive data, especially if there aren’t sufficient resources to protect that information appropriately. An institution’s risk tolerance should be defined through policies (e.g., for donor agreements and takedown requests) and practices (e.g., appraisal and retention).
- The donor has been made aware of the likelihood of hidden content on storage devices and is capable of making a decision about what content will be kept and/or made publicly available by the repository.4
- Appraising files with donors pre-acquisition may provide guidance about whether to create a disk image or not.
- The considerations in this document assume you or your institution has the available digital storage required to create and/or retain disk image files. For example, you will need 2 TB of storage space to successfully create a disk image of a 2 TB drive.
- Files may contain embedded metadata or information in file headers. File system metadata is not stored within the file itself. Therefore, a logical copy is only guaranteed to preserve file metadata, and creating a disk image is one way to capture certain file system metadata. Retaining file system metadata may be important for certain organizations, specific collections or types of assets (e.g., software) or to support current or future research cases.
- You know -- or have clues that can point you to -- what file systems are contained on your storage device.

## Factors for when to image

### Is the storage device fragile or do you have reason to believe it might be failing?
When storage devices are degrading or failing, imaging may be the most reliable way to successfully capture any of the content on it; at worst, the next read may be the last read, in which case you’ll want the next read to be the imaging process, since you may not know what the media holds. It can sometimes be impossible to know in advance when storage media is headed towards failure, but there are some ways to make a judgement call on this factor.
- Are there noticeable signs of damage to the storage device? (e.g., has the donor reported that their hard drive sounded extremely noisy?)
- Has the storage device been stored in less-than-ideal conditions? (e.g., damp or humid environments, exposure to the elements, etc.)
- If the storage device is an obsolete format, or if it is more than fifteen years old, it is highly likely -- though not guaranteed -- to be fragile.

### Is content otherwise inaccessible on your workstation?
What you see displayed on a processing workstation might not include data you may want to look through and appraise, so imaging the original storage media may create a more comprehensive view of its content as opposed to viewing it through the lens of a different and possibly incompatible environment.5 We have provided some illustrations of differing views of the same content in an appendix to this document.
- A host system running Windows can attach a drive but not mount it if the drive is formatted with a Mac-based file system (e.g., HFS/HFS+/APFS). Windows’ Disk Management tool can detect that something is attached, but Windows cannot assign a drive letter, or read from and write to the drive.6 These drives can still be imaged with a tool like FTK Imager.
- Multiple file systems or partitions may be present on a single piece of media but may not immediately be visible depending on the setup of a processing workstation. Creating a disk image of the media will capture multiple file systems and/or partitions present.
- Certain characters in filenames may make it difficult or impossible to work with in other operating systems, even though the files may be visible. For example, a colon (:) may exist in a Linux filename, but if that volume is later mounted by a Windows host machine, Windows will report an error if the user attempts to take action on the file. Logically copying files with incompatible characters can be time-consuming and require file-by-file remediation; a disk image may be faster to create and may provide information about the file system and encoding to provide a reference for future processing.
- Older media may likely contain legacy file systems, which may be incompatible with contemporary computing environments and for which you may inadvertently lose critical data needed for access unless you image. Legacy and/or different file systems (than the one on your processing workstation) may have features that aren’t visible or supported on the file system on a workstation for archival processing. For instance:
    - Resource forks were used in Mac file systems prior to the mid-1990s (pre-OSX). They were a proprietary data structure for storing images, icons, and code in a structured file format. They were often necessary to run an executable, though any file type may have an associated resource fork.7
    - Older material may contain character encodings that are no longer widely used. Encodings and how bytes are rendered have changed over time, and since the disk imaging process is a byte-for-byte copy of the original media, it will capture the information as it was on the disk, rather than present a current system’s interpretation of the data.
- Older material may contain file formats created by obsolete software. Acquiring a disk image may increase the chance of capturing the appropriate software version or dependencies to read and/or render this material, as these dependencies may be in system folders, possibly outside the scope of a logical copy of a user’s Desktop or home directory.

### Is interactivity a desired function for researchers?
Do you intend, or is it important, that researchers will be able to interact with the media object, whether it be a hard drive, video DVD, software package/application, or something else? If so, creating a surrogate disk image will enable this interactivity.
- Is the goal to provide researchers access to the whole drive as an artifact?
- Do you intend to replicate a working environment, such as that of a donor’s hard drive (i.e., is there an artifactual quality to the disk)?
- If you’re working with a video DVD, will you want a researcher to be able to interact with menus?
- If you’re working with software, do you expect to use disk images for installation or other kinds of replication?
- Do you need a disk image to support the use of the media object and its contents in an emulated environment?


## Factors for maybe imaging
### Is capturing storage device file system features important?
Was the drive used as part of a donor’s work practice and/or used for the creation of records, and is file system metadata important to retain for evidentiary value? Does the media object contain software specifically designed for and compatible with specific hardware? Deciding on which file system metadata and/or features that are important to retain can guide whether imaging is an appropriate pathway. In contrast, if the media object was only used to transfer copies of files to the archive (e.g., the donor purchased or was provided a new drive specifically to transfer documents) you may not need to capture this information, and, consequently, imaging may not be necessary.
- It may be expedient to image a media object to capture file system features, but it may not always be required to do so. If, for instance, only timestamps are important, there are several ways to capture this outside of an imaging workflow.8
- If, for instance, the material is known to contain software, there might be importance to retaining the file system features and/or content captured during imaging, (e.g., NTFS extended attributes, file fragments, resource forks). These may be difficult to capture without imaging.

### Does your workflow require imaging?
There may be reasons to consider imaging for workflow-related reasons. Does your institution's workflow or staffing levels separate acquisition from further appraisal, arrangement, and description? If final decisions about retention, preservation, access, or use are made by different staff members or at a later date, creating a disk image may be the most efficient way to approach the acquisition step. Creating a disk image will also allow you to avoid taking irreversible actions on the content of the media object before making final decisions.
- Does your workflow require a one-to-one correspondence between a digital asset and an original storage device?
- Does your end user access process require disk images (e.g., if you are using BitCurator Access)?
- Does your donor agreement allow for the return of physical carriers to donors? (e.g., media carriers may only be temporarily in your collection while materials are accessioned, giving little to no chance to ever revisit source materials)
- Does the institution want to include in its provenance an audit trail of preservation events9 that start from the “source” of the material (e.g., disk image creation, redaction), and are difficult to document otherwise without a disk image?
- Are you creating disk images for future processing because your institution hasn’t determined processing guidelines or workflow, or you want to retain the capacity for additional processing at a later date?
- Are you unsure whether you may want to have a disk image in the future?
- Are you working with tools to transfer media that require imaging? Some tools may require a disk image to be created first in order to review the contents from the media (e.g., floppy disk imaging tools such as the DeviceSide Floppy FC5025 and the Kryoflux).


## Factors for when not to create a disk image
### Do you have a storage device that you do not need to, or cannot, or (probably) should not image?
- If a storage device was used only for transfer and was not a working drive, it is less likely to have “artifactual value.” While imaging may be required if there are technical issues accessing contents of the drive, the content value is not likely to be a deciding factor.
- Storage media that are compatible and interoperable with current computer operating systems and file systems facilitate more accurate and complete transfer of data. The compatibility of storage media does not guarantee one-to-one transfer, however, so it is important to consider what (if any) file system metadata is important to retain and the most appropriate transfer operation to ensure this information is captured.
    - For instance, if the storage device is an NTFS or exFAT-formatted external hard drive and your processing workstation is a PC running Windows, you are less likely to lose technical metadata in the transfer process since the file system of the storage device and the workstation are compatible.
- Additionally, certain media present challenges when imaging, and the resulting disk images may require additional processing to interpret. Acquiring the content on these media should not be handled by the traditional imaging process.
    - Audio CD10
    - Optical media with multiple sessions11
    - Devices with copy protection that prevent disk imaging

### Have you or your donor/the creator discussed data loss and retention?
- You’ve assessed the risk of data loss and retention to the best of your ability with the donor, if desired or necessary, and are comfortable with the possible outcomes.
- The donor has expressed concern about information they expressly do not wish to be retained in the archive. This may include known and documented types of information, as well as hidden content12 (e.g., file slack, file system information, stored user data like browsing history, deleted files).

### Do you face institutional limitations?
- Storage space to save disk images of large drives, even temporarily, may be at too high a cost.
- Limits to staffing or other crucial resources may make creating or storing disk images (either as an intermediate format or a finalized format) undesirable or unsustainable.
- You are not equipped to store potentially sensitive information that might be present in a disk image, even temporarily. The risk of transferring sensitive information is not eliminated when logically copying files, but depending on your workflow, you might have more control over what gets transferred into your systems with a logical copy operation.

## Appendix
In order to illustrate how various environments and utilities differ in their display of the same content, we have provided the following screenshots using the [Where in the USA is Carmen SanDiego?](https://archive.org/details/Where_in_the_USA_is_Carmen_Sandiego_Broderbund_1998) CD-ROM disk image provided from the [Internet Archive](https://archive.org/).

### CD-ROM disk image in FTK Imager Evidence Tree[13]
![This screenshot shows the disk image as loaded into the program FTK Imager. It is shown to illustrate that there are multiple file system views present, each with differing files present.](/assets/dif-ftk.jpg "Disk image in FTK Imager Evidence Tree")

FTK Imager shows multiple file systems and their respective file listings; notice that they differ slightly.

### CD-ROM disk image displayed in IsoBuster
![This screenshot shows the disk image display in the IsoBuster software. Of note is that the navigation panel on the left displays two different file systems representations -- ISO9660 and HFS -- and there are different files listed under each.](/assets/dif-isobuster1.jpg "Disk image displayed in IsoBuster")
![This screenshot shows a close up view of the navigational panel of the IsoBuster software. The two file systems -- ISO9660 and HFS -- are present, and some of the folders are expanded to further illustrate the differences between the two views.](/assets/dif-isobuster2.jpg "Disk image displayed in IsoBuster - Closeup")

IsoBuster also shows the ISO9660 and HFS file systems, and you can see that the file listings are slightly different in each.

### CD-ROM disk image mounted in Windows 10
![This is a screen capture of the CD-ROM disk image as mounted in a Windows 10 system. This is shown to illustrate that the Macintosh-compatible portion of the disk (which is shown in later examples) is not present at all in this view.](/assets/dif-windows-mounted.jpg "Disk image mounted in Windows 10")

Note that none of the HFS file names show up when this disk image is mounted in a Windows system.

### CD-ROM disk image in Disk Utility on MacOS 10.15
![This screenshot illustrates what happens when you try to open up the disk image using Disk Utility on a Mac. The warning text reads, "The following disk images couldn't be opened." The reason is listed as, "image not recognized."](/assets/dif-macOS-disk-utility.png "Disk image in Disk Utility on a Mac")

Note that MacOS no longer supports the ability to mount an HFS volume in Finder.[14]

### CD-ROM disk image in Disk Image Access Tool in BitCurator (Ubuntu 18.04LTS)
![This screenshot shows the disk image loaded into the Disk Image Access tool from BitCurator. No contents are displayed, and in the Image Info panel, the text reads "No image information found."](/assets/dif-disk-image-access.jpg "Disk image in Disk Image Access Tool in BitCurator (Ubuntu 18.04LTS)")

The Disk Image Access screen in BitCurator is built on top of The Sleuth Kit libraries[15], which does not support reading from HFS volumes. Even though there is an ISO9660 file system present on this disk image, that is not visible with this utility.

### CD-ROM disk image in HFSExplorer in BitCurator (Ubuntu 18.04LTS)
![This screenshot shows the disk image loaded into the HFSExplorer utility. It shows that only Macintosh files, and not the files that are shown in other programs that read ISO9660 filesystems.](/assets/dif-hfsexplorer.jpg "Disk image in HFSExplorer in BitCurator (Ubuntu 18.04LTS)")

HFSExplorer will show the HFS file names of this disk image, but it will not present the user with a list of the ISO9660 file names as they are arranged in that file system view.

### Fiwalk output run against disk image
![This screenshot shows the XML output of the tool fiwalk run against the disk image. Of note are the multiple error lines stating that the utility cannot determine the file system type at various offsets using various sector sizes.](/assets/dif-fiwalk.jpg "Fiwalk output run against disk image")

Fiwalk is also built on The Sleuth Kit libraries, and it is unable to detect any file systems on this disk image on this particular run (with no additional flags).

### mmls output run against disk image
```
    ➜  ~ mmls /Users/mercury_in_retrograde/Where\ in\ the\ USA\ is\ Carmen\ Sandiego\ \(Broderbund\)\(1998\).ISO
    MAC Partition Map
    Offset Sector: 0
    Units are in 512-byte sectors
    
          Slot      Start        End          Length       Description
    000:  -------   0000000000   0000000000   0000000001   Unallocated
    001:  000       0000000001   0000000003   0000000003   Apple_partition_map
    002:  Meta      0000000001   0000000003   0000000003   Table
    003:  001       0000000004   0000000176   0000000173   ISO9660_system
    004:  002       0000000177   0002089859   0002089683   Apple_HFS
```

### disktype output run against disk image
```
    ➜  ~ disktype /Users/mercury_in_retrograde/Where\ in\ the\ USA\ is\ Carmen\ Sandiego\ \(Broderbund\)\(1998\).ISO
    --- /Users/mercury_in_retrograde/Where in the USA is Carmen Sandiego (Broderbund)(1998).ISO
    Regular file, size 623.7 MiB (653965312 bytes)
    No type and creator code
    Apple partition map, 3 entries
    Partition 1: 1.500 KiB (1536 bytes, 3 sectors from 1)
      Type "Apple_partition_map"
    Partition 2: 86.50 KiB (88576 bytes, 173 sectors from 4)
      Type "ISO9660_system"
    Partition 3: 0.996 GiB (1069917696 bytes, 2089683 sectors from 177)
      Type "Apple_HFS"
      HFS file system
        Volume name "Carmen USA 3.5"
        Volume size 0.996 GiB (1069907968 bytes, 65302 blocks of 16 KiB)
    ISO9660 file system
      Volume name "CS_USA"
      Preparer    "OMI QUICKTOPIX 2.20"
      Data size 88 KiB (90112 bytes, 44 blocks of 2 KiB)
```

## Endnotes
1 Terms that may be used interchangeably here include digital object, digital asset, media object, carrier.

2 This section was influenced by the [four factor test](https://www.copyright.gov/fair-use/more-info.html) for [evaluating fair use exceptions to copyright](https://fairuse.stanford.edu/overview/fair-use/four-factors/).

3 It is also possible to transfer “hidden” files and folders through a logical copy, and individual files themselves may contain data that a donor might not realize are accessible (e.g., creator metadata in a PDF; tracked changes in a Word document).

4 For a more nuanced exploration, see [Balancing Care and Authenticity in Digital Collections](https://journals.litwinbooks.com/index.php/jclis/article/view/125).

5 Tools used to view and analyze disk images may not support all possible file systems, as well, though.

6 There is specific paid software that will allow one to read/write to disks meant for other systems, such as [MacDrive](https://www.macdrive.com/) and [Microsoft NTFS for Mac](https://www.paragon-software.com/us/home/ntfs-mac).

7 QuickTime movies are one type of file that often had resource forks, and may not work when transferred to a filesystem that does not support resource forks. See the explanation referenced in [Missing Resource Fork](https://aeroquartet.com/treasured/missing%20resource%20fork.en.html).

8 For instance, one may use a write-blocker (or use another read-only technique) and run [walk_to_dfxml.py](https://github.com/simsong/dfxml/blob/master/python/walk_to_dfxml.py) to generate [Digital Forensics XML (DFXML)](https://github.com/simsong/dfxml/) from a directory, which will record timestamp information in metadata for select directories and files. One can transfer files on the command line using commands such as [rsync](https://ss64.com/bash/rsync.html) or [cp](https://ss64.com/bash/cp.html) with flags to preserve attributes like timestamps at the destination for the files themselves.

9 This can either refer to actions specifically defined by the [PREMIS events controlled vocabulary](https://www.loc.gov/standards/premis/v3/preservation-events.pdf) or to more general digital preservation activities.

10 For audio CDs, transforming digital audio into files readable on a computer is known as digital audio extraction. See the [Wikipedia page on CD rippers](https://en.wikipedia.org/wiki/CD_ripper) for an overview and list of software suitable for this purpose.

11 See the [Wikipedia page on sessions on optical discs](https://en.wikipedia.org/wiki/Track_(optical_disc)#Sessions), [An Introduction to Optical Media Preservation](https://journal.code4lib.org/articles/9581), and [An Optical Media Preservation Strategy for New York University’s Fales Library & Special Collections](https://archive.nyu.edu/handle/2451/43877) and [its appendices](https://archive.nyu.edu/handle/2451/43876) for more information.

12 For example, a donor may not want any information related to their children included, and so took the step to delete such files, not realizing that the information may still be retrievable.

13 Note about FTK Imager: The [digital archives community has discussed the ethical implications of using software outside of their original contexts](https://bitcuratorconsortium.org/bitcurator-consortium-roundtable-practice-values-situating-digital-forensics-tools-in-archives/). We are including a screenshot of FTK Imager here because it is currently in use by library and archives professionals in their workflows and since the interface will be familiar to them, it will provide a way to contextualize the display of the contents of this disk image.

14 See the [History section of the HFS Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_File_System#History) entry.

15 See [HFS on the Sleuth Kit wiki](https://wiki.sleuthkit.org/index.php?title=HFS).

## Acknowledgements
The following people contributed to this document:
- Laura Alagna, Northwestern University
- Alex Chassanoff, North Carolina Central University
- Dianne Dietrich, Cornell University Library
- Brian Dietz, NC State University Libraries
- farrell, Duke University Libraries
- Lara Friedman-Shedlov, University of Minnesota
- Shira Peltzman, UCLA Library
- Tracy Popp, University Library, University of Illinois Urbana-Champaign
- Elise Tanner, UA Little Rock Center for Arkansas History and Culture
- Valerie Waldron, University of Michigan Library
- Paige Walker, Tisch Library, Tufts University
- Lauren Work, University of Virginia Library

We are grateful for the feedback from the members of the community that shaped this and previous versions of the document.
