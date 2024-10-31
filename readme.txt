=== Permalink Editor ===
Contributors: hardikmeckwan
Donate Link: http://www.hardikmeckwan.com
Author Profile: http://www.hardikmeckwan.com
Tags: permalink, url, link, post, page, custom, modifier, redirect, edit, structure, category, tag, author
Requires at least: 3.1
Tested up to: 3.5.1
Stable tag: 0.2.12
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Fully customise the permalink for an individual page or post and globally set the permalink structure for pages, categories, tags or authors.

== Description ==

This plugin adds two areas of functionality: Global page, category or tag permalink structures and individual custom permalinks.

Options are added to the Permalinks Settings page allowing you to specify the structure for pages, categories, tags and authors.

By default - if custom permalinks are enabled - pages are accessible in the format `/page/` or `/parent/page/`.

You can modify this format in many different ways, for example:

* Add an extension: `/%pagename%.html`
* Add a parent directory name: `/content/%pagename%/`
* Prefix the page name: `/page-%pagename%/`
* Or using a combination of the above.

This same format applies for categories, tags and authors, however the structure tokens differ:

* Categories: `%category%` (E.g. `/category/%category%.html`)
* Tags: `%post_tag%` (E.g. `/tag/%post_tag%.html`)
* Authors: `%author%` (E.g. `/author/%author%.html`)

Each *permalink base* can be edited directly via these settings, for example using `/people/%author%.html` as the Author permalink structure will replace `/author/` with `/people/`.

If no prefix is found, permalinks will be prepended with a default (category, tag or author) - with the exception of pages.

**Note:** Ensure you have included the correct structure tag somewhere in the url.

Additionally, an option is added to the edit screen allow you to specify the permalink for an individual post or page.

== Installation ==

1. Unzip the package, and upload `page-permalink` to the `/wp-content/plugins/` directory.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Go to the permalink settings page *(Settings > Permalinks)* and set your custom global page permalink structure.
1. Individual post permalinks can be edited via the edit post screen.

readmore: http://www.hardikmeckwan.com

== Frequently Asked Questions ==

= Why is the customise button now showing? =

If you have not enabled custom permalinks *(Settings > Permalinks)* and they are set to the default option,
the plugin will not recognise that custom permalink structures are enabled.

= What is a permalink alias? =

A permalink alias is an additional permalink value that can be set to redirect to the actual permalink.

If a user enters the URL of an existing alias value, it will header redirect *(301)* them to the correct location.

= How can I remove a custom permalink? =

* Click the `Customise` permalink button on the admin edit screen.
* Empty the input containing the permalink.
* Click on `OK` and update the entry to apply the changes.

The default permalink structure will then be applied.

= Why do numbers keep appearing at the end of my permalink? =

Permalinks should by unique across your site, if you are trying to define a duplicate a numeric value will be appended to the end.

For example, if there is an existing custom slug of "/post.html", it will be turned into "/post.html2".

= What features are there still left to implement? =

* Complete removal of the Category or Tag base.
* Option to remove parent categories from the category permalink, e.g. "/parent/child/" becomes just "/child/".
* Ability to customise the archive pages, e.g. "/2011-02.html".
* Option to edit the author name in author permalinks.
* Ability to disable individual / custom page permalinks to speed up sites using custom structures only.

= What is the order of priority used for redirects? =

1. Find an existing page by the specified path, if one exists then redirect to that page.
1. Check for a custom permalink if the current request returns a 404 error. *(Defined on the individual edit page)*
1. Lookup an alias permalink if no existing page is found. *(Defined on the individual edit page)*
1. Use the global permalink structures. *(Defined on the permalink settings page)*

== Screenshots ==

1. The customise button is activated in pages, posts etc...
1. Customise button allows you to edit the whole permalink.
1. The permalink alias box appears towards the bottom of the edit screen.
1. Define the permalink structures on Settings > Permalinks options page.

== Upgrade Notice ==

= 0.1.0 =
* No specifics. Automatic upgrade works fine.

== Changelog ==

* *Updated 2013-04-26.*