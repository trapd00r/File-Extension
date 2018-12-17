[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=65SFZJ25PSKG8&currency_code=SEK&source=url) - Every tiny cent helps a lot!

# NAME

File::Extension - explain file extensions

# SYNOPSIS

      use File::Extension qw(extplain filter_by_meta);

      my @filetypes = qw(nes pl pm gb p6);

      for my $what(@filetypes) {
        printf("%s is a %s\n", $what, extplain($what));
      }

      my $document_extensions = filter_by_meta('doc');

# DESCRIPTION

File::Extension exposes functionality for getting information on
filetypes based solely on their file extension.

This is useful in cases where libmagic doesn't work, i.e on empty or
corrupted files.

The extensions and descriptions are taken from [http://fileinfo.com](http://fileinfo.com).

# EXPORTS

None by default.

# FUNCTIONS

## extplain()

Parameters: $file\_extension

Returns:    $explanation

    my $explanation = extplain('nes'); # Nintendo (NES) ROM File

## filter\_by\_meta()

Parameters: $extension

Returns:    \\%filtered

    my $results = filter_by_meta('doc');

Filters the hash by a raw string or regular expression, returning the results.

# HISTORY

This module was initially crafted while exploring ideas for generating
the world's largest LS\_COLORS file:

["https://github.com/trapd00r/LS\_COLORS/issues/112"](#https-github-com-trapd00r-ls_colors-issues-112)

# SEE ALSO

[https://github.com/trapd00r/LS\_COLORS](https://github.com/trapd00r/LS_COLORS)

# AUTHOR

    Magnus Woldrich
    CPAN ID: WOLDRICH
    m@japh.se
    http://japh.se

# CONTRIBUTORS

None required yet.

# COPYRIGHT

Copyright 2018 the **File::Extension**s ["AUTHOR"](#author) and
["CONTRIBUTORS"](#contributors) as listed above.

# LICENSE

This library is free software; you may redistribute it and/or modify it under
the same terms as Perl itself.
