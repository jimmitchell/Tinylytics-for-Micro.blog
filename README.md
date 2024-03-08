# Tinylytics-for-Micro.blog

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/TinylyticsHeaderArt.png" alt="Tinylytics for Micro.blog title" width="800" />

A Micro.blog plug-in to easily add Tinylytics tracking to your site.

>[!IMPORTANT]
> ## Save 20% on a Tinylytics Subscription
> 
> Save 20% off your first year of Tinylytics by using this coupon code when you sign up:
> 
> ```TINYPLUGINMB```
> 
> *Note: This coupon is only good for new accounts and requires you to select the yearly plan option at sign up. See the sign up link below.*

>[!NOTE]
> ## Support Development
>
> If you believe this plug-in is worth supporting financially, feel free to make a donation on my [Ko-fi](https://ko-fi.com/jimmitchellmedia) page. A donation is not needed to use the plug-in, but if you do choose to support my work, you have my undying gratitude -- and you'll get priority support.
>
> [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/E1E3MTQ61)

## How To Use This Plug-in

Before anything else, you'll need to sign up for a [Tinylytics.app](https://tinylytics.app) account for the plug-in to work. Be sure to use the 20% off coupon above.

Once you've signed up and have the plug-in installed, enter your unique site id from your [Tinylytics.app](https://tinylytics.app) site configuration page:

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/tinylytics.jpg" alt="tinylytics site id example" width="800" />

## Tinylytics Settings

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/tinylytics-settings.png" alt="tinylytics configuration example" width="800" />

* **Tinylytics Site Id** -- This is your unique site id & embed code which can be found near the bottom of your site configuration page on Tinylytics. For the plugin to work, a site id must be entered in the plugin settings.
* **Show Hits?** -- This setting enables the display of how many hits your site has recieved overall, as well as for the unique page hits when adding the shortcode to a page. More on shortcodes below.
* **Link to your public stats?** -- If you've enabled public stats in your Tinylytics site configuration, enabling this option will add a link to your public stats page. If disabled, it simply links back to the main Tinylytics site.
* **Public Stats Label** -- If you've enabled public stats in your Tinylytics site configuration, adding a custom label value here will be reflected in the footer embed if you use it.
* **Show uptime?** -- Uptime is a premium feature for paying Tinylytics subscribers. If you have a premium membership and want to display uptime, enable this option. If you do not have a premium membership, it's recommended that you leave this option disabled.
* **Show country flags?** -- This option will display the country flags of visitors to your site in either the footer embed code or a shortcode added to a page. Again, more on shortcodes below.
* **Show Kudos?** -- Kudos allow users to leave feedback about the post or page they're viewing. Enabling this option will allow you to add the Kudo shortcode to a page or post that users can interact with. Leaving disabled will prevent Kudos from being displayed.
* **Kudos label** -- You can add a custom label to the Kudos counter as either text or an emoji. If you leave this option empty, a 👋 emoji will be shown by default.
* **Show Webring?** -- This option enables the Tinylytics webring feature that will display a link to another Indie Webring site. This is a great way to help your readers discover other blogger's content.
* **Webring label** -- You can set a custom webring lable for the link that's displayed. If nothing is set, 🕸️💍 will be displayed.
* **Show webring avatar?** -- A new feature in version 3.1 and later, this will display a webring's avatar to the left of your webring label.

## Showing Total Hits, Uptime, Webring Link and Country Flags in Your Micro.blog Footer

Maybe you'd like to display a hit counter, uptime, webring link and/or country flags in the global custom footer of your Micro.blog site without having to change any template files. Since shortcodes don't work in the Micro.blog custom footer, this can be accomplished using a partial embed instead.

```hugo
{{ partial "tinyhits/embed.html" (dict "context" . ) }}
```

An example of that looks like this:

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/footer-partial-example.png" alt="tinylytics kudos shorcode" width="800" />

## Shortcodes

If you'd like to avoid making changes to your theme template files, you can use select shortcodes instead. To add a kudos, post view counter or country flags to a post, simply add them using the following shortcodes:

```hugo
{{< tinykudos >}}
{{< tinyhits >}}
{{< tinyflags >}}
```

An example of using shortcodes looks something like this:

<img src="https://raw.githubusercontent.com/jimmitchell/Tinylytics-for-Micro.blog/main/screenshots/shortcode-example.png" alt="tinylytics hits shorcode" width="800" />

**A new feature:** Adding a ``{{< tinyhits >}}`` shortcode to a post will give the number of views *for just that post*, not the overall site views.

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

If you have questions or find a bug in the plug-in itself, connect with me on [Micro.blog](https://micro.blog/jimmitchell), [Mastodon](https://mastodon.social/@jimmitchell), or go old-school and shoot me an [email](mailto:hello@jimmitchell.org). For Tinylytics platform support, contact [@vincent](https://micro.blog/vincent) on Micro.blog, or email him at [hello@tinylytics.app](mailto:hello@tinylytics.app).
