# Part 2 - The twentieth century

## Interoperability

For historical reasons, phone numbers and email have a very useful property: interoperability.

Interoperability is an idea in electronic systems, which has largely been forgotten in our modern technical world, which is dominated by gigantic corporations looking to extract every nickel from your every digital move. 
The story of how we got there is worthy of a read, but I'll try and give the quick hits here.

Alexander Graham Bell invents the telephone in the late nineteenth century, and in true American fashion immediately establishes one of the most ruthless monopolistic corporations to ever exist: American Telephone and Telegraph Company (AT&T). 

In 1913, AT&T bought the other telecommunications monopoly Western Union, who had consolidated the telegraph system as the telephone took market share.
This was a little too close in time to Teddy Roosevelt's trust bustin' movement, and brought about the ire of the US government.

Faced with commupance from the federal government, AT&T negotiated an out of court settlement called the [Kingsbury Commission].
The Kingsbury Commission forced AT&T to divest itself from Western Union, and, important to our phone number story, forced them to allow smaller networks to connect to their long-distance infrastructure. 
This required AT&T and the other networks to start down the path on standardizing some sort of protocol for keeping their identifiers unique, and interoperable.

In the sixties, Thomas Carter invented the Carterfone, a device which was essentially a walkey-talkey connected to a phone receiver so folks could talk via radio to other folks on a phone.
AT&T magnanimously told Carter to pound sand when he tried to use their network.
This led the FCC to tell AT&T that not only did they have to allow Carter, but they had to allow anyone to connect to their network so long as it didn't harm the network. 

By the time Carter's case reached the FCC, the agency had started to recognize the need for computers to connect to each other.
They used the carterfone case as an opportunity to revisit AT&T's ability to block devices from connecting to their network.
AT&T was faced with a similar reality. 
Carter's device was little more than a nuisance, but the rapid rise of computers, and the fact that their modems were largely supplied by AT&T's Bell Labs, meant allowing firms to connect to their network could be more lucrative than maintaining their monopoly. 

I had to track down a picture of Thomas Carter to see what this legend looked like.
I was not disappointed.

![Thomas Carter looks like a character out of Dynasty with a ten gallon hat, bolo tie, mutton chops, and amber aviators](./tom-carter.jpg)

It doesn't get much more American than some guy jury-rigging a way for those in the oil fields of Texas to phone home to let their people know they haven't blown up yet that day taking on the largest company in the country, and winning so that it can ultimately make more money.

### Multi-user

These newfangled computers that were using AT&T's network to talk to each other had a problem though. 
Unlike humans that have distinct voices, the machines all talked the same. 
So to have any reasonable notion of who was behind the machine, we had to introduce _auth_.

Nowadays there are a lot of auth protocols, but back in those days it was good ol' username and password.
You need both because passwords can't be unique, and usernames don't need to be secret.

And thus as Narsil was sundered as it severed the ring from Sauron's hand, the interoperability of this original network was broken. 

## America goes online

There's an interesting problem in statistics called the [birthday problem][birthday].
It shows that you only need 23 people chosen at random to have a greater than 50% chance of two of them having the same birthday. 
The reason for this comes down to some simple math. 

Probabilities are usually represented as fractions less than one.
In this case, if we had only two people the probability that they would _not_ have the same birthday is 364/365 since there are 364 days the second person could be born on that would be different than the first person's birthday. 
The third person would then have a probability of 363/365 instead because now there are two different days that people have birthdays on. 
You continue ticking down the numerator for each person added to the test.

To find the total probability of this series of probabilities, you just multiply them all together, and when you do that for 23 people you get the probability that two people will have the same birthday just over 50%. 

What does this have to do with the price of beans in Boston?

Well that whole username and password thing was working just fine for computers connecting to things, but as the number of people grew, people started birthday probleming their desired usernames. 
There are somewhere around 20,000 common six-letter words in English.
You know how many people need to be selecting words before there's a 50% chance of two people selecting the same one?

167.

Those of you who are known as ponies724 know what I'm talking about.

This wasn't so bad when there was just one thing to sign into, but as places with usernames proliferated you had to deal with someone snaking you on ponies724.
Then you'd have to _remember_ not only your password, but which incarnation of your username to use.
Zweibel is German of onion, but it's also two-bell.
So when it's taken I use Dreibel (three-bell).
There's even one place where I'm Vierbel (four-bell).
I don't remember where that place is, but I remember it's out there somewhere. 

So the online folks went searching for a "username" that was unique to the user so they could carry them around with them. 
Something cheap, and easy to give to anyone. 
Maybe something where ponies724 could just be ponies alongside other ponies. 
Something like email.

### You've got mail

Listen, I was there.
Hearing the digitized low-fi voice of [Elwood Edwards][elwood] [^2] was awesome, and the first few emails you got were so novel and cool.
But soon there would be such a deluge of emails that had to be forwarded to ten friends to avert disaster, that it was impossible to keep up. 
Obviously those were all spam since nothing bad has happened since the mid 90s...

Email was then, and mostly still is now, the simplest open and interoperable thing that exists in cyberspace.

![Walter from the Big Lebowsky saying "I can get you a toe by 3pm," but toe is crossed out and says "email server" instead](./walter.jpg)

All you need is a domain and a computer, and you can set up an email server.
Now if you lookup how to do this you'll find a lot of things telling you not to, and the reason for that is that nowadays there're a ton of hoops to jump through to make it so that your emails actually go through.
But I can't really tell if that's to keep the spam out, or to keep the people beholden to the email giants who are gatekeeping this in the first place.
I mean, how do you feel they're doing at keeping out spam?

Once the internet got going in full swing, AOL started to lose its shine, and people started looking to alternatives for email. 
Hotmail, and Yahoo were the major players of the late nineties, and a lot of people jumped over.
There were other factors of course, but the incredible flood of users claiming free emails is partly what fueled the dotcom bubble that saw Yahoo with a market valuation of $125 billion, and made Microsoft the highest market valued company in the world (do you see a trend here?).

Then in 2000 the bubble would pop, and as so often happens the human phoenix of innovation would rise from the ashes.
And as so doubly often happens, that phoenix would exploit the masses for profit.

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
