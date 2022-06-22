<h1 align="center">Brave Search Goggles</h2>

<p align="center">
  <em>
    Search
    · Open Ranking
    · Algorithmic Transparency
  </em>
  <br />
  <em>
    <a href="https://search.brave.com/goggles">Try it</a>
    · <a href="https://search.brave.com/goggles/discover">Discover</a>
    · <a href="https://brave.com/goggles">Whitepaper</a>
  </em>
</p>
<br/>

Goggles enable anyone, be it individuals or a community, to alter the ranking
of Brave search by using a set of instructions (rules and filters). Anyone can
create, apply, or extend a Goggle. Essentially Goggles act as a custom
re-ranking on top of Brave’s search index.

This means that, instead of a single ranking, Brave Search can offer an almost
limitless number of ranking options. While Brave Search doesn't have editorial
biases, all search engines have some level of intrinsic bias due to underlying
data (the Web) and some algorithmic choices of features to select. Goggles
allows for users to counter such intrinsic biases in the ranking, and also to
create custom search experiences that couldn’t be covered by an all-purpose
search engine such as Brave Search.

Goggles are owned solely by their creators and, if public, can be used by
anyone on top of Brave Search index.

Want to start building your own goggles, or fork or extend existing ones? Check
out our Goggles [quickstart guide](./goggles/quickstart.goggle).

Want to learn more about the motivation for Goggles? Check out the [Goggles whitepaper](https://brave.com/goggles).

## [Getting Started](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#getting-started)

* [Goggles syntax](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#goggles-syntax)
* [Creating a Goggle](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#creating-a-goggle)
* [Updating a Goggle](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#updating-a-goggle)
* [Deleting a Goggle](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#deleting-a-goggle)
* [Learn by example](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#learn-by-example)
* [Fine-tuning a Goggle](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#fine-tuning-a-goggle)
* [Sharing a Goggle with the world](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#sharing-a-goggle-with-the-world)
* [What happens when two instructions are conflicting?](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#what-happens-when-two-instructions-are-conflicting)
* [How can I exclude any result not matched by my Goggle?](https://github.com/brave/goggles-quickstart/blob/main/getting-started.md#what-happens-when-two-instructions-are-conflicting)

## [FAQ](https://github.com/brave/goggles-quickstart/blob/main/faq.md#faq)

* [Who owns a Goggle?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#who-owns-a-goggle)
* [Why can’t I apply multiple Goggles at the same time?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#why-cant-i-apply-multiple-goggles-at-the-same-time)
* [Can Goggles ownership be transferred?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#can-goggles-ownership-be-transferred)
* [Do Goggles contribute to polarization?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#do-goggles-contribute-to-polarization)
* [What’s next for Goggles?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#do-goggles-contribute-to-polarization)
* [Why is Goggles in Beta?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#why-is-goggles-in-beta)
* [Why is a particular page not recoverable with Goggles?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#why-is-a-particular-page-not-recoverable-with-goggles)
* [Can anyone create a Goggle or is it only for developers?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#can-anyone-create-a-goggle-or-is-it-only-for-developers)
* [How can I discover new Goggles?](https://github.com/brave/goggles-quickstart/blob/main/faq.md#how-can-i-discover-new-goggles)


## Privacy considerations

To apply a Goggle, a user needs to pass the Goggle URL together with a query.
We treat Goggle URLs with the same strict provisions we use to handle other
data elements (like IP or geo-coordinates) that could serve as identifiers.
Brave does not track the queries of any of its users, and searching with
Goggles is no exception. However, note that if a Goggle is used only by one, or
a very small number of people, the Goggle URL could serve as an identifier, and
enable the creation of a profile of the user’s queries while using that
particular Goggle.

Learn more about our [privacy policy](https://search.brave.com/help/privacy-policy).
