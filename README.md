[![Build Status](https://travis-ci.org/stphnlyd/perl5-Python-Version.svg?branch=master)](https://travis-ci.org/stphnlyd/perl5-Python-Version)

# NAME

Python::Version - Python PEP440 compatible version string parser in Perl

# VERSION

version 0.0000\_02

# SYNOPSIS

```perl
use Python::Version;

my $v = Python::Version->parse("1.2.3pre2.dev1+ubuntu-1");

print($v->normal);
print($v->original);

# Comparing versions
 
if ( version->parse($vstr1) == version->parse($vstr2) ) {
  # do stuff
}
 
# Sorting versions
 
my @ordered = sort { version->parse($a) <=> version->parse($b) } @list;
```

# DESCRIPTION

This module provides a parser as well as comparion method for Python PEP440
compatible version string.

# METHODS

## parse($version\_str)

Class method. It takes a PEP440-compatible string and returns a Python::Version
object.

## base\_version()

## is\_prerelease()

## is\_postrelease()

## is\_devrelease()

## local()

Returns local version label.

## normal()

Returns a string with a standard normalized form.  

## original()

Returns the original version string which was used to create the object.

## public()

Returns the public version.

# SEE ALSO

PEP 440 [https://www.python.org/dev/peps/pep-0440/](https://www.python.org/dev/peps/pep-0440/)

# AUTHOR

Stephan Loyd <sloyd@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2018 by Stephan Loyd.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
