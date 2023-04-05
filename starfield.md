convert -size 1280x720 xc: +noise Random -channel R -threshold 0.5% -negate -channel RG -separate +channel -compose multiply -composite stars.png

convert -size 150x90 xc: stars-01.bmp
convert stars-01.bmp +noise Random stars-02.bmp
convert stars-02.bmp -channel R -threshold 0.5% stars-03.bmp
convert stars-03.bmp -negate stars-04.bmp
convert stars-04.bmp -channel RG -separate +channel stars-05.bmp
convert stars-05-0.bmp stars-05-1.bmp -compose multiply -composite stars-06.bmp
convert stars-06.bmp -resize 200% -threshold 10% stars-06-rounded.bmp

