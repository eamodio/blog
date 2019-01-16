---
layout: post
title:  "It's not (just) about the blame"
date:   2019-01-15 01:00:00 -0500
categories: gitlens
mins: 4
image: assets/posts/2019-01-15.gif
---

OK fine, sometimes it is, but let's go beyond finger pointing and talk about the far more valuable aspect of the blame features of [GitLens][gitlens] for [VS Code][vscode]. Why? Because often when I hear people talking about GitLens, it's about using these features to blame past you or someone else.<!-- more -->

{% include image.html url="assets/posts/2019-01-15.gif" %}

 If you aren't already familiar with GitLens, please [check it out ][gitlens]&mdash; go ahead, I'll wait 😁&mdash; otherwise feel free to skip over the next section.

---

### GitLens &mdash; <small>Git supercharged</small>
[GitLens][gitlens] is an open-source extension I created for VS Code. GitLens, together with Git support built into VS Code, offers a fairly complete Git GUI directly in your editor. Here's a quick summary:
> GitLens **supercharges** the Git capabilities built into Visual Studio Code. It helps you to **visualize code authorship** at a glance via Git blame annotations and code lens, **seamlessly navigate and explore** Git repositories, **gain valuable insights** via powerful comparison commands, and so much more.
>
> GitLens simply helps you **better understand code**. Quickly glimpse into whom, why, and when a line or code block was changed. Jump back through history to gain further insights as to how and why the code evolved. Effortlessly explore the history and evolution of a codebase.

---

So GitLens is often mentioned in the context of blaming someone &mdash; even though mostly tongue-in-cheek and often self-deprecating. Aside from obvious comedic effect, my guess is this is largely because of the poor naming of its headline feature &mdash;_ blame_. While GitLens adopted this naming because it's what Git and other Git tools call it (Who am I to buck the trend?), the feature is far more valuable than just blaming yourself or someone else. Now you might be rightly thinking, “_Boo hoo! You just don't like being called out for your 💩 code_”, but hear me out. 

---

> GitLens simply helps you **better understand code**. Quickly glimpse into whom, why, and when a line or code block was changed.

---

GitLens, utilizing the blame feature of Git, adds an annotation to the current line which displays the author, date, and message of the most recent commit that changed that line.

{% include image.html url="https://raw.githubusercontent.com/eamodio/vscode-gitlens/master/images/docs/current-line-blame.png" description="GitLens adds a blame annotation to the end of the current line" %}

{% include image.html url="https://raw.githubusercontent.com/eamodio/vscode-gitlens/master/images/docs/hovers-current-line.png" description="Hovering over the annotation reveals more details and actions" %}

I should also mention that GitLens provides instant, on-demand blame annotations for the whole file as well.

{% include image.html url="https://raw.githubusercontent.com/eamodio/vscode-gitlens/master/images/docs/gutter-blame.png" description="GitLens adds blame annotations to the gutter for the whole file" %}

From those simple annotations, you can now answer 3 important questions in understanding code and how it evolved &mdash; **when** did the code last change, **why** did it change, and finally **who** changed it. And by increasing the visibility and accessibility of that information &mdash; which has been part of our source control systems forever, GitLens drastically reduces the friction of answering those important questions. Now depending on what you are trying to accomplish one of those may be more important than the others, but they all aid in helping you better understand the code.

Here are just a few simple scenarios: 

- Trying to understand why the code is the way it is? Walk back in time to read the blame history about why the code evolved the way it did. 

- Hunting for a recently introduced bug? Knowing when code changed can be invaluable.

- New to a codebase or section of code and need help? Figure out who might be best in answering questions about it or collaborating on changing it.

And those are just a few of the possible use-cases and benefits &mdash; I'm sure you can think of many more. These answers, now readily available at your finger tips, provide us with powerful tools to aid in better understanding code. After all, understanding code is one of the hardest problems in software development, after of course the other two: naming, cache invalidation, and off-by-1 errors.

---

A quick aside about commit messages, since I know we always write beautifully crafted and insightful commit messages. Amirite? Yeah. Anyway, now that commit messages are highly visible and accessible, it is even more important that they are meaningful and well-structured. Git has long recommended a structured format for commit messages (below) and using that (or similar) structure is important in increasing the utility of them.

```
Short (50 chars or less) summary of changes

More detailed explanatory text, if necessary.  Wrap it to
about 72 characters or so.  In some contexts, the first
line is treated as the subject of an email and the rest of
the text as the body.  The blank line separating the
summary from the body is critical (unless you omit the body
entirely); tools like rebase can get confused if you run
the two together.

Further paragraphs come after blank lines.

  - Bullet points are okay, too

  - Typically a hyphen or asterisk is used for the bullet,
    preceded by a single space, with blank lines in
    between, but conventions vary here
```
<figcaption>Copied from <a href="https://www.git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project#_commit_guidelines">Distributed Git</a></figcaption>

---

Hopefully I have now demonstrated how much more valuable the poorly named blame feature is rather than just pointing fingers &mdash;_ shakes fist at past me_. Now if you still haven't tried [GitLens][gitlens] and/or [VS Code][vscode], what are you waiting for? 😄

[gitlens]: https://gitlens.amod.io
[vscode]:  https://code.visualstudio.com

