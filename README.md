[![Build Status](https://travis-ci.org/stphnlyd/perl5-Python-Version.svg?branch=master)](https://travis-ci.org/stphnlyd/perl5-Python-Version)

# NAME

Python::Version - Python PEP440 compatible version string parser in Perl

# VERSION

version 0.0002

# SYNOPSIS

```perl
use Python::Version;

my $v = Python::Version->parse("1.2.3pre2.dev1+ubuntu-1");

print($v->normal);
print($v->original);

# Comparing versions
 
if ( Python::Version->parse($vstr1) == Python::Version->parse($vstr2) ) {
  # do stuff
}
 
# Sorting versions
 
my @ordered = sort { Python::Version->parse($a) <=> Python::Version->parse($b) } @list;
```

# DESCRIPTION

This module provides a parser as well as comparison method for Python PEP440
compatible version string.

# METHODS

## parse($version\_str)

Class method. It takes a PEP440-compatible string and returns a Python::Version
object.

```perl
my $v = Python::Version->parse($version_str);
```

## base\_version()

Returns the normalized base part of the version.

## is\_prerelease()

Returns a boolean value for if the version is a pre-release.

## is\_postrelease()

Returns a boolean value for if the version is a post-release.

## is\_devrelease()

Returns a boolean value for if the version is a dev-release.

## local()

Returns the normalized local version label.

## normal()

Returns a string with a standard normalized form.  

## original()

Returns the original version string which was used to create the object.

## public()

Returns the normalized public version.

# SEE ALSO

PEP 440 [https://www.python.org/dev/peps/pep-0440/](https://www.python.org/dev/peps/pep-0440/)

# AUTHOR

Stephan Loyd <sloyd@cpan.org>

# CONTRIBUTOR

perlancar <perlancar@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2018 by Stephan Loyd.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
