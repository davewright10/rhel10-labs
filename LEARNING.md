# Learning Plan — Ghori RHCSA RHEL 9 book, 16 weeks

Page numbers = PDF page numbers (not the printed ones).
This is the reference: what each week covers and why. The day-by-day schedule is [DAILY.md](DAILY.md) — work from that.
Each week: read → do every in-chapter exercise → do every DIY lab → answer review questions → write it up ([LABS.md](LABS.md)).

## Phase 1 — Fundamentals (weeks 1–5)

| Wk | Chapters | PDF pages | Exercises / DIY labs | EX200 objectives covered | Supplement (not in book) |
|---|---|---|---|---|---|
| 1 | **Ch 1** Local Installation (skim) · **Ch 2** Initial Interaction | 75–163 (skim), 164–241 | Lab 1-1 (build server2 — clone, don't reinstall) · Labs 2-1 → 2-4 | Shell, man pages, `/usr/share/doc`, directory tree | Rename `rhel10-lab` → `server1`; snapshot both VMs |
| 2 | **Ch 3** Basic File Mgmt · **Ch 4** Advanced File Mgmt | 242–329, 330–383 | Ex 3-1 → 3-3, Labs 3-1 → 3-3 · Ex 4-1 → 4-6, Labs 4-1 → 4-4 | tar/gzip/bzip2, vim, hard/soft links, permissions, setuid/setgid/sticky, umask, `find` | — |
| 3 | **Ch 5** Basic User Mgmt · **Ch 6** Advanced User Mgmt | 384–442, 443–493 | Ex 5-1 → 5-4, Labs 5-1 → 5-4 · Ex 6-1 → 6-6, Labs 6-1 → 6-5 | useradd/usermod/userdel, passwd/shadow, chage, groups, su/sudo, chown | — |
| 4 | **Ch 7** Bash Shell · **Ch 8** Processes & Scheduling | 494–551, 552–599 | Ex 7-1, Labs 7-1 → 7-2 · Ex 8-1 → 8-4, Labs 8-1 → 8-2 | Redirection, grep/regex, variables, ps/top, nice/renice, signals, at, cron | **systemd timers**: write a `.service` + `.timer` pair, `systemctl list-timers` |
| 5 | **Ch 9** Basic Package Mgmt · **Ch 10** Advanced Package Mgmt | 600–648, 649–711 | Ex 9-1 → 9-2, Labs 9-1 → 9-2 · Ex 10-1 → 10-3, Labs 10-1 → 10-3 | rpm, dnf, repos (ISO-mounted local repo), package groups, GPG | **Flatpak**: `dnf install flatpak`, add Flathub remote, install/list/remove an app |

→ End of week 5: **Project 1 ships** (two-node lab build). See LABS.md.

## Phase 2 — System operation (weeks 6–8)

| Wk | Chapters | PDF pages | Exercises / DIY labs | EX200 objectives covered | Supplement |
|---|---|---|---|---|---|
| 6 | **Ch 11** Boot, GRUB2, Kernel · **Ch 12** systemd, Logging, Tuning | 712–767, 768–838 | Ex 11-1 → 11-3, Labs 11-1 → 11-3 · Ex 12-1 → 12-2, Labs 12-1 → 12-3 | Boot targets, **root password reset**, GRUB config, kernel install, systemctl, targets, journald, rsyslog, logrotate, tuned | Drill root-password reset until it's under 3 minutes — it's on every exam |
| 7 | **Ch 13** Storage Mgmt | 839–941 | Ex 13-1 → 13-13, Labs 13-1 → 13-7 | GPT partitions (`gdisk`, `parted`), PV/VG/LV, extend/reduce, add storage non-destructively | Add 3 virtual disks to `server2` in Fusion before starting (Ex 13-1). VDO: do once, low priority |
| 8 | **Ch 14** File Systems & Swap | 942–1013 | Ex 14-1 → 14-5, Labs 14-1 → 14-5 | ext4/xfs/vfat, mount by UUID/label, `/etc/fstab`, resize, swap | — |

→ End of week 8: **Project 2 ships** (storage build-out).

## Phase 3 — Network, services, security (weeks 9–11)

| Wk | Chapters | PDF pages | Exercises / DIY labs | EX200 objectives covered | Supplement |
|---|---|---|---|---|---|
| 9 | **Ch 15** Networking · **Ch 17** Hostname Resolution & Time | 1014–1078, 1124–1173 | Ex 15-1 → 15-5, Labs 15-1 → 15-2 · Ex 17-1, Labs 17-1 → 17-2 | hostname, nmcli, connection profiles, `/etc/hosts`, resolv.conf, dig/host, chrony, timedatectl | **IPv6**: add a static IPv6 address with `nmcli con mod ... ipv6.addresses`, verify with `ip -6 a` |
| 10 | **Ch 16** NFS & AutoFS · **Ch 18** SSH | 1079–1123, 1174–1208 | Ex 16-1 → 16-5, Labs 16-1 → 16-2 · Ex 18-1 → 18-2, Labs 18-1 → 18-2 | NFS export/mount, autofs direct/indirect maps, automount homes, ssh keys, sshd_config, sftp | — |
| 11 | **Ch 19** Firewall · **Ch 20** SELinux | 1209–1239, 1240–1297 | Ex 19-1 → 19-3, Labs 19-1 → 19-2 · Ex 20-1 → 20-5, Labs 20-1 → 20-5 | firewalld zones/services/ports, SELinux modes, file contexts, `restorecon`, port labels, booleans, `ausearch`/`sealert` | — |

→ End of week 10: **Project 3 ships** (NFS + autofs + time/DNS).
→ End of week 11: **Project 4 ships** (hardened RHEL server).

## Phase 4 — Automation, containers, exams (weeks 12–16)

| Wk | Chapters | PDF pages | Exercises / DIY labs | EX200 objectives covered | Supplement |
|---|---|---|---|---|---|
| 12 | **Ch 21** Shell Scripting | 1298–1355 | Scripts 01 → 12, Labs 21-1 → 21-3 | if/elif, for loops, exit codes, positional params, command substitution | Write one extra script that uses a `while` loop and `case` — the exam can ask for either |
| 13 | **Ch 22** Containers *(not on EX200 v10 — portfolio only)* | 1356–1449 | Ex 22-1 → 22-11, Labs 22-1 → 22-7 | — | Use `ubi10` images instead of `ubi9`. Rootless container as a user systemd service is the piece worth keeping |
| 14 | **Sample Exams 1 & 2** | 1450–1461 | Timed, 3 hrs each, on a fresh snapshot | All | Skip container tasks; add one Flatpak task + one systemd-timer task to each |
| 15 | **Sample Exams 3 & 4** | 1462–1473 | Timed, 3 hrs each, on a fresh snapshot | All | Redo every task you missed in weeks 14–15 until clean |
| 16 | **Exam week** | — | One last full timed mock (Mon), rest, sit EX200 | All | Book the exam on **Mon Dec 14** (start of week 12) — holiday slots fill up |

→ End of week 12: **Project 5 ships** (bash automation toolkit).
→ End of week 13: **Project 6 ships** (podman service under systemd).

## EX200 v10 objective checklist

Tick each one only when you can do it from memory, on a clean VM, without the book.

**Essential tools**
- [ ] Shell, redirection, pipes
- [ ] grep + regex
- [ ] ssh to a remote system
- [ ] Manage user sessions (`w`, `who`, `last`, `pkill -u`)
- [ ] tar / gzip / bzip2
- [ ] vim: create + edit files
- [ ] Hard and soft links
- [ ] Standard permissions + umask
- [ ] man, `/usr/share/doc`

**Software**
- [ ] Configure a dnf repository (local ISO + remote)
- [ ] Install / remove RPM packages
- [ ] Configure a Flatpak remote *(supplement, wk 5)*
- [ ] Install / remove a Flatpak *(supplement, wk 5)*

**Shell scripts**
- [ ] if / elif / else
- [ ] for / while loops
- [ ] Positional parameters `$1 $# $@`
- [ ] Command substitution `$( )`

**Operate running systems**
- [ ] Boot, reboot, shutdown
- [ ] Boot into a target (`rescue`, `emergency`, `multi-user`)
- [ ] Interrupt boot → reset root password
- [ ] Find + kill CPU/memory hogs
- [ ] nice / renice
- [ ] tuned profiles
- [ ] journalctl + `/var/log`
- [ ] Start / stop / enable services
- [ ] scp / sftp

**Local storage**
- [ ] GPT partitions with gdisk / parted
- [ ] PV / VG / LV create
- [ ] Extend a VG and LV non-destructively
- [ ] Mount by UUID and by label in `/etc/fstab`

**File systems**
- [ ] vfat / ext4 / xfs create + mount
- [ ] Mount an NFS share
- [ ] autofs (direct + indirect)
- [ ] Extend an LV + grow the filesystem (`xfs_growfs`, `resize2fs`)
- [ ] Diagnose a permission problem

**Deploy / configure / maintain**
- [ ] at, cron, **systemd timers** *(supplement, wk 4)*
- [ ] Services start at boot
- [ ] chrony (time client)
- [ ] Install from repos + local RPM files
- [ ] GRUB: change default timeout / kernel args

**Networking**
- [ ] Static IPv4 with nmcli
- [ ] Static IPv6 with nmcli *(supplement, wk 9)*
- [ ] Hostname + `/etc/hosts` + DNS resolution
- [ ] Services reachable through firewalld

**Users / groups**
- [ ] Create, modify, delete users
- [ ] Password aging (`chage`)
- [ ] Group membership
- [ ] sudo access

**Security**
- [ ] firewalld zones, services, ports
- [ ] umask defaults
- [ ] SSH key-only auth
- [ ] SELinux enforcing / permissive
- [ ] `restorecon` + `semanage fcontext`
- [ ] `semanage port`
- [ ] `setsebool -P`

## If you fall behind

- Weeks 1–5 can compress: they're mostly things you already do. Don't let them eat into week 7.
- Weeks 7, 11, 13 are the heavy ones. If one runs over, push the exams by a week — don't skip DIY labs.
- Never skip: root password reset, LVM extend, fstab by UUID, autofs, SELinux contexts, firewalld. Those are the exam.
