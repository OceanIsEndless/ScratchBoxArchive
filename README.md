# ScratchBox Archive

This repo has the goal of periodically saving all publicly available user-generated content from [ScratchBox](https://github.com/ScratchEverywhere/ScratchBox) for archival purposes.

## Why?

The following reasons are probably good ones:

* If the ScratchBox server fails or database corrupts, projects and metadata remain safe until service is restored. (Unlikely, but possible.)
* Projects could be edited, made private, or deleted at any time, so having an active archive helps preserve them. (Could also happen.)
* Why not? There's no harm in it. Archivees are made every few and far between, consist solely of public data, and do not cause any noticeable strain on the server.
* Because... lost media? ¯\\\_(ツ)\_/¯

## Efforts

The following two methods are currently employed to archive ScratchBox:

- Automatically running [Save Page Now](https://web.archive.org/save) on ScratchBox web pages every few hours using [GitHub Actions](https://github.com/OceanIsEndless/ScratchBoxArchive/actions) (saves website)
- Manually downloading all public user data via the ScratchBox API and uploading it to the Internet Archive (saves projects)

### Website

A GitHub Actions workflow in this repository is set to run every six hours or so. It asks the [Internet Archive](https://archive.org/) to save various pages on the ScratchBox website, if possible. This way, a history of ScratchBox is automatically built up over time!

### Projects

Every once in a while, a backup (i.e. archive) will be made of all public ScratchBox project and user data. This is currently created manually on my computer using an automated script. This is because Cloudflare (a system providing security for ScratchBox) seems to block requests for projects from both Save Page Now _and_ GitHub Actions.

> I'm sure that there's a way to make it work, and that way would be preferred if it were reliable as it would require no intervention from me, but for now me pressing a button every once in a while is the best solution available.

The backup is then [uploaded to the Internet Archive](https://archive.org/search?query=creator%3A%22ScratchBox%22&sort=-publicdate) as a file for safekeeping. (Saving it in this repo was considered, but Git storage limits are too constraining.)

Each archive is a .zip file, at minimum 120MB in size. (This is primarily due to large assets contained within downloaded project files, and archive sizes will only grow bigger as more projects are added.)

Once unzipped, an explanation of how it is structured can be found inside (`README.md`). You can then do with the data as you please, though do be mindful that this is for archival purposes only and should not be used for anything with malicious intent or otherwise bearing negative consequences.

| Date (ISO 8601 GMT) | Size   | Places saved                                                   |
|---------------------|--------|----------------------------------------------------------------|
| 2025-09-13 16:06:50 | 133.7M | [Internet Archive](https://archive.org/details/sba-1757779610) |
| 2025-09-13 09:19:31 | 123.4M | [Internet Archive](https://archive.org/details/sba-1757755171) |

#### Is saving people's projects allowed?

I'm not sure if anyone cares about their projects being preserved. However, if so, I would like to say that projects are only archived if:

* They are set to public **OR** the project link has been shared and added for archival (private projects cannot be found if they are not linked to or shared publicly in any way, so user privacy remains secure)
* They have been up for a few hours (the archive does not run constantly, so a user can still change their mind about publishing a project on ScratchBox well before it can be found and saved)
* You upload them in the first place (nothing is ever truly gone from the Internet, so by uploading it to an external server you do already kind of allow your project to be accessed by third parties)

If a project contains sensitive information or you want it removed for whatever reason, you can ask me and I will manually remove the project from the archive. However, it does take effort to do this (all archives containing the project will have to be reuploaded), and I wish to save as many projects as possible, so there should be a serious reason to have it removed from the archive other than something insignificant like "it's buggy" (no project is perfect, and past project versions could come in handy) or "cringe" (hopefully no one is out to judge your archived project). I can also just omit it from _future_ archives if you would settle for leaving previous archives untouched.

#### Will private ScratchBox projects be archived?

**No.** Not only is the ScratchBox API designed with privacy in mind (private projects cannot be found without their link, IDs are completely randomized), but your projects are your projects, and if you make them private and keep them private, then they will not be archived here.

..._However,_ that being said, if you happen to share the link to your project with others somewhere public (on a Scratch Everywhere! GitHub repo, the SE! Discord server, or a related platform) then I _might_ add your project to a list for archival. The list is in this repo under [`IDs.txt`](https://github.com/OceanIsEndless/ScratchBoxArchive/blob/main/IDs.txt). They are archived just to ensure that as many projects as are known of and could have future significance are archived as possible. If you would like your project removed from this list, I can do that, but again, there should be a serious reason for it to not be archived.

#### Will projects outside of ScratchBox be archived?

No... yes? Maybe. Not really. The main goal of this project is to archive ScratchBox. I have been running Save Page Now on some projects linked to on the Scratch Everywhere! repo and Discord (project hosted on services that could potentially fail or vanish), but I do not really see a reason to save any other projects, and if someone wants to let their project disappear to time then it is their prerogative.

To be honest, archiving ScratchBox is already somewhat questionable and a little unnecessary, so trying to archive more random projects would probably be... more questionable and unnecessary? Let's just say I do not need this to become the next ScratchDB. It was just a little thing to make sure there's backups of ScratchBox out there, somewhere. That's all.
