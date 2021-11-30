# Terminal Commands for Images
Convert, Resize, Rename etc


## Convert *.CR2 to *.JPG
```
for i in *.CR2; do sips -s format jpeg $i --out "${i%.*}.jpg"; done
```

## Resize Images to max width/height 
Using Sips 
```
for i in *.jpg; do sips -Z 1200 $i --out "${i%.*}.jpg"; done
```
Using Magick
```
magick mogrify -resize 60% *.jpg
```
## Resize Images to fixed height / width
Using Sips 
```
for i in *.jpg; do sips -z 768 1024 $i --out "${i%.*}.jpg"; done
```
