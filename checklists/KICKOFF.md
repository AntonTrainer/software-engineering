# Project Kickoff Checklist

## Step 0 - Grease everything

## 0.0 - Project Management

**"If you want to build anything bigger than youself, you need solid management principals"**

* [ ] Strategy
  * [ ] Have a project management strategy
  * [ ] Stakeholders are briefed on the strategy and buy in
  * [ ] Team members are briefed on the strategy and buy in
* [ ] Communication
  * [ ] Communication lines are well defined
  * [ ] All project actors know who and how to communicate to
  * [ ] Document of contact info is cultivated and published
* [ ] Resources
  * [ ] Where to find project documentation and resources are advertized
  * [ ] Technical documentation has a place
  * [ ] Non-tehcnical (administrative) documentation has a place
* [ ] Finances
  * [ ] Source of funding is secure
  * [ ] Developers know what the limits of spending are
  * [ ] Developer needs and client expected costs are in line

## Step 1 - What

* [ ] You're sure nobody else has solved this problem, right?

### 0.1 - Problem Framing

* [ ] What type of problem is this?
  * [ ] Traditional software engineering?
  * [ ] Data engineering/transformation?  
  * [ ] Data science with a focus on statistical analysis/analytics?
  * [ ] Machine learning - straightforwards classification/regression?
  * [ ] Hardcore deep learning?
    * [ ] NER?
    * [ ] NRE?
    * [ ] QA?
    * [ ] RL?
    * [ ] etc...
    * [ ] New horizon?

### Data Engineering/Transformation Workflows

* [ ] Have properly mapped schemas of source data?
* [ ] Have properly mapped schemas of transformed data?
* [ ] Have ensured there are viable interfaces and libraries to interact with existing data?
* [ ] Have considered how the volume of data will affect architectural and system needs to process?
  * (If you have 1TB of shit, you cant process that in RAM - be prepared to plan accordingly)
* [ ] Determined interval at which the transformation needs to occur?
  * [ ] Have ensured infrastructure to perform transfer on said interval is feasible?
* [ ] Have ensured there is a viable interface to write and interact with data post transform?
* [ ] Have run a cost analysis of data at its desination?
* [ ] Have enumerated ways in which the data transform could fail?
* [ ] Have addessed each of the ways the data transform could fail?

### Data Science/Analytics Workflows

* [ ] Have you tried more transformations and visualizations than you could possibly hope to report on?
* [ ] Have you found a good framework or platform for displaying your results?
  * [ ] Excel charts?
  * [ ] Plotly charts --> reports?
  * [ ] Dash interactive apps?
* [ ] Have you selected visualizations that will be best recieved by your audience? (Audience > your reception)
* [ ] Have you visualized each result in multiple ways and selected the best?
  * [ ] Have you considered how colors will affect reception?
  * [ ] Have you considered how shape will affect reception?
  * [ ] Have you considered how size will affect reception?
  * [ ] Have you considered how relation to other data will affect reception?

### Machine Learning + Deep Learning Workflows

* [ ] Have listed initial techniques that will be used?
* [ ] Have researched more cutting edge techniques for the frame?
* [ ] Have determined the best layer to insert various models at?
  * (Have vision for a model harness that allows hot swapping different models for testing)
* [ ] Have compute resources required for training phatty models? (or have means of acquiring them?)
* [ ] Have enough time build into the estimate for Engineer to learn intracasies of model being used?

### 1.1 - Requirements

#### Functional Requirements

* [ ] Are system boundary conditions specified?
  * [ ] Inputs?
  * [ ] Outputs?
  * [ ] Results formats?
* [ ] Are software needs specified?
  * [ ] Is there any reason any OS MUST or CANNOT be used?
  * [ ] Rough idea of what open source software will be used?
  * [ ] COTS software has been profiled and is within budget?
* [ ] Are compute needs are properly specified?
  * [ ] Using cloud? On-prem? Personal Compute?
  * [ ] Need GPUs? Special RAM loads?
* [ ] Do you have a detailed enough description to build the system?

#### Quality Attribute Requirements

* [ ] Do you have definitions of:
  * [ ] Success?
  * [ ] Failure?

* [ ] Are tradeoffs between attributes documented?

##### Quality Attributes: Tier One

* [ ] Are **availability** requirements specified?
  * [ ] Uptime needs?
  * [ ] What types of events will lead to the system being down?
  * [ ] Are **error** handling requirements specified?
    * [ ] Consequences of software failure are noted?
    * [ ] Vital system information is documented?
    * [ ] Vital system components are documented?
    * [ ] Error detection strategy is documented?
    * [ ] Error recovery strategy is documented?
* [ ] Are **interoperability** requirements specified?
  * [ ] Are all interfaces to external systems specified?
  * [ ] Are all protocols to communicate with external system specified?
  * [ ] Are all auth considerations for external communication specified?
* [ ] Are **modifiability** requirments specified?
  * [ ] Have things that are NOT likely to change been noted?
  * [ ] Have things that are likely to be changed noted?
  * [ ] Have the likelihoods and conditions of change been noted?
  * [ ] If a change needs to be made, who will need to make it?
  * [ ] What kind of cost will a change incur?
* [ ] Are **performance** requirements specified?
  * [ ] Have all classes of events been catalogued with their expected responses?
    * [ ] Periodic events - predictable and on regular interval?
    * [ ] Stochastic events - can arrive on some probabilistic distribution?
    * [ ] Sporatic events - circumstantial or otherwise non-pattern events?
  * [ ] Are **timing** requiremnts specified?
    * [ ] Response times? (latency)
    * [ ] Jitter - variations in latency?
    * [ ] Processing time?
    * [ ] System trhoughput?
    * [ ] Data transfer rates?
    * [ ] Number of events not processed (due to system being bogged down)?
* [ ] Security
* [ ] Testability
* [ ] Usability

##### Quality Attributes: Tier Two

#### Constraints

#### Recap

* [ ] If every requirement is satisfied, will the product be complete?
* [ ] Aggreed upon reqs are reasonable:
  * [ ] Nothing is impossible to implement
  * [ ] **No reqs that only serve to appease a customer or boss**
* [ ] Each requirement is testable:
  * [ ] Can see how developing tests will be easy?
  * [ ] Requirements are able to be tested by a third party?
* [ ] Have you made the requirements easy to navigate in the future?
  * [ ] Properly indexed?
  * [ ] Stored with proper visibility?
  * [ ] Easy to revisit and mobilize for ass coverage?


### 1.2 - Estimation

(I dont know squat about estimation yet - where does this land priority wise?)

## Step 2 - How

### 2.1 - Architecture

### 2.2 - Design

## Step 3 - Implementation

### 3.1 - Programming

### 3.2 - Software Metrics

(Read the books, bum)

### 3.3 - Quality Assurance

(bundling these in b/c retrofitting is ass and this needs to be baked in from the gitgo)

* [ ] Performed peer reviews of the system
* [ ] Automated tests
* [ ] Performed non automated required tests

### 3.4 - Maintenance

* [ ] Code is written in a readable way
  * [ ] Review programming standards + best practices - focus on decoupling + naming conventionss
* [ ] Documentation is current
* [ ] Documentation is easy to keep current
* [ ] Code base is maintainable by someone that didnt write it?
  * [ ] ! Confirmed by a maintainer that didnt write it !
* [ ] Maintentance strategy has been developed
  * [ ] WHO will be maintaining the project?
  * [ ] How will users be able to contact the maintainers?
  * [ ] Where does maintenance of this project sit in priority compared to other maintained and current projects?
  * [ ] How much time/wk is expected in maintenance for this project?
    * [ ] Have these time estimates been factored into resource allocations for maintainers and their current obligations?