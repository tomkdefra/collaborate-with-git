# Collaborative Story Writing with Git and GitHub

Welcome to our "Exquisite Corpse" style collaborative story writing game using Git! In this activity, each participant will add to a story with a hint left in the commit message, maintaining the element of surprise.

To avoid participants prematurely seeing the story file and ruining their surprise, we will use the echo command in a Git Bash terminal to add our lines to the story. The -e flag enables interpretation of backslash escapes, so at the end of our addition we can add a \n newline character to keep our story formatting nice and tidy. 

## Workflow

### First Participant

1. **Write the first part of the story in `story.txt`:**

    ```bash
    echo -e "Our story is going to be great and stuff is going to happen. Suddenly, something happened... \n" > story.txt
    ```

2. **Commit and push:**

    ```bash
    git status
    git add story.txt
    git status
    git commit -m "Suddenly, something happened..."
    git status
    git push origin main
    ```

### Second Participant

1. **Pull changes:**

    ```bash
    git pull origin main
    ```

2. **See commit message hint:**
    - _Suddenly, something happened..._

3. **Write the next part of the story in `story.txt`:**

    ```bash
    echo -e "Blah blah blah and etc...\n" >> story.txt
    ```

4. **Commit and push:**

    ```bash
    git status
    git add story.txt
    git status
    git commit -m "and etc..."
    git status
    git push origin main
    ```

### Third Participant

1. **Pull changes:**

    ```bash
    git pull origin main
    ```

2. **See commit message hint:**
    - _and etc..._

3. **Write the next part of the story in `story.txt`:**

    ```bash
    echo -e "Blah blah blah and etc...\n" >> story.txt
    ```

4. **Commit and push:**

    ```bash
    git status
    git add story.txt
    git status
    git commit -m "and etc..."
    git status
    git push origin main
    ```

### Final Merge

1. **Once every participant has had a couple of turns, we can pull all changes and read the story:**

    ```bash
    git pull origin main
    code story.txt
    ```
