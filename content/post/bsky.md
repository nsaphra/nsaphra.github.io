---
title: The AI Researcher's Guide to a Non-Boring Bluesky Feed

date: 2025-04-24

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors:
    - admin

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags:
    - manifesto

summary: How to migrate to bsky without a boring feed.

---

I am fortunate to have a decent follower count on X. However, since the algorithm started promoting bluecheck premium accounts explicitly, I have found it less useful for sharing my research. I don’t give X money to spend on destroying the American scientific ecosystem, even if it would promote my own work.

Lately, I’ve found [bluesky](https://bsky.app/) suits my needs better. In spite of my similar follower counts on the different platforms, my posts are often more reshared and liked there. The discussion is more intelligent and informed, frankly, with less vapid LLM-generated engagement bait in my paper threads.

However, if you just migrate without a plan, you’ll find yourself with a pretty boring feed. So here’s my guide for AI researchers looking to actually have fun on bsky.

## Custom feeds

Bluesky doesn’t default to an official algorithmic feed. By default, you’ll be in a chronological “Following” feed. But they do allow custom algorithmic feeds through the API! You just pin and save the ones you like.

If you are an AI researcher, I absolutely recommend adding three feeds:
- [Paper Skygest](https://bsky.app/profile/paper-feed.bsky.social/feed/preprintdigest): a personalized feed of just posts that link to papers, curated based on your follow network.
- ~~[ML Ranked Feed](https://bsky.app/profile/smcgrath.phd/feed/aaals4dn6kcoi): Trending machine learning posts. Tracks popular terms and any post with the emoji sequence 🤖🧠 (so put it in your posts if you want them picked up!)~~ Ranked is discontinued and replaced with [ML Feed Blend](https://bsky.app/profile/smcgrath.phd/feed/MLBlend), which I highly recommend!
- [MLSky](https://bsky.app/profile/alexr.bsky.social/feed/MLSky): This feed is a bit of a firehose. It’s worth following, but it’s chronological so occasionally it’ll just show the last 30 links simultaneously posted by some arxiv tracker bot.

Additionally, you should definitely be following:
- ~~[Discover](https://bsky.app/profile/bsky.app/feed/whats-hot): Says what it is, this is the official personalized trending feed. Not bad but a lot of politics in mine.~~ **Update:** I now recommend [For You](https://bsky.app/profile/spacecowboy17.bsky.social/feed/for-you), a MASSIVE improvement over the official Discover.
- [Best of Follows](https://bsky.app/profile/bsky.app/feed/best-of-follows): Another official feed, trending posts from accounts you follow.
- [Quiet Posters](https://bsky.app/profile/did:plc:vpkhqolt662uhesyj6nxm7ys/feed/infreq): This is the most important feed, especially if you are trying to follow science and not politics. Everyone you follow who posts infrequently. If your follow list is like mine, it’ll be more papers and research chat.

Of course, you can also [search](https://blueskyfeeds.com/en) whatever [keywords](https://bsky.app/search?q=NLP) you like to find other feeds. You might pick one as your “default” home feed, for example to check new paper posts before your Following feed if that’s your main objective with social media. If you run out of interesting Following content, switch to another pinned feed.

The best way to use these feeds is by having them featured in your Following feed. After pinning and saving your favorite third party feeds, go to `Settings -> Content and media -> Following Feed Preferences`, and check off “Show samples of your saved feeds.” Now even your default feed will include an assortment of extra stuff you like!


## Who to follow

I can’t tell you who to follow. But a lot of people have assembled starter packs, which make it easy to follow a lot of people at once. Dan Roy even assembled grumpy, upbeat, and balanced ML researcher [mood packs](https://bsky.app/profile/roydanroy.bsky.social). You can [search for starter packs](https://blueskydirectory.com/starter-packs/all?q=machine+learning) by keyword easily.

Another step is to import your existing X follow list. If they use the same name or handle on bluesky, you’ll find them through [Sky Follower Bridge](https://www.sky-follower-bridge.dev) but you may want to double check the generated list, which cannot be validated automatically, rather than mass following blindly.

By using your custom feeds, you’ll also identify lots of active users who post interesting content. Definitely follow them immediately. 

## Getting seen

Like any social media platform, bluesky can be hard to break into. Fortunately, popular feeds like ML Ranked and MLSky can share your posts based on keywords. Of course, engaging in discussion on other people’s posts will also help you connect to the community. Eventually, you’ll find yourself with more followers.

## Culture starter tips

The current bluesky culture includes a lot of artists who are anti-AI, a lot of people who are ready to correct you if you forget alt text on an image, and a lot of professors rather than students or tech industry people. As the user base shifts, I expect that these cultural patterns will change. Post how you like, I have no culture tips.

I recommend against following curated blocklists, a weird feature. They are a bad feature and the curator is likely to have you blocking people on bad faith.

It can be pretty boring to visit social media and only see paper discussions. You could have joined LinkedIn! So I also recommend looking for fun topics. I follow feeds for marine biology, nudibranch art, and philosophy of science. I follow some podcasters and comedians to spice things up as well.

## Why hasn’t mass migration happened?

One of the largest attempts to move AI researchers en masse from Twitter to Bluesky went poorly, antagonizing and driving away several early adopters. What happened? A huggingface employee collected a small representative sample of posts, which are public under the AT protocol, to support algorithmic feed development. This dataset triggered a huge backlash. Early users on Bluesky were often artists and writers, who are largely anti-AI. Even among AI researchers, skeptics and critics made the move long before tech optimists. This community can have a negative atmosphere around AI, especially because Bluesky doesn’t explicitly promote the bluecheck hype-men whose vapid enthusiasm dominates X. However, I have never had negative experiences sharing my work (though some have) and the negativity towards AI in my feed comes from people I’ve deliberately chosen to follow. You can make other choices!

There was one other bottleneck event: After the Trump inauguration, it became impossible to see anything but US political news on bluesky for a couple weeks. Many researchers gave up. Now, the continued improvement and proliferation of custom feed algorithms should help prevent the same issue from cropping back up.

These aren't fundamental problems. Many senior academics have migrated to Bluesky, leaving students and tech industry workers as the bulk of X's remainders. Other scientific fields have switched in their entirety. AI research appears to be more of an outlier if anything, due to the overlap between scientific research and the tech industry.

## Addendum: Bonus Tips

After writing this post, I immediately learned two more tips that have improved my own Discover feed!
- The official Discover Feed actually has a "show more / less like this" menu item on each post, which I will be taking advantage of.
- I removed a lot of the politics from my non-focused feeds through `Settings -> Moderation -> Muted Words & Tags` where I added: "Trump", "RFK", and "Elon".

I hadn't been using Discover lately because it was all politics, but it's looking much better now!


