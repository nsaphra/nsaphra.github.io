---
title: What Does a Coder Do If They Can't Type?
date: 2019-08-08

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors:
    - admin

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags:
    - personal

summary: In August of 2015, my hands stopped working. This is what happened next.

---

In August of 2015, my hands stopped working. I could still control them, but every movement accumulated more pain, so every motion came with a cost: getting dressed in the  morning, sending a text, lifting a glass. I was interning at Google that summer about to begin a PhD in Scotland, but coding all day would have left me in agony. In relating this story, I often mention that for months before I learned to work without my hands, I had nothing to do but go to a bar and order a shot of vodka with a straw in it. This is a very funny joke.

I have been in pain for four years.

---

## Talon

Due to this disability, I cannot type or write by hand. Many people have asked me about the stack that enables me to be productive in spite of this limitation. I hope this information is helpful both for people with more severe limitations, and for programmers with mild repetitive stress injuries who can benefit from reducing their keyboard use.

The star of the show is [Talon](https://talonvoice.com/), a system which makes it easy to write customized grammars and scripts that work with speech recognition systems to enable programming. Commands range from simple aliases for common symbols to complex meta-commands which repeat a previous utterance or  change dictation modes. For example, just in the case of parentheses, I have separate commands for `(`, `)`, `()`, and `()⬅️` (which leaves the cursor between parentheses so my next utterance is bracketed).

 Each Talon user has a number of personal scripts. The most precious script that I've written is probably my indexed clipboard:

{{< highlight python >}}
 from talon.voice import Key, press, Str, Context
 from talon import clip
 from .talon_community.utils import *

 ctx = Context('clipboard')

 def copy_selection(m):
     with clip.capture() as sel:
         press('cmd-c')
     if len(m._words) > 1:
         key = ' '.join(parse_words(m))
         value = sel.get()
         keymap['paste %s' % key] = value
         ctx.keymap(keymap)
         ctx.reload()
     else:
         clip.set(sel.get())

 keymap = {
     'paste': Key('cmd-v'),
     'clip [<dgndictation>]': copy_selection,
 }

 ctx.keymap(keymap)
{{< / highlight >}}

 The use is simple. After selecting a particular phrase using my cursor control commands, I say "clip [foo]", and every time I want to enter the same phrase after, I say "paste [foo]". I therefore only have to dictate a particularly obnoxious variable name once. However, it does introduce a new challenge: every variable has two names, its written name and its spoken name. This unfortunate side effect exacerbates the difficulty of naming variables, which has been called "the hardest problem in computer science".

 If you are a vim or Emacs power user, this may all feel familiar to you. I have commands for searching, moving a cursor, selection, and manipulating the clipboard. Learning to dictate code is a lot like learning a new text editor very thoroughly, down to the challenge of customizing for your particular languages and needs.

The [Talon community](https://github.com/dwiel/talon_community) has specialized commands that take effect depending on application or programming language. For a Perl user, for example, a good starting point might be to borrow settings from Emily Shea:

 {{< youtube Mz3JeYfBTcY >}}

 My Talon setup relies on Dragon for the speech recognition side. Unfortunately, Nuance has discontinued OSX Dragon editions that make scripting possible. The coder behind Talon, [Ryan Hileman](http://ryanhileman.com/), is working on a suitable replacement but at time of writing, it is not yet ready.


---

### Interlude

People often ask for my diagnosis, but it officially depends on the country I'm in. After an initial assumption that carpal tunnel was to blame, a rheumatologist gave me my first American diagnosis: *fibromyalgia*, a word which is Doctorspeak for "go away".

I did not go away. A neurologist performed a skin biopsy that led to my official American diagnosis of "idiopathic small fiber neuropathy", meaning that I am missing crucial nerve fibers that transmit heat and pain but nobody knows why. *Idiopathic* is also Doctorspeak for "go away".

I went away to the UK. I brought my medical records from America, but my British neurologist did not read my records or perform examinations. After a brief conversation, he gave me my British diagnosis by submitting a note that he had no evidence of any physical cause, and he "suspected significant functional overlay", which is how they teach you to call someone delusional in medical school.

My GP read the note and informed me: He would not prescribe me painkillers. He would not send me for a second opinion from a neurologist, or treatment from any other specialist. The only referral he would write would be to a psychologist to help me "resolve the underlying issues behind my pain".

He then kicked me out of his office for using the word "fucking". "We do not tolerate cursing", said a sign in the lobby.

---

## Equipment

For dictating, I use two different microphones. In the office, I use a [Sennheiser ME-3](https://en-uk.sennheiser.com/me-3-ii), while for travel I use a Bluetooth headset, the [Sennheiser MB Pro 2](https://en-uk.sennheiser.com/mb-pro-1-uc-ml-and-mb-pro-2-uc-ml).

Another essential piece of equipment for me is my foot pedal, a [PageFlip Firefly](https://www.pageflip.com/products/firefly). It is programmable, so I have modified the settings to include one that is useful for reading papers in [Skim](https://skim-app.sourceforge.io/), with the left pedal corresponding to a click and the right pedal corresponding to down arrow. I can use my feet to scroll, and to click for annotations. Another pedal setting I have added maps the pedals to click and shift+enter. This setting is useful for Jupyter notebooks and writing my research notes and mathematical scratch work in [Quiver](https://happenapps.com/).

When my hands are unusually aggravated, I cannot nudge my mouse around anymore and I fall back on [shortcat](https://shortcatapp.com/), which allows me to press buttons by dictating keyboard strokes instead of using a mouse.

My final essential piece of equipment is a pair of [large wrist braces](https://www.futuro-usa.com/3M/en_US/futuro-us/products/~/FUTURO-Night-Wrist-Support/?N=4318+3294508029+3294529207&rt=rud). The primary purpose of my braces is to discourage me from habitual hand use. I always wear them at conferences, because wearing them is easier than constantly repeating, "I cannot shake hands due to a disability".

---

### Interlude

I struggle with sleep. I dream that my thumbs fall off. I dream that every bone in my hands breaks. I dream that my arms break out in open bleeding sores. I wake up and the pain remains like an invisible nightmare.

---

## Limitations

Maybe ironically, the largest concern if you begin to dictate code is that you do not develop a repetitive stress injury in your vocal tract. Speaking quietly can actually cause more damage, hydration is important, and better posture will prevent damage in your voice as well as the rest of your body. I strongly recommend finding a vocal coach who teaches actors and singers how to protect their voices. It is important to take breaks, and you may find talking tiring outside of work.

Speech recognition technology is not perfect, and the error rate is even higher if you have an unusual accent. Furthermore, it may force you to take time off from programming every time you develop a cold or sore throat. I live in fear of even minor colds.

Having a private space to dictate in is essential. I was unable to be productive working from home, but as soon as I had a private office I developed momentum on several research projects. I know that this is a huge limitation for a lot of people because of the productivity-destroying, soul-sucking trend towards open offices for all programming work. If your workplace has fallen prey to this trend, you may still have options. In many countries, large companies will be obligated to provide a space to work in if you are disabled.

---
### Conclusion

Life with my disability is not easy, but thanks to [hedonic adaptation](https://en.wikipedia.org/wiki/Hedonic_treadmill) as well as satisfying [work](http://nsaphra.github.io/publication/) and [hobbies](https://auldreekierollerderby.com/2019/08/10/the-one-gift-i-received-along-with-my-disability/), I am actually very happy. If you have recently developed a disability or chronic pain condition, it may feel like you could never adjust to the lifestyle required. That is why I have tried to give you a lens into my challenges as well as my successes. It is easy to respond to anyone who has overcome adversity with one of two reactions: "It can't be that hard," or "I could never do that". Move past both reactions. It is that hard. You can do it.

If you are currently able-bodied, please support your disabled colleagues, coworkers, and anyone you have power over in their quest to do valuable and fulfilling work. I encourage other disabled scientists and programmers to reach out to me with any questions they have.

---
*Thank you for comments on early drafts: [Annabelle Carrell](http://www.cs.jhu.edu/~vandurme/Carrell.html), [Craig Innes](http://www.craiginnes.com/), [Matthew Summers](https://twitter.com/uscm_), [Dina Lev](https://www.dinalevitan.com/), [Dominik Schlechtweg](https://www.ims.uni-stuttgart.de/institut/mitarbeiter/schlecdk/index.en.html), and [Yuhe Faye Wang](https://americanstudies.yale.edu/people/yuhe-faye-wang) (who is in The Humanities!). Thank you to [The Recurse Center](https://www.recurse.com/) for providing a private space for me to learn to dictate code. Thank you to my PhD advisor, [Adam Lopez](https://alopez.github.io/), who has unfailingly supported me and made all of this possible.*
