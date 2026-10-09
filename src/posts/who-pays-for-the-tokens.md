---
layout: post.njk
title: "Who Pays for the Tokens?"
excerpt: "AI features cost money every time someone uses them. That changes how products get priced, and it makes cost a product decision."
author: "Mari Anuashvili"
date: 2026-10-08
tags: ["product-management", "ai", "pricing", "unit-economics"]
---

Software used to have a great deal going for it. Once you built the thing, serving one more customer cost almost nothing. That's how SaaS companies got away with charging a flat price per seat and keeping most of every dollar.

AI changed the math. When someone clicks "summarize," the product calls a model, and that call costs money. So the more people use your AI features, the more you pay. One venture firm's [2026 benchmark](https://avanteventures.com/en/library/ai-startup-gross-margin-benchmark-2026) puts gross margins for AI startups at 50 to 60 percent. Traditional SaaS was built on something closer to 80.

It's easy to see that as the finance team's problem. I don't think it is. PMs decide which features call a model and how often, which means a lot of these costs get locked in during product meetings, long before anyone in finance sees a bill.

## Your biggest fans cost the most

With flat pricing, a customer who uses your AI feature twice a month is great for business. The customer who uses it all day, the one who loves your product, might cost you more than they pay. So the better the feature does, the worse your margins get. That's a strange place to end up.

## How companies are dealing with it

The most common answer is to keep a simple seat price, budget for average usage, and put limits on heavy users. Customers like predictable pricing, so this is easy to sell. The catch is that you're guessing how people will behave, and when you guess wrong, the limits land on your most engaged users.

Some companies charge for usage instead, with credits or pay-as-you-go plans. Cost and revenue finally move together. But people don't like surprise bills, and once every click feels like it costs something, they start using the product less.

Then there's the option we picked for DevSum: let users bring their own API key.

## What we chose for DevSum

DevSum turns a developer's GitHub activity into daily AI summaries. Each user connects their own OpenAI key and pays for their own usage. For developers, that made a lot of sense. Many already have a key, plenty of them want control over where their code goes, and we didn't have to set a price before we knew how people would actually use the product.

Where it hurt was onboarding. Asking someone to go create an API key and paste it in before they've seen a single summary is a lot. If I built it again, I'd let new users try a few summaries on our key first, so they see the value before we ask them to do any setup.

## Cost is a design decision now

The shift I find most interesting is that plenty of engineering decisions are really pricing decisions.

Take something as small as when a summary runs. Generating one on every commit versus once a day sounds like a technical detail, but it can multiply your costs several times over. Same with which model you use. The most capable model probably isn't necessary for every task, and a cheaper one might be fine where nobody will notice the difference. Even caching matters, since nobody wants to pay twice for the same answer. Each of these choices trades a little quality or freshness for a lot of margin, and I think the PM should be part of every one of them.

One habit I'd recommend before shipping any AI feature: estimate what it costs per user per month for a light user and a heavy one. If you can't, you probably don't understand the feature well enough to ship it yet.

## The question I ask now

Whenever I look at a new AI feature, my first question is who pays each time someone clicks it. The answer says a lot about whether the feature can survive its own success.