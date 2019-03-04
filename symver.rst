=======================
Symbolic Versioning 1.0
=======================

Summary
=======

0. Do not use symbolic versioning with software bearing a public API.
1. The number of version places you include is at your discretion.
2. Major versions are major.
3. Minor versions are not quite minor.
4. Patch versions are for troubleshooting.

Introduction
============

In the world of software development, many have heard the word about semantic
versioning. Blighted by dependency hell, its reason rescued countless projects
and brought coherency back to the things developers depend on. But what about
the things developers make and don’t depend on? It’s the elephant in the room:
the applications themselves.

In the 90s, software versions were amorphous. Programs were chronicled using
continually-incremented decimals, and the more you added to the number, the
more you were suggesting was changed… or so goes the notion. There was no
consistency in this, but there was an implicit understanding which even laymen
could wrap their heads around at the time. As the worldwide web exploded and
consumed most of the markets for computer science, practises evolved and moved
away from this. Google wasn’t your average Win32 application, complete with a
README file and a changelog.

With the adoption of semantic versioning, the symbolic nature of versions was
completely ironed away, replaced by a strict, concrete practise of helping
developers help themselves. For one reason or another, the businessfolk and
other laymen of note never bothered to reclaim this practise, despite the
advantages it gave in marketing updates and changes to their userbase. Firefox
and the Chromium legion shifted their release paradigm into semver and have
had hundreds of major releases among them, which users surely couldn’t tell
apart. Why should users care?

This question is difficult to convincingly answer in the current world of
cloud computing, microservices, the flourishing of for-profit APIs, and so on.
These are more comparable to a living thing than they are to a commodity in
any sense, and symbolic versioning would be useless for them. But just as
well, all living things must die, and the terminus for a tape drive is quite
different in nature. Symbolic versioning provides the means for authors of
software to tell their users what they did on the level that they understand,
long after they’re gone, or the API is consumed, the service is retired, and
so on.

People may never return to the copying of floppies, or archiving of media onto
tape drives. There is a power to the living API that is surely everlasting.
However, people will always vie for stability and guarantees on some level in
what they do. As time goes on, software will evolve to recognise this need,
and developers can fashion a means to provide this to their users with symver.

Symbolic Versioning Specification
=================================

Sorry if you haven’t been spoiled up to this point, but well… unlike semantic
versioning, symbolic versioning doesn’t work under a rigid, objective
standard. Throughout these guidelines, it’s assumed you have good judgment
and opinion on the weight each tenet carries with respect to your specific
project.

That said, there is one rule symver strongly recommends: **don’t use it in
place of semantic versioning!** Any program whose main purpose involves a
developer-facing API should use semver. It should be noted, however, that
you can use symver alongside semver without issues - for instance, a product
you’re marketing with symver that also has a plugin API using semver.

These examples use Acme Co. and its main product, Acmecomp to illustrate.

1. **The number of version places you include is at your discretion.**
	Generally you won’t want more than two numbers, major and minor, and the
	latter can be dropped in more general contexts. When you need to push
	technical updates, the third “patch” number is your go-to.
2. **Major versions are major.** So you’ve had modest successes with its first
	version. Now you’re looking at releasing Acmecomp 2, completely rewritten,
	rethought, and better than ever. This work you’ve done should hold as much
	value as possible to your users, so make sure to give them something worth
	buying into with this!
3. **Minor versions are not quite minor.** When everyone bought Acmecomp 2,
	they were enthralled. But you haven’t stopped working on it, and you have
	a release filled with updates, fixes and improvements that you’d feel more
	than a little guilty to charge for, so you release it as Acmecomp 2.1.
	Everyone who bought Acmecomp 2 is entitled to a free update to this
	version, so while it’s not such a huge deal they need to rebuy, it’s no
	small change either and most users will find the time to get it.
4. **Patch versions are for troubleshooting.** For everyone who posted that
	timeless help thread and got back, “what version are you on?” This is
	perfect to stick in an about box, or a page footer, for when you need it.
	It shouldn’t mean much in relation to features.

About
=====

This specification was authored by `Alexander Nicholi
<https://nicholatian.com/>`_. If you’d like to leave feedback or propose
changes, please `open an issue or PR on GitHub
<https://github.com/symver/symver/issues>`_.

Licence
=======

`Creative Commons – CC BY-SA 4.0
<https://creativecommons.org/licenses/by-sa/4.0/>`_
