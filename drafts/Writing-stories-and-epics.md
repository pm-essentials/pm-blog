# Writing Stories and Epics

Writing good stories is an art. When done effectively, the product development team is both clear on what is to be done, and the team can also see the logic of why we need to do it. We write stories to communicate the what and the why only, the wise product manager stays clear of defining the how.

I learned the basics of story writing from [Principles To Effective Story Writing: The Pivotal Labs Way][pivotal-story-writing]. This entry distills the most relevant lessons from that post, and extends from there.

## Stories and Acceptance Critieria

User stories must have three essential parts: The title, a short description, and acceptance criteria. Each should be short, but descriptive enough to give the product developer a clear idea of how the user will accomplish the task, and why.

### Story Titles

My preference is to use jobs to be done-style story titles. This means that sometimes, my story titles are a little long. I do this for an important reason. When an epic is broken down into stories, you should be able to look at all of the stories in the epic, and read them like a paragraph. Doing this properly opens your work to a much wider audience.

Without any context, compare these two examples:

| Terse style | Jobs to be done |
| --- | --- |
| Parent buys snacks and drinks |  As a parent volunteer, I want to purchase snacks and drinks so that we will have product to sell. |
| Combination lock on the snack shack door | As a school coordinator, I want the parent to be able to unlock the snack shack so they can store the snacks. |
| Snack shack calendar | As a school coordinator, I want to have a calendar of which sports teams will run the snack shack so that I know who to coordinate with. |
| Open the snack shack | As a parent volunteer, I want to open the snack shack on my assigned date so that we can be prepared to start selling snacks. |
| Process transactions | As a parent volunteer, I want to use a cash register so that I can take payments when selling snacks and drinks. |
| Take credit cards | As a parent volunteer, I want access credentials and instructions available so that I can take credit cards as payment. |
| Lock up | As a parent volunteer, I want instructions in the snack shack on lock-up procedures so that I can leave the shack in a clean and secure state. |
| Day-after validation | As a school coordinator, I want to inspect the snack shack the following day so that I can ascertain that the parents have followed the procedures properly. |
| **(release banner)** | **Release:** School stadium has a snack shack run by parent volunteers |

Many PMs write stories in the terse style. They could do worse. Some real examples that don't take the user into account are, "Fix incorrect stride calculation for unbacked symints during autotuning," and, "Verify performance of NHWC convolutions."

**I think that jobs-to-be-done titles do a much better job of comunicating what the outcome of the epic will be.** Putting the extra effort into writing story titles in this manner means that any non-technical person from outside of the product development team can quickly scan the titles, and without clicking in for additional detail, should glean a pretty good idea of how we intend to achieve the desired outcome. Your effort shows respectf for their time. Your boss, their manager, or the VP above them haven't got time to review your stories. If you take the effort to make sure the epic summarizes itself, they'll understand what you're trying to accomplish very quickly, and will appreciate the effort of the team. It's also useful in gathering validation. When we're deep into execution, I've called up my partners in the field, "Hey, can I just show you the order of the steps, so that you can let me know if this still makes sense?" I've changed the ordering of the backlog real-time while reviewing with our stakeholders.

### Acceptance Criteria

**Acceptance criteria** describes the actual steps the user will follow in order to achieve each task. Focusing on writing clear acceptance criteria can save you and the team a lot of time, because it reduces the chances of micromanagement and miscommunication.

While there are many story templates available, I find Gherkin syntax is clear, without overcommunicating and drowning out the intent of the story. I have found that it works in nearly every scenario. Briefly, it follows the form of "given / when / then," with the occasional "and/or" clause thrown in.

Toy example:<br>
**Title:** As a college student, I want to order pizza delivery **so that** I can maximize my study time.<br>
**Given**: I am hungry<br>
**When** I order a pizza using the app<br>
**Then** A pizza is delivered<br>
**And** I'm not hungry anymore.<br>

True story:
> One day, our startup CEO came into the office, very upset. "You people have caused the iOS app screen to be static - you've removed all dynamic content!" I looked at today's release. He was right. I went to the engineer, "What happened here?" and she responded, "I did what the story told me to do. I thought it was odd, but I trust our product manager." I went to our QA person, "How did this get through?" and he responded, "I saw the behavior. I thought it was odd, but I trusted the product manager. The engineers did what the story specified, so I marked it as valid." I went to the product manager, "Why did you tell the team to do this?" and she face-palmed, "I never realized the implications. All the dynamic content is now below the fold! Why didn't anyone tell me?!"

Despite being an excellent product manager, this story wasn't written to focus on the desired outcome. It was specific, "Pin the 6 most popular categories to the top of the users' content stack." Let's try that again using Gherkin syntax:

**Title:** As a user of the app, I want to see the most popular categories at the top, **so that** I always have the chance to discover fresh content<br>
**Given** I've been using the app for some time,<br>
**When** I open the app's home screen,<br>
**Then** I see the most common categories and my personalized categories below.<br>

Taking the time to translate every requirement, every feature, even every bug (if possible) to describe the user's workflow and desired outcome will enable everyone to think critically and ensure that the implementation moves us toward the goal.

Note: Subsequently, I worked at a company where the product managers performed the acceptance criteria themselves, before allowing a story to be added to a release. It was hard work, but the feedback loop to the engineers was very fast, and as a result, the team shipped good product that had a good chance of meeting customers' needs. This activity was called, "acceptance." Acceptance criteria work best when someone actually does the work of accepting every story! When stories have limited scope, it's fast and easy to give timely feedback, "wait this doesn't look right," before the product developers have moved on to new stories, and forgotten the context.

## Epics and Customer Requirements

TODO: Describe the difference between requirements and acceptance critiera.


[pivotal-story-writing]: https://medium.com/product-labs/principles-to-effective-story-writing-the-pivotal-labs-way-76da56031f82
