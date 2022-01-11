---
layout: page
title: Disk Imaging Decision Factors
---
This document was written in tandem with the [DANNNG Digital Archives Technical Glossary](https://dannng.github.io/digital-archives-technical-glossary). Glossary terms (and synonyms) will be bolded the first time they are introduced in this document.

- [Disclaimer](#disclaimer)
- [Introduction](#introduction)
  * [Definition of Disk Image](#definition-of-disk-image)
  * [Audience](#audience)
  * [Assumptions](#assumptions)
- [Factor: Type or condition of the storage device](#factor-type-or-condition-of-the-storage-device)
- [Factor: Compatibility of the storage device or content](#factor-compatibility-of-the-storage-device-or-content)
- [Factor: Expected access to content](#factor-expected-access-to-content)
- [Factor: Retention of important contextual information](#factor-retention-of-important-contextual-information)
- [Factor: Processing workflow](#factor-processing-workflow)
- [Appendix](#appendix)
- [Endnotes](#endnotes)
- [Acknowledgements](#acknowledgements)

## Disclaimer
Participation in the development of this document is not intended to imply a recommendation or endorsement by any of the authors or their employers, nor is it intended to imply that any specific software or toolkit is necessarily the best available for the purpose.

## Introduction
The purpose of this document and other [outputs of DANNNG](https://dannng.github.io/) (Digital Archival traNsfer, iNgest, and packagiNg Group) is to demystify disk imaging and the decisions that factor into format selection, creation, handling, and retention.

**Disk imaging** was integral to early guidance<sup id="a1">[1](#en1)</sup> for handling storage devices containing born-digital materials. Archivists were encountering digital **media**<sup id="a2">[2](#en2)</sup> formats likely at the end of their working life (e.g., floppy disks, CD-ROMs, ZIP disks, old HDDs), and separating the data from the fragile media was an important first step to protect against data loss. A **disk image** provided an exact copy of the storage device onto a stable system, eliminating the need to continually access (possibly) deteriorating physical media in order to evaluate and appraise its content. Combined with a read-only access technique (on the storage device itself or using a write-blocker), disk imaging emerged as a way to clearly demonstrate **provenance** and assert that no action performed by the archivist had altered or corrupted the content. Workflows and tools developed using the disk image as a unit by which to organize nearly all aspects of a workflow, from **capture** to appraisal and processing, to **retention** and access.

Consequently, the digital archives community often focuses on disk images, but that does not mean that all storage devices must be imaged. In fact, the field has been moving away from imaging by default toward doing analysis of storage devices to determine the most appropriate transfer mechanism. While it was common guidance to create and retain a disk image as a "default" action on storage devices, organizations now increasingly base their processing decisions on a number of factors, many of which we explore in this document.

In this resource, we have tried to provide guidance on the factors that go into the decision to image or not. The factors involved in deciding to image are often exceptional, so we have provided additional detail in our explanations of them. This is not intended to imply a preference for disk imaging over **logical acquisition** as a strategy. Additionally, we use "disk image" generically and do not intend to recommend one type over another. (See [Definition of Disk Image](#definition-of-disk-image)).

### Definition of Disk Image
A disk image (sometimes referred to as an "image") is a digital **file** that is a copy of the readable area of a storage device (or media object), (e.g., hard drive, **optical disc**, floppy disk). An image replicates the content and structure of the original storage device. Content includes visible files, but also system files, hidden files, and even deleted files; it can include things the user may not realize are saved, such as downloaded email and web browsing history. It may also include unused, empty, or **slack** space. A disk image will be about the same size as the storage device being imaged. There are proprietary and open source tools that can be used to create an image; there are also proprietary and open disk image file formats. A disk image can be "**raw**," "**forensically-packaged**," **physical**, **logical**, **compressed**, and/or split up into several files, and these qualities are not mutually exclusive. In this resource, we are focused on physical disk images, but we make no recommendations regarding raw, forensically-packaged, and so on.

### Audience
DANNNG created this resource to fill a gap in existing guidance regarding when—and when not—to image storage devices. This resource is designed to provide practitioners at all levels with a deeper understanding of the broad range of considerations associated with decision-making for creating and maintaining disk images. As a result, the audience for this resource is necessarily broad—it encompasses anyone who is looking to reconsider or revise existing workflows, as well as those wishing to implement a workflow from scratch.

### Assumptions
- You are familiar with the concept and uses of a disk image.
- You will apply the factors in this document as you see fit for your institution.
- Not all storage devices need to be imaged, but there are often compelling reasons to do so. 
- Creating a disk image does not imply permanent retention of the disk image.
- The factors in this resource are not the only determinants when deciding whether to image a media object. Other determinants that are more specific to the storage device or the repository or local context should be considered and may influence the decision one way or another.
- This resource does not recommend specific disk image file formats, (e.g. raw, forensically-packaged, compressed). An institution may choose to use different disk image formats for different use cases: for example, a compressed image format may be appropriate where there are concerns over storage availability; an **uncompressed** image format may be appropriate when **emulation** is a key access strategy; a forensically-packaged disk image may be appropriate in cases where provenance metadata is important to retain within the disk image file itself.
- This resource does not define "best practices," just considerations to be evaluated, which may lead to local and accepted practices.<sup id="a3">[3](#en3)</sup>
- Loss is a regular part of our jobs. Archives should accept and be transparent about data loss through incomplete captures of collections materials, whether through disk imaging or not.

## Factor: Type or condition of the storage device

### In favor of imaging
Do you have reason to believe the storage device is fragile or failing? When storage devices are degrading or failing, imaging may be the most reliable way to successfully capture any of the content on it; at worst, the next read may be the last read, in which case you’ll want the next read to be the imaging process, since you may not know what the storage device holds. It can sometimes be impossible to know in advance when a storage device is headed towards failure, but there are some ways to make a judgement call on this factor.

- If the storage device is an obsolete format, or if it is more than fifteen years old, it is highly likely—though not guaranteed—to be fragile.
- Are there noticeable signs of damage to the storage device (e.g., has the donor reported that their hard drive sounded extremely noisy)? A good rule of thumb: if you plug in a storage device and you hear it moving but you see no visual output on your monitor, imaging may help in recovering the contents of the drive.<sup id="a4">[4](#en4)</sup>
- Has the storage device been stored in less-than-ideal conditions (e.g., damp or humid environments, exposure to the elements, etc.)?
- Is the storage device very old or do you expect it to have older content on it? While it isn’t a guarantee that you won’t be able to **mount** something old on your current working systems, it might signal that the content contained on the storage device might have incompatible (i.e., unreadable) content. (See [Compatibility of the storage device or content](#factor-compatibility-of-the-storage-device-or-content).)

### Weighing against imaging
If you don’t have a physical storage device (e.g., a hard drive, optical disc, floppy disk, etc.), there is nothing that can be imaged. (As opposed to, for example, a set of files stored on a server or transferred over email.)

Acquiring the content from certain media types should not be handled by the traditional imaging process.

- Audio CD (CD-DA): For audio CDs, transforming digital audio into files readable on a computer is known as digital audio extraction<sup id="a5">[5](#en5)</sup>
- Optical media with multiple sessions present challenges when imaging, and the resulting disk images may require additional processing to interpret<sup id="a6">[6](#en6)</sup>
- Devices with copy protection that prevent disk imaging
- LaserDisc<sup id="a7">[7](#en7)</sup>

If the storage device is newer, it may be more likely to be in good working condition and contain content that is compatible and readable with current processing workstations. (See [Compatibility of the storage device or content](#factor-compatibility-of-the-storage-device-or-content).)

## Factor: Compatibility of the storage device or content
### In favor of imaging
Is the content otherwise inaccessible on your workstations? If you mount a device on a processing workstation, what you see may represent only a portion of the data that the device  contains. A storage device may look empty but may not be depending on the system you’re inspecting it on; alternately, you may not be able to see all files present on a storage device. Imaging the original storage device will capture the full range of data and will in turn enable you to use analysis tools to identify, manipulate, and export all the data rather than just the subset of data that may be visible on your workstation.<sup id="a8">[8](#en8)</sup> We have provided [some illustrations of differing views of the same content in an appendix](#appendix) to this document.

- A host system running Windows can attach a drive but not mount it if the drive is formatted with a Mac-based **file system** (e.g., HFS/HFS+/APFS). Windows’ Disk Management tool can detect that something is attached, but Windows cannot assign a drive letter, or read from and write to the drive.<sup id="a9">[9](#en9)</sup> These drives can still be imaged with a tool like FTK Imager.
- Multiple file systems or **partitions** may be present on a single storage device but may not immediately be visible depending on the setup of a processing workstation. Creating a disk image of the media will capture multiple file systems and/or partitions present.
- Certain **characters** in filenames may make it difficult or impossible to work with in other operating systems, even though the files may be visible. For example, a colon (:) may exist in a Linux filename, but if that **volume** is later mounted by a Windows host machine, Windows will report an error if the user attempts to take action on the file. Logically **copying** files with incompatible characters can be time-consuming and require file-by-file remediation; a disk image may be faster to create and may provide information about the file system and **encoding** to provide a reference for future processing.
- Older storage devices may likely contain legacy file systems, which may be incompatible with contemporary computing environments and for which you may inadvertently lose critical data needed for access unless you image. Legacy and/or different file systems (than the one on your processing workstation) may have features that aren’t visible or supported on the file system on a workstation for archival processing. For instance:
    - **Resource forks** were used in Mac file systems prior to the mid-1990s (pre-OSX). They were a proprietary data structure for storing images, icons, and code in a structured file format. They were often necessary to run an executable, though any file type may have an associated resource fork.<sup id="a10">[10](#en10)</sup>
    - Older material may contain character encodings that are no longer widely used. Encodings and how bytes are **rendered** have changed over time, and since the disk imaging process is a byte-for-byte copy of the original storage device, it will capture the information as it was on the disk, rather than present a current system’s interpretation of the data.
- Older material may contain file formats created by obsolete software. If a complete disk image is captured, one may be able to render the disk image in an emulation environment to recreate the native computing environment. This functionality requires the retention of software and dependencies which may not be transferred when creating a logical copy of a user’s Desktop or home directory. When appraising legacy file formats, installed software and information about software versions assessed in situ within a replication of the native environment may also facilitate rendering legacy file formats and provide key contextual information.

### Weighing against imaging
Storage devices that are compatible and interoperable with current computer operating systems and file systems facilitate more accurate and complete transfer of data. The compatibility of storage devices does not guarantee one-to-one transfer, however, so it is important to consider what (if any) **file system metadata** is important to retain and the most appropriate transfer operation to ensure this information is captured.

For instance, if the storage device is an NTFS or exFAT-formatted external hard drive and your processing workstation is a PC running Windows, you are less likely to lose technical metadata in the transfer process since the file system of the storage device and the workstation are compatible.

## Factor: Expected access to content
### In favor of imaging
Is interactivity a desired function for you, your colleagues, or your researchers? Do you intend, or is it important, that users will be able to interact with a full representation of the storage device, whether it be a hard drive, video DVD, software package/application, or something else? If so, creating a surrogate disk image will enable this interactivity. 

- Is the goal to provide researchers access to the whole drive because of its research, evidentiary, or archival value (e.g., to replicate a working environment)?
- If you’re working with a video DVD, will you want a researcher to be able to interact with menus?
- If you’re working with software, do you expect to use disk images for installation or other kinds of replication?
- Do you need a disk image to support interaction with or appraisal of the storage device and its contents in an emulated environment?

Alternatively, does your end user access process require disk images (e.g., if you are using BitCurator Access)?

### Weighing against imaging
If the expected or intended model of access is only to the logical directory or files, there may be no need to create a disk image.

## Factor: Retention of important contextual information

### In favor of imaging
Was the drive used as part of a donor’s work practice and/or used for the creation of records, and is file system metadata important to retain for evidentiary value?<sup id="a11">[11](#en11)</sup> Files may contain embedded metadata or information in **file headers**. File system metadata is not stored within the file itself. Therefore, a logical copy is only guaranteed to preserve file metadata, and creating a disk image is one way to capture certain file system metadata. Retaining file system metadata may be important for certain organizations, specific collections or types of **assets** (e.g., software) or to support current or future research cases. 

Does the storage device contain software specifically designed for and compatible with specific hardware? Deciding which file system metadata and/or features are important to retain can guide whether imaging is an appropriate pathway. If the material is known to contain software, there might be importance to retaining the file system features and/or content captured during imaging, (e.g., NTFS **extended attributes**, **file fragments**, resource forks). These may be difficult to capture without imaging.

### Weighing against imaging
If a storage device was used only for transfer and was not a working drive, it is unlikely to have research, evidentiary, or archival value. While imaging may be required if there are technical issues accessing contents of the drive, the content value is not likely to be a deciding factor.

It may be expedient to image a media object to capture file system features, but it may not always be required to do so. If, for instance, only timestamps are important, there are several ways to capture this outside of an imaging workflow.<sup id="a12">[12](#en12)</sup>

Imaging a person’s working drive may increase the likelihood that you capture sensitive data, including content applicable to local laws (e.g., the Health Insurance Portability and Accountability Act (HIPAA) and the Family Education Rights and Privacy Act (FERPA) in the U.S.) as well as financial or personal identity.<sup id="a13">[13](#en13)</sup> This may also include known and documented types of information, as well as hidden content<sup id="a14">[14](#en14)</sup> (e.g., file slack, file system information, stored user data like browsing history, deleted files). 

Appraising files with donors pre-acquisition may provide guidance about whether to create a disk image or not. If the donor<sup id="a15">[15](#en15)</sup> has expressed concern about information they expressly do not wish to be acquired by the archive, or if the donor can’t or doesn’t want to make a decision on retention of access of such data, and/or if the repository has relevant policies regarding such data, disk imaging may be contraindicated. However, it should be noted that logical copying does not mean you will not capture or have to remediate sensitive data.<sup id="a16">[16](#en16)</sup>

## Factor: Processing workflow
### In favor of imaging

Does your institution's workflow or staffing levels separate acquisition from further appraisal, arrangement, and description? If final decisions about retention, preservation, access, or use are made by different staff members or at a later date, creating a disk image may be the most efficient way to approach the acquisition step. Creating a disk image will also allow you to avoid taking irreversible actions on the content of the media object before making final decisions.

- Does your workflow require a one-to-one correspondence between a digital asset and an original storage device?
- Does your donor agreement allow for the return of storage devices to donors (i.e., they may only be temporarily in your collection while materials are accessioned, giving little to no chance to ever revisit source materials)?
- Does the institution want to include in its provenance an **audit trail** of preservation events<sup id="a17">[17](#en17)</sup> that start from the "source" of the material (e.g., disk image creation, redaction), and are difficult to document otherwise without a disk image?
- Are you unsure whether you may want to have a disk image in the future?

Alternatively, are you working with hardware and associated software that require a disk image to be created first in order to review the storage device’s contents (e.g., floppy disk imaging tools such as the DeviceSide Floppy FC5025 and the Kryoflux)?

### Weighing against imaging
Imaging can be an easy way to build a backlog. Compared to logical acquisition, disk imaging may be seen as a more expedient option upfront, but making a disk image is often associated with a number of additional downstream actions such as exporting content, mounting for appraisal, weeding content, or packaging for end user access, making it a potentially more resource-intensive action than transferring files.<sup id="a18">[18](#en18)</sup>

Storage space to save a disk image of a large drive (even temporarily during processing) may not be available.

Limits to staffing, equipment, or available storage may make creating, storing, retaining, and addressing the privacy issues and ethical concerns<sup id="a19">[19](#en19)</sup> associated with disk images (either as an intermediate or final format) unsustainable.<sup id="a20">[20](#en20)</sup>

You may not be equipped to store potentially sensitive information that might be present in a disk image, even temporarily. The risk of transferring sensitive information is not eliminated when logically copying files, but depending on your workflow, you might have more control over what gets transferred into your systems with a logical copy operation.

## Appendix

In order to illustrate how various environments and utilities differ in their display of the same content, we have provided the following screenshots using the [Where in the USA is Carmen SanDiego?](https://archive.org/details/Where_in_the_USA_is_Carmen_Sandiego_Broderbund_1998) CD-ROM disk image provided from the [Internet Archive](https://archive.org/).

  * [CD-ROM disk image in FTK Imager Evidence Tree](#cd-rom-disk-image-in-ftk-imager-evidence-tree)
  * [CD-ROM disk image displayed in IsoBuster](#cd-rom-disk-image-displayed-in-isobuster)
  * [CD-ROM disk image mounted in Windows 10](#cd-rom-disk-image-mounted-in-windows-10)
  * [CD-ROM disk image in Disk Utility on MacOS 10.15](#cd-rom-disk-image-in-disk-utility-on-macos-1015)
  * [CD-ROM disk image in Disk Image Access Tool in BitCurator (Ubuntu 18.04LTS)](#cd-rom-disk-image-in-disk-image-access-tool-in-bitcurator-ubuntu-1804lts)
  * [CD-ROM disk image in HFSExplorer in BitCurator (Ubuntu 18.04LTS)](#cd-rom-disk-image-in-hfsexplorer-in-bitcurator-ubuntu-1804lts)
  * [Fiwalk output run against disk image](#fiwalk-output-run-against-disk-image)
  * [mmls output run against disk image](#mmls-output-run-against-disk-image)
  * [disktype output run against disk image](#disktype-output-run-against-disk-image)

### CD-ROM disk image in FTK Imager Evidence Tree
![This screenshot shows the disk image as loaded into the program FTK Imager. It is shown to illustrate that there are multiple file system views present, each with differing files present.](/assets/dif-ftk.jpg "Disk image in FTK Imager Evidence Tree")

[FTK Imager](https://en.wikipedia.org/wiki/Forensic_Toolkit)<sup id="a21">[21](#en21)</sup> shows multiple file systems and their respective file listings; notice that they differ slightly.

### CD-ROM disk image displayed in IsoBuster
![This screenshot shows the disk image display in the IsoBuster software. Of note is that the navigation panel on the left displays two different file systems representations -- ISO9660 and HFS -- and there are different files listed under each.](/assets/dif-isobuster1.jpg "Disk image displayed in IsoBuster")
![This screenshot shows a close up view of the navigational panel of the IsoBuster software. The two file systems -- ISO9660 and HFS -- are present, and some of the folders are expanded to further illustrate the differences between the two views.](/assets/dif-isobuster2.jpg "Disk image displayed in IsoBuster - Closeup")

[IsoBuster](https://www.isobuster.com/) also shows the ISO9660 and HFS file systems, and you can see that the file listings are slightly different in each.

### CD-ROM disk image mounted in Windows 10
![This is a screen capture of the CD-ROM disk image as mounted in a Windows 10 system. This is shown to illustrate that the Macintosh-compatible portion of the disk (which is shown in later examples) is not present at all in this view.](/assets/dif-windows-mounted.jpg "Disk image mounted in Windows 10")

Note that none of the HFS file names show up when this disk image is mounted in a Windows system.

### CD-ROM disk image in Disk Utility on MacOS 10.15
![This screenshot illustrates what happens when you try to open up the disk image using Disk Utility on a Mac. The warning text reads, "The following disk images couldn't be opened." The reason is listed as, "image not recognized."](/assets/dif-macOS-disk-utility.png "Disk image in Disk Utility on a Mac")

Note that MacOS no longer supports the ability to mount an HFS volume in Finder.<sup id="a22">[22](#en22)</sup> The ISO9660 partition should be mountable, but it may take some work. 

### CD-ROM disk image in Disk Image Access Tool in BitCurator (Ubuntu 18.04LTS)
![This screenshot shows the disk image loaded into the Disk Image Access tool from BitCurator. No contents are displayed, and in the Image Info panel, the text reads "No image information found."](/assets/dif-disk-image-access.jpg "Disk image in Disk Image Access Tool in BitCurator (Ubuntu 18.04LTS)")

The Disk Image Access screen in BitCurator is built on top of The Sleuth Kit libraries, which does not support reading from HFS volumes.<sup id="a23">[23](#en23)</sup> Even though there is an ISO9660 file system present on this disk image, that is not visible with this utility.

### CD-ROM disk image in HFSExplorer in BitCurator (Ubuntu 18.04LTS)
![This screenshot shows the disk image loaded into the HFSExplorer utility. It shows that only Macintosh files, and not the files that are shown in other programs that read ISO9660 filesystems.](/assets/dif-hfsexplorer.jpg "Disk image in HFSExplorer in BitCurator (Ubuntu 18.04LTS)")

[HFSExplorer](https://www.catacombae.org/hfsexplorer/) will show the HFS file names of this disk image, but it will not present the user with a list of the ISO9660 file names as they are arranged in that file system view.

### Fiwalk output run against disk image
![This screenshot shows the XML output of the tool fiwalk run against the disk image. Of note are the multiple error lines stating that the utility cannot determine the file system type at various offsets using various sector sizes.](/assets/dif-fiwalk.jpg "Fiwalk output run against disk image")

[Fiwalk](https://manpages.debian.org/unstable/sleuthkit/fiwalk.1.en.html) is also built on The Sleuth Kit libraries, and it is unable to detect any file systems on this disk image on this particular run (with no additional flags).

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

[mmls](http://www.sleuthkit.org/sleuthkit/man/mmls.html), part of the The Sleuth Kit libraries, shows the partition table and information, including the ISO9660 and HFS partitions of this disk image. The bit-sector offsets can be used in extracting data from each partition.

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

[disktype](http://disktype.sourceforge.net/) is a C library that can display the format of a disk or disk image. The output also shows the ISO9660 and HFS partitions, along with various other data points. 

## Endnotes
<b id="en1">1</b>. For example, [“Digital Forensics and Born-Digital Content in Cultural Heritage Collections”](https://www.clir.org/pubs/reports/pub149/) by Matthew G. Kirschenbaum, Richard Ovenden, and Gabriela Redwine.[↩](#a1)

<b id="en2">2</b>. Terms that may be used interchangeably here include media, media object, and storage device.[↩](#a2)

<b id="en3">3</b>.See [Never Best Practices: Born-Digital Audiovisual Preservation](https://journal.code4lib.org/articles/14244) for a discussion of this in the audiovisual preservation sphere.[↩](#a3)

<b id="en4">4</b>. Depending on your organization's policies and budget, you may be able to send damaged storage devices to a data recovery vendor.[↩](#a4)

<b id="en5">5</b>. See the [Wikipedia page on CD rippers](https://en.wikipedia.org/wiki/CD_ripper) for an overview and list of software suitable for this purpose.[↩](#a5)

<b id="en6">6</b>. See [Imaging CD-Extra / Blue Book discs](https://openpreservation.org/blogs/imaging-cd-extra-blue-book-discs/) by the Open Preservation Foundation, [Wikipedia page on sessions on optical discs](https://en.wikipedia.org/wiki/Track_(optical_disc)#Sessions), [An Introduction to Optical Media Preservation](https://journal.code4lib.org/articles/9581), and [An Optical Media Preservation Strategy for New York University’s Fales Library & Special Collections](https://archive.nyu.edu/handle/2451/43877) and [its appendices](https://archive.nyu.edu/handle/2451/43876) for more information.[↩](#a6)

<b id="en7">7</b>. Despite its appearance, LaserDisc is an analog format. See the [Wikipedia page on LaserDisc](https://en.wikipedia.org/wiki/LaserDisc) for more information.[↩](#a7)

<b id="en8">8</b>. Tools used to view and analyze disk images may not support all possible file systems, as well, though.[↩](#a8)

<b id="en9">9</b>. There is specific paid software that will allow one to read/write to disks meant for other systems, such as [MacDrive](https://www.macdrive.com/) and [Microsoft NTFS for Mac](https://www.paragon-software.com/us/home/ntfs-mac).[↩](#a9)

<b id="en10">10</b>. QuickTime movies are one type of file that often had resource forks, and may not work when transferred to a filesystem that does not support resource forks. See the explanation referenced in [Missing Resource Fork](https://aeroquartet.com/treasured/missing%20resource%20fork.en.html).[↩](#a10)

<b id="en11">11</b>. File system metadata provides a granular view of the data as it was stored on the original storage device (including timestamps as recorded by the media's file system and the byte offsets where objects were stored). Such metadata is one way of documenting the content's original order. When choosing not to create a disk image, take care to capture files in a way that preserves or retains as much of this information as possible. Note that certain contextual information will not be capturable without imaging.[↩](#a11)

<b id="en12">12</b>. For instance, one may use a write-blocker (or use another read-only technique) and run [walk_to_dfxml.py](https://github.com/dfxml-working-group/dfxml_python) to generate [Digital Forensics XML (DFXML)](https://github.com/simsong/dfxml/) from a directory, which will record timestamp information in metadata for select directories and files. One can transfer files on the command line using commands such as [rsync](https://ss64.com/bash/rsync.html) or [cp](https://ss64.com/bash/cp.html) with flags to preserve attributes like timestamps at the destination for the files themselves.[↩](#a12)

<b id="en13">13</b>. Institutions or their parent institution may have data classification policies, identifying categories of data and defining their level of sensitivity. Some examples include those from [Cornell](https://it.cornell.edu/regulated-data/regulated-data-chart), [Stanford](https://uit.stanford.edu/guide/riskclassifications), or [Duke](https://security.duke.edu/policies/data-classification-standard) Universities. If your institution has such a policy, it should be referred to when considering a policy and practice around disk image creation. Though beyond the scope of this document, if your institution does not have a data classification policy, consider developing one.[↩](#a13)

<b id="en14">14</b>. For example, a donor may not want any information related to their children included, and so took the step to delete such files, not realizing that the information may still be retrievable.[↩](#a14)

<b id="en15">15</b>. We are using the [SAA definition of donor](https://dictionary.archivists.org/entry/donor.html) in this document.[↩](#a15)

 <b id="en16">16</b>. To give examples, it is also possible to transfer "hidden" files and folders through a logical copy, and individual files themselves may contain data that a donor might not realize are accessible (e.g., creator metadata in a PDF, tracked changes in a Word document).[↩](#a16)

<b id="en17">17</b>. This can either refer to actions specifically defined by the [PREMIS events controlled vocabulary](https://www.loc.gov/standards/premis/v3/preservation-events.pdf) or to more general digital preservation activities. See a [definition of audit trail](#https://dictionary.archivists.org/entry/audit-trail.html) in the SAA Dictionary of Archives Terminology.[↩](#a17)

<b id="en18">18</b>. These downstream actions can also be associated with a workflow based on logical acquisition, although pre-processing may be easier in those cases.[↩](#a18)

<b id="en19">19</b>. For a more nuanced discussion of the privacy issues and ethical concerns associated with disk imaging, see: Lassere, Monique and Jess M. Whyte. “Balancing Care and Authenticity in Digital Collections: A Radical Empathy Approach to Working with Disk Images,” in “Radical Empathy in Archival
Practice,” eds. Elvia Arroyo-Ramirez, Jasmine Jones, Shannon O’Neill, and Holly Smith. Special
issue, Journal of Critical Library and Information Studies 3. Available at: [https://journals.litwinbooks.com/index.php/jclis/article/view/125](https://journals.litwinbooks.com/index.php/jclis/article/view/125).[↩](#a19)

<b id="en20">20</b>. The cultural heritage community has discussed the environmental impact of digital preservation. When considering long-term preservation of disk images, it is important to understand the impact of our decisions will largely derive from our retention decisions.[↩](#a20)

<b id="en21">21</b>. Note about FTK Imager: The [digital archives community has discussed the ethical implications of using software outside of their original contexts](https://bitcuratorconsortium.org/bitcurator-consortium-roundtable-practice-values-situating-digital-forensics-tools-in-archives/). We are including a screenshot of FTK Imager here because it is currently in use by library and archives professionals in their workflows and since the interface will be familiar to them, it will provide a way to contextualize the display of the contents of this disk image.[↩](#a21)

<b id="en22">22</b>. See the [History section of the HFS Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_File_System#History) entry.[↩](#a22)

<b id="en23">23</b>. See [HFS on the Sleuth Kit wiki](https://wiki.sleuthkit.org/index.php?title=HFS).[↩](#a23)

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

We are grateful for the feedback from the members of the community that shaped this and previous versions of this resource.

version is 1.0.1