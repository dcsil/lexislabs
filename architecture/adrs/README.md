## ADRs

For any architectural/engineering decisions we make, we will create an ADR (Architectural Design Record) to keep track of what decision we made and why. This allows us to refer back to decisions in the future and see if the reasons we made a choice still holds true. This also allows for others to more easily understand the code.

**ADRs will follow this process:**
* They will live in the repo, under a directory `architecture/adrs`
* They will be written in Markdown
* They will follow the naming convention `adr_NNN_<decision-title>.md`, where the decision title in the filename must use snake case
  * NNN must be the number associated with the Jira ticket in the DCSIL Coursework project
  * NNN can be discontinuous between chronologically consecutive ADRs, but the numbering must be unique and monotonic (i.e. an older ADR must have a lower number than a more recent ADR)

**The common sections that each ADR should have are:**
* Title, Context, Decision, Status, Consequences
* Use this article as a reference: https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions
