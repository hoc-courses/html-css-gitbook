# Branching

Collaboration, multiple developers working within the same repository, requires a workflow, or set of rules for how changes are going to be made. A core concept in the workflow is "branching", or creating separate, protected areas where developers can work on changes without impacting the stable code base that is production ready.

There are many different workflows that are used, but there are a couple that have been adopted by the industry. The two most popular are "Git Flow" and "GitHub Flow". You can easily search for these two terms on Google to explore them in more depth.

Git Flow is a workflow designed for a release process that needs to support more than one simultaneous release in production. For example, most desktop applications have to support multiple versions concurrently. Take Microsoft Word as an example, some customers are using really old versions. Companies need to fix bugs in older version as well as fix bugs and work on new features in the latest version. The "Git Flow" workflow describes a git branching methodology that supports this type of release process.

GitHub flow is a workflow designed for more "continuous deployment", meaning that the development team is continually making changes and moving those changes to the master branch. This is a typical cycle for teams building web applications. It is a much more lightweight workflow. There is a single main branch, and developers create short-lived feature branches where they can work in isolation, and then merge the feature branch back into the main branch when they are finished.

Below is a short overview of the two workflows.

{% embed url="https://youtu.be/w2r0oLFtXAw" caption="" %}

Below is a guide to the GitHub Flow workflow.

{% embed url="https://guides.github.com/introduction/flow/" caption="" %}

{% embed url="https://www.youtube.com/watch?v=MnUd31TvBoU&t=643s" caption="" %}

{% embed url="https://stackoverflow.com/questions/3876977/update-git-branches-from-master" caption="" %}

