# vpxenc_tests
Preliminary tests on Unimi's and ITALTEL's GPU-accelerated vpxenc VP8 encoder.

Test suite provided by Google ( https://chromium.googlesource.com/webm/contributor-guide/+/HEAD/webm-contributor-guide.html )

Source files mainly taken from https://media.xiph.org/video/derf/ and others.
720p and 1080p executed on 125 or 150 frames.


Command-line:
./vpxenc $i -o $i-$b.vp8.webm --best --cpu-used=0 --target-bitrate=$b --auto-alt-ref=1 -v --minsection-pct=0 --maxsection-pct=800 --lag-in-frames=25 --kf-min-dist=0 --kf-max-dist=99999 --static-thresh=0 --min-q=0 --max-q=63 --drop-frame=0 --bias-pct=50 --minsection-pct=0 --maxsection-pct=800 --psnr --arnr-maxframes=7 --arnr-strength=3 --arnr-type=3 --codec=vp8

Test machine:
Intel Xeon E5-2620 v3 @ 2.40 GHz, 64 GB ram, Linux Ubuntu 14.05 64-bit, NVidia GTX980 with 4 GB of GDDR5 video memory.
