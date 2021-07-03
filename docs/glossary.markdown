---
layout: page
title: Glossary DRAFT
---
## Disclaimer
Participation in the development of this document is not intended to imply a recommendation or endorsement by any of the authors or their employers, nor is it intended to imply that any specific software or toolkit is necessarily the best available for the purpose.

## Overview
### What is this?
This document is a glossary of terms related to digital archives. There is some overlap between the digital archives and digital forensics communities; although digital forensics glossaries exist, this document seeks to contextualize technical vocabulary in the context of cultural heritage.

This document supports Disk Imaging[a] Decision Factors.

### Audience
The glossary is intended for library, archives, and museum workers who are applying digital forensic practices or tools in cultural heritage organizations.

### Expectations about common knowledge
The glossary assumes introductory knowledge of digital forensics. The glossary is not intended to be comprehensive. Links to resources will be provided where available and appropriate.

## Glossary

### Audit trail
The SAA dictionary provides a definition here:
(https://dictionary.archivists.org/entry/audit-trail.html)

### BIN/CUE files
For optical media, one disk imaging approach is to create BIN/CUE pairs, wherein the BIN file stores the content and a CUE file stores ancillary information such as track names and offsets to where tracks begin and end.

See also:
- Imaging CD-Extra / Blue Book Discs by Open Preservation Foundation
- Cue sheet (computing) WikiPedia page
- Brown, G. (2012). Developing Virtual CD-ROM Collections: The Voyager Company Publications. The International

Journal of Digital Curation, 7(2), 13. doi:https://doi.org/10.2218/ijdc.v7i2.226

### Blank space
Unused space that does not contain deleted files or file fragments. Applies to all storage system layers. A scan of blank space should reveal an absence of content, such as all disk sectors in a suspected blank region being filled with the byte value 0.
Synonyms: contentless space 

### Capture
In the context of the disk imaging use cases document, capturing is a synonym for disk imaging.

An expanded definition is provided by the Society of American Archivists. 

### Character
A computer-interpretable unit of information that displays as an alphabetic letter, number, or symbol. 

Examples include: punctuation, white space, accented Latin letter, Chinese glyph, Korean syllabic block, Unicode snowman (☃).

Note that characters can be represented in multiple-byte-wide encodings, which is applicable in most non-Latin character sets.

See also:
- SAA Dictionary’s definition, though, note that depending on the character encoding, a character may comprise more than one byte (e.g. in UTF-8, a character can be 1--4 bytes).
- DPC definition for 'byte'

### Character encoding
The method by which a series of bits corresponds to glyphs that have meaning to human readers. The most common as of 2020 is UTF-8, maintained by the Unicode foundation, which uses between 1 and 4 8-bit bytes. The variability of UTF-8 allows for the encoding of a large number of characters, ensuring that many of the world’s character sets can be encoded in UTF-8, allowing for a level of international interoperability not available previously. While UTF-8 is common now, this has not always been the case. Older encodings abound, and create complications for users attempting to understand objects, particularly those whose creating environment were in non-English western languages, or non-Western character sets at all.

An expanded definition of encoding in general is provided by FADGI

### Container
A container is a data encapsulator, but requires a program to present its data. The general container can store files or, recursively, other containers.
For instance, a file system is a container of files. A floppy disk that is fully devoted to a FAT12 file system is a container for that file system, and also indirectly is a container for the file system’s files. A larger disk will typically have a partition system, which contains partitions, each of which contains a file system, each of which contains files. A Zip file contains files, and can yield files when opened with an unzipping program.

Examples: Partitioned disk medium, disk image of a partitioned disk medium, disk partition formatted with a file system, email with attachments

Synonyms: Physical container (when needed to distinguish from the reduced-scope logical container)

### Copy (v)
An act of replicating content.

Related to files: An act of replicating at least the primary contents of a file. The method of copying can carry other implications for the metadata that is preserved by the operation.  This covers activities such as bit-stream copying with dd, or using a GUI to copy files from one system to another.

### Cyclic redundancy check (CRC)
A non-cryptographic checksum that verifies the integrity of fixed length chunks of data in an object. Can be employed by forensically packaged disk image formats such as AFF3 and E01. 

Note: The ISO9660 optical medium file system and the Zip file format include CRC checksums as part of their basic storage structure.

### Data retention
Data retention can be interpreted as preserving semantic interpretations of original data, or retaining untransformed data from media, if not the original media themselves. 

### Digital Asset
See an expanded discussion of digital (or "cyber") assets in NISTIR 7693, Specification for Asset Identification 1.1

### Disk image
A disk image (sometimes just “image”) is a digital file that is a copy of the readable area of a storage device (or media object), (e.g., hard drive, optical disc, floppy disk). An image replicates the content of a media object. Content can include visible files, but also system files, hidden files, and even deleted files; it can include things the user may not realize are saved on their hard drives, such as email and web browsing history. It may also include unused, empty, or slack space. A disk image will be about the same size as the storage device being imaged. There are proprietary and open source tools that can be used to create an image; there are also proprietary and open disk image file formats. A disk image can be “raw,” “forensically-packaged,” compressed, and/or split up into several files.

Examples: format examples include Expert Witness Format, gzip-compressed, AFF4, and others.

Note: There is some nuance in a disk image taken of a Redundant Array of Independent Disks (RAID) array. A RAID array will present a virtual, composite "Disk" from member disks. An image of the RAID array would treat this virtual disk as a single medium which has no physically corresponding single disk.

### Disk imaging
As a term of practice, disk imaging has come to mean the process of "Acquiring and preserving the contents of a disk." There are two major forms of the most immediate output of a disk imaging process:

1. A disk image, being either a raw disk image, or a forensically-packaged disk image.
2. A logical image that is a collection of all files extractable from a disk.

In digital forensic contexts outside of the cultural heritage community, the phrase disk imaging more often means the former, while "imaging"---especially "imaging a device"---may more equally likely mean either. Logical file transfer is a phrase that unambiguously means a logical set of files, and not a disk image, will be produced.

See also:
- SWGDE glossary, term "image" (page 10)

### Emulation
The accessible reproduction of a legacy media object in a modern computing environment, especially involving a legacy file system or software. Because emulation involves running legacy operating systems, file systems, and software, most emulation solutions require mountable volumes to be found in raw disk images and cannot natively understand a forensically-packaged disk image. This does not necessarily mean that forensically-packaged disk images are a poor choice, but does mean that users may need to re-create a raw disk image from a forensically-packaged disk image in order to make its contents compatible with an emulation solution.

See also:
- NDSA’s definition
- DPC's definition

### Extended attribute
A file system feature that pairs files with arbitrary name-value pair metadata that is not interpretable by the file system. Whether a file system makes use of extended attributes depends on the file system itself, the mounting operating system, and applications that know how to make use of extended attributes. An extended attribute is not likely to persist if a file is copied to a different file system type that does not support a given extended attribute (e.g., from NTFS to exFAT). 

Examples include: storing the URL from which a file was downloaded, which is done by Apple's Safari, GNU wget with the '--xattr' flag, and a Windows interface that uses NTFS extended metadata to mark downloads. 

Note: Special commands are typically necessary to view extended file metadata, such as the mdls command or the "Get Info / More Info" context-menu Finder interaction in macOS environments, the xattr command in Linux environments, or [something in Explorer] in Windows environments.

### File
A stream of contents with some attached metadata, typically at least a name and associated timestamp (via a filesystem or container such as a zip).

See also:
- SAA’s definition
- FADGI definition for ‘digital file’

## File fragment
A portion of a file's contents that remains on a disk. This occurs most commonly when files are deleted and previously used storage sectors are only partially re-written. 

### File header
A file header may include annotative and configurative information about the main "body" of a file's contents. For instance, outside of the context of files, a table has a "header" section with column titles, and then a "body" section with data that are interpretable thanks to the configurative information in the column heads.

In the context of files, a header can contain:
- Signature information, such as a magic number (like "JFIF" at the beginning being the "Magic" bytes of a JPEG file)
- Annotative information, such as EXIF data in a JPEG file
- Configurative information, such as Discrete Cosine Transform tables needed to decompress a JPEG's contents.

Note that a header is not necessarily going to appear at the beginning of a file. A Zip's "header" comes at the end of the file, and includes configurative information like pointers back into the file's earlier contents to identify where members of the zip begin.

SAA provides a helpful summary statement: A header is logically separate from the data it describes.

See also:
- SAA's definition
- Wikipedia: List of file signatures
- parametric.press Unraveling The JPEG

### File system
A defined structure that dictates how and where data is organized on a volume. When preserving a file system, some care should be taken to note that file system's extended attributes.

Examples include NTFS, HFS, APFS, exFAT, FAT12, and FAT32. Others can be found at:
- "File system" on wikidata:
	- Term definition
	- Query for known instances (requires pushing "play" button on left)

### File system metadata
Can refer to:
1. Metadata about the file system writ large (e.g., superblock-housed data, statistics about file counts), or
2. Metadata about a file that is stored not in the file, but in the file system. 

See also:
﻿﻿Metadata, embedded - Glossary - Federal Agencies Digitization Guidelines Initiative

### Forensically-packaged disk image
A type of disk image that copies all content on a media object, but compresses blank space and might losslessly compress other contents, and might be a partial image of an original medium (such as when a disk sector cannot be read due to damage). Forensically-packaged disk images preserve all data on a media object, and include annotative metadata about the imaging process and the process's results. The additional metadata can be used to verify hashes of the objects found in the disk image. A forensically-packaged disk image will generally have a smaller footprint than unpackaged raw disk images. Many formats have internal hash check functionality. Like raw disk images, they preserve slack space. Forensically-packaged disk images are often in a proprietary format, though a popular commercial format (EWF) has been reverse engineered by open-source developers. Forensically-packaged disk image formats allow the user to reconstruct the acquired raw disk image from the package, and some present virtual views of the raw disk without expanding to fill disk space (such as via a File System in Userspace [FUSE] mount).

Examples include: EWF, AFF3, AFF4

Synonyms: forensic disk image, compressed disk image

### Hash
"Hash" among DANNNG documentation is a shorthand for "Cryptographic hash."

See also:
- Wikipedia: Cryptographic hash function 

### Logical container
Logical containers are used to store files and file metadata that have been interpreted from their direct-parent container. Logical containers have varying support for file metadata, but typically provide a name of a file along with that file’s contents. For example:
- An email message is a logical container for an attached file, but contains no standard metadata indication of the file’s modification time from its source container.
- A zip file provides a file’s name and, if requested, modification time.
- A file system provides a file’s name, timestamps, and other metadata.

A logical container is a container selected to store the output of a logical imaging process. 

Examples: ZIP, TAR, AFF4, Bagger

See also:
- "Bundling file format" on digitizationguidelines.gov
- "Package" in NDSA Glossary
- The result of "packing" in PREMIS preservation events

### Logical file transfer
Copies active/visible files on an object, but does not copy blank space or slack space. A logical file transfer preserves active/visible files without preserving files that may pose higher risks. It also has a smaller storage footprint, but cannot inherently verify hashes or allow for emulation since the file system is not retained.

An end result of this process is the production of a set of files extracted from a disk device or disk image. Logical file transfer is meant to disambiguate from disk imaging.

Examples include: AFF4, AD1, L01, LX01 

Synonyms[1]: logical copy, logical acquisition, logical file acquisition, logical transfer, logical image

See also:
- SWGDE Digital & Multimedia Evidence Glossary, "Logical Acquisition/Copy"

### Magnetic media
Storage objects that store data using magnetic particles scattered over a magnetized surface. Data is written to and read from such media using read/write heads in tracks and sectors. The simplest examples feature a single surface (e.g. a floppy disk, a tape cartridge), while more complex examples feature multiple magnetic surfaces in a stack (2.5" or 3.5" large capacity hard drives).

Examples include: floppy disks, internal hard drives, external hard drives, tape-based media

See also:
- SAA Dictionary: magnetic media

### Media Object
A physical piece of computer-readable hardware that contains some number of digital files. Digital archives tend to focus on legacy objects, and while it is theoretically possible to consider RAID arrays and server hardware featuring a storage component, these are largely outside the scope of this document.

Examples include: a flash drive, a floppy disk, a CD

Synonym: storage device

### Mount (v)
As opposed to simply “attaching,” mounting implies a process of interpreting a bitstream as a file system, for the purposes of browsing, retrieving, or storing files. It is possible to mount devices, or in some special cases, files.

### Operating system
The primary software that runs on a volume and communicates between computer hardware and other software. Examples include Windows 10 and MacOS High Sierra.

See also:
- SAA’s definition

### Optical media
Removable storage objects that can be read and/or written using a laser. 

Examples include: CDs, DVDs, CD-ROMS, and Blu-Ray discs.
- SAA’s definition of ‘optical disk’
- SAA’s definition of ‘magneto-optical media’

### Partition
A partition is a region of a storage device defined by a partition system. It is the container for a file system, setting the total amount of space the file system can use.

See also:
- SWGDE Glossary, page 13

### Provenance metadata
Metadata that describes the origin, chain of custody, and processes that led to an object.

See also: 
- "Metadata, process" in FAGDI Glossary
- "Functional provenance" in SAA Glossary
- "Provenance" in NDSA glossary
- "Chain of Custody" and "PDI" in DPC Glossary
- The W3C PROV Data Model

### Raw disk image
A disk image that copies a media object bit-for-bit with no further annotation or transformation. It preserves all data, can be used to verify hashes of the objects found in the disk image, and can allow for emulation because it is uncompressed. Raw disk images preserve all the data present on the media object data--including slack space and blank space--and are as large as the source media object. Raw disk images are uncompressed.

Example file extensions include: .img, .dd 

Synonyms include: physical disk image, bit-for-bit disk image

Similar to: uncompressed disk image

### Render
To take raw data and convert it into human-consumable format.

E.g., raw contents of jpeg as bitstream vs rendering as picture, html doc rendered as audio stream by screen reader 

### Resource fork
In HFS file systems, a secondary stream of content that includes extra data, such as GUI placement data determining where a file should appear in a window. For executable content, there is other metadata embedded in the resource fork that must be preserved in order to execute content.

See also:
- Wikipedia: Fork (file system)

### Sector
The smallest unit of storage on a disk, usually 512, 2048, or 4096 bytes. Applies to physical disks and disk images, and some file systems. A sector is said to be a bad sector when it is permanently damaged, usually as a result of physical damage. An operating system can recognize bad sectors, flag them, and avoid them in future storage. 

### Slack space
Previously used space that has not yet been overwritten, and may contain deleted files or file fragments. Applies to all storage system layers.

### Solid State media
Storage objects that store data in circuits and so do not require moving mechanical parts. Examples include: thumb drives, external hard drives, internal hard drives, SD cards, Solid State Drives (SSDs).

Synonyms: flash storage, non-volatile storage

### Storage system layers
End users typically think of computer storage systems at their highest semantic layer--where the files live. However, several layers of organization exist before one gets to files. Storage system design and digital forensics research literature often describes such layering in general terms like, "the storage model." Within this document, we use the term "storage system layers."

The storage system stack in this glossary refers to digital artifacts representable as files, effectively whole or partial copies of the digital contents of a physical disk. In general:
- A disk image can provide one or more partition systems.
- A partition system can provide one or more partitions.
- A disk partition can contain a file system.
- A file system can contain files.

These layers form the storage system stack. While generally one would walk through the layers in the order listed above, an illustration of less-common transitions between the layers was presented at BUF 2018 by Nelson and Dietrich.

Synonyms: "storage system stack"

### Unallocated space
Storage space that is available for use, but may contain ephemeral content (e.g., deleted files, file fragments) that can be overwritten upon next use. Unallocated space is different from blank space, since it is available but not necessarily blank. 

Synonyms: free space 

See also:
- "Unallocated space" in the SWGDE Glossary

### Uncompressed disk image
An uncompressed disk image is a file that contains a bit stream representing the contents of a disk image, with no compression applied. This is similar to raw disk images, except raw disk images contain no embedded metadata relating to any disk image format. Some uncompressed disk images are like raw images with an extra header or footer region. For instance, the Microsoft VHD "Fixed Hard Disk Image" format is a raw disk image with an additional footer sector of metadata.

See also:
- Microsoft. "Virtual Hard Disk Image Format Specification," version 1.0, 2006-10-11. Referenced in: About VHD (Windows)

### Volume
A storage area defined at the operating system level, which has a single file system and usually resides on one disk partition.

Warning: “Volume” is a confusing term that has been used in a variety of capacities throughout the storage systems research, digital forensics, and digital archiving communities. DANNNG documentation will prefer the “file system” interpretation.

For examples of ambiguities, volume can be taken to mean a formatted storage device [1, 4, 8], disk partition [1, 3, 8], file system [1, 2, 5, 7], collection of byte blocks of equal size (but happens to mean file system) [2], or virtual block device onto which a file system can be formatted [6, 8], among various documentation sources.

References on "volume":
[1] Storage Device Stacks, Storage Volumes, and File System Stacks - Windows drivers
[2] Github: dfxml_schema/dfxml.xsd at master · dfxml-working-group/dfxml_schema
[3] File and Volume System Analysis
[4] Volume Management - Win32 apps
[5] See if your Mac shares space across APFS volumes in System Information
[6] ZFS Volumes - Oracle Solaris ZFS Administration Guide
[7] btrfs Wiki: Glossary
[8] debian Wiki: LVM (Logical Volume Manager)

## Other references
Society of American Archivists Dictionary

National Digital Stewardship Alliance Glossary

Glossary - Digital Preservation Handbook

Library of Congress - Preservation Events Controlled Vocabulary

SWGDE Digital & Multimedia Evidence Glossary

Federal Agencies Digital Guidelines Initiative Glossary

## Acknowledgements
The following people contributed to this document:
- Erin Barsan, Pratt Institute School of Information
- Alex Chassanoff, North Carolina Central University
- Dianne Dietrich, Cornell University Library
- Brian Dietz, NC State University Libraries
- Brenna Edwards, Harry Ransom Center, The University of Texas at Austin
- Alex Nelson, National Institute of Standards and Technology
- Margaret Peachy, Digital Collections & Archives, Tufts University
- Paige Walker, Tisch Library, Tufts University

We are grateful for the feedback from the members of the community that shaped this and previous versions of the document.
________________
[1] Some nuance is present between these synonyms, but they are left out of scope of this document's first version.
[a]will need to update this link to THE use cases we settle on
