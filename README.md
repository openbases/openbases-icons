# Open Bases Icons

 - [Preview the icons](https://openbases.github.io/openbases-icons/preview)
 - [Use the API](#open-bases-icons-api)
 - [Create your own API](#create-your-own-icon-api)

These fun, beautiful sets of images can be used as placeholders for generated
PDFs and other content used by the openbases! The idea is to provide them in
a separate repository so the primary repos don't need to each serve the files.
The author of most of these icons is Freepick, and each folder
coincides with a particular icon collection on the site. Specific links and 
attributions are contained within. Thank you Freepik for this invaluable
resource to make science a little more fun!

## Open Bases Icons API

### Python API

For a quick python wrapper to use the API, 
see [openbases-python](https://openbases.github.io/openbases-python/html/usage.html#icons).

### Command Line API

There is a simple API served by the repository to make it easy for you to
programmatically get an icon! If you look at the base, you can see there
is an endpoint for text, and for json:

```bash
$ curl https://openbases.github.io/openbases-icons/
{
  "icons": {
    "text": "https://openbases.github.io/openbases-icons/icons.txt",
    "json": "https://openbases.github.io/openbases-icons/icons.json",
    "svg": "https://openbases.github.io/openbases-icons/svg.json"
   }
}
```

If you then parse each endpoint, you get the expected format! Each serves a list
of icons, and that's it. Here is a list of files ([icons.txt](https://openbases.github.io/openbases-icons/icons.txt)):

```bash
$ curl https://openbases.github.io/openbases-icons/icons.txt
https://openbases.github.io/openbases-icons/ic/openjournals/joss-logo.png
https://openbases.github.io/openbases-icons/ic/openjournals/jose-logo.png
https://openbases.github.io/openbases-icons/ic/iconarchive/tuxlets/zwartepiettux2.svg.png
https://openbases.github.io/openbases-icons/ic/iconarchive/tuxlets/yellowtux2.svg.png
https://openbases.github.io/openbases-icons/ic/iconarchive/tuxlets/wizzardtux2.svg.png
https://openbases.github.io/openbases-icons/ic/iconarchive/tuxlets/wintertux2.svg.png
...
https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/clipboard-icon.png
https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/briefcase-bag-icon.png
https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/archive-folders-icon.png
```

And here is the equivalent for [icons.json](https://openbases.github.io/openbases-icons/icons.json):

```bash
curl https://openbases.github.io/openbases-icons/icons.json

["https://openbases.github.io/openbases-icons/ic/flaticon/in-the-zoo/penguin.png",
"https://openbases.github.io/openbases-icons/ic/openjournals/joss-logo.png",
"https://openbases.github.io/openbases-icons/ic/openjournals/jose-logo.png",
"https://openbases.github.io/openbases-icons/ic/iconarchive/tuxlets/zwartepiettux2.svg.png",
"https://openbases.github.io/openbases-icons/ic/iconarchive/tuxlets/yellowtux2.svg.png",
...
"https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/color-catalog-icon.png",
"https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/clipboard-icon.png",
"https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/briefcase-bag-icon.png",
"https://openbases.github.io/openbases-icons/ic/iconarchive/office-set/archive-folders-icon.png",
"https://openbases.github.io/openbases-icons/ic/flaticon/in-the-zoo/penguin.png"]
```

If you then parse each endpoint, you get the expected format! Each serves a list
of icons, and that's it. Here is a list of files ([icons.txt](https://openbases.github.io/openbases-icons/icons.txt)):

## Random Selection

### Bash

To select an icon using bash:

```bash
OPENBASES_ICONS=(`curl https://openbases.github.io/openbases-icons/icons.txt`)
OPENBASES_ICON=${OPENBASES_ICONS[$RANDOM % ${#OPENBASES_ICONS[@]} ]}
echo "${OPENBASES_ICON}"
wget ${OPENBASES_ICON} -O myicon.png
```

# Create Your Own Icon API

You simply need to:

 1. Fork this repository, and then put icons (svg and png supported) in subfolders
of [ic](ic). E
 2. Edit the [_config.yml](_config.yml) to be specific for your Github repository and site.
 3. Push to Github, and turn on Github Pages to deploy from master.

If you have any more questions, please [open an issue](https://www.github.com/openbases/openbases-icons) to ask!
