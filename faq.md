# FAQ

## Who owns a Goggle?

The sole owner of a Goggle is the person who controls the URL in which it’s
hosted. That person or community has the sole rights to update it.

Brave has no claim on the ownership of Goggles. Anyone can create and use a
Goggle; there is no sign-up or identification required from Brave Search. We
believe this is the best setup for the community to flourish and come up with
alternative rankings that cater to a wide range of use-cases—rankings that
would be otherwise impossible to handle for an all-purpose search engine such
as Brave Search.

At the same time, Brave Search has no responsibility to ensure a Goggle's
quality or truthfulness, which can only be estimated based on the reputation of
the authors/maintainers.

The only Goggles owned by Brave are those in the [goggles folder](./goggles)
from this repository, which are exclusively meant for educational purposes, and
are best-effort and as-is. Brave does not intend to expand or continue
maintaining these in any shape or form, as we expect community-owned Goggles to
cover those use-cases better in the near future. We will however try to keep
the examples functional.

Goggles are by definition open-source, however, the authors can choose any
license they please. People forking a Goggle are subjected to the terms of its
license as any other open-source piece of software.
 

## Why can’t I apply multiple Goggles at the same time?

At this point we don’t feel comfortable allowing multiple Goggles at once, as
instructions in multiple Goggles could collide in non-intuitive ways, which
would lead to surprising results. This problem can also appear in a single
Goggle, though this is less likely, and the maintainer(s) would be able to
resolve the conflict since they have access to all the instructions.

In case you really want to apply multiple Goggles, nothing prevents you from
creating a new Goggle with the instructions of all your favorite Goggles. If
the end result is satisfactory, please share it with the community.

Goggles are meant to be modified, forked, and extended.


## Can Goggles ownership be transferred?

The identifier of a Goggle is the URL to its specification. Purposely hosted
outside Brave control, no identity or sign-up is required to create or use a
Goggle.

Again, a Goggle does not belong to Brave in any shape or form, but rather
entirely to the community or individual that created it.

A side effect of this approach is that the URL itself is the proof of
ownership, which can make migrations to a different URL impossible without
starting from scratch.

Anticipating this problem, we built a simple transfer model. To transfer a
Goggle, you need to add the `transferred_to` metadata attribute to the old
Goggle, pointing to the hosting URL of the new Goggle. You can then submit the
old Goggle again to signify the transfer to Brave Search. For example:

```
! name: Original
! description: This is the original Goggle
! author: John
! public: true
! transferred_to: https://gist.github.com/paul/965503febec9a9e917fb816b1ff8820e
```

Where `https://gist.github.com/paul/965503febec9a9e917fb816b1ff8820e` is the
URL hosting the instructions from now on (i.e. "transferred_to").

Both URLs must be registered Goggles for the transfer to be successful. In the
case of success:

* All users of the old URL will be redirected to the new one, so no followers of the Goggle will be lost. This also includes statistics such as popularity.
* A copy of the content of the Goggle on the old URL will be stored by Brave indefinitely as immutable. Once transferred a Goggle cannot be updated further.
* A Goggle can only be transferred once (after successful transfer the Goggle is immutable).
* All transfers will be logged and publicly accessible for transparency and traceability (coming soon).

Note, there are no guarantees of the truthfulness or accuracy of any Goggle
outside the reputation of their creators/maintainers. 


## Do Goggles contribute to polarization?

We believe that Goggles do not contribute to polarization or echo chambers. In
fact, we believe they can help combat these issues.

First, Goggles does not always have to be about polarizing topics such as
politics. Of course, this kind of Goggles will exist and be popular. For
instance the team at [Allsides](https://allsides.com/) have already built
multiple addressing different political leanings. 

However, we believe that most Goggles will deal with specific use-cases that
are too niche to be properly covered by an all-purpose search engine, which of
course caters to the largest audience possible. The educational “Tech Blogs” or
“1k short” Goggles would be good examples of this. The Web is too large to fit
on a single result page; Goggles aim to tackle this problem.

It is very important to stress out that Goggles alterations are explicit.
Contrast this with the current “personalization” found in search or social
media (which naturally tend toward echo chambers by social affinity), which are
implicit. Users are mostly oblivious to the fact that results have been
“tailored” to their taste.

The person using Goggles is making a conscious act when applying a Goggle, and
contrarian perspectives should be readily available. This explicitness alone is
an improvement from the current landscape, where this kind of alteration is
made without the person realizing it.

Of course, Goggles won’t solve polarization in society. Not all problems have
technical solutions, especially when involving people living in societies.
Biases, propaganda, and untruthful information always have—and always
will—exist. We take responsibility by not making the problem worse, which is a
significant improvement over Big Tech’s status quo.

Will Brave at least censor some Goggles? No, we will treat Goggles the same as
Web results: Brave will not censor or police them, with the notable exception
of CSAM content and those cases that we are legally obliged to comply with.
Goggles belong solely to their creators, and users are free to use them or not.
We adhere to the fact that it’s a conscious choice by the user that must be
respected, regardless of personal opinions.


## What’s next for Goggles?

Goggles is in beta, and subjected to evolution depending on the most important
factor: the community of creators.

We believe that the current state is enough to be open, but we’ll closely
monitor feedback.

There are some things that we already know need to be improved or expanded, for
which we welcome the community to contribute, including:

* Make it easier for non-technical people to write their own Goggles. There are multiple approaches to this goal:
  * An online editor.
  * Extensions for a tighter integration with the user, be it import of bookmarks, history and / or in-browsing tagging of domains
* We will continue to work on performance to make the expanded recall set
  larger. The instructions defined in a Goggle are not applied to Brave
  Search’s entire index, but to what we call the “expanded recall set,” which
  in turn is a function of the query. The set of candidate URLs can be in the
  tens of thousands, which is often more than enough to observe a noticeable
  effect; however, there are no guarantees that all possible URLs are surfaced
  (in search terminology, we have no guarantees on recall).
* We will work on making the Goggles language more powerful and able to target
  results in more diverse ways. For example, by allowing a match on page
  titles, descriptions, or content.


## Why is Goggles in Beta?

Goggles represents a fundamental push towards algorithmic transparency and
openness in search. The community plays a crucial role in this vision. While in
beta, we will keep Goggles on a dedicated tab at
https://search.brave.com/goggles. Once out of beta it will be integrated into
the main search interface.

Goggles, especially while in beta, is a living project. It will evolve thanks
to the feedback and needs of the community of builders.


## Why is a particular page not recoverable with Goggles?

With Goggles, it’s straightforward to implement custom search engines like a
site search. However, you might notice that some pages you know exist cannot be
retrieved.

Goggles do not apply to the whole Brave Search index, but to the expanded
recall set which is a function of the input query. So if the target pages
aren’t in the recall set, or even be in the Brave Search index, they won’t be
captured by the Goggle.

As of June 2022, the Brave Search index contains about 12 billion pages. This
is of course a much smaller number of pages than exist on the Web. Also note
that we don’t index all the content in a page, but rather only fragments that
our models consider relevant. This, too, reduces the recall options.

These particular design decisions are to limit our infrastructure costs, and to
help us deal with the “garbage-in, garbage-out” problem. Building a
fully-fledged search engine is a massive task; to offer a true alternative to
Big Tech, we must be smart about how to do it. Following conventional design is
not an option.

Want to help us improve recall and coverage? Check out the [Web Discovery Project](https://github.com/brave/web-discovery-project/blob/main/modules/web-discovery-project/sources/README.md).


## Can anyone create a Goggle or is it only for developers?

Everyone should be able to use or create a Goggle.

For simple Goggles, the [Goggles syntax](./goggles/quickstart.goggle)
can be mastered in a few minutes.

The most important thing is to create a Goggle domain knowledge. If you’re
knowledgeable about a particular topic, for instance gardening, you’re probably
aware of a handful of very good domains, and several more that rank highly
despite so-so content.

A simple Goggle could be just boosting those “very good” domains and demoting
the “so-so” ones. That alone could improve the search results for your
gardening queries a great deal; it could also improve the search results of
other gardening lovers.

You don’t have to create a new Goggle from scratch—you could also use an
existing one, discover it’s missing some relevant domains, and message the
Goggle owner to adjust.

Of course, if you’re a developer you’ll easily be able to gather more
comprehensive lists, and fine-tune the Goggle faster. But don’t let the syntax
or developer lingo discourage you—knowledge about the domain is the most
crucial factor for a useful Goggle.


## How can I discover new Goggles?

This question is about discovering Goggles as a user; as a creator, please
check the question “Sharing a Goggle with the world.”

There are basically two ways to discover a Goggle:

1. Any link to Brave search that contains a Goggle URL will automatically make
   use of that Goggle, and you can follow it if you want to keep using it in
   the future. The community that created it might have the link on their
   website. Its users might also tweet about it or send the link by email.
   Brave is not in control of the Goggle—it belongs to the owner(s), as it
   should be.
2. Another way to discover Goggles is to visit the discovery page at
   https://search.brave.com/goggles/discover, where you can search among all
   existing public Goggles and see if there’s one that fits your needs.

It’s early, but we believe that Goggles are best discovered by links on a
community of interest. Following the prior question example, a gardening
hobbyist might be part of a couple of forums, and chances are that some other
forum members have already put their domain knowledge about gardening into a
Goggle.
