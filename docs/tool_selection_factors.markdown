---
layout: page
title: Tool Selection Factors
---

- [Introduction](#introduction)
- [Factor: Documentation and support](#factor-documentation-support-and-maintenance)
- [Factor: Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost)
- [Factor: Extensibility](#factor-extensibility)
- [Factor: Inputs](#factor-inputs)
- [Factor: Installation requirements and processes](#factor-installation-requirements-and-processes)
- [Factor: Interface](#factor-interface)
- [Factor: Lists compatible hardware](#factor-lists-compatible-hardware)
- [Factor: Logging](#factor-logging)
- [Factor: Output formats available](#factor-output-formats-available)
- [Factor: Tool impacts](#factor-tool-impacts)
- [Appendix A: Applying the Tool Selection Factors through narrative profiles](#appendix-a-applying-the-tool-selection-factors-through-narrative-profiles)
- [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets)
- [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes)
- [Appendix D: Log file samples](#appendix-d-log-file-samples)
- [Acknowledgements](#acknowledgements)

## Disclaimer

Participation in the development of this document is not intended to imply a recommendation or endorsement by any of the authors or their employers, nor is it intended to imply that any specific software or toolkit is necessarily the best available for the purpose.

## Introduction

### Purpose

The digital archival community has access to a lot of different tools that can support many workflows. But, not all tools do the same thing, and tools that have similar functionalities may not do those things exactly the same way. Some tools may have the capability to serve multiple purposes, and some tools do one thing really well. Generally, tools in our area of work can be categorized as supporting imaging media and analyzing and extracting data from them; packaging data and transferring data; and reporting and evaluating. Regardless of purpose, the Factors can be applied to assessing related tools. (See [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes).)

DANNNG created this resource to fill a gap in existing guidance regarding how to assess and select software tools for digital archives workflows. This resource is designed to provide practitioners at all levels with a deeper understanding of the broad range of considerations associated with decision-making for assembling and maintaining a toolset. As a result, the audience for this resource is necessarily broad—it encompasses anyone who is looking to reconsider or revise the toolset they use in existing workflows, those wishing to implement a workflow from scratch, as well as managers and administrators who want to understand how members of their teams select tools.

### Assumptions

- While this resource contains many of the factors that one might use to select tools, DANNNG does not intend it to be a comprehensive listing of all possible factors, nor of all of the features of any tools referenced within the resource.

- DANNNG authors and reviewers included tools for illustrative and exemplary purposes, often adding tools based on their own familiarity and experience.

- As you select tools for your workflow, it is appropriate to build on collective knowledge. However, the explanatory text on factors and tools in this resource is not a substitute for understanding your individual and organizational needs, and investigating and testing these tools for their appropriateness to meet those needs.

### Your need and the capabilities of the tool

Before beginning tool assessment and selection, it is important to understand the problem you are trying to solve or the task you are trying to accomplish, and whether a technical solution is the best fit. If you have determined that a technical solution is best, matching your need to the functionality provided by a tool (or set of tools) should be your starting point. As a baseline, a tool has to do what you need it to do to be useful in your workflow. The selection factors presented here are designed to guide you through the assessment and selection process for tools that meet this baseline requirement.

### How to use the guide

Usage of the Tool Selection Factors guide will vary based on what information you are seeking. For example, if you are an early-career practitioner evaluating tools to create a workflow from scratch, you may utilize all of the factors to develop an assessment matrix for selecting tools. Those with existing toolsets and workflows may use a subset of the factors to compare and differentiate a small set of tools for a specific task. Managers and administrators may review the factors to understand what aspects of tools are important for their team's success.

The resource is structured as a set of factors against which to evaluate software tools. Factors addressed include:

- [Documentation and support](#factor-documentation-support-and-maintenance)
- [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost)
- [Extensibility](#factor-extensibility)
- [Inputs](#factor-inputs)
- [Installation requirements and processes](#factor-installation-requirements-and-processes)
- [Interface](#factor-interface)
- [Lists compatible hardware](#factor-lists-compatible-hardware)
- [Logging](#factor-logging)
- [Output formats available](#factor-output-formats-available)
- [Tool impacts](#factor-tool-impacts)

Each factor contains a descriptive and explanatory text that defines the factor and explains its significance in relation to tool selection. Following the text are a series of short user stories that provide examples of how you may use the factor to evaluate tools. All user stories are in the format of "As a \[role\], I need to \[do something\], so that I can \[achieve something\]." For example, the [Interface](#factor-interface) factor contains a user story that reads: "As a digital archivist, I want to use tools with a command line interface, so that I can more easily automate parts of my workflow." See [Appendix A](#appendix-a-applying-the-tool-selection-factors-through-narrative-profiles) for a more detailed guide to analyzing your local context and constructing your own user stories through narrative profiles.

Following the factors are four appendices that: provide several full-length examples of how to use the factors to evaluate tools and select those that meet particular individual and organizational needs, explain how multiple inputs may combine to make compound input sets against which you can evaluate tool compatibility, list some common tools and their primary purposes in digital archival workflows, and show examples of log files from several tools, respectively.

- [Appendix A: Applying the Tool Selection Factors through narrative profiles](#appendix-a-applying-the-tool-selection-factors-through-narrative-profiles)
- [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets)
- [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes)
- [Appendix D: Log file examples](#appendix-d-log-file-samples)

### Related resources

- [Community Owned Digital Preservation Tool Registry (COPTR)](https://coptr.digipres.org/index.php/Main_Page)

- [A beginner's guide to digital preservation tools](https://www.dpconline.org/handbook/technical-solutions-and-tools/tools) - Digital Preservation Handbook, Digital Preservation Coalition

- Scott Prater (2018): How to Talk to IT about Digital Preservation, Journal of Archival Organization, DOI: [10.1080/15332748.2018.1528827](http://digital.library.wisc.edu/1793/78844)

- [Library of Congress Recommended Formats Statement](https://www.loc.gov/preservation/resources/rfs/index.html)

## Factor: Documentation, support, and maintenance

### Documentation

Following the factors are four appendices that: provide several full-length examples of how to use the factors to evaluate tools and select those that meet particular individual and organizational needs, explain how multiple inputs may combine to make compound input sets against which you can evaluate tool compatibility, list some common tools and their primary purposes in digital archival workflows, and show examples of log files from several tools, respectively. How complete and up-to-date is the documentation for the tool? A tool might have limited documentation, meaning that if you encounter unexpected behavior, it might be difficult to troubleshoot what went wrong. Tool documentation that is updated and complete can make your work much smoother, but there are cases where an under-documented tool is the best fit for your particular workflow and needs. Complete documentation might include accurately described procedures and explicit explanations of what happens to the media while the tool is processing or otherwise interacting with it. You may be able to figure out when a tool is performing a given function without documentation.

### Support

Is the level of support available for a tool workable for you, given your capacity, comfort-level with troubleshooting and/or debugging, and the availability (or non-availability) of colleagues you can call on for assistance?

What is the user community for the tool? Some tools are well-known in the digital preservation and archival community, meaning that it may be easier to find guidance implementing the tool in a workflow or context similar to your own. If a particular tool is widely used, but perhaps not in the archival community, it is still possible to find support and guidance, but you might have to be on the lookout for hidden assumptions that might affect how the tool works in your own context.

Listservs and/or forums give you a sense of how active a user community might be. There may be user-developed tutorials available,<sup id="a1">[1](#en1)</sup> in addition to maintainer-supplied documentation.

Additionally, there may be paid support available for the tool. You may be able to report bugs directly and work with maintainers of the tool to fix any issues. Alternatively, some free tools offer a way for anyone to report or log a bug (e.g., on GitHub or Bugzilla), but do not guarantee that all reports will be addressed or bugs fixed. You may be able to see a list of a developer's open issues to get a sense of what they're working on and how open they are to considering bug reports and feature requests.

### Maintenance

The level of maintenance may also factor into your decision. Some tools are no longer maintained or actively developed, which can pose problems if, for example, security issues are discovered. Unmaintained tools might not be compatible with current input standards and may not produce outputs that align with current standards.

See Factors: [Inputs](#factor-inputs), [Output formats available](#factor-output-formats-available); See [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes)

### User stories 

The following examples illustrate decisions related to this factor:

- As an early career archivist/librarian, I want a tool that is well documented by the maintainer or user community so that I can use it in my work without needing to develop the workflow from scratch.

- As an archivist, I want a tool with an engaged user community, so that I can ask edge case questions and have a reasonable expectation that answers will provide some insight.

- As an archivist, I want the tool's users to include digital preservation and archival users, so that any issues I encounter and seek assistance on will be received by other users with similar use cases or needs.

- As a digital archivist selecting tools to support my workflows, I want to find tools with robust documentation so that I understand not only how the tool functions, but also how it may affect the materials on which I will be using it.

- As an IT professional/archivist, I want to use actively maintained tools so that I can ensure support with modern operating systems and I can mitigate introducing security issues into our systems.

## Factor: Developer, vendor, license, and cost

### Developer and vendor 

Who develops the tool can be important. You may only be permitted to use tools developed or sold by an approved vendor (e.g., Microsoft, Oracle, Apple, Adobe) or software publisher. This can often limit one's ability to install many applications in our space, as they are niche, and may be maintained by an individual or company that is not recognized as a trusted vendor. Some tools are collectively developed and maintained, such as many of the command line utilities found in a Linux distribution, and do not have a singular "vendor" defined.

### License 

The license may limit what you may or may not do with the software, such as use it on multiple computers or in non-educational/commercial settings. The license may also have language around which user groups are allowed to use the software in specific settings.<sup id="a2">[2](#en2)</sup>

### Cost 

Cost will likely factor in, as well. Some tools operate on a subscription model, while others require a one-time fee. You may or may not get discounts for upgrades. The pricing model may be different depending on the type of institution you're affiliated with or for multiple licenses. Cost can also be impacted by whether support would be provided by a vendor, or would instead only be provided by a user community.

### Examples

- Guymager

  - Open source

  - Included in the BitCurator suite of tools

  - Free

  - Maintainer: Guy Vonken


- IsoBuster

  - Closed-source, proprietary commercial software

  - Has personal, professional, and enterprise licenses


- FTK Imager

  - Closed-source, proprietary commercial software published by Exterro

  - Free (companion tools that are part of the FTK suite are not free)


- ddrescue

  - Publicly licensed (GNU)

  - Free


### User stories

The following examples illustrate decisions related to this factor:

- As a digital archivist, I want to determine if I have the financial resources to acquire and use this tool so that I can incorporate it into my workflow.

- As a digital archivist working in academia, I want to factor in potential discounts available to those using the tool in an educational context so that I can get an accurate total cost to purchase a tool to show my administrators.

- As an archivist working for an organization that has certain requirements in place for publishers of software tools it purchases, I want to know if any available tools meet those requirements so that I can determine whether I can use these tools in my workflow.

- As a project manager, I want to know what the most cost-effective choice is to integrate with existing hardware and workflows so that I can make the most effective use of existing resources.

- As an archivist, I want to know who or what entity is responsible for a tool's maintenance and development and whether there is a way for me to contribute to these costs (e.g., through membership, licensing, or other funding options) so that I can fully understand my options for extending the feature set of a tool.

## Factor: Extensibility

It may be important to consider extensibility, that is, whether and how you can extend the functionality of a tool. Some ways a tool may be extensible include:

- Direct modification of source code.

- Plugin architecture that allows for users to develop their own plugins and/or select from a library of community-developed plugins.

- Tool outputs are machine-consumable and can be used directly in other tools.

Some licensing structures may prevent you from extending the capability of a tool.

### Examples

- Locally hosted instances of ArchivesSpace can be modified to suit local needs, and those changes can be suggested for consideration for merging into the main code base.

- Some developers host their code in a way (e.g., GitHub) so that others may contribute to the development by submitting code for suggested changes, which may then be incorporated into the main code base.

See Factors: [Output formats available](#factor-output-formats-available), [Logging](#factor-logging), [Interface](#factor-interface)

### User stories

The following examples illustrate decisions related to this factor:

- As a digital archivist, I want to be able to modify a tool so that I can meet the specific needs of my organization.

- As a digital archivist, I need the ability to modify a tool to output XML for a specific workflow so that its output can be incorporated into existing workflows that consume XML.

- As a digital archivist, I want to be able to reformat output into a CSV file so that I can ingest it into another piece of software.

## Factor: Inputs

Different tools are compatible with different types of inputs. Thinking about the kinds of media and devices you're working with will help you identify the tools that may be appropriate for different use cases. Some inputs may require additional hardware (e.g., disk drives) or peripherals (e.g., cables) in order for you to use them. These combinations of media, hardware, and peripheral inputs can be considered to compose a "compound" input; see [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets) for more details.

### Examples

- Kryoflux software takes as input a floppy disk in a disk drive, that itself requires additional hardware to connect to your computer.

- tapeimgr takes as input data tapes.

- tar takes as input any logical set of files readable on your computer.

- ISOBuster takes as input optical media that is mounted to your computer.

- ClamAV can take a disk image as input, as well as a logical set of files or a mounted device readable by your computer.

### User stories

The following examples illustrate decisions related to this factor:

- As a digital archivist I need a tool that can run checksums on files hosted on a network storage location that is mapped as a drive to my Windows workstation, so that I can verify checksums before and after transfer.

- As a digital archives assistant I need a tool that will accept SATA input, so that I can determine whether I should create a disk image or make a logical file transfer from a 3.5-inch form factor internal hard drive with a SATA connection.

- As a processing archivist, I need a tool that can extract files from a disk image with an HFS file system, so that I can further assess content and possibly re-package in another container format.

See [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets), [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes)

## Factor: Installation requirements and processes

Installation requirements and processes are often key factors in determining whether a tool will work for your situation and whether it is worth your time or money to set it up.

### Installation requirements

- Tools can require certain hardware (drives, etc.) to work, see [Lists compatible hardware](#factor-lists-compatible-hardware) for additional considerations.

- Some tools are only compatible or can be installed on certain systems. Sometimes it might be possible to run a tool on a platform it was not made for (e.g., running a Windows program using Wine, running GNU applications on Windows using Cygwin), but that might introduce undesired complications or unintended instability to a workflow.

- Some tools are pre-packed and run from a single installer, while others may need to be installed using a package manager (e.g., Homebrew on Mac, apt on Debian-related Linux distributions, yum/dnf or rpm on Fedora-related Linux distributions) or by compiling from source. Some tools, such as ClamAV, require additional configuration even after you've installed it.

- Some tools for different platforms share the same name and do similar things, but are written as different implementations and behave slightly differently. An example is the GNU and BSD versions of the tar application. It is important to try to understand some of the differences in how these tools run and function, and whether the different tool editions are compatible with one another (e.g., through conformance to some in-common specification).

- Some software cannot be installed or run without administrative privileges on your system either due to the requirements of the tool/operating system or restrictions put in place by an IT department. If these privileges are required and you do not have them, you will need to contact your IT department to determine a solution or find an alternative tool without these requirements.

- Depending on the security and storage requirements of the media and data you're working with, you may need to install and work with software solely on a local machine.

- Some tools may require an active internet connection for installation or product activation.

### Installation processes

Assuming your setup meets the installation requirements of the tool, consider which installation process might work best for your situation. Some tools may only have one installation option, while others will offer many options depending on your preference or system.

Here are some factors to consider with the installation methods listed below:

- How comfortable are you with the command line interface (CLI) as opposed to graphical user interfaces (GUIs)? See [Interface](#factor-interface) for additional details.

- Is the installation process well-documented? How much help might you have in the installation process? See [Documentation and support](#factor-documentation-support-and-maintenance).

- Do you have time or willingness to troubleshoot installation issues?

- What are your user needs (for instance, do I need to install this for just me or all accounts on this computer?)

#### Common installation methods

- No installation - [Software as a Service (SaaS)](https://simple.wikipedia.org/wiki/Software_as_a_service) through a hosted vendor, see [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost) for more considerations.

- Pre-installed with the operating system: Some tools are part of the operating system on the machine in use, such as Disk Utility in MacOS or File Explorer in Windows.

- Installation [wizard](https://en.wikipedia.org/wiki/Wizard_(software)) 🧙‍♂️: Some tools require you to install them, but come with a user interface that breaks the installation process into smaller, more accessible steps. This can be used by software providers in conjunction with other installation methods on this list.

- Executable packaged installer (.exe, .msi, .dmg, .deb): These tools require installation, but don't require input from the person installing them past running the installer.

- Executable without installer: You need to download the code for these tools to your computer, but they don't require installation: they are self-contained and can simply be run. They can also be run with a launch script (e.g., a .bat file in Windows or .sh file in Linux/Unix/Macintosh systems). These tools may not have a GUI and may require the use of the command line.

- Digital distribution platform: Some tools can be downloaded and installed through platforms like the Mac App Store or Windows Store. These platforms may require you to make an account with them.

- [Package manager:](https://en.wikipedia.org/wiki/Package_manager) Some tools can be downloaded and installed using package managers. These can either be run on the command line ([apt](https://en.wikipedia.org/wiki/APT_(software)), [homebrew](https://en.wikipedia.org/wiki/Homebrew_(package_manager)), [chocolatey](https://en.wikipedia.org/wiki/Chocolatey), etc.) or through a GUI.

- [Containerized](https://en.wikipedia.org/wiki/Containerization_(computing)) installation: Some tools come packaged in containers, computing environments that contain software and its dependencies in an isolated virtual environment that can be run independent of other software or environments on a host computer.

- Scripted install using a shell script: Some tools can be installed using the command line and a shell script, sometimes called install.sh. Other tools may require the use of [Makefiles](https://en.wikipedia.org/wiki/Make_(software)) to build them.

- Compiling from source: Some tools are only available as source code and require you to compile the code into an executable program. This requires use of the command line.

### Other considerations

#### Dependencies

- There may be features of a tool that require dependencies (other components) to be installed separately. These dependencies may not be free and/or may require their own licenses. See [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost) for considerations regarding dependencies.

- Are dependencies included in the install package or automatically retrieved in the install process? If they are automatically retrieved, you will most likely need to be connected to the internet at that time. This is important to consider for computers not connected to a network, such as some forensic workstations. You would either need to connect temporarily or seek alternative methods if possible.

- You may need to install drivers for the tool to work with associated hardware. See [Lists compatible hardware](#factor-lists-compatible-hardware) for additional considerations.

#### Additional installation setup

- After installing the tool, you may need to spend additional time changing internal tool settings or registering your software so that it functions correctly with your system.

See Factors: [Documentation and support](#factor-documentation-support-and-maintenance), [Lists compatible hardware](#factor-lists-compatible-hardware), [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost)

### User stories

The following examples illustrate decisions related to this factor:

- As a digital archivist, I would like a compatible tool I can install via a GUI installer that doesn't require administrative access so that I can manage processes for disk imaging DVDs from my laptop without needing IT support.

- As a records manager, I want a tool with a simple installation process that I can provide to content creators to facilitate transfer to records management and archival storage so that I do not need to provide as much technical support.

- As an archivist visiting donors, I want to know if a tool requires an environment that is already installed on my laptop so that I can decide whether I need to plan to install that environment or pack another computer that has that environment installed.

- As an archivist managing multiple computing environments, I want as many cross-platform tools as possible, so that my environments can behave like one another in interface and data output, even with different hardware- or OS-based setup prerequisites.

## Factor: Interface

A tool's interface provides the means of interacting with and passing commands to the tool. Often abbreviated, the three types of interfaces are graphical user interface (GUI), command line interface (CLI), and application programming interface (API). Tools may have more than one interface with overlapping and/or unique functionality between interfaces. Selecting a tool with an interface that matches your skill set and objectives is critical for a successful outcome.

### Graphical user interface (GUI)

With a GUI, users interact with and pass commands to a tool via graphical icons. GUIs have become the standard for general use of computers and mobile devices, and for the majority of applications used on these devices. GUI functionality is often contained in a series of discrete pages organized by a menu. While using a GUI may have an easier learning curve (in general) than for CLIs or APIs, and while some tools have batch functionality via the GUI, the need for manual interaction limits useability for scripted automation.

### Command line interface (CLI)

With a CLI, users interact with and pass commands to a tool using text inputs via a command prompt or script. CLI interaction requires precise command syntax and some organizations may limit command line use to users with administrator privileges. A tool's CLI may include enhanced (or more granular) functionality than its GUI. Additionally, via scripting, users can often automate a tool's function and string together multiple actions or tools into an automated workflow. Some tools may have only a CLI.

### Application programming interface (API)

With an API, users program one application to interact directly with another. In this way, one tool may be able to offer the functionality of another tool or provide data stored elsewhere. APIs may be custom-built between tools or follow certain standards or styles (e.g., REST APIs, also called RESTful APIs, conform to the constraints of the [REST architectural style](https://en.wikipedia.org/wiki/Representational_state_transfer)).

### Examples

- Guymager has a GUI
- ddrescue is a CLI application
- ArchivesSpace has a documented API

### User stories

The following examples illustrate decisions related to this factor:

- As a digital archivist, I want to use tools with a command line interface, so that I can more easily automate parts of my workflow.

- As a digital archives practitioner, I need a disk imaging tool that has a graphical interface because my workflow involves those who prefer working via GUIs so that I can support those colleagues in their work.

- As a developer, I want to connect the data in multiple repositories as inputs for a single tool so that the users of that tool can have a seamless experience.

- As a records manager, I want a tool with multiple interface options so that I can evaluate a server-side application environment in different ways to determine whether that application needs preservation.

## Factor: Lists compatible hardware

Some tools are capable of working with a variety of media and their associated hardware (e.g., floppy drives, optical drives), and some are designed for specific media. Some may not work properly or at all with certain types of hardware. Similarly, some tools are designed to work exclusively with files on external media, as opposed to logical files on your own filesystem (e.g., a directory of files on your Desktop). If the tool lists its hardware compatibilities (or incompatibilities), it is easier to take into consideration the specific purpose of the tool when determining if it fits your needs.

Some types of hardware require additional tools called device drivers to facilitate communication between the hardware and the operating system. Installing these may require administrative permissions, which is another detail to keep in mind. Some pieces of hardware will also require other hardware, like adapters, in order to properly interface with the host computer.

### Examples

- Device Side Data's Disk Image and Browse software tool requires the FC5025 controller and a 5.25-inch floppy disk drive.

- Kryoflux software requires the Kryoflux board and 3.5-inch or 5.25-inch floppy disk drive.

- GNU ddrescue can be used to image connected devices, including USB connected flash drives and many optical media formats.

- tar can be used to package non-media based content as well as files on various connected devices and mounted volumes.

See Factor: [Inputs](#factor-inputs); See [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets)

### User stories

The following examples illustrate decisions related to this factor:

- As a digital preservation practitioner, I want to determine whether a piece of software will integrate well with my existing hardware and workflows so that I can evaluate the tool's suitability for my needs.

- As a digital archivist, I want to know if I have the tools to work with a specific kind of media a donor is offering, so that I can determine the level of support I can provide for the material and decide whether or not to accept the donation.

## Factor: Logging

Log files can provide documentation and evidence to support a variety of objectives. A log file can serve as a record of processing steps, provide technical transfer details, encode metadata, and more.

Some tools do not provide a log as a default, but have logging capabilities in parameters, flags, or options. A log file may be intended to be human-readable or machine-readable. Some log files are intended for a particular purpose, such as being used as input for a specific tool. Structured data allows for more automated analysis and can be used as input to subsequent processing tools.

### Examples

While it is impossible to list all possible data that might be included in a log file, here are some examples:

- Checksum values (of media at source, of resulting disk image, of transferred data)

- Information about the media and/or the drive used during transfer

- Time elapsed during capture

- Time of image creation or copy operation

- Skipped and/or unreadable sectors

- Skipped files

- Structure of data on media

- The specific command invoked, including any options or parameters invoked

- Transfer history

- Preservation-centered metadata (e.g., PREMIS)

See [Appendix D: Log file samples](#appendix-d-log-file-samples)

### User stories

The following examples illustrate decisions related to this factor:

- As an accessioning archivist, I want a record of exactly what was transferred from original media or a networked storage location, and when it was, so I can document the chain of custody and prove that the files I acquired are the correct files and that they were transferred securely.

- As a media analyst, I want to know whether a piece of media had any unrecoverable regions, so I can document this for researchers so they understand that the files they are accessing may not be a complete copy of what was given to the archive.

- As a materials presentation preparer, I want to know whether any recoverable files were omitted from an extraction, and if so, why, such as PII recognition or known-file-signature recognition.

- As an archivist, I want records of whether anything was network-retrieved during the process (e.g., album art), and if so from where, because this could affect reproducibility and possibly security review.

- As a workflow architect, I want to review what tools (whether open source or commercial) are in use in the workflow and whether logs record the tool and version used so that I can know if a process was completed with a current or previous version of that tool.

- As a digital preservation specialist, I want actions to be logged using a specific metadata standard (e.g., PREMIS) so that I can have this output to store alongside assets in my preservation repository.

- As an archivist, I want a complete list of files that were virus-scanned and a description of the virus database version used in the scan, not just a summary statement that a given directory is safe, so that I can record this information at an item level in my digital asset management system.

## Factor: Output formats available

*Output* refers to the *objects* produced by the tool in the course of its regular function. Primarily, the output of a given tool is likely to be considered the *content* that the user wants to perform actions on, including metadata extraction, transformation, packaging, and transfer to a storage environment. Some tools have additional outputs, including logs, that are further described elsewhere in this guide.

One consideration when selecting a tool is what output formats are available. Some tools have multiple output options, while others may only have one output format. Along similar lines, there may be tool-specific definitions of output formats to be aware of; for example, IsoBuster refers to a 2,352 byte-per-sector image of a CD-ROM as "raw"; when selecting the "Linux dd raw image" format in Guymager on a CD-ROM, the output is a 2,048 byte-per-sector image. These distinctions may or may not be important for your workflow and subsequent processing. For example, you may prefer IsoBuster as the primary tool for acquiring data from CD-ROMs, but keep Guymager in your toolkit as a backup in case IsoBuster's output from a specific CD-ROM does not conform to your expectations.

While it is beyond the scope of this guide to compare specific output formats, considering the following questions may help guide you as you compare and select tools for object acquisition:

- Does your workflow include migration or emulation?

- What are your plans for providing access to this material?

- What do you know about your user base and their expectations for access?

- Do you plan on exploring or implementing an emulation program?

- Do you have the ability to access the logical files on a storage device?

- Are you working with removable media or materials transferred via a network or cloud storage solution?

### Examples

Some examples of the tools that produce different outputs:

- Raw disk image (e.g., .img, .dd, .001)

  - Kryoflux

  - Guymager

  - FTK Imager

  - ddrescue


- .iso

  - IsoBuster

  - Ddrescue

  - FTK Imager


- bin/toc/cue

  - Cdrdao

  - IsoBuster


- KryoFlux Stream files

  - Kryoflux


- Expert Witness Format forensically-packaged disk image

  - Guymager

  - FTK Imager


- TAR archive files

  - tar

  - 7-zip


- ZIP archive file

  - ZIP

  - 7-zip


- Logical files

  - rsync

  - Robocopy

  - Teracopy


See Factor: [Logging](#factor-logging)

### User stories

The following examples illustrate decisions related to this factor:

- As an accessioning or acquisition archivist, I want to create a disk image of a legacy storage media object, so that I can do additional work on the copy without returning to the source media, or so that I can mount it in an emulated computing environment.

- As an archivist investigating compression options to save on storage space, I want to use compression to store disk images, so that I minimize the storage footprint of born-digital materials.

- As an archivist, I want to acquire and preserve only the logical files identified by the donor, curator, or dealer so that I do not accidentally store sensitive, restricted, or otherwise nonpermanent files.

## Factor: Tool impacts

This factor pertains to the impact of a tool on the source material, including data and filesystem metadata, and the correspondence of the data source and destination post-processing actions.

Tool impact on source material refers to the effects that a tool has on material it interacts with. Different tools offer different levels of transparency regarding the effects they have on the material they're processing; that is, the actual actions of the tool may be more or less readily apparent to the end user. When evaluating your workflow, consider the set of properties you expect to remain the same prior to processing and after processing. While maintaining source file data fixity is often a requirement for digital archives capture or transfer workflows, you may also wish to maintain source filesystem metadata such as file timestamps, file owner and groups, and file paths.

Checking the correspondence of source and destination files refers to ensuring the transferred data and its filesystem metadata match those of the data source. Calculating checksums is one way to verify the correspondence between source and destination files. Some tools may provide this verification step automatically, while with other tools, these steps have to be initiated by the user. Some tools may calculate and compare checksums on both the source files and the destination files it generates; others may only calculate checksums on destination files, to be used for fixity checking going forward.

Additionally, some tools that copy content from one location to another may not preserve source filesystem timestamps at the destination.

### Examples

- Some tools used for accessioning, packaging and transfer may, on the same file system, copy files rather than move them, thereby creating new files on the same filesystem with new file metadata.

- On a Mac, one can use hdiutil to read-only mount many disk image files.

- Some tools may change the Date Created or Date Modified metadata of files they interact with.

- Some tools change the input itself and sometimes in ways that are opaque to the user. For example, when opening legacy binary Microsoft Office file formats in current Microsoft Office programs, those programs will add a date accessed value to the actual bitstream of the file, changing the checksum of the file.

### User stories

The following examples illustrate decisions related to this factor:

- As a digital preservation practitioner, I want to know if the tool I am using to copy data is verifying that the copies made from source or file location are identical, or if it is instead creating a fixity digest of the new copy for monitoring and verification of that copy going forward.

- As a digital archivist, I want to mount a disk image read-only without modifying the original, so that I can avoid modification and maintain provenance.

- As a digital preservation practitioner, I want to monitor the fixity of files in a directory over time so that I can ensure and document their integrity.

- As an operations manager, I want to be able to report that my chain of custody for materials received from a donor was reviewed at the beginning and end of processing (e.g., whether hashes were received, matched, and reviewed after processing), so that I can show that any descriptions made at the beginning of processing still pertain to the materials at the end of processing.

- As a digital preservation analyst, I want a tool which makes it clear when filesystem metadata or other elements of a file or disk image are modified so that I can ensure there were no alterations to content.

## Appendix A: Applying the Tool Selection Factors through narrative profiles

As institutional constraints and affordances range widely, DANNNG created this guide to be as context-neutral as possible so as to be applicable for the widest range of organizations and individuals. While complementary to tool registries that describe aspects of various tools, the DANNNG Tool Selection Factors is a stand-alone resource to aid in selection of tools for your particular workflows and context. To achieve this, we recommend that you reflect on your local situation and develop a scenario similar to the examples given below. Developing a narrative scenario may make it easier for you to determine and prioritize the criteria that are significant for you to achieve a successful outcome. Once you have a set of criteria, you can use them along with the factors in this guide to evaluate and select those tools that would work best for your individual and organizational context.

### Creating Your Narrative Profile

To help create your narrative profile, we suggest that you think about the following questions:

- What is your role? Does your interaction with born-digital materials make up your entire portfolio or a portion of it?

- What is your organizational context? Academic library; state, local, or federal government agency; independent non-profit, etc.?

- Who are the end users of your work? Will they need to interact only with the output of the tool(s) you select or with the tool(s) as well?

- What technological constraints are you working with? Do you have autonomy to select your own computing environments? What decisions does your institution impose upon you?

- What technological skill set do you, and anyone else who will be using the tool(s), have?

- What is your budget? Think about your budget for a one-time purchase as well as for ongoing license fees.

To help guide your narrative creation, you can use this template. The secondary points for each item are examples, which are discrete for each field and not intended to be a cohesive scenario if taken together. For examples of narratives and how to apply them to the Tool Selection Factors, see the [Example Narratives and Factors Use](#example-narratives-and-factors-use) section below.

- I work as a \[**role**\] in \[**describe organizational context**\].

  - I work as an archivist in a state historical society. My role is split between working with analog and digital materials.

  - I work as a digital archivist in a manuscript library. My role is entirely devoted to born-digital materials.

  - I work as a records manager in an institutional archives. My role is involved in the acquisition of analog and digital records.
<br>
- I want to \[**describe your goal**\] so that I can \[**describe the intended outcome, including any end users**\].

  - I want to capture data from internal hard drives so that I can  provide a copy of the data to curators and archivists for appraisal and processing. The curators and archivists will not need to interact with the capture tool, only with the resultant data.
<br>
- In particular, I need to \[**describe any specific details of your goal**\].

  - In particular, I need to ensure that I am creating a complete and accurate copy of the original, and need a tool that will provide logs or documentation to prove this.
<br>
- For technology, I \[**describe your technology environment and any constraints**\].

  - For technology, I use Windows operating system and have limited institutional IT support for my work. I need special authorization to have administrator privileges and must have all new software tools approved by my supervisor and IT.
<br>
- To ensure the technology fits my and my colleagues' skill sets, I \[**describe important tool features or aspects as they relate to skill sets**\].

  - To ensure the technology fits my and my colleagues' skill sets, I would prefer tools with graphical user interfaces, but could write procedures for tools with command line interfaces as long as there is easy-to-follow existing documentation.

  - To improve efficiency and reduce my and my colleagues' manual workload, I would prefer tools with command line interfaces that I could use in a script or other automated fashion.
<br>
- I have a budget of \[**describe your budget for technology purchasing or licensing**\].

  - I have a budget of $100 for initial purchase or ongoing annual license fees.

### Example Narratives and Factors Use

#### Narrative 1: Digital Archivist in an Academic Institution

I work as a digital archivist in a library at an academic institution; my role is entirely devoted to born-digital materials. I want to develop a suite of data capture tools so that I can have a consistent capture process that feeds data into my appraisal and processing workflows. After reviewing the [Disk Imaging Decision Factors](https://dannng.github.io/disk-imaging-decision-factors.html), I determined that I want to create raw disk images for some of my capture scenarios and logical transfers for others. In both cases, I need to prove that the copy I create is identical to the original source data. For technology, I am reliant on my organization's IT department for desktop support and am limited to Windows OS, however I have administrative privileges on the computer I use in my workflows. While I am comfortable using command line tools, to ensure the tool fits my colleagues' skill sets as well, I would prefer tools with intuitive graphical interfaces so they can participate in workflow actions as needed. I have a limited budget for this project and could make a proposal for a commercial license if needed.

Reviewing my narrative profile, I can create a list of criteria that are important for my tool selection:

- Build a suite of tools for consistent workflow inputs (implied: longevity of tools to avoid frequent tool cycling)

- Ability to create disk images and logical file outputs (may be separate tools)

- Provide proof that outputs are identical to the source inputs

- Maintain or document source file system metadata

- Run on Windows OS with or without administrator privileges

- Graphical user interface preferred, command line interface acceptable

- Limited monetary cost

I can then compare my criteria to selection factors, which will help guide my tool choice:

- Build a suite of tools for consistent workflow inputs

  - I don't want to have to frequently cycle which tools I use for a particular purpose, so the [Documentation and support](#factor-documentation-support-and-maintenance) factor may be important to understand the level of community support and developer maintenance of the tool.


- Ability to create disk images and logical file outputs

  - I will need to find a tool that can handle both types of outputs, or identify multiple tools to satisfy this criterion. I can start with the [Output formats available](#factor-output-formats-available) factor to understand how to review tools' output formats and then can see some additional examples in [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes). I'll also need to ensure that the tools I select work with a range of source media and data, which I can assess with the [Inputs](#factor-inputs) factor and [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets).


- Provide proof that outputs are identical to the source inputs

  - The [Logging](#factor-logging) and [Tool impact](#factor-tool-impacts) factors discuss information related to documenting proof that my outputs are identical to the source material. The [Documentation and support](#factor-documentation-support-and-maintenance) factor would be important for understanding whether a tool provides technical details and documentation on how it works.


- Maintain or document source file system metadata

  - This requirement is a bit more complex than it seems at first glance, and the following factors may help in my tool selection on this point: [Inputs](#factor-inputs), [Tool impact](#factor-tool-impacts), [Logging](#factor-logging), and [Documentation and support](#factor-documentation-support-and-maintenance). Additionally, [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets) may be useful. A key decision is whether I want to document the source file metadata or have that metadata maintained on the destination file system for the files after copy/transfer.
<br>
- Run on Windows OS with or without administrator privileges
<br>
- Graphical user interface preferred, command line interface acceptable

  - My system and interface requirements are well-defined here, but the [Interface](#factor-interface) and [Installation requirements and processes](#factor-installation-requirements-and-processes) factors may discuss other aspects to consider.
<br>
- Limited monetary cost

  - I should review the [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost) factor to ensure I don't spend time evaluating tools with large up-front costs or significant ongoing license fees.

#### Narrative 2: Archivist at a Local Historical Society

I work as an archivist at a local historical society where my role is split between analog and digital materials. I want to capture data from a set of USB flash media created by an amateur photographer so that I can provide access to the photographs and videos for my institution's patrons. After reviewing the [Disk Imaging Decision Factors](https://dannng.github.io/disk-imaging-decision-factors.html), I determined that logical transfer would be best for my use case as I will be preserving and providing access to individual files after minimal processing, and I don't have a lot of spare storage space for potentially larger disk images. For technology, I have access to both Windows and Mac operating system environments, but my organization doesn't have any formal IT support. I am not comfortable working with the command line and don't have a budget for tool implementation other than my time.

Reviewing my narrative profile, I can create a list of criteria that are important for my tool selection:

- Limited variety of source media or inputs (implied: one-time project or no attempt to build a larger workflow at this time)

- Ability to create logical files, as end goal is access for patrons and there is limited storage available (implied: output format should be one that can serve as both preservation and access copy)

- A tool that works on Windows or Mac with a graphical user interface required

- Easy for end-user to deploy without IT support

- No monetary cost

I can then compare my criteria to selection factors, which will help guide my tool choice:

- Limited variety of source media or inputs

  - I am not attempting to build a comprehensive set of workflows for digital formats, and should instead focus on tools that can work with USB flash media. Referring to the [Inputs](#factor-inputs) and [Lists compatible hardware](#factor-lists-compatible-hardware) factors may be good starting points for understanding my needs. [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets) will also be helpful.


- Ability to create logical files

  - I will be exporting logical files from the source media, so will need a tool that either only exports files or can export both disk images and logical files. While I could look at tools that create disk images and only store them temporarily, the limited storage capacity at my institution makes this less attractive. I will review the [Output formats available](#factor-output-formats-available) factor and [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes) to assess tools that are in scope.


- A tool that works on Windows or Mac with a graphical user interface required

  - My system and interface requirements are well-defined here, but the [Interface](#factor-interface) and [Installation requirements and processes](#factor-installation-requirements-and-processes) factors may discuss other aspects to consider.


- Easy for end-user to deploy without IT support

  - The [Documentation and support](#factor-documentation-support-and-maintenance) and [Installation requirements and processes](#factor-installation-requirements-and-processes) factors will help me think through the relative ease of deployment and use.


- No monetary cost

  - My requirement is well defined here, but the [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost) factor will help me identify information I may not be considering related to free or freemium software.

#### Narrative 3: Records Manager in a Corporate Archives

I work as a records manager in a corporate archives. My role requires me to assess digital records against my organization's retention schedule and to maintain active records, destroy records that have met their retention period, or transfer records of permanent value to the corporate archivist. I want a tool that facilitates my evaluation of records on network attached and cloud storage so that I can assess active records for retention without altering the originals. I then need a tool that can package and/or transfer files so that I can transfer permanent records to the archives. Additionally, for permanent records, I need to document file system metadata of the source material so that my organization can show who created the files, who had access, and the last time someone modified a file. For technology, I am reliant on my organization's IT department for desktop support, and have access to Windows environments. I am comfortable with the command line and could receive IT support for API implementation. I will be using these tools myself so I don't need to consider the skill sets of my colleagues in this case. For budget, licensing tools up to $2,500 per year is within scope, provided I can justify it to my department head.

Reviewing my narrative profile, I can create a list of criteria that are important for my tool selection:

- Ability to view files and structure on local network attached storage and cloud storage (implied: need a tool that can interpret a file system for network storage and, potentially, an object-based storage environment for cloud storage)

- Need to assess the files without altering the files or their file system metadata

- A tool that allows selective logical packaging and/or transfer of files

- Documentation of the original file system metadata (additional criterion to consider: if cloud storage is object based, need a tool that can interpret file-system-like metadata embedded in files)

- Tools that run on Windows with a GUI, CLI, or API

- A budget of $2,500 per year

I can then compare my criteria to selection factors, which will help guide my tool choice:

- Ability to view files and structure on local network attached storage and cloud storage (implied: need a tool that can interpret a file system for network storage and, potentially, an object-based storage environment for cloud storage)

  - My first task is to assess the files in their original storage locations. If the materials are on legacy media, information in the [Inputs](#factor-inputs) factor, as well as [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets), will help identify criteria related to this need. 
<br>
- Need to assess the files without altering the files or their filesystem metadata

  - As I need to ensure that my assessment does not alter the files or their file system metadata, reviewing the [Tool impact](#factor-tool-impacts) and [Documentation and support](#factor-documentation-support-and-maintenance) factors will help me assess tools against this criterion.
<br>
- A tool that allows selective logical packaging and/or transfer of files

  - The [Inputs](#factor-inputs) and [Output formats available](#factor-output-formats-available) factors, as well as [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes), can guide my selection of tools that allow for selection of files for logical packaging or transfer.
<br>
- Documentation of the original file system metadata (additional criterion to consider: if cloud storage is object based, need a tool that can interpret file-system-like metadata embedded in files)

  - My need for documentation of file system metadata may be met by my assessment or capture tool, or potentially another tool. I also need to assess tools for compatibility with object-based cloud storage. I can review the [Inputs](#factor-inputs), [Logging](#factor-logging), [Documentation and support](#factor-documentation-support-and-maintenance) factors to help me with this decision. [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets) and [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes) may be helpful as well. Additionally, the [Extensibility](#factor-extensibility) factor would be good to consider as there may be tools that have add-ons or plug-ins, or allow direct modification of the source code, to meet my needs.
<br>
- Tools that run on Windows with a GUI, CLI, or API

  - Using the [Interface](#factor-interface) and [Installation requirements and processes](#factor-installation-requirements-and-processes) factors will help me select tools that meet my technology requirements.
<br>
- A budget of $2,500 per year

  - With a well-defined budget, I can use the [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost) factor to assess tools against this criterion.

#### Narrative 4: Archivist in a State Archives

I work as an archivist in a state government archives. My role is predominantly working with digital materials, and involves preserving records in digital form and documenting their provenance. For records transferred on physical storage media, I determined that creating raw disk images would be best for all cases where it is technically possible so that I can have a standardized workflow for my team. We also increasingly transfer records from cloud or other networked storage and would need to conduct logical transfers in these cases. For technology, I am limited to a Windows environment and the archives must follow guidance from our IT department, which conducts a security review to determine if a tool is acceptable for our use as a government entity. For my team, I would prefer a tool with a graphical user interface, while I am comfortable using the command line as well. While I have a limited budget, IT's preference is for commercially-licensed software.

Reviewing my narrative profile, I can create a list of criteria that are important for my tool selection:

- I have two capture scenarios: I want to create raw disk images of storage media and I want to conduct logical file transfers from networked or cloud storage (implied: creating a faithful copy of the original is important to maintain the evidential, and potentially evidentiary, value of the records).

- My technology choices are limited to Windows-based tools that can pass a security review by our IT department.

- Preference for graphical user and command line interfaces to facilitate use by myself and colleagues.

- Limited budget, but commercial licensing likely preferred to open source.

I can then compare my criteria to selection factors, which will help guide my tool choice:

- I have two capture scenarios: I want to create raw disk images of storage media and I want to conduct logical file transfers from networked or cloud storage (implied: creating a faithful copy of the original is important to maintain the evidential, and potentially evidentiary, value of the records)

  - Having a single tool that can create both output types would make for an easier IT review, but having two tools fit to purpose may result in better archival outcomes. I can use the [Inputs](#factor-inputs) and [Output formats available](#factor-output-formats-available) factors, and [Appendix B: Tool inputs as compound input sets](#appendix-b-tool-inputs-as-compound-input-sets) and [Appendix C: (Some) tools and (their) purposes](#appendix-c-some-tools-and-their-purposes), to select tools that meet my needs in this area.
<br>
- My technology choices are limited to Windows-based tools that can pass a security review by our IT department

  - The need to pass an IT-security review is a non-negotiable part of tool selection in my role. Assessing tools using the [Installation requirements and processes](#factor-installation-requirements-and-processes), [Documentation and support](#factor-documentation-support-and-maintenance), [Logging](#factor-logging), [Extensibility](#factor-extensibility), and [Tool impact](#factor-tool-impacts) factors will be important for creating a short list of tools for IT's review.
<br>
- Preference for graphical user and command line interfaces to facilitate use by myself and colleagues

  - Having both a GUI and CLI would allow my team to have a graphical experience for ease of use while I could use the command line when it benefits my workflow. I'll use the [Interface](#factor-interface) factor to assess tools against this need.
<br>
- Limited budget, but commercial licensing likely preferred to open source

  - The [Developer, vendor, license, and cost](#factor-developer-vendor-license-and-cost) factor will be key to help me limit the scope of tool assessment to those that are likely to meet with IT approval.

## Appendix B: Tool inputs as compound input sets

The types of inputs that a tool can accommodate will help to define the scope of use cases for which the tool may be appropriate. Discrete inputs combine to create a compound input set with which a tool will interact. Assessing the discrete inputs to build a compound input set will help you determine which software tools will meet your use case.

Discrete inputs include:

- Media object
- Drive/reader
- Drive/reader controller and/or connector
- File system

Working through an example can be helpful to understand how to build compound input sets. We can identify a media object as a **5.25-inch floppy disk**. Reading the label shows that it is an **MS-DOS 1200k** disk (we'll come back to this in a moment). As it is a 5.25-inch floppy disk, we know that we will need a **5.25-inch floppy disk drive**. These drives require low-voltage power, separate data connections, and discrete **drive controllers**. We'll need a **power adapter** to convert from 120v to 12v/5v and a **4-pin Molex cable** to connect the adapter to the drive. We'll also need a specific type of **IDE data cable** to connect the drive to the floppy controller (NOTE: to ensure read-only functioning, we may need to change a physical setting on the floppy controller). Finally, we'll need a **USB cable** to connect the floppy controller to the computer. Now back to that disk label. As an MS-DOS 1200k disk, it is likely that the file system is in the **FAT** family. Additionally, 1200k disks require higher disk drive RPMs, so we'll need a floppy controller that allows us to change the drive RPM to 360 from the default value of 300.

This example leaves us with a compound input set of:

- 5.25-inch floppy disk
- 5.25-inch floppy disk drive
- 5.25-inch floppy disk drive controller
- 120v to 12v/5v power adapter
- 4-pin Molex cable
- IDE data cable (card edge 34-pin female to 34-pin female)
- USB cable (often USB 2.0 B male to A male)
- FAT file system family; MS-DOS 1200k

Using this compound input set, we can evaluate and rapidly narrow down our list of prospective tools, primarily based on the need for a tool that can run a 5.25-inch floppy disk drive and interpret the data on a 5.25-inch floppy disk. One tool that would meet the needs of this compound input set is the Kryoflux software tool (in conjunction with the Kryoflux floppy controller). We could use either its command line interface, which allows for the setting of multiple parameter values for capture, or its graphical user interface by making a modification of the MFM sector image to include the command to change drive RPM to 360.

A compound input set may contain many discrete inputs like our example or it may be much simpler (e.g., external hard disk drive, USB cable, exFAT file system). There can also be cases where you do not have all of the information you need to build your compound input set. In these cases, you may need an intermediate tool (such as a utility that can identify the file system) or you may need to rely on contextual information (such as finding a Wang word processing software disk as a clue that other disks in the collection may have been used on a Wang word processor).

### Input types

The following are examples of input types across data structures, media objects, and hardware.

Data structure
- File system
  - For floppy disks
    - FAT (multiple versions)
    - HFS, HFS+
    - Specialized file systems for word processors (e.g., DEC, Wang)
  - For optical discs
    - ISO9660
    - Joliet/Rock Ridge
    - UDF
  - For hard drives/network storage
    - NTFS
    - exFAT
    - APFS
- Object store

Media objects
- Magnetic media
  - Floppy disks (8, 5.25, and 3.5 inch)
  - Zip disks
  - Jaz disks
  - Hard disk drives (3.5-inch and 2.5-inch form factors; internal and external drives)
  - Data tape reels and cartridges

- Optical media
  - CDs (multiple types)
  - DVDs (multiple types)
  - MiniDiscs
  - Blu-Ray discs
  - SyQuest discs

- Flash memory media
  - Solid state drives
  - USB flash drives
  - Memory cards (SecureDigital \[SD\], CompactFlash \[CF\])

Drive/reader
- Floppy disk drive (8, 5.25, and 3.5 inch)
- Optical disc drive
- Memory card reader
- iomega Jaz disk drive
- iomega Zip disk drive
- USB input device

Drive/reader controllers
- FC5025
- Kryoflux

Connection type
- USB input device
- SATA
- eSATA
- IDE
- SCSI

## Appendix C: (Some) tools and (their) purposes

Generally, tools in our area of work can be categorized as supporting imaging media and analyzing and extracting data from them; packaging data and transferring data; and reporting and evaluating. More tools may be listed on the [COPTR registry](https://coptr.digipres.org/index.php/Main_Page).

### Imaging media

There are many tools that can be used for creating disk images in different formats and with different features, including:

- Brasero
- cdrdao
- FTKImager*
- GNU ddrescue
- Guymager
- HFSExplorer
- IsoBuster*

Note: Starred tools provide functionality that allow for the inspection of media (e.g., browse contents, identify file systems) prior to imaging.

There are tools that can be used for extracting data and properties from disk images, such as:

- disktype
- HFSUtils
- isoinfo
- sleuthkit

### Packaging and unpackaging data

There are tools that can be used to package content, such as:

- Bagger, python-bagit
- unar
- tar
- zip, unzip

### Transferring

There are tools that can be used for transferring content between storage devices, such as:

- Copy (with -a flag)
- rsync (with -a or -t flag)
- Teracopy
- robocopy

Note: Some tools have the same name on different platforms, so you should check the documentation for all flags and/or options before you use a tool in a production workflow.

### Reporting and evaluating

There are tools that can be used for assessing content and generating reports:

- ClamAV for virus scanning
- bulk_extractor for privacy scanning
- brunnhilde, to generate aggregate reports from multiple tools including Siegfried, bulk_extractor, ClamAV, tsk_recover, HFS Explorer, and fiwalk
- Walk_to_dfxml to generate DFXML from a directory listing
- tree for printing a directory structure
- Treesize for viewing a directory structure and assessing data usage, among other information.
- DROID and Siegfried for file format identification
- fslint, fdupes, jdupes, BeyondCompare, and FileMerge to identify duplicate files

## Appendix D: Log file samples

Not all tools provide log files of tool actions, and there can be varied
levels of detail in logs across tools that do. Below are sample logs .

### Guymager
```
GUYMAGER ACQUISITION INFO FILE
==============================

Guymager
========

Version          	: 0.8.8-3                                                                            	 
Compilation timestamp: 2019-02-20-15.50.35                                                                	 
Compiled with    	: gcc 8.2.0                                                                          	 
libewf version   	: 20140807 (not used as Guymager is configured to use its own EWF module)            	 
libguytools version  : 2.0.5                                                                              	 
Host name        	: computer-name                                                                      	 
Domain name      	: (none)                                                                             	 
System           	: Linux computer-name 5.4.0-100-generic #113-Ubuntu SMP Thu Feb 3 18:43:29 UTC 2022 x86_64


Device information
==================
Command executed: bash -c "search="`basename /dev/sr0`: H..t P.......d A..a de.....d" && dmesg | grep -A3 "$search" || echo "No kernel HPA messages for /dev/sr0""
Information returned:
----------------------------------------------------------------------------------------------------
   No kernel HPA messages for /dev/sr0

Command executed: bash -c "smartctl -s on /dev/sr0 ; smartctl -a /dev/sr0"
Information returned:
----------------------------------------------------------------------------------------------------
   smartctl 7.1 2019-12-30 r5022 [x86_64-linux-5.4.0-100-generic] (local build)
   Copyright (C) 2002-19, Bruce Allen, Christian Franke, www.smartmontools.org
   
   === START OF ENABLE/DISABLE COMMANDS SECTION ===
   unable to fetch IEC (SMART) mode page [scsi response fails sanity test]
   A mandatory SMART command failed: exiting. To continue, add one or more '-T permissive' options.
   smartctl 7.1 2019-12-30 r5022 [x86_64-linux-5.4.0-100-generic] (local build)
   Copyright (C) 2002-19, Bruce Allen, Christian Franke, www.smartmontools.org
   
   === START OF INFORMATION SECTION ===
   Vendor:           	TSSTcorp
   Product:          	DVD+-RW TS-H653G
   Revision:         	D200
   Compliance:       	SPC-3
   >> Terminate command early due to bad response to IEC mode page
   A mandatory SMART command failed: exiting. To continue, add one or more '-T permissive' options.

Command executed: bash -c "hdparm -I /dev/sr0"
Information returned:
----------------------------------------------------------------------------------------------------
   SG_IO: bad/missing sense data, sb[]:  70 00 00 00 00 00 00 0a 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
   
   /dev/sr0:
   
   ATA device, with non-removable media
   Standards:
  	 Likely used: 1
   Configuration:
  	 Logical   	 max    current
  	 cylinders    0    0
  	 heads   	 0    0
  	 sectors/track    0    0
  	 --
  	 Logical/Physical Sector size:       	512 bytes
  	 device size with M = 1024*1024:       	0 MBytes
  	 device size with M = 1000*1000:       	0 MBytes
  	 cache/buffer size  = unknown
   Capabilities:
  	 IORDY not likely
  	 Cannot perform double-word IO
  	 R/W multiple sector transfer: not supported
  	 DMA: not supported
  	 PIO: pio0

Hidden areas: unknown


Acquisition
===========

Linux device        	: /dev/sr0                                    	 
Device size         	: 54083584 (54.1MB)                           	 
Format              	: Linux split dd raw image - file extension is .xxx
Image path and file name: /home/username/Desktop/Test01.xxx	 
Info  path and file name: /home/username/Desktop/Test01.info    
Hash calculation    	: MD5, SHA-1 and SHA-256                      	 
Source verification 	: on                                          	 
Image verification  	: on                                          	 

During acquisition, 24773 bad sectors have been encountered. They have been replaced by zeroed sectors. The sector numbers are:
   300-11556, 12002-18758, 19204-25960, 26406-26407
During verification, 24773 bad sectors have been encountered. The sector numbers are:
   300-11556, 12002-18758, 19204-25960, 26406-26407
State: Finished successfully (with 24773 bad sectors)

MD5 hash               	: 35659ff9fdf25d394622b4e64368d08d                           	 
MD5 hash verified source   : 35659ff9fdf25d394622b4e64368d08d                           	 
MD5 hash verified image	: 35659ff9fdf25d394622b4e64368d08d                           	 
SHA1 hash              	: 71bd797e6fe66966d9fc96ac6bd83908d4994c79                   	 
SHA1 hash verified source  : 71bd797e6fe66966d9fc96ac6bd83908d4994c79                   	 
SHA1 hash verified image   : 71bd797e6fe66966d9fc96ac6bd83908d4994c79                   	 
SHA256 hash            	: 1562e71dc3e58e928cd230a312a76b17c979eb884a60e2725676d0e67c681309
SHA256 hash verified source: 1562e71dc3e58e928cd230a312a76b17c979eb884a60e2725676d0e67c681309
SHA256 hash verified image : 1562e71dc3e58e928cd230a312a76b17c979eb884a60e2725676d0e67c681309
Source verification OK. The device delivered the same data during acquisition and verification.
Image verification OK. The image contains exactly the data that was written.

Acquisition started : 2022-05-16 14:46:53 (ISO format YYYY-MM-DD HH:MM:SS)  
Verification started: 2022-05-16 15:21:28                              	 
Ended           	: 2022-05-16 15:55:58 (1 hours, 9 minutes and 5 seconds)
Acquisition speed   : 0.02 MByte/s (0 hours, 34 minutes and 35 seconds)	 
Verification speed  : 0.02 MByte/s (0 hours, 34 minutes and 29 seconds)	 


Generated image files and their MD5 hashes
==========================================

No MD5 hashes available (configuration parameter CalcImageFileMD5 is off)
MD5                           	Image file
n/a                           	Test01.000
```

### ddrescue
```
# Mapfile. Created by GNU ddrescue version 1.23
# Command line: ddrescue -n -b 2048 /dev/cdrom ddrescue_example.iso ddrescue.log
# Start time:   2022-05-16 14:32:09
# Current time: 2022-05-16 14:35:12
# Finished
# current_pos  current_status  current_pass
0x03394000     +               1
#      pos        size  status
0x00000000  0x00096000  +
0x00096000  0x00000800  -
0x00096800  0x015FC000  /
0x01692800  0x00000800  -
0x01693000  0x000DE000  +
0x01771000  0x00000800  -
0x01771800  0x00D32000  /
0x024A3800  0x00000800  -
0x024A4000  0x000DE000  +
0x02582000  0x00000800  -
0x02582800  0x00D32000  /
0x032B4800  0x00000800  -
0x032B5000  0x000DE000  +
0x03393000  0x00001000  -
```

### rsync
```
2023/01/13 14:34:24 [50721] receiving file list
2023/01/13 14:34:24 [50721] cd+++++++ sourcetest/
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/10_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/1_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/2_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/3_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/4_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/5_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/6_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/7_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/8_DOCUMENT.txt
2023/01/13 14:34:24 [50721] >f+++++++ sourcetest/9_DOCUMENT.txt
2023/01/13 14:34:24 [50721] sent 250 bytes  received 253 bytes  total size 21
2023/01/13 14:37:39 [50805] receiving file list
2023/01/13 14:37:39 [50805] sent 24 bytes  received 9 bytes  total size 0
2023/01/13 14:37:48 [50813] receiving file list
2023/01/13 14:37:48 [50813] .d..t.... sourcetest/
2023/01/13 14:37:48 [50813] >f.st.... sourcetest/5_DOCUMENT.txt
2023/01/13 14:37:48 [50813] >f..t.... sourcetest/9_DOCUMENT.txt
2023/01/13 14:37:48 [50813] sent 74 bytes  received 289 bytes  total size 21
```

## Endnotes
<b id="en1">1</b>. See the [Archivist's Guide to Kryoflux](https://github.com/archivistsguidetokryoflux/archivists-guide-to-kryoflux/tree/master?tab=readme-ov-file), winner of the [2018 DPC Award for Teaching and Communications](https://www.dpconline.org/events/digital-preservation-awards/digital-preservation-awards-2018), as an example of a user-developed tutorial.

<b id="en2">2</b>. For more information, [Wikipedia maintains a listing of software licenses and types of licenses](https://en.wikipedia.org/wiki/Software_license).

## Acknowledgements

The following people contributed to this document:

- Joe Carrano, MIT Libraries (ORCID: [0000-0003-2218-5838](https://orcid.org/0000-0003-2218-5838))
- Alex Chassanoff, UNC Chapel Hill, School of Information and Library Science
- Dianne Dietrich, Cornell University Library (ORCID: [0000-0002-0009-8736](https://orcid.org/0000-0002-0009-8736))
- Brian Dietz, NC State University Libraries (ORCID: [0000-0001-7190-2755](https://orcid.org/0000-0001-7190-2755))
- Brenna Edwards, Harry Ransom Center, The University of Texas at Austin
- farrell, Duke University Libraries (ORCID: [0000-0003-1502-2651](https://orcid.org/0000-0003-1502-2651))
- Lara Friedman-Shedlov, University of Minnesota (ORCID: [0000-0001-9573-2826](https://orcid.org/0000-0001-9573-2826))
- Dillon Henry, Georgia Tech
- Elizabeth-Anne Johnson, University of Calgary Libraries and Cultural
  Resources
- Alex Nelson, National Institute of Standards and Technology (ORCID: [0000-0002-3771-570X](https://orcid.org/0000-0002-3771-570X))
- Keith Pendergrass, Harvard Business School
- Alice Sara Prael, Yale University Libraries
- Carolina Quezada Meneses, Mike Kelley Foundation for the Arts
- Jonas Rosland, Hit Save!
- Elise Tanner, UA Little Rock Center for Arkansas History and Culture
- Andréa Tarnawsky, Special Collections and Rare Books, Simon Fraser University
- Tyler Thorsted, Brigham Young University (ORCID: [0000-0003-0292-0962](https://orcid.org/0000-0003-0292-0962))
- Christina Velazquez Fidler, The Bancroft Library, University of California, Berkeley
- Lauren Work, Yale University Libraries
- Jacob Zaborowski, Getty Research Institute

We are grateful for the feedback from the members of the community that shaped this resource.

version is 1.0.0