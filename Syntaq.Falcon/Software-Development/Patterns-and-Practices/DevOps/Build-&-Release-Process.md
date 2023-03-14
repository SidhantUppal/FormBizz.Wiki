Create Bug Items 
User Stories

Each week we run Theme and User Story Planning session to ensure we have captured all the necessary information about feature/ bug so the developers can build with confidence. 

Each Fortnight we run a Sprint Planning and Prioritisation session so we can clearly communicate what the team will be working on and when a feature/ bug will be released to our clients. 

We don't just assign a priority to the task in this session we also assign tasks owners and apply story points to give us an idea of the number of tasks that we will ultimately be able to build in each sprint. TBC SPRINT ALLOCATION!!!

Each fortnight on a Thursday (last day of a sprint) we will release an Artifact into the Production environment. This Artifact will contain all user stories and bugs which have successfully passed user acceptance testing.

So how do we get a User Story from the backlog into our production environment?


| Stage/ State |Description|Activities |
|--|--|--|
| Backlog |All user stories that have not yet been allocated to a sprint  | User story planning and analysis |
|Analysis (Design)|Review and analyse user stories, wireframes and any additional information provided by the Owner| Review and preparation of a TDD|
| Active | User stories that a Developer is working on | Building or Fixing Code, @mention senior devs if require help|
| Review (Doing) | All user Stories or Bugs that need to be reviewed | Review and Feedback, tag high priority items with BF Review |
| Review (Done) | All User stories or Bugs that have been reviewed |  |
| Deployed Test (Doing) | All User Stories or bugs that have been bundled into a Deployment Artifact | Testing & Verification, xUnit & Cypress, tagging as passed or failed, @menton testing team for user acceptance testing |
| Deployed Test (Done) |All User Stories or Bugs that have been tested (passed or failed)| Agreeing what will be in the staging artifact, moving all failed User Stories or Bugs to Active, add description to release note field, prepare support documentation & verify automated release note |
| Deployed Staging | Artifact that was deployed from Test | Run xUNit and Cypress tests  |
| Deployed Production |Artifact that was deployed from Staging | Run xUNit and Cypress tests |

Sprint Cycle


| Fri| Sat | Sun | Mon | Tues | Wed | Thurs | Fri |Sat  | Sun | Mon | Tues | Wed |Thurs  |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| Stand Up | xx | xx |  Stand Up  |  Stand Up  |  Stand Up  | Stand Up | Stand Up | xx | xx | Stand Up | Stand Up | Stand Up | Stand Up |
| Sprint Start & Retrospective(TBC) |xx  | xx | Theme & User Story Planning |  |Peer Code Review  |  | |||| Sprint Planning & Prioritisation|Peer Code Review|Deployment to Production| 
||||Training|||||||Training||||

Build Pipeline Process
Builds the artifact that will be deployed to an environment

Deployment Pipeline Process
A Multi-step pipeline process with traffic light indicators and Workflow for approval









