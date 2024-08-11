---
title: "Agile and Waterfall Methods in Software World"
dateString: Dec 2020
draft: false
tags: ["Agile", "Waterfall", "Scrum", "Kanban"]
weight: 104
cover:
    image: "/blog/agile-and-waterfall/agile-vs-waterfall.jpg"
---

# Introduction
One of the most used concepts in the software world is SDLC (Software Development Life Cycle). So, what is SDLC? Briefly, it is the processes that include the development, design, and testing of a product.

Understanding software development processes is as important for a test engineer as test quality, types, and test tools. In this article, I tried to briefly convey the most common SDLC processes, Agile and Waterfall modeling. :)

# AGILE MODEL
The Agile model is a method that is more flexible than traditional software development models and involves the user in the software development process.

In the Agile model, tasks are progressed by breaking them into small pieces, aiming to bring the product to the user faster. Thanks to this flexibility in the Agile model, user change requests can be quickly responded to.

The team mentality prevails over the individual, emphasizing team spirit. Test and development are not seen as separate parts. The entire team is considered responsible for the quality of the development made.

The most common processes progressing with Agile modeling are Scrum and Kanban.

![](/blog/agile-and-waterfall/scrum-kanban-agile.png)

# Scrum
Scrum is a management model used for the management of complex software projects. Simplicity is the basis, so it is easy to understand. Scrum focuses on the product and continuously improving and developing the product. Teams consist of a small number of people.

The Scrum team consists of a product owner, scrum master, and development team.

*Product Owner:* The person responsible for managing the developed product and maximizing its value. They ensure communication between the team and the management they are connected to but are not the manager of the team.

*Scrum Master:* The leader who serves the team, product owner, and organization. They ensure that the team understands and grasps the agile philosophy, coaches in developing high-value products, and helps remove obstacles in front of the team.

*Development Team:* A team consisting of test engineers, developers, and business analysts responsible for product development. It consists of individuals working with cross-functionality. The quality and responsibility of the product belong to the entire development team.

In Scrum processes, planning is divided into “sprints.” A sprint is a project development cycle with a duration of 1 month or less. During the sprint, the focus is on the quality of the product, not just delivering a working product. Sprint durations are fixed; one sprint starts after another ends.

Specific meetings held within each sprint include:

*Daily Scrum:* Held daily to share the tasks targeted to be completed within the day. By the end of the day, the targeted tasks are expected to be completed, ensuring the product development targeted at the end of the sprint.

*Sprint Review:* At the end of each sprint, a sprint review is held to share which tasks were completed and which tasks faced issues.

*Sprint Planning:* Tasks and their deadlines are pre-determined in a way suitable for the team. Sprint planning includes a product backlog and a sprint backlog. The product backlog contains every requirement for the product, while the sprint backlog includes only the parts to be worked on in that sprint.

*Sprint Retrospective:* After each sprint ends, a retrospective meeting is held. The purpose of the retrospective is to improve the team and teamwork. Various activities are also held to make the work more enjoyable for team members, and they make suggestions to each other.

# Kanban
Kanban is a method that progresses project processes based on visuality. (One of the differences from the Scrum methodology is that tasks are tracked via the Kanban Board.) The task load in Kanban can be adjusted according to the intensity of the team members. There are no defined role distributions in Kanban, but this can be changed. The entire team is responsible for product development. The team consists of self-coordinating individuals.

In the Kanban methodology, the process progresses through a Kanban Board as mentioned above. In office environments, we can see workflows on an actual board, but mostly task tracking is done via online tools like JIRA. Planning is done as follows:

*To Do:* Tasks to be done are listed here. These tasks are broken into small modules, and the time needed for each is pre-determined.

*In Progress:* Tasks that are in the development stage are listed here.

*Test:* Tasks that have completed development and are ready for testing are listed here. After development, the environment should be stabilized for testing. Necessary data for testing should also be prepared. Otherwise, tests will be delayed, and there will be delays in delivering the product to the user.

*Done:* Tasks that have successfully completed development and testing are listed here. After this point, the developed product is ready to be delivered to the user.

# WATERFALL MODEL

The most common traditional software testing process is the waterfall process. In waterfall processes, start and end times are pre-determined and cannot be changed. Development is applied to the entire product, not just a part. The user communicates the desired product development at the beginning of the process and receives the output at the end, not being involved in the process. Waterfall processes proceed based on documentation, which facilitates the subsequent phases of projects. Project management is easier compared to Agile modeling.

Everyone has a specific job description and cannot deviate from it. The role distribution is as follows:

*Project Manager:* Responsible for the project's objectives and how it will be carried out. Actively follows the project's and process's progress, ensuring the flow of information and removing obstacles in front of the team.

*Analyst:* Acts as a bridge between the user and the team developing the product. Analyzes the desired product development, prepares necessary documents, and conveys them to other teams.

*Developer:* Designs and develops the product according to the specified requirements. Considering project constraints and the time needed, the best design is chosen for the product.

*Tester:* After the product development is completed, tests the product and its quality according to the specified requirements. Tests the product from the user's perspective, communicates the errors to the development team, and rechecks the parts marked as resolved. Thus, ensures the product is delivered to the user in a healthy manner.

In the waterfall model, the process progresses as follows:

![](/blog/agile-and-waterfall/waterfall-process.png)

*Planning:* Planning is done first. The project's purpose, output, and the duration of each phase are determined.

*Analysis:* After planning is completed, the project analysis is done. The details of the project are researched, and its needs are determined.

*Design and Development:* The project design is made. The architecture of the product is determined, and the design is chosen in the most suitable way for the project. Then, coding is done according to the chosen design.

*Test:* After development is completed, it is checked whether the product works successfully as expected. This phase may require multiple tests, depending on the development done, such as unit testing, regression testing, and integration testing.

*Deployment and Maintenance:* After successful completion of the tests, the product is put into use. At this step, product checks should continue even after delivery, and problems in the live environment should be quickly detected and resolved.

*SOURCES*

- Scrum Kılavuzu — Ken Schwaber ve Jeff Sutherland
- https://softwarehut.com/blog/it-project-management/waterfall-101
- https://www.atlassian.com/agile/kanban

[Medium](https://mervebozkir.medium.com/yazilimda-agile-ve-waterfall-modelleme-a830ed9cc08b)