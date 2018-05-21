# EUCookieLaw 3 Themes & Design Guide
# About this repository

**This repository contain the public styles and design guideline for EUCookieLaw.** 
The main repository is named [EUCookieLaw3](https://github.com/diegolamonica/EUCookieLaw3).
You can find the WordPress version either on [GitHub](https://github.com/diegolamonica/EUCookieLaw3-wp) 
and WordPress Plugins Repository.

# Donations

If you find this tools useful, and since I've noticed that nobody did this script before of me,
I'd like to receive [a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=me%40diegolamonica%2einfo&lc=IT&item_name=EU%20Cookie%20Law%203%20Themes&no_note=0&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHostedGuest). :)

# Available Themes

To use a theme in your website, just download the file you want and link it in the page:

```html
<link rel="stylesheet" type="text/css" href="<path-to-the-theme-css-file.css>" />
```

Follows a list of available themes for EUCookieLaw.

## Bootstrap like
This theme is a grabbed simplified version of bootstrap modal dialog classes.

* File name: `bootstrap-like.css`
* Version: `20180521`   
* Author: Diego La Monica

## Darky Miky
This theme is the default dark theme for EUCookieLaw-wp.

* File name: `darky-miky.css`
* Versione: `20180521`
* Author: Micaela Esposito

# Design Guidelines

The following is a generic representation of EUCookieLaw3 dialog banner.

```html
<div data-eucookielaw-id="dialog-container" id="eucookielaw-57867" class="modal fade eucookielaw-modal in" style="display: block;">
	<div data-eucookielaw-id="dialog" class="modal-dialog modal-lg">
		<div data-eucookielaw-id="dialog-content" class="modal-content">
			<div data-eucookielaw-id="header-container" class="modal-header">
				<strong class="modal-title">Dialog title</strong>
			</div>
			<div data-eucookielaw-id="body-container" class="modal-body">
				<p data-eucookielaw-id="body-text-content">
					Dialog text/HTML content
				</p>
				<p data-eucookielaw-id="body-button-container" class="eucokielaw-dialog-button-container">
					<a data-eucookielaw-id="review-button" href="#" class="btn btn-default btn-block ">Review consents</a>
				</p>
				<div data-eucookielaw-id="cookie-group-list" class="list-group">
					<div data-eucookielaw-id="cookie-group-list-item" class="list-group-item rejected" data-group="service-1">
						<strong>Service #1 - title</strong><br>
						<span class="text-muted">
							Service #1 - extended description
						</span>
					</div>
					<div data-eucookielaw-id="cookie-group-list-item" class="list-group-item rejected" data-group="service-2">
						<strong>Service #2 - title</strong><br>
						<span class="text-muted">Service #2 extended description</span>
					</div>
				</div>
				<div data-eucookielaw-id="button-container" class="buttons text-right">
					<a data-dismiss="modal" data-eucookielaw-id="close-button" href="#" class="btn btn-primary">Done</a>
				</div>
			</div>
			<div data-eucookielaw-id="footer-container" class="modal-footer">
				<div class="eucookielaw-dialog-footer">
					<small>
						Powered by 
						<a href="https://diegolamonica.info">
							EUCookieLaw 
							<img src="data:image:..." scale="0">
						</a>
					</small>
				</div>
			</div>
		</div>
	</div>
</div>
```

Each special element of EUCookieLaw3 has a data attribute `data-eucookielaw-id` that uniquely identify the role of
the component:
* `dialog-container` is the main container (the envelope of the entire dialog box)
  it has 4 classes: `modal`, `fade`, `eucookielaw-modal`.
  
  When the modal is shown the class `in` is applied to the element and the class `modal-open` is applied to the body. 
  
* `dialog` is the modal dialog component, it has 2 classes: `modal-dialog` `modal-lg`

* `dialog-content` is the dialog. It has the class `modal-content`

* `heaer-container` is the header of the modal. It has the class `modal-header` and has a non predictable HTML element 
  due is configured through the [EUCookieLaw Configuration Builder](https://diegolamonica.info/tools/eucookielaw/builder/). However the class of the inner HTML element is
  `modal-title`.
   
* `body-container` has a class `mdodal-body`

* `body-button-container` has the class `eucookielaw-dialog-button-container` and contains the review button. The 
  user could define a custom set of additional classes.
  
* `review-button` is the button which allows user to view more details.

* `cookie-group-list` the container of the treatments. It has the class `list-group`
* `cookie-group-list-item` is the single treatment item. It has the class `list-group-item` and an additional class 
  `approved` or `rejectd` according to the user consent about the treatment. Those two classes can change its name 
  due to the custom configuration.  
  Its structure is composed by a `strong` element and an adjacent `span` element with class `text-muted`
* `button-container` is the container of the close button, his class is `buttons` and `text-right`  
* `close-button` is the button which the user can touch/click to close the dialog. Has the class `btn btn-primary`
* `footer-container` is the footer of the dialog, has the class `modal-footer`.

To disallow any kind of conflict with other rules, it's recommended to prefix all the CSS rules for the modal with 
the container class `eucookielaw-modal`.

# Share your style 

If you want to share your custom theme for EUCookieLaw3, you are free to create your own theme but remeber to:

1. Add copyright row at the top of the theme informing about Theme name, your name and your website, the Project MUST be always `EUCookieLaw3`, the version number of your theme and the License model, like:
   ```css
    /*
     * Theme: Bootstrap-like
     * Author: Diego La Monica (https://diegolamonica.info)
     * Project: EUCookieLaw3
     * Version: 20180521
     * Copyright (c) 2018 Diego La Monica CC-BY-NC
     */
	``` 
2. Create all the required rules (as described above).

3. Create a pull request for this repository