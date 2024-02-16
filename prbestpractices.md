# PR Best Practices

## What is a PR
- What is a pull request?
	- A proposal to merge a set of changes (delta) from one branch into another
	- Collaborators can review and discuss the delta before they integrate the changes into the main codebase
- A process to systematically promote changes to fix defects or introduce new features for end-user consumption
- An forum to allow people to learn openly

## What does a PR contain?
- The code change
	- Well written code that serves as the technical documentation
- Evidence of automated checks passing
- Respective use case based tests integrated
# As a Developer
- Before opening PR
	- Your branch needs to 
		- describe the outcome of the work
		- include the story number
		-  e.g. resolveNextButtonUnclick_B-12345678
	- Scrub your delta for easy to catch errors
		- unnecessary comments
		- dead code
		- out of scope code
	- Update your branch to be in sync with trunk
		- squash/rebase strategy
		- merge strategy
- Don't snowball too many changes into your PR
	- Smaller PR are easier to process for both the dev and reviewer
	- PR should be the outcome of one sprint of work (e.g. less than 10 days of work)
	- If the PR is unavoidably big, schedule a quick 30 min session to go over it and give context to the reviewer
- Tag your PR with any relevant tags
	- e.g. referencing some issue
	- defect? bugfix? cleanup? feature?
- Follow up on reviewer comments
	- Is it a NIT? Your discretion to implement if you have bandwidth
	- Changes requested?
		- Implement or follow up for more clarification
- Don't take comments personal. 
	- PR's are opportunities to discuss and learn.
	- The **artifact** under review is the **code**, not you. 
	- Assume the reviewers best intention to make for a healthy code base and application. If there is a repeated pattern of less-than-friendly interactions, bring it to the attention of the team to dispel any dissonance. 

# As a Reviewer
- Make sure to understand how the feature works prior to doing a review
	- Quick 5 min call for context?
	- Recall some prior design meeting?
- Give the developer the benefit of the doubt when reviewing
	- Understand that we all have differing experiences. Ask for clarification and/or provide a suggestion in your comment
	- Use positive language when clarification is needed in the PR
- When calling out an action item, provide alternatives and/or examples. Don't let the developer assume what you mean.
	- e.g. Lines 13 - 27 can be extracted into a method. I suggest  `doVeryImportantThing`, what do you think?
- Differentiate between **recommendations, **follow ups**, and **NITs**
	- Recommendations are things that are trivial to implement or revise in the PR
	- Follow up indicate you would like to understand the nature of the change while recommending a change.
	- NITs are more quality of life recommendations to the code that are nice to haves but not detrimental if timelines take priority
- One reviewer is required. The more reviewers the better, so long as it doesn't become a blocker to merge the work. One additional day should be the max buffer time if an additional reviewer is required or requested.
- Productive and effective communication is key when requesting changes on the PR.
- Don't drag the review timeline. If you can jump on a call to explain or discuss, go for it.
- Constructive criticism is key, you are a gatekeeper of the codebase and all have a shared responsibility for it's upkeep; however, praise and feedback from a place of empathy goes a long way. 
	- You build trust within the team and upkeep it's collective success.
	- Consider asking opened ended questions to allow for effective communication
	- Be careful not to scope creep if there is a lot of tech debt to refactor. Some is OK but anything that requires additional effort (e.g. two days extra), needs to be it's own unit of work.


