# Video transcriber
## How to auto generate subtitles for your video?
### If it is public video
You can send it to youtube and they use `subtitles` button or website like https://youtubetranscript.com (which uses this button).
And paid API such as Google/Amazon, etc.

### What if video is private and you don't want to send it or its audio outside your computer
1. ubuntu/wsl
2. `sudo apt install ffmpeg`
3. `ffmpeg -i your_file.mp4 -vn -acodec pcm_s16le -ar 44100 -ac 2 your_file.wav`
4. `pip3 install vosk` # https://alphacephei.com/vosk/install
5. `wget https://alphacephei.com/vosk/models/vosk-model-en-us-0.22.zip; wget https://alphacephei.com/vosk/models/vosk-model-ru-0.42.zip` # https://alphacephei.com/vosk/models
6. `unzip vosk-model-en-us-0.22.zip; unzip vosk-model-ru-0.42.zip;` # there will be folders `vosk-model-en-us-0.22` and `vosk-model-ru-0.42`
7. **EN**: if you want subtitles (srt): `vosk-transcriber -m vosk-model-en-us-0.22 -i your_file.wav -t srt -o your_file.srt` OR if you want text `vosk-transcriber -m vosk-model-ru-0.42 -i your_file.wav -o your_file.srt`
8. **RU**: if you want subtitles (srt): `vosk-transcriber -m vosk-model-ru-0.42 -i your_file.wav -t srt -o your_file.srt` OR if you want text `vosk-transcriber -m vosk-model-ru-0.42 -i your_file.wav -o your_file.srt`

## How to make summary :)
1. chatgpt
    * give me the summary of following text ctrl+v
2. google bard
    * the same
