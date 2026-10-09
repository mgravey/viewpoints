---
title: "Why should we NOT get used to it?"
slug: "why-should-we-not-get-used-to-it"
topic: "Habits, systems, and scientific reasoning"
summary: "Adapting to a problem can make it easier to leave unresolved. We should keep questioning habits, examining their costs, and expecting improvement."
date: 2026-10-09
updated: 2026-10-09
tags: [research-practice, scientific-reasoning, statistics, systems]
status: published
---

{% include topic-figure.html src="/assets/images/viewpoints/clearing-the-path.webp" alt="Walkers follow a long detour around a fallen branch while one person lifts it out of the direct path." caption="We can keep following the workaround, or remove the problem that made it necessary." loading="eager" %}

In French, we have a familiar expression: *« On fait avec. »* We make do. We accept the situation and find a way to live with it.

Sometimes, we have to. But we too easily turn this temporary necessity into a permanent expectation.

A system does not work properly. We point out the problem. Changing it meets resistance, so eventually we stop asking and adapt. The problem remains, consuming a little more time and energy every time someone encounters it.

For whoever can change the system, resisting may be the cheapest option. Fixing something requires work; letting other people work around it requires much less. The cost has simply been transferred to everyone who has to use it.

And when we give up, we risk sending a convenient signal: apparently, fixing it was unnecessary. People adapted.

Our ability to cope becomes an excuse to leave the problem unresolved.

{% include topic-figure.html src="/assets/images/viewpoints/cycle-of-acceptance.webp" alt="A cycle runs from problem to workaround to habit to accepted as normal, then back to the unresolved problem. An alternative path leads from the problem to question and improve, then to less effort for everyone." caption="A workaround can become a habit that keeps the original problem in place. Questioning it opens another path." %}

I think we should keep expecting things to improve. We should question unnecessary friction, challenge choices that no longer make sense, and be willing to improve systems—or replace them when necessary.

This applies to research too.

When we get used to a method, an approximation, or even a mistake, we can gradually forget the reasoning behind it. A choice becomes a habit, and the habit becomes something nobody is expected to question.

Take principal component analysis, or PCA. People often keep the “most important” components. Here, *important* usually means *explaining the most variance*.

But why is variance what we care about?

Imagine that the quantity you want to predict depends entirely on the component with the least variance. You begin by removing that component because it explains so little of the total variance. You have just discarded the information you need to make the prediction. Preserving most of the variance does not necessarily preserve what matters for your question.

We should be able to explain why a criterion fits our objective. “This is the usual preprocessing step” is not enough.

Consider p-values as another example. Their interpretation depends on a specified null hypothesis and the assumptions of a statistical model. A p-value alone cannot establish scientific importance or replace reasoning about the question being studied. These problems are discussed in the [ASA statement on p-values](https://doi.org/10.1080/00031305.2016.1154108), [*Statistical tests, P values, confidence intervals, and power: a guide to misinterpretations*](https://doi.org/10.1007/s10654-016-0149-3), and one of my favourites, [*A Dirty Dozen: Twelve P-Value Misconceptions*](https://doi.org/10.1053/j.seminhematol.2008.04.003).

What worries me is the moment when we include an analysis because we expect a reviewer to demand it, even when we cannot justify its relevance. We might explain why it does not answer the scientific question—and still add it to get the paper accepted.

The consequences extend beyond that paper. Once published, it can become the reference a reviewer cites to demand the same analysis from someone else. A concession made to satisfy a reviewer becomes a justification for future requirements. Repetition gives the practice an appearance of legitimacy, even though its scientific justification was never established.

Eventually, satisfying the expectation becomes a reflex, and the original question disappears: *why are we doing this?*

We cannot each fight every problem every day. But we can keep recognising a workaround as a workaround, and an unresolved problem as an unresolved problem.

Getting used to something does not make it reasonable. We should keep asking why, and keep expecting better.
