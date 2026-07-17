---
title: OpenKore
permalink: /OpenKore/
---

## The history of OpenKore

### About me

This story is written by me, VCL. I'm the OpenKore project leader, and
I'm one of the people who started OpenKore back in late 2003. I'm also
one of the few people who haven't left the Ragnarok Online botting
community. The first time I started playing Ragnarok Online was in May
or July 2002, when iRO (the international server) was still in a period
call "beta 2", and was free.

### The history of botting

I first played manually, but it soon became boring and tedious. That's
how I started looking at bots. I can't say a lot about the history of
bots before I was introduced to them, so I'll just tell you what I know.

In mid 2003, there were many bots. I won't bore you with the details,
but here are the most widely known:

| Name | Quality | What happened to it? |
|----|----|----|
| **Revemu** |       Good |       Dead |
| **Kore** |       Good |       Dead |
| **ApezBot** |       Sucks, a lot |       Dead |

Yeah, you've read it right. *They're all dead by now!* With "dead", I
mean:

- They're not being developed anymore by the authors.
- They don't work anymore on today's RO servers.

They died because their authors have lost interest in RO.

### That's great, but what about OpenKore?

You must have noticed Kore in the above table. The name looks so much
like OpenKore! Surely it has got something to do with OpenKore... right?

Yes, that's right. Of all bots, Kore was unique: it was the only **open
source** bot. Now, what was open source again? Open source means that
anyone can view, modify and redistribute the source code. It may sound
crazy to some people, but that is the sole reason why OpenKore exists
today, and why I'm maintaining OpenKore. It encouraged people to
contribute improvements back into the community, so that everyone can
benefit.

Kore had one fatal flaw though: Kura, the original author who wrote
Kore, didn't do anything with most of the contributions. Most
contributions are just laying on the forum gathering dust, while Kura
only merged a few contributions back into the main Kore program. It
shouldn't come as a surprise that many contributors were not happy about
that. As a result, many **forks** of Kore emerged.

A few prominent Kore contributors at the time were: Kura, Karasu, Solos.

### Did you say "fork"?

Yes.

\<!-- TODO: изображение не найдено: /images/fork.jpg -->

No, I'm not talking about *that* kind of fork! The forks I'm talking
about are separate versions of Kore, maintained by other people. For
example, one of the contributors, *Solos*, made his own version called
**[Solos Kore](http://ro.horoy.com/)** (*skore* for short) which
includes his own improvements. There were other forks, but not much is
known about them. For some unknown reason, Kore's website went down for
months, and Kura was unavailable during all that time. So all the users
who used Kore moved to skore instead. Soon skore became the most popular
Kore fork.

This is not to say that Kura isn't a brilliant guy though. He was. His
technical skills were very high, and he wrote most of Kore's codebase.
His project management skills could use some improvements though.

Skore seemed to have replaced Kore, but Solos had the same flaw as Kura:
he didn't really merge contributions back into the main program. As a
result, *more* forks appeared, this time based on Skore. To make matters
worse, after a few months Solos mysteriously left - he probably lost
interest in RO. Things became *very* ugly after that:

- iRO was upgraded to Comodo, which broke a lot of bots. Bots couldn't
  detect some players and monsters. As a result, not only could bots
  easily die, they also kill steal people.
- There were still contributors on the Skore forums. A fix was released
  by those contributors, but only Solos had access to the website (where
  the download page resides). So the modified Skore version, which was
  called **Skore-revamped** by the authors, was released by posting
  download links in 'sticky' topics on the forum!
- The download page on the Skore website was never updated though. So
  lots and lots of people tried the version on the download page, which
  didn't work, and came to the forum to complain that it didn't work -
  without reading the sticky topics on the forum which link to
  Skore-revamped.

We received new complaints every day.

### Zzz.... tell me about OpenKore already!

OK OK, I'll go to the point! Obviously things couldn't go on like that.
I had a lot of experience with open source project management, and it
surprised me that neither Kura nor Solos used collaboration tools such
as CVS. So I teamed up with the other Skore contributors, and founded
the OpenKore project. **OpenKore is based on Skore-revamped.** OpenKore
would not make the same mistake that Kore and Skore made:

- The OpenKore project encourages developers to unite and to cooporate.
  So that means less forks, not more.
- Through the use of collaboration tools like CVS (kindly offered by
  SourceForge, which hosts many open source projects), many people could
  work on OpenKore at the same time, thus increasing efficiency greatly.
- Multiple people could update the OpenKore website.

So if I ever leave RO or get hit by a bus, the other people can pick up
where I left without having to reinvent the wheel over and over again.
The "Open" part of OpenKore emphasises OpenKore's open source nature.

The original Kore website came back online, this time hosted on
SourceForge (just like OpenKore). But Kore was as good as dead - Kura
left the scene shortly after.

Prominent developers at this time were: xlr82xs, blueviper22, junq,
Dn4cer, brokencard and myself.

**=====\> At this point, we are at late
2003.**

### Enter Modkore

One of the other Kore forks was **Modkore**, developed by Star-Kung. We
at OpenKore tried to keep low-profile because the Skore forum was
seriously polluted by people who post junk, and we didn't want those
people to find OpenKore. As a result, after the fall of Skore, more and
more people started using Modkore.

But Modkore - surprise surprise - suffered from the exact same flaw as
Kore and Skore! Well, not exactly the same. Star-Kung did use CVS, and
Modkore had multiple developers. But Modkore didn't have the cooperation
and contribution culture as OpenKore had. So OpenKore slowly gained more
developers, while Modkore's number of developers remained pretty much
constant. A rough estimation of the botting market share at the time is:

| Name         | Market share                     |
|--------------|----------------------------------|
| **Modkore**  | \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* |
| **OpenKore** | \*\*\*\*\*                       |
| **Revemu**   | \*                               |

### The pRO catastrophe

Fast forward to **early 2005**. Many
things have changed since 2003: iRO is no longer the only non-Korean RO
server. Chinese, Japanese, Indonesian, Thai, Malaysian and Philippines
servers emerged. In fact, the Philippines server (pRO) was (and still
is!) the server with the most people! If you visit RO botting forums,
80% of the posts are posted by Filipinos, and almost all questions are
about Modkore. Ironically, most questions were about where to *download*
Modkore.

\<!-- TODO: изображение не найдено: /images/waterfall.jpg -->

Something weird was going on with the Malaysian server (mRO) though.
OpenKore didn't work correctly on mRO. OpenKore developers and
contributors fixed that after a few months though, while Modkore did
not. A few months later, in March, pRO's server was changed in the same
way. So all Modkore bots suddenly stopped working on pRO! Oh no, what
now? Has the Lord abandoned us? What will become of our botting life?
But wait, rumor has it that OpenKore works on pRO. In fact, it *does*
work on pRO because mRO support was fixed!

Well, it shouldn't be hard to guess what happened. The effect on
OpenKore was like a waterfall. Here's a nice graph to illustrate my
point:\
![<File:openkore-modkore-revemu-graph.png>](openkore-modkore-revemu-graph.png "File:openkore-modkore-revemu-graph.png")

Furthermore, Modkore went closed source in mid-2005. I believe their
reason was to prevent people from making kill stealing versions of
Modkore. I believe it was a mistake to go closed source. Again, the
benefits of open source far outweight the risks. And it's actually
illegal to make it closed source, as Kore is open source and licensed
under the [GPL](http://www.gnu.org/licenses/licenses.html#GPL).

Oh, and have I already mentioned that Revemu has completely died? Revemu
has been broken since late 2003, when iRO Comodo came. Not only was
Revemu closed source, they also had very few developers. During mid
2005, someone raised the question of open sourcing Revemu on the Revemu
forums. Most of the responses, even from the users, were negative, and
were like:

- "But people will steal the source code and claim that the program is
  theirs!"
- "Hackers will put viruses and trojans in Revemu!"
- Etc...

Bollocks of course. OpenKore is the living proof that being open source
brings more advantages than drawbacks. But whatever floats their boat.

Not everybody on the Revemu forums was anti-open source though. Some
people want it to be open source. Some of the OpenKore developers went
there to clarify why peoples' fears against open source are irrational.
But a Revemu forum moderator **deleted the pro-open source posts**, not
even allowing fair discussion. That's how anti-open source they were.
Eventually they opened a poll. In the first few weeks, most people voted
for "give source code only to a few selected people". After a few weeks,
"open source Revemu" became the prominent choice. But the decision was
already made - Revemu was not open sourced.

Well, we all know what happened to Revemu. Have you ever heard of Revemu
before you read this page? Have you ever used it? No? Well that
illustrates my point.

### As time passes...

...new developers come and go. Developers who came, contributed, and
went, include: jojobaoil, anu, fov, Ven'Tatsu, aputs. Without their
contributions, OpenKore would not be what it is today.

Today, Modkore is almost inactive. They have almost no developers
anymore. Star-Kung seems to have left the RO scene.

mRO and pRO are not the only servers that constantly change. Other
servers change too. Each time, OpenKore must be modified to support the
changes.

### Various bits and pieces

- There were many other Kore forks, in particular Chinese and Japanese
  ones. Very little is known about them though. All of them are closed
  source. As mentioned earlier, it's actually
  [illegal](http://www.gnu.org/licenses/licenses.html#GPL) to keep it
  closed.
- [VisualKore](http://www.visualkore-bot.com/) started in mid 2004,
  based on OpenKore. It differentiates from OpenKore in that it's a more
  polished product. However, I've made it a policy to keep OpenKore free
  and open source forever. *(Editor's note: VisualKore is now not
  developed, not supported and not working anymore. Open source still
  survives.)*

### Lessons to be learned from history

- Open source is good. Period. If you don't believe me, look at what
  happened to Revemu.
- Being open source is not good enough. The project must also be managed
  properly, or you'll end up with a fragmented community.
- RO servers change all the time. OpenKore must be constantly updated,
  or it will stop working.
- **The constant influx of developers is what made the difference.**
  Developers come and go. Without new developers, OpenKore will grind to
  a halt, and will die.

## OpenKore today, and the status of the botting community

Why are you still reading this? Oh well, it doesn't matter, it just
matters that you *are* reading this. :)

### The Good (^ω^)

OpenKore has accomplished some good things, and we should be proud on
that.

1.  OpenKore has about **95%** market share. Some people still use
    Modkore - it still works on some servers. In fact, OpenKore is the
    **only** actively maintained bot on earth.
2.  Most of the posts on botting forums are about OpenKore.
3.  We have a better website and documentation than any other RO bot has
    ever had. For instance, Revemu only has a forum - downloads are
    linked from forum topics! Kore, Skore and Modkore only have a
    manual. OpenKore on the other hand has an informative website.
4.  We have developer documentation. Kore, Skore and Modkore didn't even
    try.
5.  Our community is international.

### The Bad (¯Δ¯)

Not everything is so rosy though:

1.  Documentation isn't 100% complete. Some configuration options are
    not documented or badly documented.
2.  Developer documentation also isn't complete.
3.  I wrote 95% of the developer documentation. :( That also means that
    if I get hit by a bus, developer documentation development will come
    to a halt.
4.  Despite all efforts in improving website usability and documentation
    quality, we still have n00bs. Those people don't read anything and
    go straight to the forum to ask stupid questions. Moderators and
    long-time users are fed up with them.

### The Ugly (¯×¯)

1.  We have a huge lack of developers!
2.  Most people these days are "leeches": they use OpenKore, and they
    ask for help on the forums, but they don't contribute anything back.

\<!-- TODO: изображение не найдено: /images/noooo.jpg -->

With "ugly", I mean **very ugly**, even **alarmingly
ugly**. Let me first define the term **"support community"**. Of
the entire OpenKore community, only a part is the support community.
People in the support community actively contribute back to the
community. Contributions can include:

- Source code. That is, helping with OpenKore's development.
- Documentation, guides, manuals, FAQs, etc.
- Moderating the forum and keeping things clean.
- Well, anything that improves the state of the community.

The support community is very weak at the moment. Let's take a look at
most the posts at the forum:

- "Help meee plzz!!!"
- "Hlp me it dosnt work!!!"
- "OMG send me config plz!!"

Well, you get the point (I hope). Too many people ask questions, but not
enough people answer them. Most people just come here, ask a question,
and then they go away without bothering to help other people (the
**leechers**). They just want zeny and items, not realizing that such
behavior will make things more miserable for everybody, including
themselves. This is how the ratio looks like:

\<!-- TODO: изображение не найдено: /images/openkore-community-leechers-support.png -->

Especially alarming is the lack of developers. We have only about 3
active developers at the moment. As opposed to 15,000 users (probably
more). People ask for feature requests all the time. They report bugs
all the time. Furthermore, there are a few thousand private servers out
there, and each day people come to our forum to complain that OpenKore
does not work on their private server. Well, OpenKore won't work on
their private server unless someone develops support for that server -
but we have too few developers and we're all very busy!

Unless these things are dealt with, the
community will go down hill, and in the near future nobody will be able
to bot anymore! This is no joke, nor am I trying to scare you:
I'm just being realistic.

### What can I do?

\<!-- TODO: изображение не найдено: /images/we-want-you.jpg -->

**You** can make the difference! In fact, people like you *are* the ones
who make a difference. OpenKore is created by the community, for the
community. Join the support community! Join us to make the botting
community a better place! You don't have to be a developer to be able to
help.

- Be helpful. Answer peoples' questions on the forum. Write/improve
  documentation, guides, etc.
- Read  to see some
  things you can do.
- If you have an idea that's not on the todo list, be my guest and add
  it. :) Or better, just do it!
- If you're a developer, please join our development team. You don't
  need to subscribe or announce yourself, just posting your contribution
  on the forum is enough.

Thank you.

## The people who made a difference


