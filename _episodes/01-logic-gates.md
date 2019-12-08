---
layout: post
title: "Logic Gates"
permalink: logic-gates
date: 2019-12-07 16:42:46 -0500
---

Logic gates are a fundamental building-block when it comes to describing
computations. In binary logic we represent two states. Let's use two types of
cookies to represent that state: chocolate chip and shortbread.

![Chocolate chip cookie and shortbread](/assets/choco-shortbread.svg){:width="60%"}

We feed these cookies through so-called "logic gates" that take one or more
cookies as inputs and provide one or more cookies as outputs. Let's start
with the simplest gate: the identity gate.

## The Identity Gate and Your New Role as a Cookie Logician

Consider you had the job of a "cookie logician". You come into work every day
to a desk with a cookie tin to your left, a cookie tin to your right, and a
very small oven with which you can bake chocolate chip or shortbread cookies.

Your role is simple: every time a new cookie lands in your left tin you pick
up the cookie and eat it. You evaluate whether the cookie is a chocolate chip
cookie or a shortbread cookie. If it's a chocolate chip cookie you quickly
bake a chocolate chip cookie and place it in the tin on your right. If it's a
shortbread cookie, you do the same except baking a shortbread cookie.

When describing logic gates we can construct truth tables to be more
succinct. These tables show the output for every combination of inputs.

| Left Tin                        | Right Tin                       |
|---------------------------------|---------------------------------|
| {% include chocolate-chip.md %} | {% include chocolate-chip.md %} |
| {% include shortbread.md %}     | {% include shortbread.md %}     |

You've gotten pretty good at your cookie identifying job, good for you! The
higher-ups have also noticed and decided you're ready to tackle something
slightly more complicated.

## The Inverter (NOT) Gate

The next day you get assigned to an inverter desk. You'll need to use your
noodle a bit more in this role, but the pay is higher too, so that's nice.
Instead of eating a cookie and baking the same one you'll be eating a cookie
and baking the *opposite* one.

| Left Tin                        | Right Tin                       |
|---------------------------------|---------------------------------|
| {% include chocolate-chip.md %} | {% include shortbread.md %}     |
| {% include shortbread.md %}     | {% include chocolate-chip.md %} |

Wow, you're doing great. And the folks in the towers have noticed too, you're
ready for *the real deal*, you're ready to move on to gates with multiple
inputs.

## AND Gates

Up until now you've been perfectly happy treating individual flavors of
cookies as having no real semantic meaning. You know how to reproduce the
same cookie, or produce the opposite, but the cookies themselves don't have
any real meaning.

For your next role you'll need to expand your mind a bit and assign some
meaning to the flavors.

| Flavor                          | Meaning |
|---------------------------------|---------|
| {% include chocolate-chip.md %} | No      |
| {% include shortbread.md %}     | Yes     |

In other universes `No` could map to a `0` and `Yes` could map to a `1`, but
cookie logicians try not to think about such things.

With the semantic meanings out of the way, you sit down at A Big Desk with
*two* inputs with the letters AND printed in large type on the desk. You know
from your training this means if both of your inputs map to `Yes` then you
should output `Yes`, otherwise you should output `No`.

| Input A                         | Input B                         | Output                          |
|---------------------------------|---------------------------------|---------------------------------|
| {% include chocolate-chip.md %} | {% include chocolate-chip.md %} | {% include chocolate-chip.md %} |
| {% include chocolate-chip.md %} | {% include shortbread.md %}     | {% include chocolate-chip.md %} |
| {% include shortbread.md %}     | {% include chocolate-chip.md %} | {% include chocolate-chip.md %} |
| {% include shortbread.md %}     | {% include shortbread.md %}     | {% include shortbread.md %}     |

Strangely enough as you look around you notice that the only desks in the
entire logician office are `AND`s and `NOT`s now. You're not sure why, but you
try not to think about it. Despite that, you have a strange recollection that
there's more to cookie logic than just `AND`s and `NOT`s.

## OR Gates

While daydreaming in your swanky new `AND` position (it can get repetitively),
you begin thinking about other ways you could be doing your job. You remember
hearing about `OR`s, that they might exist somewhere. As a cookie logician
you quickly realize that, semantically, an `OR` should output a `Yes` if
either of its inputs are `Yes`, but `No` otherwise.

| Input A                         | Input B                         | Output                          |
|---------------------------------|---------------------------------|---------------------------------|
| {% include chocolate-chip.md %} | {% include chocolate-chip.md %} | {% include chocolate-chip.md %} |
| {% include chocolate-chip.md %} | {% include shortbread.md %}     | {% include shortbread.md %}     |
| {% include shortbread.md %}     | {% include chocolate-chip.md %} | {% include shortbread.md %}     |
| {% include shortbread.md %}     | {% include shortbread.md %}     | {% include shortbread.md %}     |

## XOR Gates

You're bored again, it happens. The logician's floor is hot, and your mind
begins to wonder. You consider one more way to do your work. Consider the
case where you wanted to output a `Yes` in the cases where your inputs
differ. In a way, this is like an `OR` gate where you discount the case where
the inputs are both `Yes`.

| Input A                         | Input B                         | Output                          |
|---------------------------------|---------------------------------|---------------------------------|
| {% include chocolate-chip.md %} | {% include chocolate-chip.md %} | {% include chocolate-chip.md %} |
| {% include chocolate-chip.md %} | {% include shortbread.md %}     | {% include shortbread.md %}     |
| {% include shortbread.md %}     | {% include chocolate-chip.md %} | {% include shortbread.md %}     |
| {% include shortbread.md %}     | {% include shortbread.md %}     | {% include chocolate-chip.md %} |

You're not quite sure why you find this particular gate interesting, but it
does have a kind of beautiful symmetry to it. You're not sure what your real
role is here, looking around you see cookies being moved all over the place
from tin to tin, as far as you can tell it's cookies and desks as far as the
eye can see. You try not to think about it too hard. You further consider
you're not sure quite how you got to the desk that morning, or any morning,
or what even a morning *is*, but you try not to think about it too hard. As
you try not to think about it too hard you pause for a beat, trying to
recall the cookies you most recently ate.

That beat stretches to a minute and you have a hard time recalling, all this
`XOR` distraction caused you to absentmindedly devour both of your input
cookies. Running your tongue along your teeth and gums you try to find any
sign of a chocolate chip cookie. You
*think* you found it, but was that from the last set of cookies? How many
cookies have you eaten today? Why are you still so hungry?

The cookies are starting to stack up on your left, and the cookie couriers
bringing them to your desk look increasingly more worried. You eventually
decide to just bake a shortbread cookie, you're *pretty* sure that's the
right thing to do.

You pass the shortbread on, and everything seems fine. You continue doing
your job, but eventually your oven stops working. This has never happened
before. You look around and notice everyone else has stopped working. You
begin feeling very hungry. You're not quite sure what hunger is, but you know
you don't like it. You grow increasingly hungry but there's no more cookies
coming in. You wonder why the cookies have stopped, why you can't make new
ones.

As the hunger sets in stronger and stronger you begin to consider your
existence. Why are you here? Is there a god? If there is a god, why has he
cursed you with this insatiable hunger? You begin to let out a scream, but
you can't hear yourself. You notice your vision has begun fading slowly. You
continue to try to scream, but you still can't hear yourself. You can't even
feel yourself talking as the world continues to fad from your eyes. You try
harder and harder, but to no avail. The last bit of your vision has narrowed
to a pinpoint. And then.

Nothing.
