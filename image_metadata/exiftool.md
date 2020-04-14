ExifTool is a platform-independent Perl library plus a command-line application for reading, writing and editing meta 
information in a wide variety of files. ExifTool supports many different metadata formats including EXIF, GPS, IPTC, XMP, JFIF,
GeoTIFF, ICC Profile, Photoshop IRB, FlashPix, AFCP and ID3, as well as the maker notes of many digital cameras by Canon, Casio, DJI,
FLIR, FujiFilm, GE, GoPro, HP, JVC/Victor, Kodak, Leaf, Minolta/Konica-Minolta, Motorola, Nikon, Nintendo, Olympus/Epson, Panasonic/Leica,
Pentax/Asahi, Phase One, Reconyx, Ricoh, Samsung, Sanyo, Sigma/Foveon and Sony.

### check metadata of images in current folder 
```
exiftools -k .
```

### Change metdata date and shift one year forward 
```
exiftool "-AllDates+=1:0:0 00:00:00"  -overwrite_original "D:\DCIM\100DROIM"
```

### Change the "modifyDate"  field in metadata based on previous changes in 'Createddate' field: 
```
ExifTool "-FileModifyDate<XMP:DateTimeOriginal" "-FileModifyDate<EXIF:CreateDate" "-FileModifyDate<XMP:CreateDate" "-FileModifyDate<$IPTC:DateCreated $IPTC:TimeCreated" "-FileModifyDate<EXIF:DateTimeOriginal" DIR
```
