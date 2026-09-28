# Linux Plan — RHEL 10 / RHCSA (16 weeks)

**Goal:** Pass RHCSA (EX200, RHEL 10) and ship a public RHEL lab portfolio on GitHub + LinkedIn.
**Book:** *RHCSA Red Hat Enterprise Linux 9* — Asghar Ghori (22 chapters, 4 sample exams).
**Time:** 10–15 hrs/week. Start: week of Sep 28, 2026. Target exam: week 16 (mid/late Jan 2027).

## Three files

| File | What it is |
|---|---|
| [DAILY.md](DAILY.md) | **The calendar.** Every day from Sep 28 to exam week, with a checkbox. Start here |
| [LEARNING.md](LEARNING.md) | Chapter/page/exercise reference by week, EX200 v10 objective checklist |
| [LABS.md](LABS.md) | The GitHub repo: chapter labs, 6 portfolio projects, LinkedIn post schedule |

## Daily rhythm (~12 hrs/week)

| Day | Block | Hrs |
|---|---|---|
| Mon | Read chapter A | 2 |
| Tue | Chapter A exercises | 1.5 |
| Wed | Read chapter B | 2 |
| Thu | Chapter B exercises | 1.5 |
| Fri | Review questions + supplement/drill | 1 |
| Sat | DIY labs or project build | 3 |
| Sun | Write-ups → commit → push | 1.5 |

Holidays (Nov 26, Dec 24–25, Jan 1) are 0-hour days. Exceptions per week are in DAILY.md.

## Machines

| Machine | Use |
|---|---|
| Main PC | Read the book / this plan only |
| MacBook (VMware Fusion) | VMs, terminal, notes, Git repo |
| `server1` (RHEL 10, existing VM) | Primary lab box. Rename from `rhel10-lab` in week 1 |
| `server2` (RHEL 10, clone) | Second node — needed from Ch 15 (NFS, SSH, networking). Build in week 1 |

## Book → RHEL 10 differences (know these up front)

| Book says | You do |
|---|---|
| VirtualBox, x86, RHEL 9.1 | VMware Fusion, aarch64, RHEL 10.0. Skip Ch 1 install steps; clone `server2` from your `clean-baseline-updated` snapshot |
| `192.168.0.110` / `.120` | Use your Fusion NAT subnet; keep the last octet (`.110` server1, `.120` server2) |
| Containers (Ch 22) | **Not on EX200 v10.** Keep it — it's a portfolio project, not exam prep |
| No Flatpak | **On EX200 v10.** Supplement in week 5 |
| at + cron only | **systemd timers are on EX200 v10.** Supplement in week 4 |
| VDO (Ch 13/14) | Not on EX200 v10. Do it once, don't drill it |
| MBR + GPT partitions | EX200 v10 lists GPT only. Drill `gdisk`/`parted` GPT |
| IPv4 focus | EX200 v10 requires IPv4 **and IPv6** config. Supplement in week 9 |

## Rules

1. Every DIY lab gets a write-up in the repo the same week. No backlog.
2. Snapshot before every destructive chapter (11, 13, 14, 20).
3. One LinkedIn post per portfolio project — 6 total, plus a pass announcement.
4. Don't present unfinished projects as finished.

## Milestones

| Week | Date | Milestone |
|---|---|---|
| 1 | Sun Oct 4 | Repo live on GitHub, `server2` built |
| 5 | Sun Nov 1 | Project 1 shipped + LinkedIn post 1 |
| 8 | Sun Nov 22 | Storage project shipped + post 2 |
| 11 | Sun Dec 13 | Hardened server shipped + post 4 |
| 12 | Mon Dec 14 | **EX200 booked** |
| 13 | Sun Dec 27 | All 22 chapters done, 6 projects shipped |
| 14–15 | Jan 2–10 | 4 sample exams, timed |
| 16 | Jan 14–16 | Sit EX200 |
