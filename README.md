# Rate my Post - WP Rating System

Rate my Post - WP Rating System allows you to easily add rating functionality to your WordPress website. Visitors can rate your posts/pages and send you private feedback after rating. Functionality to create custom rating widgets that work independently of posts and pages is coming soon.

**[See Rate my Post on Wordpress.org](https://wordpress.org/plugins/rate-my-post/)**

## Welcome to Rate my Post GitHub repository

While the documentation for the Rate my Post plugin can be found on [blazzdev.com](https://blazzdev.com/documentation/rate-my-post-documentation/), you can here browse the source code, find and discuss open issues and even contribute yourself.

## Installation

1. Unzip downloaded archive
2. Upload rate-my-post folder (which is in rate-my-post-master folder) in your /wp-content/plugins/ directory
3. Navigate to Dashboard -> Plugins
4. Click Activate
5. Click Rate my Post -> Settings in the main menu and configure the plugin
6. Add shortcode [ratemypost] to your posts or embed rating widgets automatically in the Settings

If you are upgrading the plugin, first delete the old version. **Make sure that "Delete all plugin data on uninstall" is disabled in the settings**.

## Want to contribute to Rate my Post?

### Prerequisites

Please ensure you have the following tools installed before starting:

* [Node.js](https://nodejs.org/en/)

### Getting started

Within your WordPress installation, navigate to wp-content/plugins and run the following commands:

```
git clone https://github.com/blaz-blazer/rate-my-post.git
cd rate-my-post
```

To install all the necessary dependencies, run the following command:

```
npm install
```

Change proxy in gulpfile.js to match your local environment:

```
function browser_sync() {
	browserSync.init({
		proxy: 'http://localhost/wordpress' // replace with your wordpress install
	});
}
```

Start development server with the following command:

```
gulp watch
```

Build production version of the plugin (copies files to rate-my-post directory, minifies resources and creates POT file) with the following command:

```
gulp build
```

## Known Limitations

* The plugin uses CSS at-rule: @media: hover to highlight rating icons on hover. Hence rating icons will not get highlighted on [older browsers](https://caniuse.com/#feat=mdn-css_at-rules_media_hover). The at-rule is used because otherwise double tap was required on iOS devices to submit the rating.
* If ajax load results is enabled, only one rating/results widget on page will get initialized because otherwise we would cause too many script executions.
* It is not possible to have more than one rating widget for the same post on a single web page.

## Support

This is a developer's portal for Rate my Post and should not be used for support. For support, please use the [support forum](https://wordpress.org/support/plugin/rate-my-post/).

## Built With

* [Gulp](https://gulpjs.com/) - Task runner
* [Webpack](https://webpack.js.org/) - Module bundler

## Author

* **Blaz Krapez** - [BlazzDev](https://blazzdev.com/)

## License

This project is licensed under the GPLv3 License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
