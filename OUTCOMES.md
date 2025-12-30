# Exercise Outcomes Submission Template

**Student/Group Name**: Marta García Valero (Group A)
**Level Completed**: intermediate
**Date**: 30/12/2025

---

## 📋 Exercise Summary

### Exercise: Merging, Conflict Resolution, and Tagging
**Status**: ✅ Completed 

**What I did**:
In this intermediate exercise, I worked with multiple branches to intentionally create and resolve merge conflicts. Starting from the intermediate branch, I created two feature branches that modified the same file in incompatible ways. I merged these branches back into intermediate, analyzed the conflict markers, and manually resolved the conflict by combining both changes correctly.
After completing the merge, I learned how to create and manage Git tags, including annotated and lightweight tags, and how to push them to a remote repository for versioning purposes.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise

git checkout
git checkout -b
git add
git commit
git merge
git log 
git tag
git show
git push

```

**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:
$ git log --oneline -5
abc1234 feat: Add new feature
def5678 fix: Resolve merge conflict

$ git merge feature/footer
Auto-merging page.html
CONFLICT (add/add): Merge conflict in page.html
Automatic merge failed; fix conflicts and then commit the result.

$ git log --graph --oneline --all
*   987f364 (HEAD -> group-A-outcomes/intermediate, tag: v
1.0-test, tag: v1.0, origin/intermediate) Merge footer wit
h resolved conflicts
|\  
| * daac3ca (feature/footer) Add footer to page
* | 064d53a (feature/header) Add header to page
|/  
* d8074ba (origin/origin/intermediate) Upload intermediate
 README
```

**Screenshots** (if applicable):
- [Screenshot 1: page.html showing conflict markers (<<<<<<<, =======, >>>>>>>)]
- [Screenshot 2: GitHub view showing pushed tag v1.0]

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. How Git detects and reports merge conflicts
2. How to manually resolve conflicts using conflict markers
3. The difference between annotated and lightweight tags

**Skills I improved**:
- Resolving merge conflicts safely
- Reading and understanding branch graphs
- Using tags for versioning and releases

---

## 🚧 Challenges Faced

### Challenge 1: First merge conflict
**Problem**: When merging feature/footer into intermediate, Git could not automatically resolve the conflict because both branches created the same file (page.html) with different content.

**Solution**: I opened the conflicted file, analyzed the conflict markers, and manually merged both sections by keeping the header and footer together in a single file. After verifying the result, I staged the file and completed the merge commit.

**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
git merge feature/footer
git status
git add page.html
git commit -m "Merge footer with resolved conflicts"

```

---

### Challenge 2: Understanding annotated vs lightweight tags
**Problem**: Initially, it was unclear when to use annotated tags versus lightweight tags.

**Solution**: By comparing git show v1.0 and git show v1.0-test, I learned that annotated tags store metadata such as author, date, and message, while lightweight tags are simple pointers to commits.

---

## 💭 Personal Reflection

**What surprised me**:
I was surprised by how explicit Git is during conflict resolution. The conflict markers make it very clear what each branch changed, which helps prevent accidental data loss.

**What I found most difficult**:
The most difficult part was confidently deciding how to resolve the conflict without breaking the file. It required understanding the intent of each branch rather than blindly choosing one side.

**What I found most useful**:
Learning how to resolve merge conflicts was the most valuable skill, as conflicts are unavoidable in collaborative projects.

**How I would apply this in real projects**:
In real-world projects, I would use branches for feature development and rely on merge conflicts as a signal to carefully review overlapping changes. I would use annotated tags for official releases (e.g., v1.0, v2.0) and lightweight tags for temporary testing or internal checkpoints. Tags would help mark stable versions and simplify rollbacks or deployments.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [5 ] | |
| Branching & merging | [ 4] | |
| Remote operations | [ 4] | |
| Conflict resolution | [4 ] | |
| History rewriting | [ 2] | |
| Git hooks | [ 1] | |
| Security practices | [3 ] | |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/4marta/taller-master-ugr/tree/origin/intermediate`
- Key commits demonstrating your work:
  - 064d53a hash: Add header to page
  - daac3ca hash: Add footer to page
  - 987f364 hash: Merge footer with resolved conflicts

**Additional files created** (if any):
- page.html: HTML file with merged header and footer
- OUTCOMES.md: Intermediate level documentation

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [✅ ] Completed the exercise for your chosen level (including all parts)
- [ ✅] Documented all commands used with their outputs
- [ ✅] Described challenges and how you resolved them
- [✅ ] Provided a thoughtful reflection on your learning
- [ ✅] Self-assessed your confidence in each topic
- [✅ ] Pushed your outcome branch to the remote repository
- [ ✅] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

[Any additional thoughts, questions, or feedback about the exercises]

---

**Submission Date**: [30/12/2025]  
**Ready for Review**: ✅ Yes 
