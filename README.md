# StoryTeller

StoryTeller was a partwork series from the early eighties published in the UK and around the world.  This project is to create map/index files in JSON format that describes the PDF/MP3 collections and to provide code/applications in order to consume these files and display them.

It is in the very early stages and progress will not be super-fast - it is also a very niche project for a specific group of nostalgic folks who loved these stories as children and want to continue enjoying them and sharing them with their families! :)

## Index/Map File Format

This will get a full description once it has stabalized.  For now it basically indicates the name of the files expected for the PDF and MP3s, it also has hashes of the files.  I still need to find out if there are multiple versions of the collections floating around.  I have included hashes so the specific files for the index can be confirmed, this may help with identification later if there are multiple file versions.

Each page within the PDF is described and tagged with story information such as the reader of the story, the PDF page number and the contents specific page number.  There is also information on whether it is part of a multi-part story so in future the stories could be organized together into one long story.

The most complicated (and in need of the most changes) is the sound section, this indicates which mp3 to use and whereabouts the reading starts for the specific page. At the moment only minutes and seconds are specified, this will need to be adjusted to include milliseconds to give more precise page breaks.  Also, in the original sounds files there is a *ding* for the end of a pair of pages, but not for a single page.

Am also including within the sound section some instructions as to what to do if the sound range is reached, this can give hints to the application reading the file as to what should happen, for the front cover for example, if the intro music ends we can loop it, for the end of a page we can auto turn the page or just stop playing.
