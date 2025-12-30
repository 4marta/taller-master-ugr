# Exercise Outcomes Submission Template

**Student/Group Name**: Marta García Valero (Group A)
**Level Completed**: newbie 
**Date**: 30/12/2025

---

## 📋 Exercise Summary

### Exercise: Fundamentals of Git - Commands, Branches & Remote Operations
**Status**: ✅ Completed 

**What I did**:
In this exercise, I successfully cloned the provided GitHub repository using SSH and configured my Git identity. I practiced the basic Git workflow by creating files, checking repository status, staging changes, committing them with meaningful messages, and reviewing commit history. I also created and worked with branches, pushed a feature branch to the remote repository, and pulled updates from the remote newbie branch. Finally, I created an outcome branch and documented the entire process.

**Commands Used**:
```bash
# etc.
git config --global user.name 
git config --global user.email
git clone
git status
git add
git commit
git log
git branch
git checkout
git checkout -b
git push
git pull

```

**Results/Output**:
```
$ git log --oneline
5cce94fb Add personal information

$ git status
On branch newbie
nothing to commit, working tree clean

```

**Screenshots** (if applicable):
- [Screenshot 1: GitHub showing feature/my-info branch pushed to remote]

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. The difference between the working directory, staging area, and repository
2. How to create and switch between branches safely
3. How local and remote repositories interact through push and pull

**Skills I improved**:
- Using Git from the command line with confidence
- Writing meaningful commit messages
- Managing branches and remote synchronization

---

## 🚧 Challenges Faced

### Challenge 1: SSH authentication setup
**Problem**: Initially, GitHub rejected the connection when cloning the repository via SSH because no SSH key was configured.

**Solution**: I generated an SSH key pair, added the public key to my GitHub account, and verified the connection using SSH. After that, cloning and pushing worked correctly.

**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
ssh-keygen -t ed25519
ssh -T git@github.com

```

---

### Challenge 2: Understanding staging vs committing
**Problem**: At first, I expected file changes to be included automatically when committing.

**Solution**: I learned that files must be explicitly added to the staging area using git add before committing. This clarified how Git allows selective commits.

---

## 💭 Personal Reflection

**What surprised me**:
I was surprised by how Git separates changes into different states, which provides much more control than I initially expected.

**What I found most difficult**:
Understanding the staging area and why it exists was initially confusing, but it became clearer with practice.

**What I found most useful**:
Branching was the most useful concept, as it allows working on features independently without affecting the main codebase.

**How I would apply this in real projects**:
In real projects, I would use branches for feature development and bug fixes, push changes regularly to remote repositories for backup and collaboration, and rely on clear commit history to track progress.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [4 ] | |
| Branching & merging | [4 ] | |
| Remote operations | [ 4] | |
| Conflict resolution | [2 ] | |
| History rewriting | [ 1] | |
| Git hooks | [ 1] | |
| Security practices | [3 ] | |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/4marta/taller-master-ugr/tree/newbie`
- Key commits demonstrating your work:
  - 5cce94fb: Add personal information

**Additional files created** (if any):
- File 1: [Description]
- File 2: [Description]

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [ ✅ ] Completed the exercise for your chosen level (including all parts)
- [ ✅ ] Documented all commands used with their outputs
- [ ✅ ] Described challenges and how you resolved them
- [ ✅ ] Provided a thoughtful reflection on your learning
- [ ✅ ] Self-assessed your confidence in each topic
- [ ✅ ] Pushed your outcome branch to the remote repository
- [ ✅ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

[Any additional thoughts, questions, or feedback about the exercises]

---

**Submission Date**: [30/12/2025]  
**Ready for Review**: ✅ Yes 
