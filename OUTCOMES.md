# Exercise Outcomes Submission

**Student/Group Name**: Marta García  
**Level Completed**: master-of-the-universe  
**Date**: 29/01/2026  

---

## 📋 Exercise Summary

### Exercise: Branch Protection Rules and Security Best Practices
**Status**: ✅ Completed

**What I did**:  
In this exercise I implemented enterprise-level Git security practices on the repository. I configured strict branch protection rules on the `main` branch, enforced pull-request-based workflows, and verified how CODEOWNERS automatically request reviews. I tested protected vs. unprotected workflows by attempting (and failing) a direct push to `main`, then correctly working through feature branches and pull requests.

I also configured GPG commit signing, generated and registered a GPG key with GitHub, and ensured that all final commits were signed and verified. Additionally, I reviewed and improved `.gitignore` to prevent sensitive data from being committed, scanned the repository history for potential secrets, and enabled GitHub security features such as Dependabot and dependency analysis. Finally, I documented all findings and reflections in a professional outcomes branch.

---

**Commands Used**:
```bash
git checkout main
git pull origin main
git push origin main

git checkout master-of-the-universe
git checkout -b feature/protected-workflow
git add .
git commit -m "feat: Add workflow documentation"
git push origin feature/protected-workflow

gpg --full-generate-key
gpg --list-secret-keys --keyid-format=long
gpg --armor --export <KEY_ID>

git config --global user.signingkey <KEY_ID>
git config --global commit.gpgsign true

git log --show-signature
git log --all --graph --decorate --oneline
```

**Results/Output**:
```bash
$ git log --show-signature -3
gpg: Signature made Thu Jan 29 21:04:37 2026 CET
gpg:                using RSA key 0C1DA3A91757980B0A3D5E40C586D87998178907
gpg: Good signature from "Marta García (Clave GPG) <martagarv@gmail.com>" [ultimate]
Merge: 0ef6f3d 09fb63c
Author: Marta García <martagarv@gmail.com>
Date:   Thu Jan 29 21:04:37 2026 +0100
Merge remote-tracking branch 'origin/feature/protected-workflow' into feature/protected-workflow

commit 0ef6f3d81dc2d51833259272b6b62e54d721761e
gpg: Signature made Thu Jan 29 21:03:54 2026 CET
gpg:                using RSA key 0C1DA3A91757980B0A3D5E40C586D87998178907
gpg: Good signature from "Marta García (Clave GPG) <martagarv@gmail.com>" [ultimate]
Author: Marta García <martagarv@gmail.com>
Date:   Thu Jan 29 21:03:54 2026 +0100

    feat: Add fifth signed commit
```

**Screenshots**:

- Screenshot 1: Branch protection rules configured on the `main` branch
  (pull request requirement, mandatory approvals, signed commits, CODEOWNERS, and status checks).
- Screenshot 2: Failed direct push attempt to the `main` branch showing GitHub protection error.
- Screenshot 3: Pull Request creation interface showing required reviews and blocked merge until conditions are met.
- Screenshot 4: Pull Request review request automatically triggered by the CODEOWNERS file.
- Screenshot 6: GitHub security settings enabled (Dependabot alerts, dependency graph, and security analysis).

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. How branch protection rules enforce team workflows and prevent unauthorized changes.
2. How GPG commit signing guarantees authorship and prevents impersonation.
3. How CODEOWNERS integrates with pull requests to enforce review policies.
4. Why removing secrets from Git history is risky and often insufficient without credential rotation.

**Skills I improved**:
- Designing secure Git workflows
- Configuring GPG across the CLI and GitHub
- Reading GitHub security signals (verified commits, required checks)
- Auditing repositories for security risks

---

## 🚧 Challenges Faced

### Challenge 1: [GPG configuration and signed commits]
**Problem**: Initially, commits were not showing as “Verified” on GitHub due to email mismatches and missing Git configuration.

**Solution**: I regenerated and verified my GPG key, ensured the email matched my GitHub account, configured Git to always sign commits, and validated signatures locally using git log --show-signature.

**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
git config --global user.signingkey <KEY_ID>
git config --global commit.gpgsign true
```

---

### Challenge 2: [Branch protection blocking workflows]
**Problem**: Direct pushes to main failed, which initially seemed like an error.

**Solution**: 
I realized this was expected behavior due to branch protection rules. I adapted my workflow to use feature branches and pull requests, validating that the protections were working as intended.

---

## 💭 Personal Reflection

**What surprised me**:
I was surprised by how much security GitHub provides out of the box when branch protection and GPG signing are properly configured. Small configuration changes have a big impact on repository safety.
**What I found most difficult**:
The GPG setup was the most challenging part, especially understanding why commits were not verified at first and how email identity plays a crucial role.
**What I found most useful**:
Learning how branch protection rules and signed commits work together was extremely valuable. This clearly mirrors real enterprise workflows.
**How I would apply this in real projects**:
In real projects, I would always protect the main branch, require pull requests with reviews, and enforce signed commits. I would also integrate secret scanning and automate dependency security updates as part of a DevSecOps approach.
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic               | Confidence (1-5) | Notes                                  |
| ------------------- | ---------------- | -------------------------------------- |
| Basic Git commands  | 5                | Fully comfortable                      |
| Branching & merging | 5                | Confident with protected workflows     |
| Remote operations   | 5                | Strong understanding                   |
| Conflict resolution | 4                | Comfortable, still improving           |
| History rewriting   | 4                | Aware of risks and best practices      |
| Git hooks           | 3                | Basic understanding                    |
| Security practices  | 5                | Strong focus on security-first mindset |


---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/4marta/taller-master-ugr/tree/group-A-outcomes/master-of-the-universe`
- Key commits demonstrating your work:
  - Commit hash: 6f0c18ef
  - Commit hash: 0ef6f3d8
  - Commit hash: 9b83fe7e
  - Commit hash: 94637501
  - Commit hash: b4533f55
  - Commit hash: 925c1718


---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [✅] Completed the exercise for your chosen level (including all parts)
- [✅ ] Documented all commands used with their outputs
- [ ✅] Described challenges and how you resolved them
- [ ✅] Provided a thoughtful reflection on your learning
- [✅ ] Self-assessed your confidence in each topic
- [✅ ] Pushed your outcome branch to the remote repository
- [✅ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

This exercise helped me understand Git not just as a version control system, but as a critical security component in modern software development. The combination of branch protection, commit signing, and security auditing reflects real-world enterprise practices and significantly increased my confidence in professional Git workflows.

---

**Submission Date**: [29/01/2026]  
**Ready for Review**: ✅ Yes
