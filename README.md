# ProtégéVOWL – Community Maintained Release

[![GitHub release](https://img.shields.io/github/v/release/yourusername/ProtegeVOWL?label=Latest%20Release)](https://github.com/yourusername/ProtegeVOWL/releases/latest)
[![Build Status](https://github.com/yourusername/ProtegeVOWL/actions/workflows/maven.yml/badge.svg)](https://github.com/yourusername/ProtegeVOWL/actions)
[![License](https://img.shields.io/badge/License-AGPL%203.0-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

This is a **community-maintained fork** of the original ProtégéVOWL plugin (Visual Ontology Modeling Language viewer inside Protégé).

### Why this fork exists

The original project website http://vowl.visualdataweb.org/ has been defaced and is now permanently redirecting to a gambling site (as of 2025).  
The original GitHub repository https://github.com/VisualDataWeb/ProtegeVOWL contains only source code — **no pre-built JAR releases were ever published**.

Because many people still need VOWL visualization inside Protégé desktop, this fork provides:

- Ready-to-download JAR files in GitHub Releases
- Automated builds via GitHub Actions
- Minor fixes to make it compile and run smoothly on modern Protégé 5.6+ and Java 11–21
- Up-to-date build instructions

### Download (Latest Release)

Go to → https://github.com/gbasilveira/ProtegeVOWL/releases/latest  
Download `target/vowl-0.1.4-SNAPSHOT.jar` and drop it into your Protégé `plugins/` folder.

### Quick Installation

1. Download the latest `ProtegeVOWL-*.jar` from the Releases page.
2. Copy it to `<Protégé-installation-folder>/plugins/`
3. (Re)start Protégé
4. Go to **Window → Tabs → VOWL** to enable the tab

### Building from Source (if you prefer)

```bash
git clone https://github.com/yourusername/ProtegeVOWL.git
cd ProtegeVOWL
mvn clean package


___



ProtégéVOWL 
===========

Source code of the VOWL plugin for Protégé.

Note that ProtégéVOWL has some knwon has some known bugs and does not implement all visual elements defined in the VOWL specification.
A more complete implementation of VOWL is provided by the web application [WebVOWL] (https://github.com/VisualDataWeb/WebVOWL).

See http://vowl.visualdataweb.org for more information on ProtégéVOWL and WebVOWL.

## Developer Setup

### Requirements
Java JDK is required for the ProtégéVOWL build.

### Eclipse Setup
There are several options if you want to use Eclipse as IDE. You need to select the 
``Import`` within Eclipse and select the ``Maven``, ``Existing Maven Projects`` option and select the ProtégéVOWL Git Repository. Eclipse will automatically suggest to import ``pom.xml``
 
### Maven Build
Some steps are required to build ProtégéVOWL with Maven. If you use Eclipse you need to run the ``pom.xml`` as Maven build and you may need to select JDK as Alternate JRE.
In addition you need to add the goals ``clean compile package``. You will find the compiled packaged within the target folder.

### Copy to Protege
To copy the build result to your Protégé installation you need to add ``install`` to your maven goals.
In addition you have to add the parameter ``protege.home`` which leads to your Protégé installation.
If you remove the ``install`` goal the build result is not copied to Protégé.
