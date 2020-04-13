# Agile Methodologies: Scrum, Kanban

Collaboration: Version Control, Product Management

Process: How we build products

* Build easily maintainable systems
* Deliver fast
* Adapt to changes quickly

Waterfall

* The full project is divided into a sequence of sequential phases
  * Requirements --&gt; Design --&gt; Implementation --&gt; Verification --&gt; Maintenance
* In some cases, this spans multiple years
* Pros
  * Long time spent on Requirements and Design --&gt; Early discovery of problems/bugs
  * Produces a lot of documentation early on
  * Good for some industries
* Cons

  * Not suitable for changing requirements --&gt; decisions are hard to get right early on
  * User only sees the product at the end

![](.gitbook/assets/image%20%284%29.png)

Alternative: Iterative and Incremental Process

* Build the product incrementally in short iterations
* Follow sequence of phases for each iteration
* Pros:
  * Shorter iterations
    * More responsive to change
    * Easier to get feedback from users
* Cons:
  * Unclear long-term vision
    * Architecture issues may arise

![](.gitbook/assets/image%20%283%29.png)

The Agile Manifesto \(2001\)

* A high-level, general description of a certain type of software process

> Individuals and interactions over processes and tools
>
> Working software over comprehensive documentation
>
> Customer collaboration over contract negotiation
>
> Responding to change over following a plan

## Agile Processes

### XP \(eXtreme Programming\)

* In today's standards, XP is considered fairly "heavy"
  * Prescriptive process with many rules
  * Many assumptions that don't apply to many teams
* Very detailed and fairly rigid
  * Open work space and daily "stand-up" meetings are prescribed \(doesn't work for remote teams\)
  * Pair programming and Test Driven Development \(TDD\)

### Scrum

* More of a framework than a specific process
* Fairly prescriptive
* Empirical - Make predictions based on past experience

**Scrum Roles**

* Product Owner
  * Focused on value to users and stakeholders
  * Responsible for the success of the product
* Scrum Master
  * Facilitator, ensures that everything is running smoothly
* Development Team
  * Engineers, designers, creatives, QA, etc.
  * Traditionally, 3-9 people

**Scrum Events**

* Sprint
  * Scrum terminology for iteration
  * Fixed-length: usually, 1-4 weeks
  * Each sprint has the following events:
    1. Planning meeting, at the beginning of the sprint
    2. Daily \(standup\) meetings, during the sprint
       * Very short \(e.g., 15 min\), usually standing up
       * Development team members only, scrum master facilitates
       * 3 questions to ask each development team member: what did I do yesterday? what will I do today? do I see any impediment that prevents me or the development team from meeting the sprint goal?
    3. Review and retrospective meetings, at the end of the sprint
       1. Review meeting
          * Includes all players + stakeholders
          * Demo the work that was done and mention the work that wasn't done; be specific about why it wasn't done
          * Provoke a discussion: updates to the product backlog, ideas for next sprint
       2. Retrospective meeting
          * Usually, immediately after the review meeting
          * All players participate, but no stakeholders
          * The team suggests improvements to its proces based on the previous sprint \(e.g., what worked and what did not, productivity, accuracy of estimations\)

**Scrum Artifacts**

* Product Backlog
  * Ordered list of high-level requirements \(e.g., user stories\)
* Sprint Backlog
  * Backlog items to be completed during a sprint
  * Broken down to more ganular, concrete tasks
    * Short \(&lt; 1 day work\) and clearly defined
    * Estimated size are in hours or points
* Product Increment
  * Completed product backlog items

**Scrum Sprint Planning**

* Product Owner sets goals and priorities
  * Can use User stories to guide the process
* Development Team decides what can get done
  * Use planning poker
  * Has a good sense of the team's ability
  * Considers special circumstances \(e.g., someone is sick or away for a conference\)
* Development Team decides how to do it
  * Prepare the sprint backlog
    * Break product backlog items into concrete tasks and plan how to complete them \(optionally using user stories as a guide\)

Scrum Observations

* Division of Responsibility
  * Product owner on **business value**
  * Development team on **building**
  * Scrum master on **facilitating**
* Collaboration and reality checks
  * Product owner ensures focus on the **important tasks**
  * Development team ensures **realistic expectations**
* Accurate estimations are important
  * Easier when team is predictable and therefore the more the team has worked together, the easier it becomes to make good estimates
* Further into the future --&gt; Use less details
  * Tomorrow's plan is more precise than next week's, which is more precise than next month's
  * Don't plan too far into the future as requirements may change, and understanding of the problem may change, harder to predict

### Kanban

**Similaries with Scrum**

* Self-organizing team
* Break work into tasks
* Developers pull tasks
* Transparent processes
* Frequent delivery

**Differences with Scrum**

* Doesn't have prescribed roles
  * Up to the team to divide responsibilities
* No prescribed meetings
* One artifact \(the Kanban board\) and one simple concept: development process as a **pipeline**
  * Feature requests come in
  * Improved software comes out
  * Items go through the pipeline in steps
  * Goal: Maximize throughput \(limited by bottleneck\)
* The Kanbard Board
  * Columns represent pipeline steps
  * Sticky notes represent items
* Scrum uses fixed-length sprints while Kanban is an ongoing process
  * Board is never reset \(you may do "releases" to clean up the board\)
  * The team decides on the frequency, duration and nature of any meetings

Summary

* Kanban is lighter and less prescriptive
* Kanban fits well with continous development
  * Release when an item makes it to the last column, no need to wait until the end of the sprint
* Kanban gives more freedom and leaves more decisions to the team



