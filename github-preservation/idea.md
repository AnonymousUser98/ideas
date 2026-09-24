---
title: GitHub Preservation Tool
permalink: /github-preservation/
---

# GitHub Preservation Tool

This program would make it easy to download GitHub repositories in a format suitable for content preservation.


## File Format

Downloaded repositories would be stored in a **Git Preservation Container** file, which would use the `.grpc` file extension (which stands for _Git Repository Preservation Container_). It's basically a renamed 7Z file. It uses the same LZMA2 compression, has the same compression level settings as 7-Zip, and would be openable in any program that can read 7Z files.

### Directory Structure

<!-- INSERT HERE -->


### Specific Files/Folders

Click on a file name to view more details.

<dl>
    <dt><a href="file-details/meta.xml.md">meta.xml</a></dt>
    <dd>Contains various information about the repo.</dd>
    <!---->
    <dt>releases/</dt>
    <dd>Contains a subfolder for each release included in the archive. You can choose to only include specific releases to reduce file size. Only selected releases will be fully downloaded and stored, but metadata, tag information, and release descriptions will be stored for all releases. A subfolder is created for each release that gets included in the archive. Non-archived releases still get metadata entries and description files.</dd>
    <!---->
    <dt>releases/releases.xml</dt>
    <dd>Contains information about releases, including names, dates, labels, tags, and points in the Git history where the release's source code appears.</dd>
    <!---->
    <dt>releases/descriptions/</dt>
    <dd>Contains the descriptions of all releases. Each release's description is stored as a Markdown file.</dd>
</dl>
