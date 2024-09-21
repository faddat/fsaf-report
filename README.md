# Report to the Swiss Federal Supervisory Authority for Foundations (FSAF)

This is my formal report to the Swiss FSAF concerning the activities of the Interchain Foundation. I believe this information will also benefit teams actively working in the Cosmos ecosystem.

## Advice for Security Reporters in Cosmos

If you have security issues, I strongly recommend that you go directly to [Dev Ojha](https://x.com/valardragon), who is extremely accomplished, ethical, and professional. I cannot recommend contacting the Interchain Foundation due to the risks that:

- You may be harassed.
- Your issue may not be handled appropriately.
- You may incur economic losses due to your report.

For the P2P storms issue in particular, I needed to "disclose by demonstration," working in conjunction with SEAL911, a security reporting body of last resort. I also had to spend my company's funds to make a legal threat to the Interchain Foundation, as they refused to remove my company's name from a provably inaccurate report they published concerning an issue involving over $70,000,000,000 in economic losses.

## About Me

My name is Jacob Anthony Gadikian. I have worked in the Cosmos ecosystem since around 2016 and began full-time work in 2020. I am the CEO and founder of Notional Ventures, which used to run 45 validators in the Cosmos ecosystem.

- I am a direct and general beneficiary of the Interchain Foundation (ICF), as my validator nodes received delegations from them. However, this is not noted in the ICF's public-facing delegation documents, which have commits only from Informal Systems team members:
  - [ICF Delegation Information](https://github.com/interchainio/delegation)
    - Authored by Informal Systems members
  - Notional received a delegation of over 800,000 ATOMs, yielding revenue of around $60,000 a year.
- My company was [elected as the security provider to the Cosmos Hub](https://www.mintscan.io/cosmos/proposals/104).

Over time, I have noticed that issues with reporting are worsening instead of improving.

I am also a security researcher whose work focuses on the interplay between systems in cryptocurrency. My work has been categorically denied by the Interchain Foundation, despite ample proof. I prefer to speak and act directly, so I am making this report public. My report to the FSAF is this repository. I will communicate with the FSAF only over Signal, other than the initial email that I send them with this repository and my Signal contact information.

I fear retaliation, both personal and professional, and I believe that being direct about my complaint and publishing it is the safest path forward for myself and my family.

I am aware that my colleagues also fear retaliation, both personal and professional.

I believe we have good reason to be afraid.

That is why I mentioned that fear in [Cosmos Hub Proposal 787: Formally Request Full Financial Transparency from Interchain Foundation](https://www.mintscan.io/cosmos/proposals/787), which I authored.

In fact, the only reason I am making this report is that I think it is less risky to speak now and speak fully than to simply walk away.

## Incidents

Due to exploits following several of my reports, it is hard for me to say if it is safe from a network security perspective to bring security issues to the Interchain Foundation.

### Amulet and the Fee Market

Please see:

- [Issue on the Cosmos Hub relating to the discrepancy between Amulet standards and the Hub](https://github.com/cosmos/gaia/issues/3319)
  - [Backed up](https://github.com/faddat/fasf-report/issues)

Amulet, the security contractor to the Interchain Foundation, changed their Cosmos Hub reporting policies after the submission of a bug report by Joe Bowman, claiming that the incident was not covered by their reporting policy.

Here is the [Original Report](./feemarket/2024-09-06_report_2652784.pdf).

HackerOne, the reporting service selected by the ICF and Amulet, keeps versioned changes of security reports made via [HackerOne](https://x.com/Hacker0x01).

Here is a link to their versioned reporting policy, where it can be seen that changes were made only after the report was submitted.

It is notable that the security reporting process described on the Cosmos Hub does not match the one described by Amulet:

- [Cosmos Hub Security Docs](https://github.com/cosmos/gaia/blob/main/SECURITY.md)
- [Amulet/HackerOne Security Docs](https://hackerone.com/cosmos?type=team)
  - Go to the section "A Note on Gaia."
  - Here is the [versioned edition](https://hackerone.com/cosmos/policy_versions?change=3737220&type=team) of the reporting standards for the Hub:
    - We can clearly see that the standards were modified after the report was made, and that Amulet attempted to say that the security issue was somehow Skip's fault (Skip is the third party that made the fee market module).
      - At the time of the report, Joe Bowman tested Osmosis to see if the vulnerability was present there, but due to differences in how Osmosis integrated the fee market, it was not.
        - This was a Cosmos Hub issue.

### Threats Made (and Carried Out) Towards Ecosystem Participants by Strangelove Ventures, Funded by the ICF

I observed Jack Zampolin and others associated with Strangelove Ventures—the team currently leading the growth of IBC—describe various means to stop the growth of IBC via Composable specifically. To date, Composable is the only team that has meaningfully grown the IBC network. Composable has built IBC clients for both Cosmos and Polkadot, and designed 08-Wasm, a client interface.

### Proposal 104

[Proposal 104](https://www.mintscan.io/cosmos/proposals/104)

Proposal 104 selected my company, Notional, as the security provider to the Cosmos Hub.

- [Issue #852](https://github.com/cosmos/interchain-security/issues/852)

During the time that Notional was the security provider to the Cosmos Hub, members of the Informal Systems team refused to update the Hub's security contact information.

As such, security issues were not reported to the team working on the Hub's security.

### P2P Storms

I have extensively documented P2P storms in many ways and have included PDF files here that describe them. You can find those in the [p2p-storms](./p2pstorms/) folder.

P2P storms have been used to exploit Cosmos networks financially, including [Luna Classic](https://github.com/notional-labs/notional/blob/master/incidents/WTF%20HAPPENED%20TO%20TERRA.pdf) and [Osmosis](https://www.range.org/blog/levana-security-incident-in-depth-analysis). The links contain information on both exploits. Here is the chronology of exploits:

- **Game of Zones - 2020**

  All Cosmos Hub Game of Zones participants noted this issue, yet it was not investigated.

- **[Sentinel - 2021](./p2pstorms/2023-08-15_report_1395694%20(1).pdf)**

  The report linked here references the precise set of issues present in P2P storms.

- **Luna Classic - May 2022**
- **Stride - August 2023**
- **Osmosis - December 2024**

Only the exploits on Luna and Osmosis were financially consequential, but it should be noted that a P2P storm is essentially the ultimate form of a deniable blockchain attack. Since the transactions used are valid, it is impossible to prove much about these incidents except that they occurred and were financially impactful. Addressing this issue when it was first reported may have prevented or lessened the catastrophic impact of Luna's UST stablecoin failure. Please note that this is not an argument that UST was in any way risk-free or a satisfactory product; much greater care should have been used in its construction.

My reports predate any of the financial exploits and date back to [2021](./p2pstorms/2023-08-15_report_1395694%20(1).pdf).

- [Levana Security Incident Analysis](https://www.range.org/blog/levana-security-incident-in-depth-analysis)

### Banana King: Lack of Field Length Limitations in IBC

#### Reports

- First reported by [@ctrl_felix](https://x.com/@ctrl_felix) to the Interchain Foundation using their formal security reporting process.
  - Ignored
- Reported by [@getcoldy](https://x.com/@getcoldy) to me
- Reported by me to the ICF

...and totally ignored for years until I opened an issue on the topic in public:

- [Lack of Field Length Limitations in IBC](https://github.com/cosmos/ibc-go/issues/4859)

Myself and other reporters avoided making any comments in public, although an analyst later found the issue:

- [Web3 Analyst](https://x.com/web3_analyst/status/1635687287962112000)

Later, I met Jessica in person, and we discussed both Banana King and P2P storms:

- [Interview with Jessica](https://x.com/gadikian/status/1822265519304569057)

The content of IBC messages that exhibited Banana King surpasses any reasonable bounds:

- [Example Banana King Transaction](https://www.mintscan.io/osmosis/tx/D62F0F0354C4DEA0D9DFCA596D9BC3F2943DBA7D24818009DFD725F883088DD0)

Banana King could be used to execute P2P storm-style attacks, and the window to execute Banana King attacks was left open by the Interchain Foundation despite multiple reports, similar to the issues in P2P storms and the submission of an initial patch in 2022.

Banana King did not result in any financial losses, but many Cosmos chains remain vulnerable to it today. Mainly, Banana King allows for attacks on timing.

### IBC Version 3.0.0 and the Cosmos Hub

#### Use of Deprecated Module on Cosmos Hub, Leading to an Exploit That Caused 30,000 ATOM of User Funds to Get Stuck

Contrary to repeated, false claims made by the Interchain Foundation, the Cosmos Hub has been successfully exploited, with financial consequences for users (inability to access funds). This happened two weeks after I reported to both the ICF and Informal Systems that the Cosmos Hub was using an obsolete version of IBC that was tagged as `deprecated` because:

- It was subject to the `Dragonberry` vulnerability.
- It allowed ICA channels to be created only by using the counterparty's module name, enabling an attacker to block the creation of the ICA channel.
