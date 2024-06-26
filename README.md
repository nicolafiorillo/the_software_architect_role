<div align="center">
 <img src="https://raw.githubusercontent.com/nicolafiorillo/the_software_architect_role/main/images/the_software_architect_role.webp" width="600" alt="The Software Architect Role" style="border-radius: 5%">
 <br>
 <strong>
   Opinionated checklist/notes to cover every single aspect of a (ideal) software project
 </strong>
</div>

# Introduction

Goal is to have a tool to verify every single aspect of a (ideally software) project.
	
This check-list tries to be as holistic as possible, gathering information also for secondary (but not less important) aspects; tuttavia, it is more sbilanciato verso a software architecture role.

## Drivers

* business
	* goal/vision
	* problem to solve
	* stakeholder requirements

* project
	* price/budget
	* available time/deadlines
	* available materials
	* available know-how

* qualities
	* attributes (NFR)
	* -ilities
		* availability
		* security
		* reliability
		* extensibility
		* scalability

# Be prepared

_"No matter what they tell you, it's always a people problem."_ - Gerald Weinberg

## Know your customer(s)

* Company values and mission, culture
	* discover the "why" of the company
	* remember to share with the team

* Know your customer(s)'s domain
	* learn the business domain
	* "_The most valuable asset in the software industry is the synthesis of programming skills and deep context in the business problem domain in one skull. That is architecture._" James Coplien

## Behave yourself

* Remember to listen
* respect the company's past
* communication
	* cross-teams communication
		* hight aligned, loosely coupled
	* absorb (different level of) stakeholder terminology
* be prepared to work with both technical (how) and non-technical stakeholder (what and why)

## Be professional

* Apply the 5 why(s) approach
* focus on results than processes
*	analyzing and taking risks carefully
	* Prove worth with your work
	* Let results be your apology
	* Ask for forgiveness, not permission
	* innovation or old way?
	* smart risks
* principles
	* make it work, make it right, make it fast
	* beware the complete rewrite
	* Architect is a "domain expert who codes"

## Be a leader

* Values first
	* define YOUR values
* show passion
	* celebrate wins
	* show you care solution success
* be honest
	* always
	* if you have nothing good to say, don't talk
	* praise in public, criticize in private
	* admit mistakes asap
* protect you team
* fight but don't take it personally
* team, not family
* be curious
* be humble
* don't blame people
* set context, not control
	* inspiring about goals and strategies
* listen and do not justify
* “_If you want to build a ship, don’t drum up the people to gather wood, divide the work, and give orders. Instead, teach them to yearn for the vast and endless sea._” - The Little Prince

# Business analysys

* Why(s)
	* Why building *this* solution?
	* Why *building* this solution?
		* code is waste
		* code is expensive
			* build, maintenance, etc.
* Other aspects
	* Defining solution lifetime
	* Cost analisys
	* current critical aspects
		* che problemi possono impedire
		* perchè non è stato fatto prima?

# Solution goals

* User goals
	* Defining personas
	* Analyze user goals
	* Analyze user environment
		* Define involved areas
		* Define communication channels
* Product goals
	* Define commitments
	* Define scope(s)
	* Define a clear project vision and mission
	* Define (high level) functional requirements
	* Define (high level) non-functional requirements
	* Requirements not to be considered

# People

* Identify stakeholder
	* Project Manager
		* Decision-capable (and reachable) contact persons (for budget-related decisions)
	* Domain experts
		shall be reachable
	* Analysts
	* Product owner
	* UX Designers
	* Software engineers
		* always ensure backup knowledge
	* Devops
	* QA engineer
	* Customer support (level 1 and 2)
	* Identify cross-cutting requirements experts
		* (database, cloud, etc.)
	* Identify other leaders and followers
	* Defining future maintainers
* talk the people languages
* always consider the people experience

# Analysis

* ADR
* Alternative solutions/competitors investigation
	* Taking inspiration
	* Pro vs. cons analysis
* Defining user stories
	* talk to end-users, not the customer
* Lifecycle model and management
	* Waterfall/iteration approach
	* Issue tracking tool
	* Sharing knowledge, collective code ownership
	* Backlog and issue prioritization (urgency vs. severity/impact)
* Defining solution roadmap
* Defining project phases/milestones
	* Verifiable (and undisputable) outcomes
	* Prefer short phases
* Define a release strategy
* Define SLA
* Functional requirements
	* System administration functionalities
* Non-functional requirements
	* Defining product type (web, mobile, desktop, other)
	* Deployments
		* cloud
		* on-premise
	* Security requirements
	* Privacy requirements (GDPR)
		* data protection
	* Legal requirements/compliance
	* Logging requirements
	* Auditing requirements
	* Monitoring/alert (telemetry) requirements (obserability)
		* defining KPIs and metrics
		* defining plan
	* Accessibility requirements
		* responsiveness
	* Error handling (?)
	* Define API style/semantic guideline
		* share consensus
			* endpoint names
			* input parameters
			* output responses
		* consistency
			* with industrial standards
			* within the product
			* with other API methods
		* automatic verification
			* linter(s)?
		* document with correct/wrong examples
		* OpenAPI, AsyncAPI, etc.
	* Load estimation
		* number of concurrent users (average, peaks)
		* connections
		* API requests per second (average, peaks)
		* data quantity
		* bandwidth (data transfer)
		* cpu usage
	* Scalability strategies
	* Recovery strategies (in case of failures)
	* External dependencies involved
	* Defining failure scenarios
	* Declaring well-known limitations
	* consider bulk operations
		* analyze impact
		* analyze limitations
	* backup strategies
		* does local storage need?
		* duplicating data in cloud?
	* high availability
* Quality attributes
	* quality requirement template
		1. source of stimulus
		2. actual stimulus
		3. artifact affected
		4. environment
		5. effect of the action
		6. response measure
		* example
			* "_when 100 users (source of stimulus) initiate ‘complete payment’ transition (actual stimulus), the payment component (artifact affected), under normal circumstances (environment), will process the requests (effect of the action) with an average latency of three seconds (response measure)_"
	* define the tactic to achieve the quality
		* justify it
		* document it
	* Classification
		* runtime system qualities
			* measured as the system executes
			* Functionality
				* the ability of the system to do the work for which it was intended
			* Performance
				* the response time, utilization, and throughput behavior of the system
			* Security
				* a measure of system’s ability to resist unauthorized attempts at usage or behavior modification, while still providing service to legitimate users
			* Availability
				* Reliability
				* the measure of time that the system is up and running correctly; the length of time between failures and the length of time needed to resume operation after a failure
			* Usability
				* the ease of use and of training the end users of the system
				* learnability, efficiency, affect, helpfulness, control
			* Interoperability
				* the ability of two or more systems to cooperate at runtime
		* non runtime system qualities
			* cannot be measured as the system executes
			* Modifiability
				* the ease with which a software system can accommodate changes to its software
			* Portability
				*	the ability of a system to run under different computing environments
			* Reusability
				* the degree to which existing applications can be reused in new applications
			* Integrability
				* the ability to make the separately developed components of the system work correctly together
			* Testability
				* the ease with which software can be made to demonstrate its faults
		* business qualities
			* influence other quality attributes
			* Cost and Schedule
				* the cost of the system with respect to time to market and expected project lifetime
			* Marketability
				* the use of the system with respect to market competition
			* Appropriateness for Organization
				* availability of the human input, allocation of expertise, and alignment of team and software structure
		* architecture qualities
			* Conceptual Integrity
				* the integrity of the overall structure that is composed from a number of small architectural structures
			* Correctness
				* accountability for satisfying all requirements of the system
		* domain-specific qualities
			* specific to business domains
			* Sensitivity
				* the degree to which a system component can pick up something being measured
			* Calibrability
				* ability of a system to recalibrate itself to some specific working range
	* Define a deploy strategy
		* installation requirements (env target)
		* update/migration requirements (max downtime accepted)
		* define rollback plan
		* deploy documentation (release notes)
	* Define a QA strategy
		* accessibility, load, security, etc...
	* Education/training requirements
	* Tech decisions
		* operating systems, frameworks, architectural patterns, programming languages, data persistences
		* external dependencies communication
	* Risks analisys
		* cost-benefit analysis
	* Use decision records documentation - ADR
		* https://github.com/joelparkerhenderson/architecture-decision-record
	* UX analisys (iteratively with domain experts)
		* goal: became a domain expert involving domain experts
		* defining personas, create workflow/mockups
		* usability test with final users
		* acceptance test (user stories) with final users
	* Brainstorming/discussion/shared solution
		* goal: sharing domain problems, improve common domain/product knowledge
	* UI design
		* brand manual, color guide
	* requirement classification
		* urgent/not urgent
		* severity
		* complexity
		* level of errors tolerated
		* critical/nice to have
	* Strategy for encourage and receive user feedback
		* fast feedback
	* architectures
		* documentation
			* arc42
		* https://elib.dlr.de/133141/1/pragmatic-software-architecture-documentation-notes.pdf
		* https://docs.arc42.org/home/
		* beware the "Stack problem"
		* architecture process ![architecure](/images/architecture_process.png)
	* start with a PoC
	* data	
		* retention period
		* classification

# Development

* Skills required
* Create alias for email-team (inside and outside communication)
* Team and stakeholders shall be informed of:
	* project vision and mission
	* constraints
	* deadlines
	* priorities
* Defining automated test strategies
	* acceptance
	* functional
	* integration
	* unit
	* UI
	* load
	* performances/stress
	* security
	* system
	* concurrent connections
* Devops strategies
	* defining source control management repository strategy (monorepo)
	* build/test/deploy automation tools
	* defining Software Development LifeCycle (SDLC) environments (on-click enviroment deploy, creation/update)
		* local
		* development
			* latest available product image
		* test
		* staging
		* production
* Defining code review/approval strategy
* Define the DoD (Definition of Done)
	* workflows/mockups (UX)
	* product artifacts
	* documentations
		* release notes
		* User guide
		* API service
			* getting started
			* tutorials
			* sample code
			* interactive documentation
				* test in the browser
		* technical documents
		* legal conformity to
		* "Time to First Hello World"
			* to measure good documentation
		* acceptance tests positive results
* Code formatting standards consensus
	* linters
* API guideline consensus
* API specs and definition
	* API signatures must came from use cases
		* 1 API = 1 responsibility
	* document API from the beginning
		* method name
		* description/purpose
		* example request
		* example response
		* possible errors
	* always paginate collections
		* do not nest sub-collections
		* patterns
			* offset pagination
				* GET /items?limit=20&offset=100
			* keyset pagination
				* GET /items?limit=20&created:lte:2019-01-20T00:00:00
			* seek pagination
				* GET /items?limit=20&after_id=40
	* references
		* https://www.moesif.com/blog/technical/api-design/REST-API-Design-Filtering-Sorting-and-Pagination/
		* https://slack.engineering/how-we-design-our-apis-at-slack/
	* provide for filtering
		* patterns
			* LHS brackets
			* RHS colon
			* search query params
	* provide for sorting
		* patterns
			* multi-columns sort
	* return meaningful error messages
		* name_too_long vs. invalid_name
		* add error long description and/or link to get more info
	* consider rate-limit for API calls
	* avoid breaking changes
	* release an internal version of API and get feedback
	* mandatory APIs
		* /api/1/health
			* the usual returns 200 OK if everything is okay health check
			* during height workload, must have max priority over all other APIs
		* /api/1/status
			* information about what's going on in the ingestion and database
* Dev principles
	* KISS principle
	* Occam's razor
	* git usage principles
	* every commit shall contain only one modification (feature, bug fix, task) by transient branch
	* splitting requirements by tasks
	* documentation should reside as near as possible to source code
	* architecture principles
		* loose coupling
		* high cohesion
		* small components
	* SOLID principles
		* Single Responsibility Principle (SRP)
		* Open Closed Principle (OCP)
		* Liskov Substitution Principle (LSP)
		* Dependency Inversion Principle (DIP)
		* Interface Segregation Principle (ISP)
	* Extreme programming
		* collective code ownership
		* TDD
	* API
		* RESTful API design is great for developing API first platforms but not so great for developing GUI applications
		* GraphQL API Design is great for Backends for Frontends (BfFs) but not so great for data services
	* focus on a culture of refactoring
		* embracing change but also embrace stability
	* all devs are architects
	* POCs or temporary projects do not exist
		* always build things as you have to support for long time
	* naming is communication
		* bad names prevent code from clearly communicating its intent
	* Functional programming concepts
		* actions vs. calculations vs. data
		* data immutability
		* high-order functions
		* Onion architecture

	*	Coupling levels

		|          | local method   | local instance   | external instance   | configurable instance   | notification |
		| -------- | -------------- | ---------------- | ------------------- | ----------------------- | ------------ |
		| *How?*   | +              | -                | -                   | -                       | -            |
		| *Where?* | +              | +                | -                   | -                       | -            |
		| *Who?*   | +              | +                | +                   | -                       | -            |
		| *What?*  | +              | +                | +                   | +                       | -            |

		*source: [Understanding coupling - Łukasz Szydło - wroc_love.rb 2018](https://www.youtube.com/watch?v=Jy6eS9QHJOM)*

* Syncronization
	* daily standup/sync meeting
	* periodic demo to customer/management (iteration/sprint-related)
	* retrospective
* prototyping
	* both architectures and major requirements

# Deploy and Release

# Notes

* Technical specs document
	* https://stackoverflow.blog/2020/04/06/a-practical-guide-to-writing-technical-specs/
