# ScratchBox Archive

This repo has the goal of periodically saving all publicly available user-generated content from [ScratchBox](https://github.com/ScratchEverywhere/ScratchBox) for archival purposes.

## Archives

Every once in a while, a backup will be created of all public ScratchBox project and user data. It is then uploaded to the [Internet Archive](https://archive.org/search?query=subject%3A%22ScratchBox+Archive%22) for safekeeping. (Saving it in this repo was considered, but Git storage limits are too constraining.)

Each backup is a .zip file, usually at minimum 120MB in size. (This is primarily due to large assets contained within downloaded project files, and the size of the archive will only get bigger over time as more projects are uploaded to ScratchBox, unless there is a data loss of some sort which would be unfortunate.)

Once unzipped, an explanation of how it is structured can be found inside as `README.md`. You can then do with the data as you please, though do be mindful that this is for archival purposes only and should not be used for anything with malicious intent or otherwise bearing negative consequences.

| Date (ISO 8601 GMT) | Size   | Places saved                                                   |
|---------------------|--------|----------------------------------------------------------------|
| 2025-09-13 16:06:50 | 133.7M | [Internet Archive](https://archive.org/details/sba-1757779610) |
|  2025-09-13 9:19:31 | 123.4M | [Internet Archive](https://archive.org/details/sba-1757755171) |

## Why?

~~Why not?~~ The following reasons are probably good ones:

* If the ScratchBox server fails or database corrupts, projects and metadata remain safe in this archive until it can be restored. (Unlikely secenario, but certainly possible.)
* Projects could be edited, made private, or deleted at any time, so having an active archive helps preserve them. (The real reason why, really.)
* Because... lost media?

## Is this allowed?

I'm not sure if anyone cares about their projects being preserved. However, if so, I would like to say that projects are only archived if:

* They are set to public OR the project link has been shared and added for archival (private projects cannot be found if they are not linked to or shared publicly in any way, so user privacy remains secure)
* They have been up for a few hours (the archive does not run constantly, so a user can still change their mind about publishing a project on ScratchBox well before it can be found and saved)
* You upload them in the first place (nothing is ever truly gone from the Internet, so by uploading it to an external server you do already kind of allow your project to be accessed and saved)

If a project contains sensitive information or you want it removed for whatever reason, you can ask me to and I can manually remove the project from the archive. Though I do wish to hold onto as many projects as possible, so there should be a serious reason to have it removed from the archive other than something insignificant like "it's buggy."
