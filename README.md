# Random Quote Plugin

## Description

This is a simple WordPress plugin that displays a random quote every time the page loads.

## Features

- Displays a random quote from a predefined list of 100 quotes.
- Each page load shows a new random quote.
- You can easily add or modify quotes in the plugin code.

## Installation

1. Download the `random-quote` plugin folder.
2. Upload the folder to your WordPress `wp-content/plugins/` directory.
3. Go to the WordPress admin panel.
4. Navigate to **Plugins > Installed Plugins** and activate the `Random Quote Plugin`.

## Usage

To display the random quote on any page or post, simply add the following shortcode:

[random_quote]

## Code Example

function get_random_quotes() {
    $quotes = [        "Het leven is wat je ervan maakt.",        "Elke dag is een nieuwe kans.",        "Succes komt van doorzetten.",        // Add all other quotes here...    ];
    $random_quote = $quotes[array_rand($quotes)];
    return $random_quote;
}

function display_random_quote() {
    $quote = get_random_quotes();
    return "<div class='random-quote' style='font-size: 18px; color: #333; font-family: Arial, sans-serif; padding: 10px; border: 1px solid #ccc; background-color: #f9f9f9; border-radius: 5px;'>\"$quote\"</div>";
}

add_shortcode('random_quote', 'display_random_quote');

## Customization

You can easily add more quotes by editing the `$quotes` array in the plugin's code.

## Changelog

### Version 1.0
- Initial release with basic functionality.

### Version 1.1
- Updated plugin to support more quotes.

## Author

Bryce van der Werf