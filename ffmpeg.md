ffmpeg -i


ffmpeg -i /Users/foostudio/Downloads/input.mp4 -vcodec libx264 -vprofile high -preset slow -b:v 500k -maxrate 500k -bufsize 1000k -vf scale="480:trunc(ow/a/2)*2" -threads 0 -acodec aac -strict experimental -b:a 128k /Users/foostudio/Desktop/output.mp4


ffmpeg -i /Users/foostudio/Downloads/input.mp4 -b 1500k -vcodec libx264 -vpre slow -vpre baseline -g 30 /Users/foostudio/Desktop/output2.mp4


ffmpeg -i /Users/foostudio/Downloads/input.mp4 -c:v libx264 -c:a libfaac -strict experimental /Users/foostudio/Desktop/output2.mp4


ffmpeg -i /Users/foostudio/Downloads/input.mp4 -c:v libx264 -crf 22 -c:a libfaac -movflags faststart /Users/foostudio/Desktop/output2.mp4

ffmpeg -i /Users/foostudio/Downloads/input.mp4 -vcodec libx264 -vprofile baseline -preset slow -b:v 250k -maxrate 250k -bufsize 500k -vf scale="480:trunc(ow/a/2)*2" -threads 0 -acodec aac -strict experimental -b:a 128k /Users/foostudio/Desktop/output3.mp4