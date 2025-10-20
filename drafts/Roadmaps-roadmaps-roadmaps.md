Ask most people what the number one responsibility of a product manager is, and they’ll usually say, “the PM owns the roadmap.”

This definition frustrates me a little bit, but there is a kernel of truth to it. The product manager is the one person who has the most influence over the roadmap, and in many ways is responsible for maintaining it.

It turns out roadmaps aren’t easy. And since we own it, we should apply some structure to the task, so that we can be consistent ourselves (ie, not re-inventing the roadmap every few months) as well as consistent across our organization. Pretty often, we product manage some aspect of a larger product - it’s essential that our casting of the roadmap is at least compatible with the other teams, or our combined roadmap presentation will be a cacophony.

Many PMs are over busy, and don’t set aside a lot of time for a thoughtful roadmap. I have worse news for these people - I believe that it’s best if PMs maintain **three** versions of the roadmap, and that’s reflected in the title of this post.

Quick overview:
1. Quantitative roadmap - your own worksheet that allows you to apply some formula to the conflicting priorities which allows you to focus on those things which are most urgent.
2. Kanban roadmap - this is an internal representation of the product past, current, and future. It must be fungible, but most importantly, this is the representation that puts the coming release in context.
3. Published roadmap - This is the final result of the above two processes, and is curated by the product team, and contains no internal information so that it can be consumed both by high-level execs, the field, and users of the product.

Let’s unpack this. Each of these roadmap isn’t an artifact, so much as it is a **tool**. That’s why roadmaps aren’t called out in the [Three-Fundamental-Artifacts][three-artifacts] post. You can differ with me on this, it’s fine.

## Quantitative Roadmap

Tool: Spreadsheet

Quantitative roadmap should be Product Manager Lesson #1. Good product managers are nearly always swimming in data. That data can be twisted to support nearly any agenda. If there isn’t a consistent formula to compare all of the things the team could do, then over time, the data loses credibility because it's clear that the product manager is biased, and only collects data which supports their agenda.

Enter the quantitative roadmap. This allows you to apply weights to desires, based on an easily-understood formula, so that consumers of the roadmap can see the care and effort the PM has put into assembling an impartial scoring of all of the possible initiatives. The resulting ranking gives us all a good idea of what the most important things could be, but more importantly, allow us to discard the many things with relatively low scores. As mentioned in the book Farther, Faster and with Far Less Drama, giving ourselves permission not to constantly reanalyze low-priority items frees us to focus on the most important things.

Example ping pong supplier:

```mermaid
kanban
  col0["**50x** Customer commitments"]
    surface["Competition-level table surfaces"]
  col1["**20x** Announced at conferences"]
    display["Digital score-keeping display"]
  col2["**10x** Competition has (tablestakes)"]
    paddles["Paddle surfaces have 5 levels of stickiness"]
  col4["**5x** Competition does **not** have (competitive advantage)"]
    airtag["Paddles locatable via AirTag integration"]
  col5["**2x** Improves user adoption"]
    ftue["Rules of Ping Pong introductory video"]
  col6["**1x** Nice to have"]
    inet["Internet-connected table tracks # of ball-hits per rally"]
```

These weights are very generic. You can use them as-is, or you need to choose what formula makes sense for you. In a recent example from my history, the ranking of an OSS model on a leaderboard affects its prioritization - we only have so much capacity to optimize models, we might as well spend that time working on the most popular.

## Kanban-style Roadmap

Tool: Trello-style app

This next roadmap format is a really important tool to communicate, as a result of prioritization, when projects are likely to land. Just showing your stakeholders priority scores isn't very helpful - this representation takes into account the scope as provided by your product development team, so that you have a rough idea of which release each project will land.

I've used a Kanban-style to show this, both because it prevents people from asking for details many releases into the future (I can't predict that) and the simple Trello-style UX allows me to move cards around very easily. This representation has been a very powerful negotiation tool, imagine this scenario:

> I get a call from Richard, who is a Sales exec who is responsible the entire Northeast region. He's angry with me because I haven't prioritized Kevin's ask, and Kevin's on his team. Kevin has been complaining to Richard that the product team is blocking his big healthcare deal, and Richard wants to know why I'm not showing his team the love. "Let me quickly screenshare our planning roadmap," and I show him three major things all in one screen: Things we haven't sent for development yet, things that the product team is working on right now, or has released recently, and importantly, a reminder of the things we've shipped recently. By moving the cards around in real time with Richard, "OK, if I pop Kevin's ask into Ready for Implementation, making sure that the team will work on that next, then I'll have to pull something back to Scoping, and that will have to wait for the next release. Which of these things do you think is worth postponing in order to get Kevin's feature out ASAP?"
    
Nine times out of ten, Richard sees that we've done a good job of prioritizing, and that if we shuffle the order, it'll cost his greater team. On that last count, where Richard cares about Kevin and only Kevin, I can offer to escalate, "Kevin's asking us to give up a lot of opportunity. We should talk with leadership if this trade-off is really worthwhile." I can usually rely on my boss to be firm with a hothead, but you know, sometimes that healthcare deal really is strategic, and by escalating, we get permission to set aside our standard prioritization. By getting that mandate from leadership, we give the team something to rally around, "Let's go win that healthcare deal!"

```mermaid
kanban
  col0[Icebox]
    lasers[Add laser beams]
    sharks[Add shark tank]
    sub[Submarine mode]
  col1[PM Researching]
    backup[Second time machine option in case of primary failure]
    guitar[Marty McFly guitar storage]
    amp[Optional plug-in for electric guitar input]
  col2[Scoping for Release]
    controls[Improve time-and-date settings controls]
    fire[Time machine should not leave tracks of flames]
  col3[Ready for Implementation]
    headlights[Functional headlights for nighttime time travel]
  col4[In Development]
    train[Time machine should connect to train in case of engine damage]
    windmill[Optional cable to connect to windmill for lightning strike initiation]
  col5[Current GA Release]
    color[Time machine color configurable]
    tires[Introduce whitewall tire option]
  col6[Last Release]
    fly[Time machine should fly rather than drive]
    fusion[Time machine should use any kind of fuel, ie banana peels & beer]
  col7[First Release]
    flux[Flux Capacitor]
    plutonium[Plutonium storage]
    car[Time travel components should be integrated into a car]
```
- Icebox: A jumble of ideas, spanning good to terrible, that for various reasons, are not an organizational priority. This column is valuable because everyone's idea deserves to be heard, and they should know where they stand in the overall process. If they feel that their idea deserves more attention, they have an object they can point to, with some light metadata, like how long the object has languished in the icebox. This demonstrates that ideas are considered and prioritized according to the goals of the organization. If the goals change, we're always happy to re-prioritize. But if the goals haven't changed, at least nobody can claim that you've been burying, or refusing to consider their revolutionary ideas.
- PM Researching: These are ideas that have come to us from all over, and we've accepted them as possible good ideas to include in the product, but either we don't know how, or haven't chosen to prioritze them yet. This list is in semi-priority order - don't put too much effort into A above B, just enough to give some order to the list. This is usually a pretty long list.
- Scoping for Release: The PMs have decided that an idea should be included in a release, but it's not ready yet. First, we expand the scope of effort to include the balanced leadership team (not just the PMs). From here, we have to do research, decide on workflows, get feedback and approvals. etc. (See [Three-Fundamental-Artifacts][three-artifacts] for those steps.) By being in this colum, we're messaging to stakeholders, "this is important, we're putting time into the design, and it will appear in a coming release," without commiting us to a time line or specific release.
- Ready for Implementation: The balanced leadership team has done our job, this idea is now ready for final approval and will be picked up by the product development team for implementation "soon," again, without committing the team to a specific release. If there's three quarters worth of ideas that are ready for implementation, then the stack will get shipped over three different releases. Beacuse of this, this list should be in strictly priority order. Whatever's at the top of the list is definitely going into the next release. The second item maybe, the third item, not so sure, and so on.
- In Development: The product development team has accepted the design, and is in active implementation. All of the artifacts which describe this work should be available to stakeholders - the PRD, the epics, the stories. Whatever you have, make it clearly visible. This is your last chance to get validation that the team is doing this in a way which will be used by customers - get all the reassurance you can.
- Current Release, Last Release, N-1, N-2, etc.: I find it helpful to share the context of what we have shipped so far. Without this, it's hard to demonstrate momentum. I really like to show at a high level, "OK, I know you're excited for your pet feature, but look at all the value the team has shipped! You know this team is reliable - if your idea is priortized here, you know it'll ship soon." Momentum builds confidence - make sure to demonstrate that momentum and get your team the recognition they deserve. Conversely, if you've never shipped anything yet, this is a great place to show people how risky things are, "This proejct is still in its early phases; we need to focus strictly on the most fundamental things, and make sure we build a good rhythm before we get excited about a thousand knobs and buttons. I need to keep the team focused on winning those first anchor customers; for that reason, I really need to keep your idea in the backlog."

## Published Roadmap

Tool: Slide deck

The first two are your planning tools. You use them with your teams and your stakeholders to set plans in motion. They've got a ton of confidential information in them, account for all sorts of internal dysfunction, etc.

There lots of resources on [outcome oriented roadmaps][outcome-roadmaps]. It took me a long time to understand, but I agree with this approach now. Many people won't care about features at the roadmap level. If you're frustrated by that, because either you don't know the outcome a feature enables, or you think the feature enables, "so many outcomes it feels wrong to narrow it down to just one or two," then please consider my argument.

Since we spend every day with our product, product managers tend to have a lot of pride in what the team has built, "It slices, it dices, it even makes julienne fries!" Most users won't care about your product as much as you do. They probably wish they didn't need it at all. They are willing to spend money, or in other ways invest in your product beacause it's better than choosing to solve the problem on their own. Whatever that problem is, they care most about the outcome that it provides, and how easily they can access that value. (And that it's durable, secure, and supportable.) 

When we communicate our roadmap externally it's important, in as few words as possible, to describe what the users will get out of the product, rather than describe what the product is. If you are having trouble narrowing it down, think about one or two use cases that people are doing now, or short of that, what your anchor customers plan to do with the feature. It's ok if you don't explain all of the possibilities of a feature in a roadmap. People will figure it out. For now, just make sure that people get a gist for what the feature is _for_. They'll figure out the rest later, or you can fill in the gaps later with continued product marketing.

Try to avoid creating a, "roadmap slide." People ask for this all the time, but I feel that, without context, a single slide doesn't accomplish much, unless it's to be included in an overview deck along with dozens of other similarly-formatted slides. Instead, I try to create a slide deck which helps facilitate a roadmap discussion.

> I once took over as director of engineering for a service where the founders had selected all of the infrastructure themselves. Our team was having terrible trouble with the storage arrays, which the founders had selected because they had excellent ATA over Ethernet performance(!) For months we struggled with their support team till I escalated. "We're running some of the Internet's most popular services on your storage, but we're not getting the performance we expect." To my surprise, they were dismayed, "You want low-latency performance for high performance websites? We've been positioning our product as a tape library alternative. We do care about performance, but totally different than what you care about."

A roadmap meeting is a place to articulate your product's general direction by sharing your track-record so far and where you are planning to go. The goal of the meeting is for the user to decide if their needs are aligned with your goals, and to feel special that they can give you feedback on what's coming soon, to better suit their needs. When everything works well, a roadmap meeting turns into an opportunity to identify anchor customers, and cite them as high-likelihood to adopt the product in the future.

[TODO] Here's a progression that has worked well for me in the past.

[TODO] a tweet from an actual customer, "... upgrades in prod on a holiday weekend .. That has never happened in my entire career ... Just watched the pipes do what they do"

The basic organization of the roadmap area of the deck breaks things down into this progression, because not only is Biz Dev often pretty bad at Product Management, but the customers we're talking to usually aren't used to thinking this way. If you walk them through it, usually I've gotten a pretty positive response:

### Simple Roadmap Story
1. Here's a slide or two to make sure y'all remember the high-level value of our product (you spend less time doing something, something becomes self service, you can do something you were never able to do before, etc). We all agree that's why you're interested in the product overall, right?
2. Here's a list of your favorite features that you're dying to ask me about. I have them all cataloged, I get it. (So calm down, I'll get you there. But I'm not going to put dates next to each of these items.)
3. Here's how I cluster all these random "requirements" into themes; ie, areas of investment that our team concentrates year-over-year. (This is the alignment portion, the Product over all is going --> this way, is that what you want, too?)
4. Here's a wall of words that shows you how much thinking we've put into the product already. These themes break down into many dozens of features each; so please stare at this wall as an example of how much thinking we do (so that you'll pay us a lot of money)
5. And here's the customer tweet, this is what you want too, right? This should reflect/remind the value statement covered in point #1 (I forgot to show you this slide)
6. [and finally a lightweight version of the kanban roadmap, like I drew on the whiteboard, organized by investment theme]

Hope that helps, hope that makes sense.

For inspiration, look no further than the [Jordan Belfort's explanation of how to sell a pen][sell-me-this-pen] "now, the pen is a like a euphism for any product."

# One More Thing - A Note About Prioritization
Were I king of all product managers, I would make the following phrases illegal, “Customer Requirement,” “Must Have,” and P1 through P4. All of these things are sort of a cop-out for Product Management to shovel scope onto the product development team without regard to capacity.

Instead, I wish product management continually provided a list, “Here is a prioritized list of things we need to do together, from the most important to the least important. We need to ship on date X, how much of this can we get done?” The rest is down to negotiation and cutting scope. When we resort to words like, “must have,” we unintentionally move into burn-out culture, where we go from best effort to deliver at all costs. Those costs fall on the product development team. As a result, for fear of losing their jobs, the team will work all-hours, sacrifice time with their families, suffer little sleep, make poor decisions, and ultimately leave the organization as soon as they can find a more humane option.

It is a fundamental requirement of the product management function to provide a list of prioritized needs. Product management isn’t responsible for velocity, though. The only thing we are responsible for is analyzing the **impact** of the schedule, and escalating to leadership. “We are tracking to deliver X, Y, and Z. Without I, J, and K, we won’t be able to make these sales targets. If you want to continue to grow at the desired rate, work with the product development team to figure out how to increase velocity.”

[three-artifacts]:	Three-Fundamental-Artifacts.md "Three Fundamental Artifacts"
[outcome-roadmaps]: https://productschool.com/blog/product-strategy/outcome-based-roadmap
[sell-me-this-pen]:  https://youtu.be/iawLbvCyGKw?si=9sWuQvYdIxexLnxR
