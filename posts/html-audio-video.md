---
title: 'Audio and Video in HTML'
date: '2018-01-25'
readTime: '2'
---

Often times you would want to add video and audio to your website. The best and most easiest is by hosting it in a hosting service that gives you a iframe to embed your code in your site. 

```html
...
<iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
...
```

This is the best method since you are having a third party api handle the storage and servering it up for you so you don't have to. But you could have your own audio and video from your local files but you would have to be aware of the type of file it is and if it is possible for the browser to play it or not. 

For audio files it would look like this.
```html
<audio controls>
  <source src="horse.mp3" type="audio/mpeg">
</audio>
```

and for video
```html
<video width="320" height="240" controls>
  <source src="YourMovieSource.mp4" type="video/mp4">
</video>
```

They do have some options you can add to the videos and audios but really depends on the effect you want of the items. Just be sure to make sure yoour are not copyrighting anyone's media sources and cite them properly.
