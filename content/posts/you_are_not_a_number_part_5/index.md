# Part 5 - Aristophanes was right

## OAuth, and Web 2.0

In 2006 a relatively minor player in this narrative joined the party. 
Twitter quickly made waves because it was, by the standards of the time, open. 
If you were cool, people with twitter could tweet right from your site.

Eventually Twitter's openness ran into the problem that every open thing does, which is that bandits show up to shut down the party.
In this case, the trouble was that people entering their Twitter password into random websites wasn't the best security practice. 

To save the people from themselves, some very smart got together and came up with a protocol called OAuth.
It's successor OAuth2.0 would become as close to singularly dominant as software gets, being the method used by Google, Meta, Microsoft, and thus anything that uses them for authentication. 
The original [OAuth rfc][oauth] is a pithy 38 pages, and well worth the read if you want to know more about auth.

So what is oauth? 
Well basically it says that you cannot be trusted to sign into things, so instead you'll just sign in to things you trust like Google and/or Meta, and they'll handle, out of the goodness of their hearts, the hard part of keeping you safe from the internet bandits. 
For their troubles, they'll get an ongoing list of every service you use from now until the end of time. 

Sounds like an even trade right?

### The smart phone

In January of 2007, Steve Jobs stepped onto the Apple stage in his trademark black turtleneck, and told the world that Apple had put an iPod in a phone with the internet. 
Missing the opportunity to call it the phoneputer, the iPhone would launch that summer starting the smart phone on the trajectory towards arguably the most important product category on Earth. 
The first android devices would launch the next year. 

In 2005, only about 10-15% on humans owned computers, and none of those who did could take them _everywhere_ and use them _all the gosh darn time._
Fifteen years later, half of all humans owned computers, with almost all of that half owning a tiny computer that was coming with them everywhere they go. 
And pretty much all of them were signed in to Google and Facebook. 

### The cloud

2007 was an auspicious year for humanity's story with computers.
A plucky book selling company named Amazon had grown to a large enough size that they were having trouble keeping everyone's carts up to date. 
To address this, they built a system called Dynamo (now branded as DynamoDB), and presented it to the world in [a paper][dynamo] at an ACM conference in the fall. 

It was a watershed moment in distributed systems design because it allowed for the system to run on a large number of (relatively) cheap machines, as opposed to the hugely expensive enterprise systems available at the time. 
People started wondering if they could lease time on these servers, and AWS was born. 

The second iPhone, and the nascent android phones came with app stores. 
This significantly lowered the barrier of entry for developers to reach users, while also providing a rapidly growing userbase eager to use their crispy new devices.
Speed was the name of the game, and if app creators could offload the boring backend stuff to someone as prestegious as Amazon, what was a few bucks a month?

This setup for backend stuff was collectively called the Cloud, and if you were around in 06 and 07 you heard it ad nauseum, but no one could explain what the heck the Cloud was.
So allow me.

The Cloud meant that instead of buying and owning the computer(s) your software ran on, you could rent computers from someone else. 
Whether that was good or bad at the time I think could be discussed, but it certainly doesn't seem great now that two of the three largest cloud platforms are run by the world's largest advertiser, and the eCommerce shop that sells you all the garbage you get advertised to about.

This was nearly twenty years ago. 
Moore's Law suggests that machines are 1,000 times more powerful today. 
Wright's Law suggests that that should correlate to a 90% decrease in price. 

Do you feel like things in the cloud are 90% cheaper?


[fbvduguid]: https://en.wikipedia.org/wiki/Facebook,_Inc._v._Duguid
[linktree]: https://www.adamenfroy.com/linktree-alternatives
[onion]: https://theonion.com/t-herman-zweibel-in-memoriam-1819583647/
[birthday]: https://en.wikipedia.org/wiki/Birthday_problem
[elwood]: https://en.wikipedia.org/wiki/Elwood_Edwards
[oauth]: https://www.rfc-editor.org/rfc/rfc5849
[dynamo]: https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf
[bitcoin]: https://bitcoin.org/bitcoin.pdf
[sim]: https://en.wikipedia.org/wiki/SIM_swap_scam
[investigation]: https://www.vice.com/en/article/fcc-propose-fines-verizon-att-sprint-tmobile-selling-location-data/
[oh-the-forties-were-a-looong-time-ago]: https://www.nationalgeographic.com/history/article/141207-world-war-advertising-consumption-anniversary-people-photography-culture
[flatiron]: https://en.wikipedia.org/wiki/Flat_Iron_Building_(Chicago)

[^1]: "auth is short for authentication (authn) and authorization (authz). The former establishes who you are, and the latter establishes that you are able to do what you're trying to do. I like writing about auth, which is why I'm going to leave this as a footnote, and not add fifty paragraphs to this post."

[^2]: "Elwood was paid not one, but two cool Benjamins for his recording of perhaps the most well-known voice acting of the 90s."

[^3]: "If you make your money from ads, I've got no beef with you. The ad-dispensing companies have made it their mission to encroach on your creative space as much as possible to extract value from your hard work. I'm here to help carve out a path to you making more money in addition to how you use the ad networks."

[^4]: "When Google created a parent company Alphabet, Alphabet dropped the don't be evil. The don't be evil line moved to Google's code of conduct. I wanted to avoid inferring anything from this, but when you change something like don't be evil to anything else, it's worth a questioning glance."

[^5]: "I told you not to look it up"

[^6]: "This story is a little different than what I've represented here, and this is mostly based on my recollection of the film the Social Network, which was itself inaccurate, but I don't much care. Facebook is the largest deseminator of disinformation on the planet, and I'm not too worried about them getting a turn."

[^7]: "Yes there are plenty of bank fees, and some accounts do have monthly fees, but those are largely just because banks are dicks"

[^8]: "So banks don't hold a lot of cash, because cash is better used in investments. So to handle their day-to-day operation they borrow money for really short terms (like for a day) from money market funds. They pay this back with a small amount of interest, and that gets paid to the investors in the money market. When Lehman Brothers collapsed, the debt it owed to the money market represented money that was effectively gone."

[^9]: "These jamokes reneged on so many dumb promises this time, but the one that I think just really sums it all up is Haven, the healthcare venture that Warren Buffet and Jeff Bezos started to fix healthcare. It shudown unceremoniously in 2021, after doing nothing. The second richest man on Earth just gives up after a couple of years, because something's too hard, what a ballsack."

[^10]: "At the time, all Starbucks employees were granted stock options, and thus the company referred to its employees as 'partners'."

[^11]: "Both The Fediverse, and Bluesky are implementations of distributed systems based on underlying protocols. The Fediverse's ActivityPub protocol, and thus The Fediverse, came first, but despite the first-mover advantage, lags behind Bluesky these days in user adoption. The reason for this is a combo of marketing and usability, and definitely outside of the scope of this footnote."

[^12]: "There are, of course, things that are so heinous, that even if they're aren't illegal in the uploader's juristiction it will result in excommunication."
