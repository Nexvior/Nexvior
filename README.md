<pre>
<code><span style="color:#8b949e">┌─</span> <span style="color:#3fb950">nexvior@lab</span> <span style="color:#8b949e">── ~/workspace ──────────────────────────────────────┐</span>
<span style="color:#8b949e">│</span>  kernel: linux amd64 · session active · offensive research mode   <span style="color:#8b949e">│</span>
<span style="color:#8b949e">└──────────────────────────────────────────────────────────────────┘</span>

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> whoami
nexvior — security tooling, malware analysis, breaking things on purpose

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> cat .env
WEB=https://novau.xyz
LANG=python, bash, lua
FOCUS=offensive security, recon, pentest automation, malware

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> tree ~/builds -L 2 --dirsfirst
~/builds
├── arsenal/
│   ├── portscan/          # tcp/udp scanners, banner grab, rate control
│   ├── recon/             # osint + infra mapping toolkit
│   ├── pentest/           # vuln checks, fuzz helpers, exploit utilities
│   ├── tg-bots/           # telegram automation & alert pipelines
│   ├── web/               # sites, panels, landing pages
│   └── malware-lab/       # static analysis notes, ioc extraction
├── scripts/
│   └── one-off breakers   # quick probes, dirty hacks, throwaway tests
└── notes/
    └── writeups/          # ctf, samples, postmortems

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> ./arsenal/portscan/ --help
portscan module
  scan_tcp        async connect scan, custom thread pool
  scan_udp        udp probe with configurable payload list
  grab_banner     service fingerprint after open port hit
  export_json     dump results for bots / web panels
  # wip: syn scan when raw socket layer is ready

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> ./arsenal/recon/ --help
recon module
  sub_enum        subdomain discovery, permutations, dns brute
  dns_dump        a/aaaa/mx/txt/cname collection
  whois_track     registrar + nameserver pivot
  http_probe      live host detection, title grab, status map
  path_brute      directory & file discovery
  tech_id           stack detection from headers & html
  ip_range        cidr expand + reverse ptr sweep
  report_merge    combine outputs into single recon report
  # not a single script — pipeline of small tools that chain together

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> ./arsenal/pentest/ --help
pentest module
  svc_audit       weak config checks on common services
  cred_spray      controlled login attempts (lab / authorized only)
  inj_probe       parameter fuzzing for sqli/xss/ssrf patterns
  header_test     security header analysis & bypass attempts
  ssl_check       cert chain, cipher, expiry issues
  pivot_helper    tunnel & proxy glue for internal movement tests
  # built for learning and authorized scopes — not a script kiddie toy

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> ls ~/builds/arsenal/tg-bots/
alertd/           # push scan results & uptime alerts to telegram
logtail-bot/      # tail logs, filter ioc, forward to chat
cmd-bot/          # remote trigger for approved scripts
monitor/          # vps health, disk, failed auth attempts
# bots are the glue — scanners write json, bots notify, web displays

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> ls ~/builds/arsenal/web/
novau.xyz         # personal site — not the tool dump, just the front door
panel/            # internal dashboards for scan & recon output
static-sites/     # fast deploy pages, minimal attack surface
api-bridge/       # hook python tools to web frontend

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> ls ~/builds/arsenal/malware-lab/
static/           # strings, imports, entropy, pe/elf basics
sandbox-notes/    # behavior logs from isolated runs
ioc-out/          # hashes, domains, mutexes — extracted manually
# still growing. malware is read, not worshipped.

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> git status
On branch main
nothing committed yet — public repos shipping soon
local builds only for now

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> curl -sI https://novau.xyz | head -n 1
HTTP/2 200

<span style="color:#3fb950">nexvior@lab</span><span style="color:#8b949e">:~$</span> <span style="color:#8b949e">_</span>
</code></pre>

<br/>

<details>
<summary><code>nexvior@lab:~$ cat ~/builds/arsenal/recon/pipeline.example</code></summary>

<pre>
<code># typical recon chain i actually run — order changes per target

1. sub_enum      → collect hostnames
2. dns_dump      → resolve everything
3. http_probe    → find what's alive
4. tech_id       → map stack
5. path_brute    → hit hidden paths on live hosts
6. portscan      → full port pass on interesting ips
7. report_merge  → one folder, one timeline, one picture

output lands in ./out/YYYYMMDD-target/
feeds tg-bots for alerts, web panel for browsing
</code></pre>

</details>

<details>
<summary><code>nexvior@lab:~$ cat ~/builds/stack</code></summary>

<pre>
<code>python     primary — scanners, bots, glue code
linux      daily driver — vps, hardening, deployment
bash       quick and dirty when speed > elegance
lua        game tooling, scripting experiments
web        html/css/js — sites and internal panels
telegram   bot api — notifications, remote ops
malware    static analysis, ioc, lab notes
cpp        learning next — performance-critical tools later
</code></pre>

</details>

<p align="right">
<sub>novau.xyz · repos going public when ready · profile views below</sub>
</p>

![](https://komarev.com/ghpvc/?username=Nexvior&color=3fb950&style=flat-square)
