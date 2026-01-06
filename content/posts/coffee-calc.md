---
title: "I Built a French Press Calculator Because I Can't Do Math Before Coffee (or after)"
date: 2026-01-05
tags: ["projects", "coffee", "tools"]
image: "/images/but-first-coffee.gif"
---

I'll be the first to admit that doing quick calculations in my head has never been my strong suit.

So when I got my new french press (an [Espro P3](https://www.nytimes.com/wirecutter/reviews/best-french-press/), if you're curious) and the instructions threw out ratio suggestions based on roast level, I got a headache. I just wanted coffee. Instead I was staring at a bag of beans trying to do division.

So I [built a calculator](/projects/coffee-calculator/) to do the math for me.

## How it works

You pick your roast level, which sets a default ratio. Light roasts are denser and extract differently than dark roasts, so they need less water. A 1:15 ratio versus 1:17 for dark. I knew the basics, but building this sent me down a small rabbit hole confirming the details.

Then you enter either how much coffee you have (grams) or how much water you want (oz/ml) to end up with. It calculates the other. That's it.

For me, the use case is simple: I want two cups of coffee in the morning. I enter the water amount, and it tells me how many grams of beans to grind. No thinking required, which is the whole point before caffeine kicks in.

## How I built it

HTML, CSS, and JavaScript, with a lot of help from Claude. I'm many things, but a proficient coder isn't one of them. AI made this possible in an afternoon instead of a frustrating weekend.

## What I'd change

Nothing, and that's intentional.

My problem has always been overcomplicating personal projects. Adding features, anticipating edge cases, building for users who don't exist. I'm trying to learn to make simpler things and appreciate them for what they are. This calculator solves my problem. It's done.

I also considered only including dark roast since that's what I drink. But who am I to ignore people with other preferences and a similar disposition toward mental math?

**[Try the calculator →](/projects/coffee-calculator/)**