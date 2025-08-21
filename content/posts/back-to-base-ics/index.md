+++
title = "\"Back to base-ics\""
date = "2025-08-15"
updated = "2025-08-15"
+++

#### from the desk of [planetnineisaspaceship][planetnine]

# What's in a name?

Ursula K. Le Guin's fantastic A Wizard of Earthsea creates a world of magic where the greatest power one can hold over a person or thing is knowledge of its true name.
A friend of mine and I were lamenting that we never had the opportunity to run in to Le Guin while we were all in Portland (he's a big deal enough that this was a possibility, I am not). 
He also shared with me her essay on [The Carrier Bag Theory of Fiction][carrier-bag].

Those of you familiar with Planet Nine's lore will know that boats feature quite heavily. 
Boats have two properties that make them useful: they float, and they carry things from here to there. 
If we relax our definition of floating to include being carried, I hope you'll indulge me in acknowledging that the carrier bag, and the boat have much in common.

(I'd like to note too that Le Guinn acknowledges the importance of stacks in her essay, "home being another, larger
kind of pouch or bag, a container for people." 
Anyone who has been drinking with me as I try to explain stacks and boats will recognize this flexibility in terminology)

The gist of the theory, which comes from Elizabeth Fisher's Carrier Bag Theory of Human Evolution, is that though bags [and boats] are essential to humans, so much so that they were likely our earliest tool, they don't fit in well with the conflict-driven hero narratives of modern fiction.
Hero worship is not just in fiction, but I would say permeates all of popular culture in the United States. 
Whether quarterback, or diva, or pedophile-turned-president, whereas carrier bags are things you get when you donate twenty bucks to PBS, which normally you wouldn't do, but now you have to because of that stupid president.

Le Guin writes in her essay:

> One relationship among elements in the novel may well be that of
conflict, but the reduction of narrative to conflict is absurd. (I have
read a how-to-write manual that said, "A story should be seen as a
battle," and went on about strategies, attacks, victory, etc.) Conflict,
competition, stress, struggle, etc., within the narrative conceived as
carrier bag I belly I box I house I medicine bundle, may be seen as
necessary elements of a whole which itself cannot be characterized
either as conflict or as harmony, since its purpose is neither resolu-
tion nor stasis but continuing process.

> Finally, it's clear that the Hero does not look well in this bag. He
needs a stage or a pedestal or a pinnacle. You put him in a bag and
he looks like a rabbit, like a potato.

This notion of narrative as a _continuing_ process is intriguing. 
Aren't stories, by definition, in possession of an ending? 
But robbed of the need for resolution, why not just go on and on?

People haven't been writing computer programs nearly as long as we've been writing stories so we don't really know what we're doing yet, and it's probably unfair to map the latter to the former. 
But I don't think it's too far afield to say that the world of Facebook and Google has it's own hero-fetish that might not be the greatest when the story doesn't end. 
"You either die a hero or live long enough to see yourself become the villain," Harvey Dent was on to something.

If the gigantocorps are our heroes, constantly on stage peacocking about like the world owes them for their benevolence, what's the carrier bag for tech?
On Earthsea we would only have to speak its name to avail ourselves of its power.
Here on plain old Earth we need that name, and then we have to build it. 

We have an idea of what it might be.

We call it a **base**.

## Billions and billions

When the interwebs was kicking off the dotcom boom, there were six billion or so people on the planet.
Twenty-six years later there are eight billion. 
In real life, we call this increase a triumph of modern medicine, in the biz we call it a scaling problem. 

If you want to bore yourself nauseous for an hour, go look up system design interview prep where some dude from a faang company takes you through building out some system with eleventy-billion users and how cool they all are to have eleventy-billion users.
He'll let you know that you need to handle a gazillion api calls an hour, and a gajillion bytes of data per call so that they can check that you know what Amazon Web Service you need to handle that kind of volume since you're definitely not building it yourself.

According to Claude, here are the top ten apps by Monthly Active Users (MAUs):

1. Facebook - 3.07 billion MAU Most Popular Social Media Apps in 2025 | Piktochart

2. YouTube - 2.54 billion MAU Most Popular Social Media Platforms & Apps (2025)

3. WhatsApp - 2 billion MAU (some sources report up to 3 billion)

4. Instagram - 2 billion MAU Most Popular Social Media Apps in 2025 | Piktochart

5. WeChat - 1.38 billion MAU (primarily China)

6. TikTok - 1.59 billion MAU Most Popular Social Media Apps in 2025 | Piktochart

7. Facebook Messenger - 947 million MAU

8. Telegram - ~800 million MAU (estimated)

9. Snapchat - ~750 million MAU (estimated)

10. X (formerly Twitter) - 556 million MAU 

Now I trust these numbers as much as a Bernie named Madhoff, but let's just take them and do some math. 

First, there's a steep drop off from one to ten, and if we assume that whatever we're building is not going to hit billion user scale immediately, maybe we can take half a billion as a starting point.
Now 500 million feels like a big number, but if we divide it by the thirty days in a month we get 16 million DAUs. 
DAUs are of course higher than that, so, in order to make the math easier, let's say its 24 million. 

That's a million users per hour if we assume a smooth average, and that's 277 users per second.
If all of those users are making like four to five api calls that's about a thousand per second. 

![A raspberry pi 5 held in front of a gorgeous landscape. It fits in the palm of a hand](./rpi5.png)
The latest in the Raspberry Pi line.

This guy above is a Raspberry Pi 5. 
It costs a hundred dollars, and can handle a thousand api call per second no sweat. 
I don't know, let's say I'm off by a factor of ten and twitter does ten thousand api calls per second. 
Do you think nazi musk can afford ten of these bad boys?

The question then is what do these companies need with the gigantic datacenters they're actually using. 
As anyone whose had an empty drawer in their house knows, nature abhors a vaccuum. 
If you're paying for computers and storage, you better be using and filling them.

And that's what they're doing, filling them with every single last piece of data on _you_ that they can. 

They're not doing four or five api calls per user, they're making forty or fifty, tracking every last millisecond you spend on posts and videos.
Did you go down, and then up? 
Did you tap for more info, check the posters profile, like, love, downvote, favorite, swipe, breathe heavily, tremble at all, you name it they're grabbing it.

And why not? 
They don't even need to pay people to analyze the data anymore. 
They just feed it to more machines to determine what combination of colors and words and graphics will get you purchasing more. 

They have to do this to pay themselves and their investors, and now that they're buying islands and rocket ships, the checks they expect look like those numbers above. 
When things get like that, you're supposed to be able to create competition to the giant firms, but how can you possibly compete with a platform serving half of the population of the Earth?

Well first we have to answer what's competition?

## The pin factory

In The Wealth of Nations by Adam Smith, his first example is a pin factory. 
It was a good in high demand back in the eighteenth century. 
One with clear inputs, and outputs, and not a whole lot of reason for global distribution. 
There weren't technological improvements other than in the manufacturing process, and the labor wasn't particularly skilled.

One interesting thing about the economics of the eighteenth century: you couldn't move pins around the globe at close to the speed of light. 

The rules of microeconomics where firms are bounded by location, and materials, are no more in a world where bits and bytes flow through tubes unfettered. 
How on Earth, pun intended, do you start a business to compete with a business that can deliver its "goods" instantaneously to everyone? 

In the biz we talk about "products."
The product is the thing that you sell, as in the thing your customers give you money for.
Do you give Meta money to use Instagram?
Who does?

Obviously its advertisers, and behind advertisers are businesses. 
They buy ads, but what is it they're buying?

Is it reach?
Is it the demographics?
Well let's talk about both of those.

Reach is the whole kit and caboodle for the internet. 
The promise that everyone in the whole world can buy what you're selling just buy you buying a domain name and setting up a small site is just as awesome today as it was thirty years ago. 

As the gigantocorp platforms grew and grew, it became harder and harder (or more expensive) to break through the noise. 
After a while, the only way for your marketing dollars to hit the ROI (return on investment) they were looking for was to "go viral."
Guess what happens when you go viral.
Your website tips over, and you run out of inventory, and a bunch of people get pissed, and it's like the lottery winner who's broke two years later because they can't figure out how to stay rich. 

What about demographics? 
Facebook boasts four billion MAUs, and Instagram half of that. 
If you're marketing something though I think you already know which app you're marketing on. 
Before the internet, people would self-select into spaces and media to consume, and there wasn't much of a need for further segmenting within groups.
There's not a huge overlap between the people walking into Hot Topic, and the ones walking into Abercrombie and Fitch, and there's no real need for those brands to intrude on blog posts becase the people who like them, will find them. 

The premise of digital advertising is that 






> So the Hero has decreed through his mouthpieces the
Lawgivers, first, that the proper shape of the narrative is that of the
arrmv or spear, starting heTe and going straight there and THOK!
hitting its mark (which drops dead); second, that the central con-
cern of narrative, including the novel, is conflict; and third, that the
story isn't any good if he isn't in it.



[carrier-bag]: https://monoskop.org/images/9/96/Le_Guin_Ursula_K_1986_1989_The_Carrier_Bag_Theory_of_Fiction.pdf
