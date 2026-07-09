```text
nexvior@lab ~ $ ./boot
[ok] session start
[ok] load profile: offensive security / builder
[ok] link: https://novau.xyz
```

<br/>

```text
                         ┌─────────────────────────────────────┐
                         │  nexvior@lab          tty1  online  │
                         └─────────────────────────────────────┘

nexvior@lab ~ $ neofetch --offline

       .---.                    nexvior@lab
      /     \                   ─────────────
      \.@-@./                   role: security · builder
       /`\_`\                    site: novau.xyz
      //  _  \\                  shell: bash
     | \     )|_                 editor: vim
    /`\_`>  <_/ \                vcs: git
    \__________/

nexvior@lab ~ $ whoami
security-focused developer. python-first.
i build tools, bots, and small web surfaces — then point them at
systems to see what leaks, opens, or breaks.

not a toolkit collector. i write my own when existing ones lie
or when i need something that fits a specific chain.

nexvior@lab ~ $ ls -1 ~/work/
telegram-bots/
web/
scanners/
pentest-tools/
recon/
malware-notes/

nexvior@lab ~ $ cat ~/work/telegram-bots/about
────────────────────────────────────────
telegram automation
────────────────────────────────────────
  · alert bots for logs, uptime, scan results
  · admin panels for triggering jobs remotely
  · notification pipelines (vps → bot → channel)
  · long-running workers on linux vps
  · stack: python, aiogram / python-telegram-bot
  · deploy: systemd, docker when it makes sense

nexvior@lab ~ $ cat ~/work/web/about
────────────────────────────────────────
web
────────────────────────────────────────
  · landing pages and project fronts
  · dashboards for tool output / status views
  · fast static setups when possible
  · backend hooks when a tool needs a face
  · novau.xyz lives here

nexvior@lab ~ $ cat ~/work/scanners/about
────────────────────────────────────────
scanners
────────────────────────────────────────
  · tcp port scanners (connect / basic syn-style workflows)
  · banner grabbing and service probing
  · host discovery helpers for lab targets
  · async python — built for my own runs, not demo scripts
  · output: plain text / json for piping into other tools

nexvior@lab ~ $ cat ~/work/pentest-tools/about
────────────────────────────────────────
pentest utilities
────────────────────────────────────────
  · small helpers for authorized lab testing
  · payload formatters and request mutators
  · brute-force wrappers with sane rate limits
  · custom checks for misconfigs i keep hitting
  · chained with scanners + recon, not standalone magic

nexvior@lab ~ $ cat ~/work/recon/about
────────────────────────────────────────
recon (partial tooling)
────────────────────────────────────────
  · subdomain enumeration scripts
  · dns / whois / cert fragment collectors
  · target prep before deeper scanning
  · not shipping a full recon suite — focused scripts
    that do one thing and log cleanly

nexvior@lab ~ $ cat ~/work/malware-notes/about
────────────────────────────────────────
malware
────────────────────────────────────────
  · static analysis notes and ioc extraction
  · sandbox observation logs
  · mapping behavior → detection surface
  · private notes mostly; public write-ups when ready

nexvior@lab ~ $ cat ~/stack/runtime
python 3.x · linux · bash · lua (side projects)
learning: c++
infra: linux vps, ssh, nginx, systemd

nexvior@lab ~ $ git -C ~/public status
fatal: '~/public' is empty — first repos not pushed yet

nexvior@lab ~ $ tail -3 ~/log/today
building port scanner refactor
telegram bot: alert routing rewrite
drafting first public release

nexvior@lab ~ $ curl -I https://novau.xyz 2>/dev/null | head -1
HTTP/2 200

nexvior@lab ~ $ █
```

<br/>

<details>
<summary><code>nexvior@lab ~ $ tree ~/work --dirs-only</code></summary>

```text
~/work/
├── telegram-bots/     monitoring · alerts · remote triggers
├── web/               novau.xyz · tool frontends · dashboards
├── scanners/          port scan · banners · service probe
├── pentest-tools/     lab helpers · mutators · misconfig checks
├── recon/             subdomain · dns · whois · target prep
└── malware-notes/     analysis · ioc · behavior mapping
```

</details>

<details>
<summary><code>nexvior@lab ~ $ cat ~/contact</code></summary>

```text
site:   https://novau.xyz
github: https://github.com/Nexvior
status: public repos loading — tools exist locally first
```

</details>
