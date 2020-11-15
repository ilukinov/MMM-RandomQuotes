# Module: MMM-RandomQuotes

The `MMM-RandomQuotes` module returns a random quote based on the category set. Supplied quotes are courtesy
of http://brainyquote.com. Since there is no API for BrainQuote.com, you will have to manually add new ones.
See the section on `Updating Quotes` below.

## Installing the module
Clone this repository in your `~/MagicMirror/modules/` folder
````sh
git clone https://github.com/ilukinov/random_quotes
````

## Using the module
To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
			{
				module: 'MMM-RandomQuotes',
				position: 'bottom_bar',
				config: {
						// The config property is optional
						// Without a config, a random quote is shown,
						// selected from all of the categories available.
				}
			}
]
````

## Configuration options
The `MMM-RandomQuotes` module allows you to pick quotes randomly from all the provided categories, or you can
set it to only use one category. Specifying multiple categories is curently not supported.

|Options|Description|Default|
|--- |--- |--- |
|updateInterval|How often a new quote gets displayed. Value is in SECONDS.|300 seconds (every 5 minutes)|
|showAuthor|Show quote author or not|true|
|fadeSpeed|How fast (in SECONDS) to fade out and back in when changing quotes.|4 seconds|
|category|What category to pick from.|random - The random setting will pick a random quote out of all the available categories. Or you can set it to a specific category: inspirational, life, love, motivational, positive, or success.|


## Updating Quotes
Because BrainyQuote.com does not proide an API for their database, you will have to update/change the quotes manually.
You can edit the `MMM-RandomQuotes.js` file and add/remove quotes from the various sections. You may even delete an entire
section.

Most random quotes APIs out there only allow for a single 'quote of the day'. If you want to have a random quote
each time you send a request, most of them will require a paid subscription. In keeping this module 'free', I opted
to not force anyone to have to pay for a service.
