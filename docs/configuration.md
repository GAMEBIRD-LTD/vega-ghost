# Configuration
You can manage the entire theme configuration using a single `Javascript` block
from the **Code Injection** page located at
<br>
> https&colon;//yoururl.com/`ghost/#/settings/code-injection`

<br>
The `Blog Footer` field must contain a `_VEGA` block containing a Javascript object.
Sample configuration:
```
<script>
var _VEGA = {
	disqus: {
		shortname: 'vega-ghost-demo',
	},
	instagram: {
		user_id: '',
    access_token: ''
	}
}
</script>
```
The entire block is wraped in `{`, `}`, inside each configuration has it's own object,
separated by comma.
<br>
All available configuration objects are:
```javascript
debug: true,    // - true / false - controls the debug in "console"
readtime: true, // - true / false - enable or disable the read time "min" block
featured: true, // - true / false - enable or disable the featured slider
disqus: {            // Contrls the instagram slider in the footer, remove the block to turn off
    shortname: null, // - String with your disqus handle in it, if 'null' or 'false'
                     //   it will disable disqus comments
},
instagram: {             // Contrls the instagram slider in the footer, remove the block to turn off
    user_id: null,       // - Integer with your user id, more information how to get it could be found bellow
                         //   if 'null' or invalid the feed will be disabled
    access_token: null,  // - Access token is a secret string to get the instagram feed from your account
    limit: 10,           // - How many images to get from instagram, we suggest
                         //   more than 10, since the slider won't work on bigger resolutions
    margin: 20,          // - How much spaces to set between the images
},
scrollToAnchor: {   // Controls the smooth scroll to anchor '#' links
    enabled: true,  //  - true / false - enable or disable the smooth scrolling
    speed: 600,     //  - speed in milliseconds for which the scroll will be completed
},
quickRead: {         // Controls the quick read bar for the posts pages
    progress: true,  // - true / false - enable or disable the progress indicator
    readMore: true,  // - true / false - enable or disable the read more posts block
},
```

---
## Instafeed integration
Instafeed is the instagram scroller in the footer of your 'Vega' themed blog. In order
to enable the Instafeed you must activate the Instagram API for your account and get
an access token.<br>
The configuration block that handles the instafeed options is:
```javascript
instagram: {             // Contrls the instagram slider in the footer, remove the block to turn off
    user_id: null,       // - Integer with your user id, more information
                         //   if 'null' or invalid the feed will be disabled
    access_token: null,  // - Access token is a secret string to get the instagram feed from your account
    limit: 10,           // - How many images to get from instagram, we suggest
                         //   more than 10, since the slider won't work on bigger resolutions
    margin: 20,          // - How much spaces to set between the images
},
```
Full documentation on instafeed is [available here](http://instafeedjs.com/)
<br>
In order to find your instagram account id you can use Google - [What is my Instagram account ID](https://www.google.bg/search?q=What+is+my+Instagram+account+ID)
<br>
To find your details:
User ID: https://smashballoon.com/instagram-feed/find-instagram-user-id/<br>
Access token: http://instagram.pixelunion.net/<br>
If the following doesn't work you can easily Google to find new links.
