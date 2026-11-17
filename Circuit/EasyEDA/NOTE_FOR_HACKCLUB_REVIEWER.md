Note (mostly for HackClub reviewers):

Getting a ".epro" file seemingly not possible; this .zip was exported from the online EasyEDA viewer.
This is supposed to be the replacement of a .epro file, but even EasyEDA's own docs are wrong here.

---------------------------------

Message I gave in #forge-checkpoint on slack in response to the missing files:

"
[...] after hours and hours of looking, I couldn't find an export for a .epro. Not in online or offline mode, not on Windows or Linux, not with AI help. Even some of EasyEDA's docs seem to be wrong and outdated (like this one, though it IS for EasyEDA Pro: https://prodocs.easyeda.com/en/faq/import-export/), while others that seem to be newer just show how to export the file source (this one: https://docs.easyeda.com/en/Export/Export-EasyEDA-Source-File/index.html).

The best I could do was go to EasyEDA's online page, which according to AI, was supposed to give me .epro when I downloaded it, but it just gave me a .zip with the exact same .json files that it gave me during a desktop app download. So I put that Zip into OpenApolloV2/Circuit/EasyEDA on github, named "OpenApolloV2.zip", and I even included a note.md to try to explain it. I also uploaded 2 files to OpenApolloV2/Circuit/Schematic, one I exported from EDA via: File/Export/EasyEDA, and one I exported via: File/File source.
"
