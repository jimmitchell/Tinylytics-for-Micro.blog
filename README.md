# Tinylytics-for-Micro.blog

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/TinylyticsHeaderArt.png" alt="Tinylytics for Micro.blog title" width="1000" />

A Micro.blog plug-in to easily add Tinylytics tracking to your site.

> ## Save 20% on a Tinylytics Subscription
> 
> Save 20% off your first year of Tinylytics by using this coupon code when you sign up:
> 
> ### **TINYPLUGINMB**
> 
> *Note: This coupon is only good for new accounts and requires you to select the yearly plan option at sign up. See the sign up link below.*

## Support Development

If you find this plug-in is worth supporting financially, you can make a donation on my [Ko-fi](https://ko-fi.com/jimmitchellmedia) page. It's not required to use the plug-in, but if you do decide to, I'd like to thank you very much in advance for your support.

## How To Use This Plug-in

Before anything else, you'll need to sign up for a [Tinylytics.app](https://tinylytics.app) account for the plug-in to work. Be sure to use the 20% off coupon above.

Once you've signed up and have the plug-in installed, enter your unique site id from your [Tinylytics.app](https://tinylytics.app) site configuration page:

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/tinylytics.jpg" alt="tinylytics site id example" width="1000" />

## Displaying Hits

If you want to display the total hits on your site, check the "Show Hits?" checkbox. Check out the Tinylytics "[Showing a hit counter](https://tinylytics.app/docs/show_hit_counter)" help article for more details.

## Displaying Uptime

If you want to display the uptime of your site, check the "Show Uptime?" checkbox. Check out the Tinylytics "[Showing Uptime on your site](https://tinylytics.app/docs/showing_uptime)" help article for more details. **Note:** Uptime monitoring is a paid account feature. If you enable the "Show Uptime?" checkbox but to not have a paid account, you'll only see an uptime label.

## Displaying Post Kudos

If you want to display a Kudos counter on individual post pages, check the "Show Kudos?" checkbox. See the Tinylytics "[Showing kudos](https://tinylytics.app/docs/showing_kudos)" help article for more details. In addition to a Kudos counter, you can set a label using any combination of emoji and/or text. If you don't set your own label, the default emoji will be "👋".

## Showing the Webring Link

If you want to display the Tinylytics Webring Link on your site, check the "Show Webring?" checkbox. See the Tinylytics "[Showing the webring](https://tinylytics.app/docs/showing_webring)" help article for more details. You can set the link text using using any combination of emoji and/or text. If you don't set your own label.

## Displaying Country Flags

If you want to display the total hits on your site, check the "Show Country Flags?" checkbox. Check out the Tinylytics "[Showing visited countries](https://tinylytics.app/docs/showing_countries)" help article for more details.

---

## Shortcodes

If you'd like to avoid making changes to your theme template files, you can use select shortcodes instead. To add a kudos, post view counter or country flags to a post, simply add them using the following shortcodes:

```hugo
{{< tinykudos >}}
{{< tinyhits >}}
{{< tinyflags >}}
```

An example of using shortcodes looks something like this:

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/shortcode-example.png" alt="tinylytics hits shorcode" width="1000" />

**A new feature:** Adding a ``{{< tinyhits >}}`` shortcode to a post will give the number of views *for just that post*, not the overall site views.

## Showing Total Hits, Uptime, Webring Link and Country Flags in Your Micro.blog Footer

Maybe you'd like to display a hit counter, uptime, webring link and/or country flags in the global custom footer of your Micro.blog site without having to change any template files. Since shortcodes don't work in the Micro.blog custom footer, this can be accomplished using a partial embed instead.

```hugo
{{ partial "tinyhits/embed.html" (dict "context" . ) }}
```

An example of that looks like this:

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/footer-partial-example.png" alt="tinylytics kudos shorcode" width="1000" />


## Tinylytics Styles

Out of the box, Tinylytics works great without any styles applied, but if you'd like to tweak how things look to better match your site, here are the CSS classes:

```css
.tiny_counter {
    /* Styles the entire counter <span> for a custom footer embed only */
}

.tinylytics_hits {
    /* Styles the hit counter number. Works for both shortcode and embed methods. */
}

.tiny_uptime {
    /* Styles the uptime <span> for a custom footer embed only */
}

.tiny_webring {
    /* Styles the webring <span> for a custom footer embed only */
}

.tiny_countries {
    /* Styles the country flags <span>. Works for both shortcode and embed methods. */
}

.tinylytics_kudos {
    /* this class styles the entire Kudos button. Works for both shortcode and embed methods. */
}

.did_select {
    /* Styles the Kudos button to appear different/inactive once a Kudo is given. Works for both shortcode and embed methods. */
}
```

## Need Help?

If you have questions or find a bug in the plug-in itself, connect with me on [Micro.blog](https://micro.blog/jimmitchell) or go old-school and shoot me an [email](mailto:hello@jimmitchell.org). For Tinylytics platform support, contact [@vincent](https://micro.blog/vincent) on Micro.blog, or email him at [hello@tinylytics.app](mailto:hello@tinylytics.app).
