# Open Bases Icons

These fun, beautiful sets of images can be used as placeholders for generated
PDFs and other content used by the openbases! The idea is to provide them in
a separate repository so the primary repos don't need to each serve the files.
The author of most of these icons is Freepick, and each folder
coincides with a particular icon collection on the site. Specific links and 
attributions are contained within. Thank you Freepik for this invaluable
resource to make science a little more fun!

## Open Bases Icons API

There is a simple API served by the repository to make it easy for you to
programmatically get an icon! If you look at the base, you can see there
is an endpoint for text, and for json:

```bash
$ curl https://openbases.github.io/openbases-icons/
{
  "icons": {
    "text": "/openbases-icons/icons.txt",
    "json": "/openbases-icons/icons.json"
   }
}
```

If you then parse each endpoint, you get the expected format! Each serves a list
of icons, and that's it. Here is a list of files ([icons.txt](https://openbases.github.io/openbases-icons/icons.txt)):

```bash
$ curl https://openbases.github.io/openbases-icons/icons.txt
https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/stingray.svg
https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/starfish.svg
https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/squid.svg
https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/snail.svg
https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/seahorse.svg
...
https://openbases.github.io/openbases-icons/flaticon/in-the-zoo/cheetah.svg
https://openbases.github.io/openbases-icons/flaticon/in-the-zoo/chameleon.svg
https://openbases.github.io/openbases-icons/flaticon/in-the-zoo/butterfly.svg
```

And here is the equivalent for [icons.json](https://openbases.github.io/openbases-icons/icons.json):

```bash
curl https://openbases.github.io/openbases-icons/icons.json

["https://openbases.github.io/openbases-iconsflaticon/in-the-zoo/penguin.svg",
 "https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/stingray.svg",
 "https://openbases.github.io/openbases-icons/flaticon/sea-life-collection/starfish.svg",
...
 "https://openbases.github.io/openbases-icons/flaticon/in-the-zoo/butterfly.svg",
 "https://openbases.github.io/openbases-iconsflaticon/in-the-zoo/penguin.svg"]
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
```

## Icon Collections

 - [In the Zoo](flaticon/in-the-zoo)
 - [Sea Life Collection](flaticon/sea-life-collection)

When using these icons you **must** give proper attribution to the author and include the license
below. Thank you!

<div>Icons made by <a href="http://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> is licensed by <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a></div>
