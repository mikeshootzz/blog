---
title: "How I use AI as a Junior Engineer"
date: 2025-09-28
weight: 1
aliases: ["/learning/using-ai-to-learn"]
tags: ["AI", "learning"]
author: "Mike Ditton"
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: https://github.com/mikeshootzz/blog/blob/main/content
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

In August 2025, I started a new position as a junior DevOps engineer. This was my first "real" job after completing my apprenticeship. Having specialized in platform engineering, I had only briefly touched on software engineering. I learned the basics of object-oriented programming and could write simple hello world applications, but that was about it. I knew my new position would primarily involve writing code, which was largely new territory for me. So how does AI come into play here?

## Inspiration

The idea to write this article was sparked by a video called "I tried vibe coding for 30 days"

{{< youtube PDMxbbejgcA >}}
<br>
This video covered how the creator used AI exclusively to write his code for 30 days straight. Throughout his journey, he made a few key realizations: AI can't replace a human—it behaves more like another team member. The AI works best with small, junior-level tasks. As tasks become larger and more complex, the AI starts to hallucinate and becomes less reliable at following instructions. This got me thinking about how I use AI in my daily workflow to actually learn programming, rather than just "vibe coding" my way through it.

## How I go about solving a task

I think my workflow is best explained through a real-world example. When I approach solving a task, I typically follow the same four steps:

1. Understand what the task involves
2. Identify parts of the code that need changes/additions
3. Lay out a solution (pseudocode)
4. Implement the solution

Now let's walk through how I approach each of these steps:

### Understand the task

Understanding the task usually doesn't involve AI. I try to mentally map out what exactly needs to be done and ensure I understand what has to be fixed or implemented. Occasionally, I encounter topics I don't fully grasp, and in those cases, I use AI to explain certain concepts in simpler terms.

### Identifying the affected code

After I'm clear on what needs to be done, I start examining the codebase: what code needs to be modified? Are there other pieces of code that could break if I change it? This involves a lot of `ctrl` + `f` searching and digging through the implementation to understand how the code works. When I'm uncertain about how a piece of code functions, I use AI to explain it and break it down for me. In this case, AI serves as a teacher.

### Pseudocode

Pseudocode is my most powerful tool. The actual syntax of the Go language is still new to me, and I sometimes struggle to find the right constructs to use. That's why I usually lay out the implementation as pseudocode in a comment. This might look something like:

> A function that takes x, y and z as input. This should do "A" if condition "B" is met and returns "C"

I strictly avoid using AI at this point since I want to prevent writing code that I have no understanding of what it actually does.
### Implementation

Implementing the solution is where I use AI most heavily in my workflow. But before I put a prompt into [Claude Code](https://claude.com/product/claude-code), I try to write as much of the code by hand as possible. If I get stuck, I simply move on to the next part of the implementation until I reach a point where I think, "okay, now I have no clue how to proceed." That's when I turn to AI. My prompt usually looks like this:

> I tried "X" and expected result "A" but got "B"—what's wrong with my implementation?

My AI agent can then work with my existing implementation and the pseudocode comment I wrote earlier to give me the result I actually want. I give it no room to hallucinate. Claude Code typically makes the correct changes, and my code starts working. But then what? I have working code that I don't understand—great.

What I do next is chat back and forth with Claude to ensure I fully understand what was implemented and, most importantly, WHY it was implemented that way. This usually gets me to where I want to be, and I can proceed with testing everything.

## Key takeaways

There's a fine line between using AI to actually learn something and using it to be "more productive." I've done plenty of personal projects where the entire proof of concept was fully vibe coded, and yes, the code worked, but it wasn't maintainable in any way, nor did I understand any part of it.

Generative AI is a powerful tool, but you need to know how to use it properly to get the results you want. I treat AI like an engineer that extends my capabilities—it helps explain concepts I don't yet grasp, supports me in writing code, and helps me understand existing code.

I try to reduce my AI usage each day until I can write all the code by hand. Eventually, I'll probably just stick to using AI for cumbersome small tasks where I don't want to waste time writing a bash script :D
