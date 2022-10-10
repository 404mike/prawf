# PHP

Using PSR-4 create an accessible HTML interface that display's 10 thumbnail images from ```manifest.json```. 

The interface should include the Collection title in Welsh - "Trafodion Cymdeithas Sir Faesyfed".

To create a thumbnail link you must loop through sequences->canvases and extact the value from `@id` - such as `https://damsssl.llgc.org.uk/iiif/2.0/1191403/canvas/1191404.json`. 

```
"@id": "https://damsssl.llgc.org.uk/iiif/2.0/1191403/canvas/1191404.json",
"@type": "sc:Canvas",
"label": "p. unnumbered",
"height": 3941,
"width": 2515,
```

The final number `1191404` from the URL can be used to generate an image from `https://damsssl.llgc.org.uk/iiif/2.0/image/{PID}/full/,400/0/default.jpg`, replace `{PID}` with `1191404` - eg `https://damsssl.llgc.org.uk/iiif/2.0/image/1191404/full/,400/0/default.jpg`.

Each thumbnail should also include the label for that image from `label` - "p. unnumbered"

If time allows create a pagination link at the bottom of the page which allows a user to paginate through all the thumbnails in the collection.