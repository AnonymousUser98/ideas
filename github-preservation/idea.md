---
title: GitHub Preservation Tool
permalink: /github-preservation/
---

# GitHub Preservation Tool

This program would make it easy to download GitHub repositories in a format suitable for content preservation.


## File Format

Downloaded repositories would be stored in a **Git Preservation Container** file, which would use the `.grpc` file extension (which stands for _Git Repository Preservation Container_). It's basically a renamed 7Z file, but with a different compression algorithm. It uses a modified version of LZMA2 that's optimized for Git repositories.

### Directory Structure

<!-- URL: https://utilitycove.com/tools/folder-structure-generator?s=eyJSZXBvTmFtZS43eiI6eyJtZXRhLnhtbCI6bnVsbCwiYnJhbmNoZXMiOnsibWFzdGVyIjp7IjxyZXBvIGZpbGVzPiI6bnVsbH0sImRldiI6eyI8cmVwbyBmaWxlcz4iOm51bGx9fSwicmVsZWFzZXMiOnsicmVsZWFzZXMueG1sIjpudWxsLCJkZXNjcmlwdGlvbnMiOnsidjAuOS4wLXByZTEubWQiOm51bGwsInYxLjAuMC5tZCI6bnVsbCwidjEuMC4xLm1kIjpudWxsLCJ2MS4wLjIubWQiOm51bGx9LCJ2MS4wLjAiOnsicHJvZ3JhbS13aW5kb3dzLmV4ZSI6bnVsbCwicHJvZ3JhbS13aW5kb3dzLXBvcnRhYmxlLnppcCI6bnVsbCwicHJvZ3JhbS1saW51eC5BcHBJbWFnZSI6bnVsbH0sInYxLjAuMiI6eyJwcm9ncmFtLXdpbmRvd3MuZXhlIjpudWxsLCJwcm9ncmFtLXdpbmRvd3MtcG9ydGFibGUuemlwIjpudWxsLCJwcm9ncmFtLWxpbnV4LkFwcEltYWdlIjpudWxsfX0sInVwc3RyZWFtIjp7IjAiOnsibWV0YS54bWwiOm51bGwsImJyYW5jaGVzIjp7Im1hc3RlciI6eyI8cmVwbyBmaWxlcz4iOm51bGx9fX0sIjEiOnsibWV0YS54bWwiOm51bGwsImJyYW5jaGVzIjp7Im1hc3RlciI6eyI8cmVwbyBmaWxlcz4iOm51bGx9LCJvbGQiOnsiPHJlcG8gZmlsZXM%2BIjpudWxsfX19fSwid2lraSI6eyI8d2lraSBmaWxlcz4iOm51bGx9LCJjb250cmlicyI6eyIxIjp7IjxmaWxlcyBmb3IgUFIvaXNzdWUgIzE%2BIjpudWxsfSwiMiI6eyI8ZmlsZXMgZm9yIFBSL2lzc3VlICMyPiI6bnVsbH19fX0%3D -->

```
└── RepoName.7z/
    ├── meta.xml
    ├── branches/
    │   ├── master/
    │   │   └── <repo files>
    │   └── dev/
    │       └── <repo files>
    ├── releases/
    │   ├── releases.xml
    │   ├── descriptions/
    │   │   ├── v0.9.0-pre1.md
    │   │   ├── v1.0.0.md
    │   │   ├── v1.0.1.md
    │   │   └── v1.0.2.md
    │   ├── v1.0.0/
    │   │   ├── program-windows.exe
    │   │   ├── program-windows-portable.zip
    │   │   └── program-linux.AppImage
    │   └── v1.0.2/
    │       ├── program-windows.exe
    │       ├── program-windows-portable.zip
    │       └── program-linux.AppImage
    ├── upstream/
    │   ├── 0/
    │   │   ├── meta.xml
    │   │   └── branches/
    │   │       └── master/
    │   │           └── <repo files>
    │   └── 1/
    │       ├── meta.xml
    │       └── branches/
    │           ├── master/
    │           │   └── <repo files>
    │           └── old/
    │               └── <repo files>
    ├── wiki/
    │   └── <wiki files>
    └── contribs/
        ├── 1/
        │   └── <files for PR/issue #1>
        └── 2/
            └── <files for PR/issue #2>
```


### Specific Files/Folders

Click on a file name to view more details.

<dl>
    <dt><b><a href="file-details/meta.xml.md">meta.xml</a></b></dt>
    <dd>Contains various information about the repo.</dd>
    <!---->
    <dt><b>releases/</b></dt>
    <dd>Contains a subfolder for each release included in the archive. You can choose to only include specific releases to reduce file size. Only selected releases will be fully downloaded and stored, but metadata, tag information, and release descriptions will be stored for all releases. A subfolder is created for each release that gets included in the archive. Non-archived releases still get metadata entries and description files.</dd>
    <!---->
    <dt><b>releases/releases.xml</b></dt>
    <dd>Contains information about releases, including names, dates, labels, tags, and points in the Git history where the release's source code appears.</dd>
    <!---->
    <dt><b>releases/descriptions/</b></dt>
    <dd>Contains the descriptions of all releases. Each release's description is stored as a Markdown file.</dd>
    <!---->
    <dt><b>releases/[ReleaseName]/</b></dt>
    <dd>Contains all binaries and other files in the release.</dd>
    <!---->
    <dt><b>upstream/</b></dt>
    <dd>If the repo being archived is a fork, the upstream repo(s) will be archived as well. For more details, look at the <i>Upstream</i> section of this page.</dd>
    <!---->
    <dt><b>wiki/</b></dt>
    <dd>If the repo contains a wiki, it will be included in the archive and stored in this folder. Edit history is saved as well.</dd>
    <!---->
    <dt><b>contribs/</b></dt>
    <dd>There's an option to store issues and pull requests in the archive. If enabled, issues and PRs will be stored in this folder. I don't know what format would be used.</dd>
</dl>
