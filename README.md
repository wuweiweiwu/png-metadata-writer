# png-metadata-writer

library to read and write PNG Metadata

w3 PNG Chunks specification: https://www.w3.org/TR/PNG-Chunks.html

The Metadata in PNG files: https://dev.exiv2.org/projects/exiv2/wiki/The_Metadata_in_PNG_files

### metadata format

image with 300 dpi

```javascript
{
  "pHYs": {
    "x": 30000,
    "y": 30000,
    "units": RESOLUTION_UNITS.INCHES
  },
  "tEXt": {
    "Title":            "Short (one line) title or caption for image",
    "Author":           "Name of image's creator",
    "Description":      "Description of image (possibly long)",
    "Copyright":        "Copyright notice",
    "Software":         "Software used to create the image",
    "Disclaimer":       "Legal disclaimer",
    "Warning":          "Warning of nature of content",
    "Source":           "Device used to create the image",
    "Comment":          "Miscellaneous comment"
  }
}
```

### writing metadata

```javascript
writeMetadata(buffer, metadata);
```
