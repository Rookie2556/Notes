# Audio, Video and Images

## Video and audio content:

Videos can be useful to put on a webpage, e.g. the company's advertising, or introduction could be held into a video
a video would be written to a webpage as follows:

``` <video src="rabbit320.webm" controls>
  <p>
    Your browser doesn't support HTML video. Here is a
    <a href="rabbit320.webm">link to the video</a> instead.
  </p>
</video>
```

src is the source of the video, this could be a video link, or a file link to the video stored in files

controls is the controls provided to the user for the video, browsers typically have default controls, however it is possible to make
your own controls using APIs.

If the video cannot be processed for any reason, or is inaccessible for other reasoning, there is a fallback paragraph which
would ensure that users wouldn't miss any information, or an altenrative link to another video source showcasing the same video.

Browswers may not support all file types and it is important that the file is within the codec of the browser used. To ensure this
always try to use popular formats like .MP3 which contain audio and video data.

```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>
    Your browser doesn't support this video. Here is a
    <a href="rabbit320.mp4">link to the video</a> instead.
  </p>
</video>
```

There are features such as:
- width, height - specifies the sizing of the video
- autoplay - upon loading the page, the video is played, this is not advised as this is negatory in SEO and general engagment
- loop - ensures the video infinitely plays itself.
- muted - without sound
- poster - before the video is played
- preload - used for buffering, has 3 values: none (doesnt buffer), auto (buffers accordingly) and metadata (only metadata for the file)

Audios are along the similar stylings of the video, such as: 

``` <audio controls>
  <source src="viper.mp3" type="audio/mp3" />
  <source src="viper.ogg" type="audio/ogg" />
  <p>
    Your browser doesn't support this audio file. Here is a
    <a href="viper.mp3">link to the audio</a> instead.
  </p>
</audio>
``` 

It cannot have width/height, and poster - as there are no visual compoments.

However:

- Subtitles, captions and timed descriptions can be applied to audios via WEBVTT files, which are formatted like follows:

``` 
WEBVTT

1
00:00:22.230 --> 00:00:24.606
This is the first subtitle.

2
00:00:30.739 --> 00:00:34.074
This is the second.

…
``` 

Would be saved into the track element, and used like so:

```
<video controls>
  <source src="example.mp4" type="video/mp4" />
  <source src="example.webm" type="video/webm" />
  <track kind="subtitles" src="subtitles_es.vtt" srclang="es" label="Spanish" />
</video>
```
This helps the audio impaired users understand the content, like myseelf!

### Questions:

Explain how the ability to use video and audio on the web has evolved since the early 2000s.
  we used to have to use plugins to load and play videos/audio files, now most browsers support them!
  the range of files supported has increased and is more universal
  allow for the use of subtitling and timed descriptors for the audio-impaired.
Describe the use of the src and controls attributes in the <video> element.
  src is source, where the file is from. either the video link or file link
  controls containing play/pause, volume control. usually defaulted by the browser, however the designer can make their
  own.
Why is it important to have fallback content inside the <video> element?
  ensures all users can understand the content, as compatibility is not guaranteed and in that instance the user needs to know
  what they missed out n, for alternative links or brief descriptions that bypass the video.
  
