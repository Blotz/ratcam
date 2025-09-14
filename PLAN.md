
# Rat Cam

Fun goofy website which

- Serves videos of wildlife caught by our rat cam
- Identifies animals using ML
- Emails our followers with each exciting update!

## Pipeline

### Backend PI

Ingest data via bash script [here](https://www.baeldung.com/linux/shell-run-script-usb-plugged).

Then run machine learning to classify the animals.

Transcode with ffmpeg.

upload to s3 bucket with [this](https://github.com/backblaze-b2-samples/b2-python-s3-sample).

serve via [cloudflare](https://www.backblaze.com/docs/cloud-storage-deliver-private-backblaze-b2-content-through-cloudflare-cdn) 

Trigger email with latest links

### Frontend github page

[svelte](https://svelte.dev/docs/kit/adapter-static)

