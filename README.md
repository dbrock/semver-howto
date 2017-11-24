Semantic Versioning HOWTO
=========================

This is a guide to using [semantic versioning][semver], which is the
de facto standard for meaningful and machine-readable version numbers.

Unless you have a specific reason not to, you should probably use
semantic versioning for every new application you create.  This will
make it easier to integrate into package managers, as well as simply
being easy to understand for most users.

I’m going to describe the pragmatics of the semantic versioning
convention in terms of the typical application lifecycle.

Pre-alpha (0)
-------------

When you first create your application, it starts out being version 0.
It continues to be version 0, no matter how much you change it, until
you start to feel the need to actually differentiate between versions.

Alpha and beta (0.x.y)
----------------------

After version 0, the next version is either 0.0.1, if the new version
is backwards-compatible with version 0, or 0.1.0 if it’s not.

The distinction is somewhat blurry in the 0.x.y series, and you may
actually choose not to be backwards-compatible at all for a while, but
once you go to 0.1.0, you’re probably going to at least start thinking
about the distinction.

So you just continue through the 0.x.y range, incrementing y for every
backwards-compatible change, and x for every incompatible change.

(Of course, when you reach 0.9, you just go on to 0.10, 0.11, ….)

Release candidates (1.0.0-foo)
------------------------------

Before you bless a version as your first official release, you may
want make a few test runs with release candidates.  You can use any
scheme you want here, really, but 1.0.0-alpha.1 or 1.0.0-rc.1 would be
typical examples of pre-release versions.

First official release (1.0.0)
------------------------------

This is the point at which you actually start promising to follow
semantic versioning, so people can start to depend on it a bit more.

Patch releases (1.0.y)
----------------------

These are updates to version 1.0.0 that everybody is recommended to
switch to immediately, because nothing changed in the public API.

Minor releases (1.x.0)
----------------------

The first time you change the public API of your application in a
backwards-compatible way (add new APIs, or add deprecations), you
increment the minor version number.  You can also choose to do this
whenever you make any other kind of substantial change.

Then you just continue doing this for as long as you’re still
backwards-compatible with everybody.

Second major release and beyond (2.0.0, 3.0.0, …)
-------------------------------------------------

The first time you make a change that is incompatible with how people
are using the public API, you increment the major version number.

Then you keep both 1.x.y and 2.x.y versions until you manage to get
everybody to move over to 2.x.y, or decide to drop support for people
still using 1.x.y, at which point you can retire the 1.x.y versions.

This generational process continues throughout the application’s life.

Development versions of the second major release (2.0.0-0.x.y)
--------------------------------------------------------------

If you want, you can have a new 0.x.y series for the development
versions of the next major release, just by tacking it on as the
pre-release version.


Second major release candidates (2.0.0-rc.1)
--------------------------------------------

Obviously, you can use the same scheme with release candidates for
2.0.0 as you did for 1.0.0.  (Or a new one, for that matter.)

Advanced features
-----------------

There are a few more advanced features which may or may not be useful
to you; see [the semantic versioning specification][semver] if
you’re curious.

[semver]: http://semver.org
