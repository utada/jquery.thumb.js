jquery.thumb.js
===============

jquery picture thumbnails plugin

# Sample

http://jsfiddle.net/5Dsc8/1/

<pre><code class="javascript">
var entities = {
      "media": [
        {
          "id": 76360760611180544,
          "id_str": "76360760611180544",
          "media_url": "http://p.twimg.com/AQ9JtQsCEAA7dEN.jpg",
          "media_url_https": "https://p.twimg.com/AQ9JtQsCEAA7dEN.jpg",
          "url": "http://t.co/qbJx26r",
          "display_url": "pic.twitter.com/qbJx26r",
          "expanded_url": "http://twitter.com/twitter/status/76360760606986241/photo/1",
          "sizes": {
            "large": {
              "w": 700,
              "resize": "fit",
              "h": 466
            },
            "medium": {
              "w": 600,
              "resize": "fit",
              "h": 399
            },
            "small": {
              "w": 340,
              "resize": "fit",
              "h": 226
            },
            "thumb": {
              "w": 150,
              "resize": "crop",
              "h": 150
            }
          },
          "type": "photo",
          "indices": [
            34,
            53
          ]
        }
      ],
      "urls": [
      ],
      "user_mentions": [
      ],
      "hashtags": [
      ],
    "urls": [
        {
          "url": "http://t.co/0JG5Mcq",
          "display_url": "yfrog.com/Åc",
          "expanded_url": "http://yfrog.com/test",
          "indices": [
            84,
            103
          ]
        }
      ]
    };
    
$(entities.media).each(function() {
  $(this).thumbs();
  $(".text").append("<p>"+this.thumbnail_url);
});

$(entities.urls).each(function() {
  $(this).thumbs();
  $(".text").append("<p>"+this.thumbnail_url);
});
</pre>