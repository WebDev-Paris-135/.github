# Ironhack Web Dev

## Table of contents

1. [Welcome](#welcome-hackers-😎)
2. [Clone a repo](#get-the-code-on-your-computer)

### Welcome hackers 😎!

Starting 13th of May you will have 10 weeks to learn the fundamentals of Web Development.

```mermaid
%%{init: { 'logLevel': 'debug', 'theme': 'base' } }%%
timeline
  title Ironhack curriculum

  section Module-1
  Week-1: HTML
        : CSS
        : JS
  Week-2: JS Classes
        : JS DOM
        : JS Asynchronicity
        : JS Advanced
  Week-3: First Project

  section Module-2
  Week-4: ReactJS
        : props
        : state
        : state lifting
        : routing
        : JS Promises
  Week-5: LifeCycles - Fetching Data
        : Connecting to an external API
        : Creating a Mock API
  Week-5/6: Second Project

  section Module-3
  Week-7: ExpressJS
        : MongoDB
        : Mongoose
        : CRUD
        : Backend Authentication
  Week-8: React Frontend Authentication
        : React Context API
  Week-8/9: Final Project

  section Career services
  Week-10+: Job Hunt
```

### Content

<!--
- [Week-1]()
- [Week-2]()
- [Week-4]()
- [Week-5]()
- [Week-7]()
- [Week-8]()
- [Extra-Content]()
  -->

### Get the code on your computer

> [!NOTE]
> In this organisation you will find one repository for each week.
> You should **_not_ fork** the repositories but **clone them** instead (using `git clone`).

Here is the monday workflow, although it might look complex at a first glance, it's actually pretty straightforward on the student side.

You will just need to `clone` the repository once the teacher added all of the morning lesson to it.

> [!IMPORTANT]
> To clone a repo, use your terminal to go somewhere in your computer where you want to download the repository.
>
> ```bash
> git clone the-repo-url-ending-with .git
> ```

```mermaid
sequenceDiagram
    title Monday workflow
    box rgb(27, 27, 31)
    participant Teachers Local Repo
    actor Teacher
    participant Online Repo
    end
    actor Student

    Note left of Teacher: Lesson time!
    Teacher -->> Teachers Local Repo: Create a local repo
    Note over Teacher: Give a new lesson
    Note over Teachers Local Repo,Teacher: git add, git commit
    Teacher -->> Online Repo: Create the online repository
    Teachers Local Repo --> Online Repo: Link Teachers Local Repo to the Online Repo
    Teachers Local Repo ->> Online Repo: git push
    Note over Online Repo: Contain the new lesson

    rect green
    Online Repo -> Student: git clone
    create participant Local Repo
    end
    Online Repo -> Local Repo: A repo is created locally on your computer
    Note over Student, Local Repo: Now you have access to the repo<br/>from your computer
```

### Rest of the week workflow

> [!IMPORTANT]
> Once you have a locally cloned repository, if you want to get the new content added by the teacher, you don't need to make a new `clone`, you will just need the `pull` the changes

```mermaid
sequenceDiagram
    title Monday workflow
    box rgb(27, 27, 31)
    participant Teachers Local Repo
    actor Teacher
    participant Online Repo
    end
    actor Student
    participant Local Repo

    Note left of Teacher: Lesson time!
    Note over Teacher: Give a new lesson
    Note over Teachers Local Repo,Teacher: git add, git commit
    Teachers Local Repo ->> Online Repo: git push
    Note over Online Repo: Contain all of the lessons
    rect green
    Student -> Local Repo: git pull
    end
    Online Repo -> Local Repo: Local repo pull the changes from the online one
    Note over Student, Local Repo: Now you have access to the<br/>new content from your computer
```

> [!WARNING]
> If you modify something in your local repo, you will not be able to download the new changes. In order to that you will need to use some other commands, namely `git stash` and `git stash pop`

You can open the terminal at the root of the repository and use the next commands.

```bash
git stash
git pull
git stash pop
```
