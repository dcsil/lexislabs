# Team Principles

*Effective Date:* These principles will take effect after the submission of Assignment 1. Until then, the team will operate under the existing ad-hoc guidelines described [here](https://docs.google.com/document/d/1uAUhIbC1iHslmCeaTo5hZo7XY8BmFoIIOOKRFhju4Rk/edit?usp=sharing).

## Communication

- We treat each other’s ideas with respect but also a critical lens.
- Every member of the team commits to openly communicating about any blockers or foreseeable problems that will impact the team’s work or collaboration.
  - **Overcommunicate!** If a member suspects that something has any potential to cause a problem in the future, they will try to bring it up before the problem becomes a reality.
- Our main communication platform is Slack. We will regularly (i.e. at least once every day) monitor Slack.
  - If team members are unable to fulfill this, they must notify the entire team in advance.
- In case of team conflicts, we should try to confront each other openly. However, we acknowledge that some members prefer mediation; in that case, Tony or Leonid will act as a neutral mediator.
- We should provide feedback to each other at the moment it comes to mind. We accept that feedback may not always be constructively framed, and we will not take negative or critical feedback personally.

## Meetings

- We prefer in-person meetings when our schedules allow, but online meetings are still acceptable.
- We will have our weekly standup during/after the Wednesday lecture, where we discuss progress/achievements over the previous week.
- In addition to the Wednesday standup, we will have at least one more meeting each week, focusing on making progress and getting work done.
- Additional team-wide meetings will be held as necessary (e.g. for key milestones).
  - The day after a deadline for a key milestone (e.g. A1), we will organize another meeting to delegate tasks and plan what needs to be done for the subsequent assignment.
- At the end of each meeting, including the Wednesday lecture meeting, we must set a time for the next meeting. For additional meetings we hold, the “next” meeting we decide can be the Wednesday lecture meeting.
- All meetings will have an agenda outlining what should be discussed during the meeting, along with meeting minutes and next steps that members are expected to complete by the next meeting (or other deadlines as applicable)
  - Next steps will be communicated via the main communication channel (specified above) after each meeting in a shared channel.
- Team members are expected to communicate at least 6 hours in advance if they are unable to attend a meeting.
  - They are still expected to provide any relevant updates via an alternate format, such as a message on the main communication channel.
- Subteam meetings (e.g. meetings specifically involving those working on back-end development) may also be held as needed.
- Ad-hoc meetings are encouraged, especially when it would be faster than messaging. However, we acknowledge that some members may require some time to prepare their thoughts.

## Work

- If a team member feels that the amount of work assigned to them exceeds what they can handle, they should be responsible for informing others with a reasonable buffer time. Their work can then be reassigned to other members who are able to help.
- Team members are expected to complete tasks at least one day prior to key deadlines to ensure adequate time for submission and presentation preparation.
  - We will check in with each other two days prior to said key deadlines.
- All changes to the default branch of any repo should be reviewed by at least one other team member (will be enforced via GitHub rules).
- A developer must run and pass existing tests before requesting a review from other team members (except if the tests are faulty or for other extenuating reasons).
- When making important business or design decisions, we will voice all of our concerns and sincerely consider others’ concerns before finalizing a decision.
- If we need help or guidance from another team member, we will make a reasonable effort to solve the problem independently first.
- Brainstorming sessions are best held in-person as a group.
- Our deep work environment should be quiet and calm.
- When we copy code or information from external sources, we must understand what we are copying and attribute it in accordance with university-level guidelines.

### Project Management

- We will use Jira as the source of truth for all of our tasks.
- We will create tickets (Jira issues) for any TODO items determined during our team meetings. Each ticket must contain a concrete description of a well-scoped task and be assigned an owner who is responsible for its execution. The owner holds the final call on decisions pertaining to the ticket and exclusive write access to relevant assets (code or documents).
- When creating a ticket, we will fill in the "Due date" and "Story point estimate" fields. Team members who are knowledgeable about the task will collectively assign a numerical value ("points") to a ticket based on the expected complexity or workload. For our team, we will use the convention of 1 point ≈ 0.5 hours of work. Only positive numbers in the Fibonacci sequence are valid story point values.
  - An exception to the rule of assigning story point estimates is **spike tickets**. These tickets will be used to describe exploratory work and will not be pointed (assigned points). The end result of a spike ticket should be tickets describing implementation work or further spikes.
  - If a ticket is assigned a story point estimate of 13 or more, we must create child tickets to clarify steps.
- We will visualize our progress with a kanban board. To ensure the effectiveness of the board, team members must update their tickets asynchronously based on their progress.
- Every code change (pull request) must belong to a ticket. Changes to the team repo will be filed in the DCSIL Coursework project.
  - The pull request title must begin with the ticket ID, formatted as `<BOARD ID>-<TICKET NUM>: <PR TITLE>`. For example, `DCS-10: Remove all code`.
  - The corresponding branches must contain the ticket ID. For example, `DCS-10-remove-all-code`.

## Task Division and Member Responsibilities

- Wilson Sy - Project Management, Backend Engineer (support)
- Tony Hu - Testing, CI
- Krishna Cheemalapati - Front-end / UX dev
- Parth Vats - Backend Engineer (APIs, overall architecture)
- Leonid Nediak - Backend Engineer (data and AI)
