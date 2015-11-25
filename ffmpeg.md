ffmpeg -i

ffmpeg -i input.mp4 -vcodec libx264 -vprofile baseline -preset slow -b:v 250k -maxrate 250k -bufsize 500k -vf scale="1280:trunc(ow/a/2)*2" -threads 0 -acodec aac -strict experimental -b:a 128k output.mp4

ffmpeg -i input.mp4 -vcodec libx264 -vprofile high -preset slow -b:v 500k -maxrate 500k -bufsize 1000k -vf scale="1280:trunc(ow/a/2)*2" -threads 0 -acodec aac -strict experimental -b:a 128k output.mp4

ffmpeg -i input.mp4 -c:v libx264 -crf 22 -c:a libfaac -vf scale="1280:trunc(ow/a/2)*2" -movflags faststart output.mp4

ffmpeg -i input.mp4 -c:v libx264 -c:a libfaac -vf scale="720:trunc(ow/a/2)*2" -strict experimental output.mp4
