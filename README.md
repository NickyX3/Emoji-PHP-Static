# Emoji-PHP-Static - Conversion Emoji in PHP from Unified <--> HTML

This is a PHP library for conversion Emoji from some mobile phones (iOS & Android) to html code and back

Based on <a href="https://github.com/iamcal/php-emoji">php-emoji</a> by Cal Henderson

## USAGE

    <?php
        include('Emoji.class.php');
        # or use some AutoLoader which you like

        # when you recieve text from a mobile device, convert it
        # to the HTML (through Unified, Emoji or Unified -> Unified -> HTML)

        $text = Emoji::emoji_to_html($text);

        # when sending data back to mobile devices, you can
        # convert back to Unified format ( HTML -> Unified )

        $text = Emoji::html_to_emoji($text);
    ?>

When using the HTML format, you'll also need to include the <code>emoji.css</code> file, which points 
to the <code>emoji.png</code> image. These images come from the <a href="https://github.com/github/gemoji">gemoji</a> 
project and cover all current codepoints.

Also i'm add another way of conversion - Emoji to HTML-Entity (like &#x1F33A;) and back for use with downloadable web-font from <a href="http://emojisymbols.com/faq.php">emojisymbols.com</a>. This way is best way for edit (or delete, khe-khe) Emoji in textarea on desktop browsers

## USAGE

    <?php
        include('Emoji.class.php');
        # or use some AutoLoader which you like

        # when you recieve text from a mobile device, convert it
        # to the HTML-Entity (through Unified, Emoji or Unified -> Unified -> HTML-Entity)

        $text = Emoji::emoji_to_font($text);

        # when sending data back to mobile devices, you can
        # convert back to Unified format ( HTML-Entity -> Unified )

        $text = Emoji::font_to_emoji($text);
        
        # this way best way for edit (delete :-)) Emoji in textarea on desktop system
    ?>

IMPORTANT NOTE: This library currently only deals with UTF-8.

## CREDITS

Static class by Nic Latyshev <nickyx3@gmail.com>

Based on <a href="https://github.com/iamcal/php-emoji">php-emoji</a> by Cal Henderson <cal@iamcal.com>

This work is dual-licensed under the GPL v3 and the MIT license.

Image copyrights: https://github.com/github/gemoji/blob/master/LICENSE

Version 1 released on 2015-10-10
