# Foundational Works

These are the seminal papers and dissertations that established the field of intrinsic evolvable hardware. Adrian Thompson's work in the 1990s demonstrated that evolutionary algorithms could design electronic circuits directly in silicon, producing compact, unconventional designs that exploited the analog physics of FPGAs.

:material-home-circle:{ .middle } = EHW Research Group paper
{: .ehw-legend }

## Hardware Evolution (Dissertation, 1998)

**Adrian Thompson** <br>
**Publication:** Springer, Distinguished Dissertations Series, 1998 <br>

<div class="grid cards" markdown>

- [:fontawesome-brands-amazon:{ .lg .middle }
__Amazon__
](https://www.amazon.com/Hardware-Evolution-Reconfigurable-Distinguished-Dissertations/dp/3540762531)

- [:simple-springer:{ .lg .middle }
__Springer__
](https://link.springer.com/book/10.1007/978-1-4471-3414-5)

</div>

???+ abstract
    This distinguished dissertation presents the foundational work on hardware evolution — the automatic design of electronic circuits in reconfigurable hardware by artificial evolution. Thompson demonstrates that evolutionary algorithms can be applied directly to the configuration bitstreams of FPGAs, allowing evolution to exploit the full analog physics of the silicon substrate rather than being constrained to conventional digital design abstractions.

??? quote "Suggested Citation"
    Thompson, A. (1998). *Hardware Evolution: Automatic Design of Electronic Circuits in Reconfigurable Hardware by Artificial Evolution*. Distinguished Dissertations. Springer-Verlag London.

### Authors
- Adrian Thompson

---

## An Evolved Circuit, Intrinsic in Silicon, Entwined with Physics (1996)

**Adrian Thompson** <br>
**Publication:** ICES 1996 — Lecture Notes in Computer Science, Vol. 1259, pp. 390–405, Springer, 1997 <br>

<div class="grid cards" markdown>

- [:simple-springer:{ .lg .middle }
__Springer__
](https://link.springer.com/chapter/10.1007/3-540-63173-9_61)

- [:fontawesome-brands-researchgate:{ .lg .middle }
__ResearchGate__
](https://www.researchgate.net/publication/2737441_An_Evolved_Circuit_Intrinsic_in_Silicon_Entwined_With_Physics)

</div>

???+ abstract
    This landmark paper describes the first application of intrinsic hardware evolution to an FPGA. Thompson used a genetic algorithm to evolve the configuration bitstream of a Xilinx XC6216 FPGA to perform a tone discrimination task — distinguishing between 1 kHz and 10 kHz input signals. The resulting circuit used only 37 logic gates, had no clock signal, and exploited unconventional analog phenomena including feedback loops, electromagnetic interference between unconnected logic units, and transistors operating outside their saturation region. The evolved design diverged radically from conventional digital design principles and resisted traditional analysis methods.

??? quote "Suggested Citation"
    Thompson, A. (1997). An evolved circuit, intrinsic in silicon, entwined with physics. In: Higuchi, T., Iwata, M., Liu, W. (eds) *Evolvable Systems: From Biology to Hardware. ICES 1996*. Lecture Notes in Computer Science, vol 1259, pp. 390–405. Springer, Berlin, Heidelberg.

### Authors
- Adrian Thompson

---

## On the Automatic Design of Robust Electronics Through Artificial Evolution (1998)

**Adrian Thompson** <br>
**Publication:** International Conference on Evolvable Systems (ICES), pp. 13–24, Springer, 1998 <br>

<div class="grid cards" markdown>

- [:simple-springer:{ .lg .middle }
__Springer__
](https://link.springer.com/chapter/10.1007/BFb0057603)

- [:fontawesome-solid-graduation-cap:{ .lg .middle }
__Google Scholar__
](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=5UOUU7MAAAAJ&cstart=20&pagesize=80&sortby=pubdate&citation_for_view=5UOUU7MAAAAJ:Tyk-4Ss8FVUC)

</div>

???+ abstract
    This paper addresses a critical limitation of unconstrained intrinsic hardware evolution: the lack of robustness. While evolutionary algorithms had produced remarkably compact and unconventional FPGA configurations, these designs typically failed when deployed on different FPGA chips or under varying temperature conditions. Thompson establishes an "operational envelope" of robustness and demonstrates the feasibility of conducting fitness evaluations across diverse physical conditions, creating selective pressure that favors robust circuit designs.

??? quote "Suggested Citation"
    Thompson, A. (1998). On the automatic design of robust electronics through artificial evolution. In: *Evolvable Systems: From Biology to Hardware. ICES 1998*. Lecture Notes in Computer Science, pp. 13–24. Springer, Berlin, Heidelberg.

### Authors
- Adrian Thompson

---

## Explorations in Design Space: Unconventional Electronics Design Through Artificial Evolution (1999)

**Adrian Thompson, Paul Layzell, Ricardo Salem Zebulum** <br>
**Publication:** IEEE Transactions on Evolutionary Computation, Vol. 3, No. 3, pp. 167–196, 1999 <br>

<div class="grid cards" markdown>

- [:simple-ieee:{ .lg .middle }
__IEEE Xplore__
](https://ieeexplore.ieee.org/document/788688)

- [:fontawesome-solid-graduation-cap:{ .lg .middle }
__Google Scholar__
](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=5UOUU7MAAAAJ&citft=1&email_for_op=jasonayoder%40gmail.com&citation_for_view=5UOUU7MAAAAJ:d1gkVwhDpl0C)

</div>

???+ abstract
    This paper tests three key propositions regarding evolutionary algorithms in circuit design. First, that conventional design methods explore only constrained regions of the broader circuit design space. Second, that evolutionary algorithms can venture into unexplored territory beyond conventional approaches. Third, that these algorithms can generate practical designs superior to traditional methods. The researchers evolved a robot controller using reconfigurable hardware, comparing standard architectural constraints with unconstrained evolution. In the unrestricted scenario, the evolutionary process leveraged hardware capabilities in innovative ways. A tone discriminator circuit developed on an FPGA demonstrated unconventional structures and dynamics that diverge from standard design principles and resist traditional analysis methods.

??? quote "Suggested Citation"
    Thompson, A., Layzell, P., & Zebulum, R. S. (1999). Explorations in design space: Unconventional electronics design through artificial evolution. *IEEE Transactions on Evolutionary Computation*, 3(3), 167–196.

### Authors
- Adrian Thompson
- Paul Layzell
- Ricardo Salem Zebulum
