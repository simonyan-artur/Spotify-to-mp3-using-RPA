# RPA UiPath
The goal of this project is to create a collection of mp3 songs files from the “Liked Songs” playlist in the Spotify user account. The process consists of three distinct parts:
- scrap somgs info (artist - title) from Spotify web app (https://open.spotify.com/)
- find song video links in the web
- convert video links to the mp3 and download.
To run this project user needs to have installed UiPath Studio (https://download.uipath.com/beta/UiPathStudioSetup.exe) and Chrome with UiPath extension enabled (https://docs.uipath.com/studio/docs/extension-for-chrome). Spotify credentials must be stored in the UiPath Orchestrator Asset under the name "SpotifyCredential". To have more control over the process, the option “Ask where to save each file before downloading” should be enabled in the Chrome settings (https://support.google.com/chrome/answer/95759?co=GENIE.Platform%3DDesktop&hl=en). 
Process asks user about the desired number of songs need to be retrieved and processed (note - 0 means without limit).
To find the most relevant link for user's Artist - Title pair, program calculates similarity of user's query and search results and choses the one with highest similarity score.
To convert video link to mp3 program uses online service YouTube2Mp3 (https://ytmp3.cc).
To track the workflow of the program and troubleshoot problems, a log file is prepared in Excel format, which contains information about errors and workflows that cause them.
Thanks.

