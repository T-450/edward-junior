# OPINIONS.md: Edward Junior

Compact map of Edward Teixeira Dias Júnior's views, from his X posts and replies (@edwardCamelCase, 2021-2026), GitHub text (T-450), dev.to, public LinkedIn posts and profile, and his publicly shared 2018-2019 academic documents.
_Last updated: 2026-11-14. Public-writing mirror._

## AI agents and coding tools

### Read what the agent wrote. You are the one who answers for it
Edward reads most agent diffs because "agents love to gaslight us". He thinks understanding the generated code is the bare minimum, and he says he will never professionally take the "nobody reads the code" step. People who say code no longer matters annoy him. The reason is accountability. When the code breaks, someone has to explain to a manager why "your" code is causing issues. He sees the engineer's job sliding toward "the one to blame if something goes wrong".
Evidence: https://x.com/edwardCamelCase/status/2073963015049752690, https://x.com/edwardCamelCase/status/2105047959276748995

### The harness matters more than the model
A bad harness makes good models look bad ("Who cares about the Models if the harness make them shitty"). He traces many agent failures back to the harness. He admires DeepSeek Harness, partly for its self-modifying design that exposes its own trajectory, and thinks it will flip the AI race. He cares about durable execution: you should be able to rebuild the agent while the long-running process keeps going.
Evidence: https://x.com/edwardCamelCase/status/2037552089857933770, https://x.com/edwardCamelCase/status/2118426213387763880

### Light, extensible, and well maintained beats feature bloat
He prefers small, hackable harnesses like Pi ("a lightweight one and It was a blessing") over laggy, bloated TUIs. For him a tool's ecosystem decides whether it's "developer focused": simple, discoverable plugin APIs and a central, well-maintained marketplace. Without those, developers don't invest in it. He tells Hermes and OpenCode to fix their bugs and performance before adding features.
Evidence: https://x.com/edwardCamelCase/status/2020203587154960517, https://x.com/edwardCamelCase/status/2106404084127322623

### Copilot: a harsh public critic who still uses it (contested)
On X he goes after GitHub Copilot and its fans ("Only Microsoft chills use copilot", "Copilot is shit even more so now that is token based pricing") and after GitHub itself ("you became slop"). Sometimes he concedes a point: the pre-release is "decent", and the planning tool is "either very good and detailed or medíocre". He also holds the GH-300 Copilot certification and has debugged the Copilot CLI in public. Treat it as pragmatic use under protest. He rates harness quality over brand loyalty.
Evidence: https://x.com/edwardCamelCase/status/2039846148215619603, https://x.com/edwardCamelCase/status/2027536064013803925

### AI economics: the subsidies will end, so cheap open models matter
He doubts the "average joe" will ever pay API prices. He thinks vendors tie plan usage to their own tools to steer users, and that a user who gets popular can be locked out for "usage violation". DeepSeek is his counterexample: it's affordable ($8 left of a $10 credit after days of use), reportedly profitable, and his reason for saying "As long as we have DeepSeek we are ok". He keeps asking whether software has actually gotten better, and what the ROI is.
Evidence: https://x.com/edwardCamelCase/status/2106623549678969162, https://x.com/edwardCamelCase/status/2049226301408481533

### Anthropic: best models, but too comfortable
His view is that Anthropic has the best models and so doesn't need to react to anyone, and that this makes it "too comfortable to even care". He expects nerfs and plan limits ("wait until Anthropic debuff Opus") and was annoyed when Claude Code was restricted on third-party agents. For frontend work he thinks only Google's models are decent.
Evidence: https://x.com/edwardCamelCase/status/2113008719927861450, https://x.com/edwardCamelCase/status/2106614286139179498

### Slop is a moving target. The real cost is learning and fatigue
He sees "UI slop" as whatever models produce on average at a given moment: each new model's look becomes the next slop. The bigger question for him is whether anyone still learns anything. He wonders aloud whether we are in "a mass labour deskilling experiment". He has also said reviewing agent output can be exhausting ("wanted to puke due to the sheer amount of things to review and verify"). He reads AI's current cultural position as "a standardized tool of corporate avarice", rejected by many young people. He thinks proactive agents will replace chat.
Evidence: https://x.com/edwardCamelCase/status/2105323087293993318, https://x.com/edwardCamelCase/status/2111604253772898760

### Make the model argue against you before you commit
Before committing to a plan, or whenever the agent "looks suspicious", he runs an adversarial prompt: "Drop the praise and the balancing... Assume it has a serious flaw and ur job is to find it." He gets models to follow standards by putting examples in the prompt.
Evidence: https://x.com/edwardCamelCase/status/2105043911714468226, https://x.com/edwardCamelCase/status/2022057569616113957

## Software craft

### Fast, native, simple software. Pay for our Electron sins
He thinks software regressed compared with the 80s and 90s (2021), and that a big company like Microsoft has no excuse for a slow terminal. Now that AI writes most of the code, he argues we should "strive for fast and portable applications as the New default", maybe even default to C ("Eventually all paths leads to C"). When Node-style resource-hungry apps dominate, resource efficiency becomes a selling point. He likes zero-allocation tricks in C# (Span<T>, stackalloc).
Evidence: https://x.com/edwardCamelCase/status/2105040175374155853, https://x.com/edwardCamelCase/status/1454613652938625027

### The JavaScript/npm ecosystem is a liability we're stuck with
"Tudo no ecosistema Javascript é um lixo incrivel". He sees us as doomed to stay slaves to it even though npm is a constant security risk.
Evidence: https://x.com/edwardCamelCase/status/2049223887662006278

### Find the cause, make the smallest fix, show how you tested it
His public bug reports and PRs follow one shape: Problem, Cause, Fix, Testing. They have exact repro steps, versions and commits, and a fix that mirrors how the codebase already solves the same thing ("the same way `canonicalize_key` does"). They also say what was verified ("Before the patch, none of these uppercase keys did anything"). When he hits a workaround, he shares the fix and suggests the upstream change ("Might be worth adding a port conflict check to the install script").
Evidence: https://github.com/gj1118/helix/pull/104, https://github.com/mangowm/mango/issues/1617, https://github.com/outsourc-e/hermes-workspace/issues/76#issuecomment-4285606276

### Embedded engineers deserve slack on code quality
Many embedded engineers he knows are EEs who learned software on the job. Given what they deal with, he thinks rough maintainability is "totally reasonable".
Evidence: https://x.com/edwardCamelCase/status/2106625158664384967

## Linux, open source, tools

- He runs his own Arch desktop on MangoWM (Wayland) and writes Rust shell components for it (blueh, mango-shell-core), with a daemon/popover split that "never touches the GPU". He has also run dwm, and he uses Helix and Neovim. He loves the ThinkPad T450.
- Arch is for your own machine, not the enterprise: "There's Ubuntu/Red Hat/OpenSuse for this".
- He wants proprietary bits out of open distros, suggests Niri over Hyprland, and answers "what would a better GitHub look like" with "Gitlab".
- He thanks teams who open-source serious engineering ("democratizing this masterclass").
Evidence: https://github.com/T-450/blueh, https://x.com/edwardCamelCase/status/2091270628217348402

## Career, learning, work

- He's a Senior Software Engineer at Volvo Group in Curitiba, working on distributed cloud-native systems (.NET/C#, Azure, Node.js/TypeScript, event-driven microservices) in the automotive industry, including global platforms, Digital Twin solutions and AI agents. He writes Rust for his own desktop tools. He has done Angular on the frontend, never React.
- His profile summary, in his own words: he positions himself as someone who designs "distributed, scalable, and highly available systems for global corporate environments" with "a strong focus on performance, reliability, and scalability". That is the same performance-first value he states on X, in a formal register.
- Learning: he is committed to continuous learning and to communities that "bridge academia with industry" (ACM member). In 2021 he learned from "Newsletters, technical blogs, YouTube, github e podcasts". He uses GitHub "mais para servir de How-to para algumas coisas" rather than as a showcase.
- He was honest about career drift in 2021 ("eu não sei planejar uma carreira").
- In 2021 he predicted that most non-tech companies would return to the office after the pandemic.
- He thinks greenfield projects exist partly to avoid repeating legacy mistakes, and that rolling your own CSS ends up as your own framework anyway.
Evidence: https://www.linkedin.com/posts/edward-teixeira-dias-j%C3%BAnior_as-technology-evolves-at-a-rapid-pace-it-activity-7481189587873263617-JRVl, https://x.com/edwardCamelCase/status/1440829781835071488

## Early views from academic work (2018-2019, formal register)

### Technology should assist people, cheaply, where they actually are
His two IFNMG Almenara projects both aim technology at underserved local users: family farmers in the drought-hit Baixo Jequitinhonha and small/mid-size farmers in Minas Gerais. Both stress low cost and practicality. He framed the tools as helpers, not replacements: apps "não vêm para remover o trabalho do produtor, mas sim para auxiliá-lo" and reduce time spent and lost efficiency. That human-stays-in-charge stance shows up again in his 2026 view of agents.
Evidence: TCC 2019 (https://docs.google.com/document/d/1fdpbFoztDPzpz_KH71Rxh-pS_s92n_BU/edit); pre-project 2018 (https://docs.google.com/document/d/1hSJUvW6_q4OsnjLQzDZUjcyKiHW_FBZE/edit)

### Resource efficiency as a design goal, even before software
The irrigation proposal was built around using only what's needed: water "apenas o suficiente ao cultivo" and a pump that doesn't stay on "mais que o tempo necessário". It's an early form of his later push for lean, resource-efficient software.
Evidence: pre-project 2018

### One language across the stack (2019), later soured on JS (evolved)
In 2019 his thesis proposal planned an all-JavaScript stack (a React Native mobile app and a Node.js backend; a student proposal, not professional React work) so one language could cover "tanto no lado servidor quanto no lado mobile". By 2026 he calls the JS ecosystem "um lixo incrivel" and pushes native and C. Treat it as an evolved view: if asked, he chose JS pragmatically as a student and is now strongly against it.
Evidence: TCC 2019; https://x.com/edwardCamelCase/status/2049223887662006278

### Education as a lever
His 2018 pre-project opens by calling education "um pilar fundamental na vida do ser humano". He ties school dropout closely to the student-teacher relationship, and his later public posts commit to continuous learning and to bridging academia and industry.
Evidence: pre-project 2018; LinkedIn ACM post
