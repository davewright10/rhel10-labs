# Daily Plan — RHEL 10 / RHCSA, 16 weeks, day by day

**Start:** Mon Sep 28, 2026 · **Exam week:** Jan 11–17, 2027 · **Load:** 10–15 hrs/week, 0 hrs on holidays.

Chapter/page/exercise detail lives in [LEARNING.md](LEARNING.md); repo, projects and posts in [LABS.md](LABS.md). This file is the calendar. Work top to bottom; tick the box when the day is done.

## Daily rhythm

| Day | Block | Hrs | Where |
|---|---|---|---|
| Mon | Read chapter A | 2 | Main PC |
| Tue | Chapter A exercises | 1.5 | MacBook / VMs |
| Wed | Read chapter B | 2 | Main PC |
| Thu | Chapter B exercises | 1.5 | MacBook / VMs |
| Fri | Review questions + supplement/drill | 1 | Either |
| Sat | DIY labs (or project build) | 3 | MacBook / VMs |
| Sun | Write-ups → commit → push | 1.5 | MacBook |

Single-chapter weeks (7, 8, 12, 13) and exam weeks (14–16) break the pattern; the tables below say exactly what to do each day.

## Standing rules

- Snapshot before anything destructive. Days that need it say so.
- The Sunday write-up is not optional. If Saturday's labs aren't done, Sunday finishes the labs *and* writes them up — no rollover into Monday.
- Holidays (Nov 26, Dec 24–25, Jan 1) are 0-hour days on purpose. Don't "catch up" on them.
- LinkedIn posts go live the Monday after the project ships (within 48 hrs of the merge).
- If a heavy week (7, 11, 13) runs over, push the exam a week. Never skip DIY labs to stay on schedule.


## Week 1 — Ch 1 (skim) + Ch 2 · Setup

**Sep 28 – Oct 4, 2026** · Milestone: Repo live on GitHub · `server2` built · both VMs snapshotted

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Sep 28 | Setup | Create the repo (commands in LABS.md → Day 1). Rename `rhel10-lab` → `server1` (`hostnamectl set-hostname server1`), reboot, snapshot `server1-wk1`. Skim **Ch 1** pp. 75–163 — install concepts only, you're not reinstalling. | 2 |
| [ ] | Tue Sep 29 | Do | **Lab 1-1** your way: clone `server2` from the `clean-baseline-updated` snapshot in Fusion. Set hostname `server2`, confirm it gets a NAT IP, `ssh` between both nodes from the Mac. Snapshot `server2-wk1`. | 1.5 |
| [ ] | Wed Sep 30 | Read | **Ch 2** Initial Interaction, pp. 164–241. | 2 |
| [ ] | Thu Oct 1 | Do | Ch 2 hands-on: log in on `server1`, walk the directory tree, `man`, `/usr/share/doc`, `whatis/apropos`, shell basics. Type every command in the chapter. | 1.5 |
| [ ] | Fri Oct 2 | Review | Ch 1 + Ch 2 review questions, closed book. Note misses in your notes. | 1 |
| [ ] | Sat Oct 3 | Do | **Labs 2-1 → 2-4**. Then write `docs/lab-topology.md`: both nodes, NAT subnet, planned IPs (`.110` / `.120`), disks, snapshot names. | 3 |
| [ ] | Sun Oct 4 | Write | `chapters/ch02-initial-interaction/README.md` from the template. Commit + push. Week 1 done. | 1.5 |

*Week 1 total: ~12.5 hrs*


## Week 2 — Ch 3 + Ch 4 · File management

**Oct 5 – Oct 11, 2026**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Oct 5 | Read | **Ch 3** Basic File Management, pp. 242–329. | 2 |
| [ ] | Tue Oct 6 | Do | **Ex 3-1 → 3-3**. Extra: tar + gzip + bzip2 round-trips, hard vs soft link behaviour on delete, vim from scratch (no arrows). | 1.5 |
| [ ] | Wed Oct 7 | Read | **Ch 4** Advanced File Management, pp. 330–383. | 2 |
| [ ] | Thu Oct 8 | Do | **Ex 4-1 → 4-6**. Extra: setuid/setgid/sticky on a shared dir, umask math, `find` by size/perm/mtime with `-exec`. | 1.5 |
| [ ] | Fri Oct 9 | Review | Ch 3 + Ch 4 review questions, closed book. | 1 |
| [ ] | Sat Oct 10 | Do | **Labs 3-1 → 3-3** and **Labs 4-1 → 4-4** on `server1`. | 3 |
| [ ] | Sun Oct 11 | Write | `ch03-basic-file-management/README.md` + `ch04-advanced-file-management/README.md`. Commit + push. | 1.5 |

*Week 2 total: ~12.5 hrs*


## Week 3 — Ch 5 + Ch 6 · Users and groups

**Oct 12 – Oct 18, 2026**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Oct 12 | Read | **Ch 5** Basic User Management, pp. 384–442. | 2 |
| [ ] | Tue Oct 13 | Do | **Ex 5-1 → 5-4**. Extra: read `/etc/passwd`, `/etc/shadow`, `/etc/login.defs` end to end; `chage -l` on a test user. | 1.5 |
| [ ] | Wed Oct 14 | Read | **Ch 6** Advanced User Management, pp. 443–493. | 2 |
| [ ] | Thu Oct 15 | Do | **Ex 6-1 → 6-6**. Extra: a sudoers drop-in for an `admins` group, `su -` vs `su`, `chown`/`chgrp -R`. | 1.5 |
| [ ] | Fri Oct 16 | Review | Ch 5 + Ch 6 review questions, closed book. | 1 |
| [ ] | Sat Oct 17 | Do | **Labs 5-1 → 5-4** and **Labs 6-1 → 6-5**. Keep the users/groups you create — they become the Project 1 baseline. | 3 |
| [ ] | Sun Oct 18 | Write | `ch05-basic-user-management/README.md` + `ch06-advanced-user-management/README.md`. Commit + push. | 1.5 |

*Week 3 total: ~12.5 hrs*


## Week 4 — Ch 7 + Ch 8 · Shell, processes, scheduling

**Oct 19 – Oct 25, 2026**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Oct 19 | Read | **Ch 7** Bash Shell, pp. 494–551. | 2 |
| [ ] | Tue Oct 20 | Do | **Ex 7-1**, then **Labs 7-1 → 7-2**. Extra: `grep -E` with anchors/classes, redirection of stdout+stderr separately and together, `history`/tab completion. | 1.5 |
| [ ] | Wed Oct 21 | Read | **Ch 8** Processes & Scheduling, pp. 552–599. | 2 |
| [ ] | Thu Oct 22 | Do | **Ex 8-1 → 8-4**. Extra: find and kill a CPU hog you create (`yes > /dev/null &`), `nice`/`renice`, `at` + `crontab -e`. | 1.5 |
| [ ] | Fri Oct 23 | Supplement | **systemd timers** (on EX200 v10, not in book): write `~/hello.service` + `hello.timer` in `/etc/systemd/system/`, enable the timer, `systemctl list-timers`, `journalctl -u hello`. Then Ch 7 + Ch 8 review questions. | 1.5 |
| [ ] | Sat Oct 24 | Do | **Labs 8-1 → 8-2**. Then redo anything from Fri review you missed. | 2.5 |
| [ ] | Sun Oct 25 | Write | `ch07-bash-shell/README.md` + `ch08-processes-scheduling/README.md` (include the timer pair as the Exam note). Commit + push. | 1.5 |

*Week 4 total: ~12.5 hrs*


## Week 5 — Ch 9 + Ch 10 · Packages · **Project 1**

**Oct 26 – Nov 1, 2026** · Milestone: **Project 1 ships** (two-node lab) · LinkedIn post 1 drafted

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Oct 26 | Read | **Ch 9** Basic Package Management, pp. 600–648. | 2 |
| [ ] | Tue Oct 27 | Do | **Ex 9-1 → 9-2** and **Labs 9-1 → 9-2**. `rpm -qi/-ql/-qf/-V`, install a local `.rpm`, GPG key import. | 1.5 |
| [ ] | Wed Oct 28 | Read | **Ch 10** Advanced Package Management, pp. 649–711. | 2 |
| [ ] | Thu Oct 29 | Do | **Ex 10-1 → 10-3**. Build the ISO-mounted local dnf repo on both nodes — this is a Project 1 deliverable. | 1.5 |
| [ ] | Fri Oct 30 | Do + Supplement | **Labs 10-1 → 10-3**. Then **Flatpak** (on EX200 v10): `dnf install flatpak`, add Flathub remote, install/list/remove one app. Ch 9 + Ch 10 review questions if time. | 2 |
| [ ] | Sat Oct 31 | Project | **Project 1 build**: `/etc/hosts` mapping both nodes, SSH key-only between them + `~/.ssh/config` aliases, local repo + Flatpak remote on both, users/groups baseline (admins w/ sudo, aging policy, no-login service account). Write `scripts/bootstrap-node.sh` that does all of it on a clean clone. | 3 |
| [ ] | Sun Nov 1 | Write | Test `bootstrap-node.sh` on a fresh snapshot of `server2`. `projects/01-two-node-lab/README.md` + final `docs/lab-topology.md` diagram. `ch09` + `ch10` write-ups. Draft **LinkedIn post 1**. Commit + push. | 2.5 |

*Week 5 total: ~14.5 hrs*


## Week 6 — Ch 11 + Ch 12 · Boot, systemd, logging

**Nov 2 – Nov 8, 2026**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Nov 2 | Read | **Post LinkedIn post 1** (15 min). Read **Ch 11** Boot, GRUB2, Kernel, pp. 712–767. **Snapshot both VMs before Thursday.** | 2 |
| [ ] | Tue Nov 3 | Do | **Ex 11-1 → 11-3** on `server1`: boot targets, GRUB default/timeout, kernel install. Snapshot first: `server1-pre-ch11`. | 1.5 |
| [ ] | Wed Nov 4 | Read | **Ch 12** systemd, Logging, Tuning, pp. 768–838. | 2 |
| [ ] | Thu Nov 5 | Do | **Ex 12-1 → 12-2**. `systemctl` unit states/targets, `journalctl` filters (`-u`, `-b`, `-p`, `--since`), rsyslog, `logrotate`, `tuned-adm`. | 1.5 |
| [ ] | Fri Nov 6 | Drill | **Root password reset drill** — interrupt boot, `rd.break`, remount, `passwd`, `touch /.autorelabel`, exit. Time it. Repeat until under 3 minutes, three runs in a row. Then Ch 11 + Ch 12 review questions. | 1.5 |
| [ ] | Sat Nov 7 | Do | **Labs 11-1 → 11-3** and **Labs 12-1 → 12-3**. Revert to snapshot if you brick GRUB — that's what it's for. | 3 |
| [ ] | Sun Nov 8 | Write | `ch11-boot-grub-kernel/README.md` + `ch12-systemd-logging-tuning/README.md`. Commit + push. | 1.5 |

*Week 6 total: ~13 hrs*


## Week 7 — Ch 13 · Storage (heavy week)

**Nov 9 – Nov 15, 2026**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Nov 9 | Setup + Read | In Fusion, **add 3 virtual disks (5 GB each) to `server2`**, boot, confirm with `lsblk`. Snapshot `server2-pre-ch13`. Read **Ch 13** first half, pp. 839–~890 (partitioning, PV/VG/LV basics). | 2 |
| [ ] | Tue Nov 10 | Do | **Ex 13-1 → 13-6**. Use `gdisk`/`parted` for GPT only — skip MBR drills (not on EX200 v10). | 1.5 |
| [ ] | Wed Nov 11 | Read | **Ch 13** second half, pp. ~890–941 (extend/reduce, stratis/VDO if covered). | 2 |
| [ ] | Thu Nov 12 | Do | **Ex 13-7 → 13-13**. VDO: do it once, don't repeat. Focus on extending a VG with a new PV and extending an LV online. | 1.5 |
| [ ] | Fri Nov 13 | Review | Ch 13 review questions. Then from memory on a clean snapshot: GPT partition → PV → VG → LV → extend VG → extend LV. If it isn't clean, do it again. | 1 |
| [ ] | Sat Nov 14 | Do | **Labs 13-1 → 13-7**. Snapshot between labs if you're about to wipe a disk. | 3 |
| [ ] | Sun Nov 15 | Write | `ch13-storage-management/README.md`. Commit + push. If labs ran over, finish them today — don't carry them into week 8. | 1.5 |

*Week 7 total: ~12.5 hrs*


## Week 8 — Ch 14 · File systems + swap · **Project 2**

**Nov 16 – Nov 22, 2026** · Milestone: **Project 2 ships** (storage build-out) · LinkedIn post 2 drafted

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Nov 16 | Read | **Ch 14** File Systems & Swap, pp. 942–1013. | 2 |
| [ ] | Tue Nov 17 | Do | **Ex 14-1 → 14-5**: ext4/xfs/vfat create + mount, `/etc/fstab` by UUID and by label, `mount -a` to prove it, swap partition + swap LV. | 1.5 |
| [ ] | Wed Nov 18 | Do | **Labs 14-1 → 14-3**. | 1.5 |
| [ ] | Thu Nov 19 | Do | **Labs 14-4 → 14-5**. Then `xfs_growfs` and `resize2fs` after an `lvextend` — both, from memory. | 1.5 |
| [ ] | Fri Nov 20 | Review | Ch 14 review questions. Drill: bad `/etc/fstab` entry → boot to emergency → fix → reboot clean. Know this cold. | 1 |
| [ ] | Sat Nov 21 | Project | **Project 2 build** on `server2` from a clean snapshot: GPT + LVM across the 3 disks, one ext4 + one xfs + one vfat, persistent mounts by UUID and label, online extend with fs grow, swap in a partition and in an LV. Capture `lsblk` before/after. Write `scripts/make-lv.sh`. | 3 |
| [ ] | Sun Nov 22 | Write | `projects/02-storage-buildout/README.md` + `ch14-file-systems-swap/README.md`. Draft **LinkedIn post 2** (lsblk before/after). Commit + push. | 2 |

*Week 8 total: ~12.5 hrs*


## Week 9 — Ch 15 + Ch 17 · Networking, DNS, time (Thanksgiving week)

**Nov 23 – Nov 29, 2026**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Nov 23 | Read | **Post LinkedIn post 2** (15 min). Read **Ch 15** Networking, pp. 1014–1078. | 2 |
| [ ] | Tue Nov 24 | Do | **Ex 15-1 → 15-5**: `nmcli` connection profiles, set static IPv4 `.110` on `server1` and `.120` on `server2` on your NAT subnet. Verify from the Mac. | 1.5 |
| [ ] | Wed Nov 25 | Read + Do | **Ch 17** Hostname Resolution & Time, pp. 1124–1173. **Ex 17-1**: chrony client config, `chronyc sources/tracking`, `timedatectl`. | 2 |
| [ ] | Thu Nov 26 | Off | Thanksgiving. Nothing scheduled. | 0 |
| [ ] | Fri Nov 27 | Do + Supplement | **Labs 15-1 → 15-2** and **Labs 17-1 → 17-2**. Then **IPv6** (on EX200 v10): `nmcli con mod <con> ipv6.method manual ipv6.addresses fd00::110/64`, `nmcli con up`, verify with `ip -6 a` and `ping6` between nodes. | 3 |
| [ ] | Sat Nov 28 | Review | Ch 15 + Ch 17 review questions. Drill: from memory, new nmcli profile with static v4 + v6 + DNS + gateway, activated, persistent across reboot. | 1.5 |
| [ ] | Sun Nov 29 | Write | `ch15-networking/README.md` + `ch17-hostname-resolution-time/README.md`. Update `docs/lab-topology.md` with final IPs. Commit + push. | 1.5 |

*Week 9 total: ~11.5 hrs*


## Week 10 — Ch 16 + Ch 18 · NFS, autofs, SSH · **Project 3**

**Nov 30 – Dec 6, 2026** · Milestone: **Project 3 ships** (NFS + autofs + time/DNS) · LinkedIn post 3 drafted

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Nov 30 | Read | **Ch 16** NFS & AutoFS, pp. 1079–1123. | 2 |
| [ ] | Tue Dec 1 | Do | **Ex 16-1 → 16-5**: export from `server1`, mount on `server2` manually and via fstab, then autofs direct + indirect maps. | 1.5 |
| [ ] | Wed Dec 2 | Read + Do | **Ch 18** SSH, pp. 1174–1208. **Ex 18-1 → 18-2**: `sshd_config` hardening (no root login, key-only), `sftp`, `scp`. | 2 |
| [ ] | Thu Dec 3 | Do | **Labs 16-1 → 16-2**. Automounted home directories via indirect map — this is the exam favourite. | 1.5 |
| [ ] | Fri Dec 4 | Do + Review | **Labs 18-1 → 18-2**. Ch 16 + Ch 18 review questions. | 1.5 |
| [ ] | Sat Dec 5 | Project | **Project 3 build**: `server1` exports `/exports/home` + `/exports/shared`; `server2` automounts homes (indirect) and shared (direct); chrony on both; name resolution via `/etc/hosts` + DNS. Capture exports file, autofs maps, `chronyc tracking`. | 3 |
| [ ] | Sun Dec 6 | Write | `projects/03-nfs-autofs-time/README.md` + `ch16` + `ch18` write-ups. Draft **LinkedIn post 3**. Commit + push. | 2 |

*Week 10 total: ~13.5 hrs*


## Week 11 — Ch 19 + Ch 20 · Firewall + SELinux · **Project 4** (heavy week)

**Dec 7 – Dec 13, 2026** · Milestone: **Project 4 ships** (hardened RHEL server) · LinkedIn post 4 drafted

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Dec 7 | Read + Do | **Post LinkedIn post 3** (15 min). Read **Ch 19** Firewall, pp. 1209–1239. **Ex 19-1 → 19-3**: zones, services, ports, `--permanent` + `--reload`, rich rule once. | 2 |
| [ ] | Tue Dec 8 | Do | **Labs 19-1 → 19-2**. Confirm NFS from Project 3 still works through firewalld on `server1`. | 1.5 |
| [ ] | Wed Dec 9 | Read | **Ch 20** SELinux, pp. 1240–1297. **Snapshot both VMs: `pre-ch20`.** | 2 |
| [ ] | Thu Dec 10 | Do | **Ex 20-1 → 20-5**: modes, `ls -Z`/`ps -Z`, `semanage fcontext` + `restorecon`, `semanage port`, `setsebool -P`, `ausearch`/`sealert`. | 1.5 |
| [ ] | Fri Dec 11 | Do + Review | **Labs 20-1 → 20-5**. Ch 19 + Ch 20 review questions. Drill: httpd on a non-standard root + non-standard port, fix both the fcontext and the port label from memory. | 2 |
| [ ] | Sat Dec 12 | Project | **Project 4 build** on `server1`: custom firewalld zone (ssh + NFS only), SELinux enforcing with justified fcontext/port/boolean changes, SSH key-only + no root + `AllowGroups`, password aging + umask + sudo logging. Write `scripts/harden.sh`. | 3 |
| [ ] | Sun Dec 13 | Write | `projects/04-hardened-server/controls.md` — control → command → evidence → CIS RHEL benchmark item (aim for 12 rows). Project README + `ch19` + `ch20` write-ups. Draft **LinkedIn post 4** (the GRC → hands-on story). Commit + push. | 2.5 |

*Week 11 total: ~14.5 hrs*


## Week 12 — Ch 21 · Shell scripting · **Project 5** · Book the exam

**Dec 14 – Dec 20, 2026** · Milestone: **Project 5 ships** (bash toolkit) · LinkedIn post 5 drafted · **EX200 booked**

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Dec 14 | Book + Read | **Book EX200 today** for the week of Jan 11 (Thu–Sat Jan 14–16 preferred). Slots thin out around the holidays — don't wait for week 13. **Post LinkedIn post 4** (15 min). Read **Ch 21** first half, pp. 1298–~1325 (Scripts 01 → 06). | 2 |
| [ ] | Tue Dec 15 | Do | Type and run **Scripts 01 → 06**. No copy-paste from the PDF. | 1.5 |
| [ ] | Wed Dec 16 | Read | **Ch 21** second half, pp. ~1325–1355 (Scripts 07 → 12). | 2 |
| [ ] | Thu Dec 17 | Do + Supplement | **Scripts 07 → 12**. Then write one extra script using `while` + `case` + `$#`/`$@` + exit codes — the exam can ask for any of these. | 1.5 |
| [ ] | Fri Dec 18 | Do | **Labs 21-1 → 21-3** (these become `mklv.sh` and `mknet.sh`). Ch 21 review questions. | 1.5 |
| [ ] | Sat Dec 19 | Project | **Project 5 build**: `mkusers.sh` (CSV → users + groups + aging), `mklv.sh`, `mknet.sh`, `healthcheck.sh` + a systemd timer that runs it and logs to the journal. All with `--help`, all idempotent. | 3 |
| [ ] | Sun Dec 20 | Write | Test every script on a clean `server2` snapshot. `projects/05-bash-toolkit/README.md` with usage + `ch21` write-up. Draft **LinkedIn post 5**. Commit + push. | 2 |

*Week 12 total: ~13.5 hrs*


## Week 13 — Ch 22 · Containers (portfolio only) · **Project 6** · Christmas week

**Dec 21 – Dec 27, 2026** · Milestone: **All 22 chapters done · Project 6 ships** · LinkedIn post 6 drafted

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Dec 21 | Read | **Post LinkedIn post 5** (15 min). Read **Ch 22** Containers, pp. 1356–~1400. Not on EX200 v10 — read for the portfolio, don't memorise. | 2 |
| [ ] | Tue Dec 22 | Do | **Ex 22-1 → 22-6** with `ubi10` images (not `ubi9`): pull, run, port map, env vars, volumes. | 1.5 |
| [ ] | Wed Dec 23 | Read + Do | **Ch 22** pp. ~1400–1449 and **Ex 22-7 → 22-11**: rootless container as a user systemd service, `loginctl enable-linger`. | 2 |
| [ ] | Thu Dec 24 | Off | Christmas Eve. Nothing scheduled. | 0 |
| [ ] | Fri Dec 25 | Off | Christmas. Nothing scheduled. | 0 |
| [ ] | Sat Dec 26 | Do + Project | **Labs 22-1 → 22-7** — the last two labs *are* Project 6. Build: Containerfile (ubi10 + small web app), rootless, port-mapped, persistent volume, user systemd unit with linger, survives `reboot`. | 3 |
| [ ] | Sun Dec 27 | Write | `projects/06-podman-systemd/README.md` (frame it as the bridge to cloud) + `ch22` write-up. Draft **LinkedIn post 6**. Commit + push. **If Project 6 isn't done, ship it in week 14 — it's not exam content and the exams come first.** | 2 |

*Week 13 total: ~10.5 hrs*


## Week 14 — Sample Exams 1 + 2 · New Year week

**Dec 28 – Jan 3, 2027** · Milestone: Sample exams 1 and 2 taken, graded, misses redone

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Dec 28 | Audit | **Post LinkedIn post 6** (15 min). Go through the **EX200 v10 checklist** in LEARNING.md on a clean snapshot, closed book. Tick only what you did from memory. List every miss. | 1.5 |
| [ ] | Tue Dec 29 | Drill | Redo the misses from Monday's audit, from memory, until clean. Priority order: root password reset, LVM extend + fs grow, fstab by UUID, autofs, SELinux contexts, firewalld. | 1.5 |
| [ ] | Wed Dec 30 | Exam | **Sample Exam 1** (pp. 1450–1455), 3 hrs timed, fresh snapshot of both nodes. Skip container tasks; add one Flatpak task and one systemd-timer task. If you have Dec 31 off, take it tomorrow instead and drill tonight. | 3 |
| [ ] | Thu Dec 31 | Grade | Grade Exam 1 against the checklist. Redo every missed task from memory. Note the pattern in your notes. | 1.5 |
| [ ] | Fri Jan 1 | Off | New Year's Day. Nothing scheduled. | 0 |
| [ ] | Sat Jan 2 | Exam | **Sample Exam 2** (pp. 1456–1461), 3 hrs timed, fresh snapshot. Same substitutions. | 3 |
| [ ] | Sun Jan 3 | Grade | Grade Exam 2. Redo misses. Commit an `exams/notes.md` with what you missed on 1 and 2 — the list drives week 15. | 1.5 |

*Week 14 total: ~12 hrs*


## Week 15 — Sample Exams 3 + 4 · Close the gaps

**Jan 4 – Jan 10, 2027** · Milestone: Sample exams 3 and 4 taken; every missed task redone clean

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Jan 4 | Drill | Redo the combined miss list from Exams 1–2 on a clean snapshot, closed book. Time each task. | 1.5 |
| [ ] | Tue Jan 5 | Drill | Speed pass: root password reset, new user + aging + sudo, GPT + LVM + xfs + fstab, nmcli static v4/v6, NFS mount + autofs, firewalld service + SELinux port. Under 10 min each. | 1.5 |
| [ ] | Wed Jan 6 | Exam | **Sample Exam 3** (pp. 1462–1467), 3 hrs timed, fresh snapshot. | 3 |
| [ ] | Thu Jan 7 | Grade | Grade Exam 3. Redo misses. | 1.5 |
| [ ] | Fri Jan 8 | Drill | Redo anything missed twice across Exams 1–3. If nothing, rest. | 1 |
| [ ] | Sat Jan 9 | Exam | **Sample Exam 4** (pp. 1468–1473), 3 hrs timed, fresh snapshot. | 3 |
| [ ] | Sun Jan 10 | Grade | Grade Exam 4. Redo misses. Update `exams/notes.md`. Confirm exam logistics: ID, remote-exam environment check or test-centre directions. | 1.5 |

*Week 15 total: ~13 hrs*


## Week 16 — Exam week

**Jan 11 – Jan 17, 2027** · Milestone: **Sit EX200** · LinkedIn post 7 (pass + retrospective)

| Done | Day | Block | Task | Hrs |
|---|---|---|---|---|
| [ ] | Mon Jan 11 | Mock | **Final full timed mock**: re-run whichever sample exam you scored lowest on, fresh snapshot, 3 hrs. | 3 |
| [ ] | Tue Jan 12 | Drill | Redo Monday's misses. Light pass over the checklist. Nothing new. | 1.5 |
| [ ] | Wed Jan 13 | Rest | Nothing scheduled. If you booked Thursday, run the remote-exam environment check today. | 0 |
| [ ] | Thu Jan 14 | Exam | **EX200** (if booked Thu). Otherwise: 30-min speed pass on the six core tasks, then stop. | — |
| [ ] | Fri Jan 15 | Exam | **EX200** (if booked Fri). Otherwise rest. | — |
| [ ] | Sat Jan 16 | Exam | **EX200** (if booked Sat). Otherwise rest. | — |
| [ ] | Sun Jan 17 | Write | Results usually arrive within 3 business days. When they do: **LinkedIn post 7** (passed + what you'd do differently + repo link), add a retrospective to the repo README, tag the repo `v1.0`. | 1.5 |

*Week 16 total: ~6 hrs*


## Milestone dates

| Date | Milestone |
|---|---|
| Sun Oct 4 | Repo live, `server2` built, Ch 1–2 done |
| Sun Nov 1 | **Project 1** shipped (two-node lab) · Post 1 on Mon Nov 2 |
| Sun Nov 22 | **Project 2** shipped (storage) · Post 2 on Mon Nov 23 |
| Sun Dec 6 | **Project 3** shipped (NFS/autofs/time) · Post 3 on Mon Dec 7 |
| Sun Dec 13 | **Project 4** shipped (hardened server) · Post 4 on Mon Dec 14 |
| Mon Dec 14 | **EX200 booked** |
| Sun Dec 20 | **Project 5** shipped (bash toolkit) · Post 5 on Mon Dec 21 |
| Sun Dec 27 | All 22 chapters done · **Project 6** shipped (podman) · Post 6 on Mon Dec 28 |
| Jan 2–10 | Sample Exams 1–4, timed |
| Jan 14–16 | **Sit EX200** |
| After results | Post 7 — passed + retrospective |
