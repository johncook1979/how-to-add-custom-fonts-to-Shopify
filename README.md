# How to add custom fonts to Shpify when they won't work
When adding custom fonts to Shopify using the tutorials provided by Shopify, you may encounter the following messages in the console and no font.
Failed to decode downloaded font
OTS parsing error

Although you followed the instructions to the letter, the fonts will not load and appear to be corrupted. But the problem is down to Shopify.

First, instead of uploading the font files to the assets folder as insructed in the guide, upload the fonts to the files directory of the store. The same location that you upload images for products and pages.

Next, click on the font you just uploaded and copy the URL to your clipboard

Next, in the custom CSS of the theme or the themes custom css file, enter the @fontface as shown in the css file. Notice how the url is no longer src: url("{{ '[font-file-name]' | file_url }}") format("[font-format]"); and is now url('https://cdn.shopify.com/s/files/1/0754/1040/7731/files/font-file-name') format('font-format')? This gives the full direct URL for the browser to download the font without creating an error.

See the css file for an example and customise it using your own font name and URL to fonts. Ensure you upload at lease a woff and woff2 file


