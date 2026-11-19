# ECC Research — Lab 00

Owner: randommind13  
Upstream: https://github.com/affaan-m/ECC  
Research branch: `lab/ecc-research`

## Objective

Study ECC as a reference implementation for AI-agent harness design. This is a research workspace, not a production deployment or an endorsement of executing upstream scripts.

## Architecture questions

1. Which components define agent roles and responsibilities?
2. How do skills, rules, commands, hooks, and memory interact?
3. Which actions can invoke shell commands or access files, credentials, or network resources?
4. How are permissions, audit trails, and human approvals implemented?
5. Which concepts are portable to Codex and a hybrid local/cloud LLM environment?

## Lab sequence

- **Lab 00:** Fork, branching, upstream tracking, repository inventory.
- **Lab 01:** Map the harness architecture and execution flow.
- **Lab 02:** Review trust boundaries, tool permissions, hooks, and secret handling.
- **Lab 03:** Run a minimal isolated Codex experiment with explicit approval gates.
- **Lab 04:** Draft a sovereign-hybrid controller/worker architecture.

## Safety baseline

- Do not run installation scripts or hooks on production hosts.
- Do not grant access to company credentials, SSH keys, VPN profiles, or sensitive files.
- Review executable scripts and dependencies before running them.
- Use a disposable VM or isolated non-production environment for experiments.
- Keep upstream changes separate from research notes and local modifications.

## Git workflow (Windows PowerShell)

```powershell
cd "$HOME\GitLearning"
git clone https://github.com/randommind13/ECC.git
cd ECC
git remote add upstream https://github.com/affaan-m/ECC.git
git fetch origin
git switch lab/ecc-research
git remote -v
git status
```

If `upstream` already exists, inspect `git remote -v` rather than adding it twice.

## Definition of done — Lab 00

- [x] Fork exists under randommind13
- [x] Research branch created from main
- [x] Research notes committed on research branch
- [ ] Local clone and remotes verified
- [ ] Architecture inventory completed
- [ ] First security review completed

## Next step

Inventory the repository's documented entry points and configuration directories before installing or executing anything.
