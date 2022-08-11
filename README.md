# PowerShell
- Regex from file `Get-Content .\regex15.txt | Select-String -Pattern "x*[#:.]y*" | Write-Host`
- Delete files that match pattern ``Get-ChildItem | Where-Object Name -Like '*`~*' | ForEach-Object { Remove-Item -LiteralPath $_.Name }``

# ImageMagick
### GIFs
- Make `magick -delay 20 *.png movie.gif`
- Extract frames `magick mogrify -format png *.gif`
- Crop `magick input.gif -coalesce -repage 0x0 -gravity Center -crop 25% +repage output.gif`
- Spin an image `magick convert input.jpg -duplicate 23 -distort SRT %[fx:t*360/n] -set delay 10 -loop 0 output.gif`
### Filters
- Crop `magick mogrify -crop 300x300+150+150 -path ./cropped *.png`
- Grayscale `magick <img_in> -set colorspace Gray -separate -evaluate-sequence Mean <img_out>`
- Resize magick `mogrify ./ -resize 20% -quality 80  *.png`
### Other
- Make icon `magick Capture.png -define icon:auto-resize=256,64,48,32,16 capture.ico`

# Visual Studio
- Publish NuGet `dotnet nuget push <package>.nupkg --api-key <key> --source https://api.nuget.org/v3/index.json`

# FFMPEG
- Trim `ffmpeg -ss 00:07 -to 00:59 -i <input> -c:v copy -an <output>`
- Add timestamp `ffmpeg -i input.mp4 -filter:v drawtext="fontfile=/Windows/Fonts/cour.ttf:fontsize=150:fontcolor='white':box=1:boxcolor='black@0.5':boxborderw=5:timecode='00\:00\:00;00':timecode_rate=(30*1000/1001):x=(w-text_w):y=(h-text_h)" output.mp4`

# BOM
- Best wire: *Silicone Stranded Wire, Digikey: 3239-22-1-*
