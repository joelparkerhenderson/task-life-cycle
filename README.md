# Task life cycle (TLC)

Task life cycle is a process that creators (such as software developers) use to build projects (such as software applications). This page describes a task life cycle that we like to use that has six stages: start the task, create the branch, develop the work, proof the work, integrate the branch, deliver the result.

Task life cycle aligns with the concepts of [systems development life cycle](https://en.wikipedia.org/wiki/Systems_development_life_cycle) and [software development process](https://wikipedia.org/wiki/Software_development_process). Task life cycle works well with many software development methodologies and frameworks, such as [agile](https://wikipedia.org/wiki/Agile_software_development), [lean](https://wikipedia.org/wiki/Lean_software_development), [kanban](https://wikipedia.org/wiki/Kanban), [scrum](https://wikipedia.org/wiki/Scrum), [spiral](https://wikipedia.org/wiki/Spiral_model), [prototyping](https://wikipedia.org/wiki/Software_prototyping), and more.


## Stage 1: Start the task

Start by choosing your task using your team's preferred way of working.

* Some teams organize tasks, such as with to-do lists, checklists, story cards, use cases, swim lanes, a statement of work (SoW), a work breakdown structure (WBS), etc.

* Some teams categorize tasks, such as with labels, tags, keywords, icons, status indicators, skill sets, flowcharts, value stream maps, hexagonal architecture, etc.

* Some teams prioritize tasks, such as by importance, story points, value estimates, planning poker, board grooming, Gantt charts, critical scheduling, resource leveling, etc.

* Some teams notify stakeholders when work on a task starts, such as by sending a message to stakeholders, or updating the task notes, or moving a story card between swim lanes, etc.


## Stage 2: Create the branch
 
Create a new topic branch by using your team's version control.

Update your project's main branch, such as:

```sh
git checkout main
git pull
```

Checkout a new branch with a suitable topic name, such as to add a feature named "lorem ipsum", and immediately push the branch in order to begin its tracking:

```sh
git checkout -b add-lorem-ipsum
git push
```

Some teams create a teamwide git alias command that creates a topic branch in the exact way the team wants, including doing updates, first tests, notifications, and the like. For examples of topic branch aliases, see https://github.com/gitalias/gitalias


## Stage 3: Develop the work

Work as usual. 

When you're ready, and your code successfully passes all your expected tests, then commit the code, such as:

```sh
git add --all
git commit --message "Add lorem ipsum"
git push
```

Push the topic branch, ideally at least once per day, ideally when all your local tests succeed. This helps you save your work, and also helps your teammates have visibility to your work in progress.

If your team does task tracking updates, then do these, such as adding your notes for work in progress, or updating the task percent complete in the project management software, or checking off the pieces that are done so far in a task checklist, etc.


## Stage 4: Proof the work

When your code is ready for your team to proof a.k.a. review, then start this stage.

Some teams use GitHub features to help with proofing a.k.a. reviewing:

1. Go to GitHub to your topic branch. Create a pull request. 

2. Add reviewers to the pull request. GitHub will notify the reviewers.

3. If you need the review to be urgent, then also message the reviewers directly. 

4. Allow 24 hours for reviewers to read, respond, etc.

5. When all the reviewers have weighed in, and you have handled any show-stoppers, and all the reviewers have given their "thumbs up" icon, then the code is ready to merge into the main branch.

6. If the workflow has automatic review detection, then a successful review will automatically send the code along to the next step. If the workflow doesn't have automatic review detection, then you must notify the teammate who is responsible for the next step; for example, you must message the person who will merge your topic branch into the main branch.


## Stage 5: Integrate the branch

The appropriate person begins to integrate your work into the main branch, and looks for areas such as these:

1. Are there any merge conflicts? If so, resolve these.

2. Are there any dependency updates? If so, do these.

3. Are there any test failures? If so, fix these.

4. Are there any quality issues? If so, address these.

5. Are there any feature flags? If so, set these.

6. Are there any telemetry changes? If so, adjust these.

When all goes well, then your work is merged into main, and ready to deliver.

If the team's workflow uses notifications, then do the notifications.


## Stage 6: Deliver the result

Deliver the result is a.k.a. ship the code to the users.

If the team's workflow has continuous delivery, then the code is automatically delivered. 

Some teams use these steps:

1. Verify the code is working correctly for real users.

2. Verify that system processes are working correctly, such as logging, telemetry reporting, application performance monitoring, synthetic testing, high availabily scaling, disaster recovery backups, etc. 

3. If any issues turn up, then create follow-up tasks to triage them.

4. If your team does retrospectives, then add your notes to the retrospective area.

5. Notify stakeholders that the code is delivered.

6. Mark the task as finished, such as in your team's project management software.

Congratulations, your task life cycle is complete!
