# Tinylytics-for-Micro.blog

<img src="screenshots/TinylyticsHeaderArt.png" alt="Tinylytics for Micro.blog title" width="1000" />

A Micro.blog plug-in to easily add Tinylytics tracking to your site.

## How To Use This Plug-in

Before anything else, you'll need to sign up for a [Tinylytics.app](https://tinylytics.app) account for the plug-in to work.

Once you have the plug-in installed, enter your unique site id from your [Tinylytics.app](https://tinylytics.app) site configuration page:

<img src="screenshots/tinylytics.jpg" alt="tinylytics site id example" width="1000" />

## Displaying Hits

If you want to display hits somewhere on your site (say, in the footer - see below), check the "Display hits?" checkbox. Checkout the Tinylytics "[Showing a hit counter](https://tinylytics.app/docs/show_hit_counter)" help article for more details.

## Displaying Kudos

If you want to display a Kudos counter on individual post pages, check the "Show Kudos?" checkbox. See the Tinylytics "[Showing kudos](https://tinylytics.app/docs/showing_kudos)" help article for more details. In addition to a Kudos counter, you can set a label using any combination of emoji and/or text. If you don't set your own label, the default emoji will be "👋".

## Shortcodes

If you'd like to avoid making changes to your theme template files, you can use shortcodes instead. To add a kudos or site counter to a post, simply add them using the following shortcodes:

````
{{< tinykudos >}}
{{< tinyhits >}} 
````

An example of that might look something like this:

<img src="screenshots/shortcode-example.png" alt="tinylytics hits shorcode" width="1000" />

## Showing Hits in Your Micro.blog Footer

Maybe you'd like to display a hit counter in the custom footer of your Micro.blog without having to change any template files. Since shortcodes do not work in the Micro.blog custom footer, this can be accomplished using a partial embed instead.

````
{{ partial "tinyhits/embed.html" (dict "context" . ) }}
````

An example of that looks something like this:

<img src="screenshots/footer-partial-example.png" alt="tinylytics kudos shorcode" width="1000" />

**Important Note:** You can only have one hit counter on a page at a time. If you plan to use a hit counter shortcode in a post, do not use the footer embed method. The opposite goes for a global footer counter; don't use the "tinyhits" shortcode in a post.

## Tinylytics Styles

Out of the box, Tinylytics works great without any styles applied, but if you'd like to tweak how things look to better match your site, here are the CSS classes:

````
.tiny_counter {
    /* Styles the entire counter for a custom footer embed only */
}

.tinylytics_hits {
    /* Styles the hit counter number. Works for both shortcode and embed methods. */
}

.tinylytics_kudos {
    /* this class styles the entire Kudos button. Works for both shortcode and embed methods. * /
}

.did_select {
    /* Styles the Kudos button to appear different/inactive once a Kudo is given. Works for both shortcode and embed methods. */
}
````

## Need Help?

If you have questions or find a bug in the plug-in itself, hit me up on [Micro.blog](https://micro.blog/jimmitchell), [Mastodon](https://mastodon.social/@jimmitchell), or go old-school and shoot me an [email](mailto:hello@jimmitchell.org).

For Tinylytics support, contact [@vincent](https://micro.blog/vincent) on Micro.blog, or email him at [hello@tinylytics.app](mailto:hello@tinylytics.app).

## Support Development

Finally, if you find this plug-in is worth supporting financially, you can make a donation on my [Ko-fi](https://ko-fi.com/jimmitchellmedia) page. If you do, thank you very much for your support.
