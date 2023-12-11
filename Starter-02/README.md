# Virtual Scribe Assistant

The Virtual Scribe Assistant is an assistant that acts as a scribe that will take dictation of your notes, then on command, will email you the current note.

## Prerequisites

This example makes use of a [microphone package](https://github.com/deepgram/deepgram-go-sdk/tree/main/pkg/audio/microphone) contained within the Go SDK repository. That package makes use of the [PortAudio library](http://www.portaudio.com/) which is a cross-platform open source audio library. If you are on Linux, you can install this library using whatever package manager is available (yum, apt, etc.) on your operating system. If you are on macOS, you can install this library using [brew](https://brew.sh/).

## Running the Demo

To run this demo, you need to configure the config.json file with SMTP settings for your internet provider:
  
```
cd ./cmd/bin/dictation

# setup the configuration
cp config.json-ORG config.json
vi config.json
# open config.json and fill in the settings contained within

# set the EMAIL_SMTP_PASSWORD environment variable in your profile (for bash: ~/.bash_profile), then run:
go run main.go

# OR supply the environment variable on the command line
# (this should only be used for evaluation purposes)
# then run:
EMAIL_SMTP_PASSWORD="YOUR_PASSWORD" go run main.go
```

## Example Details

This is starter app makes use of the [Open Virtual Assistant](https://github.com/dvonthenen/open-virtual-assistant) project which is a framework for helping you create virtual digital assistants. The advantage is that a lot of the heavy lifting is taken care of (transcription) and you just need to implement your assistant logic only.

## Getting Help

We love to hear from you so if you have questions, comments or find a bug in the
project, let us know! You can either:

- [Open an issue](https://github.com/deepgram/[reponame]/issues/new) on this repository
- Ask a question, share the cool things you're working on, or see what else we have going on in our [Community Forum](https://github.com/orgs/deepgram/discussions/)
- Tweet at us! We're [@DeepgramAI on Twitter](https://twitter.com/DeepgramAI)

## Further Reading

Check out the Developer Documentation at [https://developers.deepgram.com/](https://developers.deepgram.com/)
