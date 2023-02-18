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
 
## Grid

Grid is an important powerful tool to allow webdesigners to create two dimensional layouts for their webpages. 
It works by dividing the entire page as columns and rows.

CSS Grid provides a variety of properties and features for controlling the grid layout, including grid-template-rows, grid-template-columns, grid-template-areas, grid-row, grid-column, and grid-area. These properties allow developers to create complex and flexible layouts that can adapt to different screen sizes and devices.
  
In a Grid layout, the container element is defined as a grid container, which is created using the display: grid property. The grid container is then divided into a grid of rows and columns, forming a grid structure. The individual items inside the grid container are called grid items. The size and position of grid items can be defined using properties like grid-row and grid-column.
  
display: grid - This sets an element as a grid container.

grid-template-rows - This defines the size and number of rows in the grid.

grid-template-columns - This defines the size and number of columns in the grid.

grid-template-areas - This creates named grid areas, which can be used to place content in specific areas of the grid.

grid-gap - This sets the spacing between grid items.

grid-row-start and grid-row-end - These properties define where a grid item starts and ends on a row.

grid-column-start and grid-column-end - These properties define where a grid item starts and ends on a column.

grid-area - This property is a shorthand for defining the grid-row-start, grid-column-start, grid-row-end, and grid-column-end properties.

justify-items - This property aligns grid items along the horizontal axis.

align-items - This property aligns grid items along the vertical axis.

justify-content - This property aligns the entire grid along the horizontal axis.

align-content - This property aligns the entire grid along the vertical axis.

Flex, on the other hand, is more suited for simpler layouts with a single row or column. It's ideal for aligning and distributing content along a single axis, and is commonly used for creating navigation menus or simple image galleries.
  
Both can be used in combination though!

### Questions:
  
How does Grid layout differ from Flex?
    Grid typically squares up slots of space, flex aligns along a single axis. Both are layout methods, Grid places them
    along rows and columns, flex places elements accordingly to each other.
Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.
     Grid container is the square in which the element is placed
     Grid item is the object inside the square
     Grid line is the lines used as parameters horizonally and vertically.
  
  
## Responsive Images

This is the scaling of imagery to ensure good viewability by all users, usually by setting max widths and such. 
and to ensure less irrelevancy is loaded, to save bandwidth for mobile users. 

This can be achieved using resolution switching for different sizes:

  ``` <img
  srcset="elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"
  sizes="(max-width: 600px) 480px,
         800px"
  src="elva-fairy-800w.jpg"
  alt="Elva dressed as a fairy" />
``` 
  
the original size is put as "800w", (max-width: 600px) is the max width of the deivce, if it is this, then set image size as:
  480px by 800px.

The max width of the device is checked automatically by the browser.
  
This is done in HTML as this is where any image files is loaded, CSS and JS are loaded AFTER the HTML.
    
Like video and audio, <Picture> is a wrapper:

``` 
  <picture>
  <source type="image/svg+xml" srcset="pyramid.svg" />
  <source type="image/webp" srcset="pyramid.webp" />
  <img
    src="pyramid.png"
    alt="regular pyramid built from four equilateral triangles" />
</picture>
```
  
srcset helps us decide which source file to use, by specifying like so:
  
```
  <picture>
  <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg" />
  <source media="(min-width: 800px)" srcset="elva-800w.jpg" />
  <img src="elva-800w.jpg" alt="Chris standing up holding his daughter Elva" />
</picture>
```

### Questions:
  
Besides making a site visually appealing across different screen sizes, why should developers make images responsive?
    Reduces loading times, and bandwidth used. 
Define the following <img> attributes srcset and sizes. Write an example of how they are used.
    ```srcset="image-small.jpg 640w,
             image-medium.jpg 1024w,
             image-large.jpg 1600w"
     sizes="(max-width: 640px) 100vw,
            (max-width: 1024px) 50vw,
            800px"
  ```
How is srcset more helpful for responsive images than CSS or JavaScript?
  HTML uses browser already captured information about the user's device, and makes changes accordingly. 
  to do otherwise would require further files which are unecesarry. 
