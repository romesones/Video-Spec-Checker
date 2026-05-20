# Video Spec Checker

Simple Python tool for validating video files against delivery specs using FFmpeg/ffprobe.

Checks:
- Resolution
- Frame rate
- Codec
- Bitrate
- Audio sample rate
- Bit depth
- Peak loudness

## Requirements

- Python 3.8+
- FFmpeg installed

## Install

```bash
brew install ffmpeg
```

or Windows:
https://ffmpeg.org/download.html

## Usage

```bash
python check_videos.py \
  --folder ./videos \
  --width 1920 \
  --height 1080 \
  --fps 29.97 \
  --codec h264 \
  --csv results.csv
```

## Example Output

```text
PASS video_01.mp4
FAIL video_02.mov
  - fps 25 != 29.97
```
