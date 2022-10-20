## Usecase
My MWP [Obsidian](www.obsidian.md) vault. Its intended use is in a setting of consultancy or similar with simple CRM functionality. The vault is configured to handle several cases relating to many different customers with many stakeholders. Dataview aggregates and show table views of atomic notes from the vault. 
A Kanban board is used to assist in management of the workflow

#### Templates
A number of templates are cretated for each type of note. Each template is configured to create a meaningfull titel and move the note to the correct place in the vault upon creation. The notes are all having some inline dataview tags such as `title::` and  `summary::`
1. case note
	-This note holds information about a specific case/job/assignment. It links to a customer and several person/meeting/lab notes may refference this note by adding an inline dataview tag `refnr::` with reference to the case
2. customer
	- Information about a customer. 
	- Dataview tables for
		- Persons referencing this customer 
		- Cases referencing the customer
		- Every thing else that may reference the customer
3. meeting
	- A simple note placed in `daily` notes. It contains a `type::` inline dataview tag which should include `meeting`.
	- Include an inline tag `refnr::` referencing a case if the meeting pertains to a case
4. person
	- A person contains inline dataview tags: `customer` and `title` and `contact`. Also contain a dataview of all notes where the person is tages as stakeholder
5. lab note
	- A note placed in `daily` notes. It contains a `type::` inline dataview tag which is set to `lab book`. These are the atomic notes you make which pertains to the execution of a certain task
2. daily note
	- A simple note to which captures(`ctrl q`) from QuickAdd plugin are added. Also Dataview of other notes (`YYYY-MM-DD_HHmm.md`) created on the same day
2. Quartely review
	- A template for quartely reviews
2. kanban template
	- Depending on the card Title an appropiate not will be made when creating notes from cards
		- starting with "CASE" - creates a case notes
		- starting with  "LAB" - creates a lab note
		- starting with "MEETING" - creates a meeting note

## Logs
The logs display different views into the vault using dataview queries.

## Plugin dependencies
### community plugins
1. [Templater](https://github.com/SilentVoid13/Templater)
2. [Dataview](https://github.com/blacksmithgu/obsidian-dataview)
3. [Kanban](https://github.com/mgmeyers/obsidian-kanban)
4. [Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks)
5. [QuickAdd](https://github.com/chhoumann/quickadd)
