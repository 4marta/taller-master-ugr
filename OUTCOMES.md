# Exercise Outcomes Submission Template

**Student/Group Name**: Marta García Valero (Group A) 
**Level Completed**: master
**Date**: 30/12/2025

---

## 📋 Exercise Summary

### Exercise: Rewriting History (Rebase and Amend Commits)
**Status**: ✅ Completed 

**What I did**:
In this master-level exercise, I practiced advanced Git history manipulation techniques. I amended commits to correct mistakes without creating unnecessary commit noise, used interactive rebase to clean up and reorganize commit history, and rebased a feature branch onto an updated master branch to achieve a linear and readable history. I also analyzed the risks of rewriting history and learned best practices for safely using these techniques in professional environments.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
git command1
git command2
# etc.
git add
git commit
git commit --amend
git log --oneline
git rebase -i
git checkout
git checkout -b
git rebase
git log --graph --oneline --all

```

**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:

$ git log --oneline -3
d270768 (HEAD -> group-A-outcomes/master, master) Update on master branch
e942aa9 Fix typo
f9825b9 Add feature B
c15e88c Add feature A
d89cf83 Add complete configuration file
cf6c875c Ammend

```

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. How git commit --amend rewrites the last commit safely
2. How interactive rebase cleans and restructures commit history
3. The risks of rewriting shared/public history and how to mitigate them

**Skills I improved**:
- Creating clean, professional commit histories
- Using rebase instead of merge where appropriate
- Recovering from and reasoning about history changes

---

## 🚧 Challenges Faced

### Challenge 1: Understanding commit SHA changes
**Problem**: After amending and rebasing commits, I noticed that commit hashes changed, which was initially confusing.

**Solution**: I learned that commits are immutable objects and any change to their content or metadata results in new SHAs. Comparing logs before and after clarified how history rewriting works internally.

**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
git log --oneline
git show <commit-sha>

```

---

### Challenge 2: Interactive rebase editor workflow
**Problem**: Remembering when to use pick, fixup, squash, or reword during interactive rebase required practice.

**Solution**: By experimenting with git rebase -i on small commit sets, I learned how each option affects the final history and how to recover using git rebase --abort when needed.

---

## 💭 Personal Reflection

**What surprised me**:
I was surprised by how powerful and potentially dangerous Git history rewriting can be. A single rebase can dramatically improve clarity—or cause serious issues if misused.
**What I found most difficult**:
The most challenging aspect was understanding when not to use rebase. Knowing the technical steps is easier than deciding if rewriting history is appropriate in a collaborative context.
**What I found most useful**:
Interactive rebase was the most valuable skill. Being able to squash fixes, reorder commits, and improve commit messages makes project history far more readable and professional.
**How I would apply this in real projects**:
In real-world projects, I would use commit --amend and interactive rebase only on private or feature branches before merging. I would rebase feature branches onto an updated main branch to maintain a linear history, but never rewrite shared history. For teams, I would document rebases clearly and use git push --force-with-lease instead of --force to avoid overwriting teammates’ work.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [ 5] | |
| Branching & merging | [ 5] | |
| Remote operations | [4 ] | |
| Conflict resolution | [ 4] | |
| History rewriting | [ 4] | |
| Git hooks | [ 2] | |
| Security practices | [ 4] | |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/4marta/taller-master-ugr/tree/master`
- Key commits demonstrating your work:
  -  cf6c875c: Ammend

**Additional files created** (if any):
- featureA.txt, featureB.txt: Files used for interactive rebase

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [✅ ] Completed the exercise for your chosen level (including all parts)
- [ ✅] Documented all commands used with their outputs
- [✅ ] Described challenges and how you resolved them
- [✅ ] Provided a thoughtful reflection on your learning
- [ ✅] Self-assessed your confidence in each topic
- [✅ ] Pushed your outcome branch to the remote repository
- [✅ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

[Any additional thoughts, questions, or feedback about the exercises]

---

**Submission Date**: 30/12/2025 
**Ready for Review**: ✅ Yes 
