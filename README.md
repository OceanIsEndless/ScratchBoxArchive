# ScratchBox Archive

This repo periodically saves all publicly available user-generated content from [ScratchBox](https://github.com/ScratchEverywhere/ScratchBox) in the [Internet Archive](https://archive.org/details/@endless_ocean/lists/1/scratchbox-data-backups?sort=-publicdate) for historical purposes.

## Why?

The following reasons are probably good ones:

* If the ScratchBox server fails or database corrupts, projects and metadata remain safe until service is restored. (Unlikely, but possible.)
* Projects could be edited, made private, or deleted at any time, so having an active archive helps preserve them. (Could also happen.)
* Why not? Archives are made few and far between, consist solely of public data, and do not cause any noticeable strain on the server.
* Because... lost media? ¯\\\_(ツ)\_/¯

## How do I use this?

* If you want to see what the ScratchBox website looked like at a previous date, use the [Wayback Machine](https://web.archive.org/https://scratchbox.grady.link/explore).
* If you want to download older versions of projects or any relevant metadata, see the [data backups](https://archive.org/details/@endless_ocean/lists/1/scratchbox-data-backups?sort=-publicdate).

## I don't want my project here!

Chill.

* If your project is private and you have not shared its link publicly, it is not here.
  * Private projects are inaccessible without their link.
* If your project is public or you have shared its link with others, then it _might_ be here. BUT:
  * Remember, this is just a backup of ScratchBox.
    * By uploading and sharing your project online, you've already allowed it to be saved by third parties, such as this archive.
  * Removing your project from the Internet Archive is a rather cumbersome process.
    * I can remove it, but there's not much of a point in it unless you have a serious reason.

So don't worry about it! This archive is just a backup of ScratchBox, which you've already freely uploaded your project to. Nothing bad is going to happen as a result of your project being available in an archived state.

## How does this work?

### Website

A GitHub Action in this repo is scheduled to send requests to the Internet Archive to save pages on the ScratchBox website approximately every six hours. This helps keep a regularly updated record of what was on the website at any given time.

### Projects

Backups of ScratchBox projects and relevant data are created using an automated script (Apple Shortcut) on my computer. It goes through a [list](https://scratchbox.grady.link/api/projects) provided by the ScratchBox API to discover publicly available projects and download them into organized folders. It puts all the data into a .zip file, which I then upload to the Internet Archive.

> [!NOTE]
>
> I have not fully automated the process of backing up the projects, so data backups may be more sparse and far between. Uploading them manually works in the short-term, but if ScratchBox gets bigger then I may not be able to keep up. 🤔

## Disclaimer

This is not endorsed by ScratchBox, Scratch Everywhere!, or their respective contributors. It's just an archive.

