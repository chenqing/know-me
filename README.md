# Know me

An agent skill that interviews you one question at a time until it has a
durable, multi-layer picture of who you are, then saves **confirmed** facts
to shared memory.

Inspired by Matt Pocock’s [grill-me](https://github.com/mattpocock/skills)
interview loop, applied to a person instead of a plan.

## Install

```bash
npx skills add chenqing/know-me --skill know-me
```

Or copy `skills/know-me/SKILL.md` into your agent’s skills folder.

## What it covers

Thirteen profile layers: identity, life narrative, values, decision style,
goals, work system, relationships, energy rhythms, tools, communication
prefs, money/time tradeoffs, Jobs-to-be-Done help jobs, taboos, plus a final
check of the agent’s mental model.

## Design notes

- One question per turn; plain language only to the user
- Full first pass in one session by default
- Confirmed semantic facts → profile; dated scenes → log
- Not therapy, not a personality test

## Theory and research behind the design

The skill keeps grill-me’s interrogation primitive (one question at a time,
branch resolution, recommended guesses). The **dimensions** come from
user-modeling and life-story research, not from a five-bucket fact list.

| Area | What we borrow | How Know me uses it |
|------|----------------|---------------------|
| Life narrative | McAdams Life Story Interview | Sample chapter titles / turning points; do not run a full clinical LSI |
| Values | Schwartz basic individual values | Scaffold choice probes; never administer a full scale |
| Soft traits | BFI-2 (incl. China validation) | Situational “slow vs wrong” style probes; no diagnostic labels |
| Vocational interest (optional) | Holland RIASEC | Optional work-environment energy probe only |
| Memory layering | Tulving episodic vs semantic; MemGPT; Generative Agents | Dated scenes → log; stable self-knowledge → profile; unverified agent guesses stay meta |
| Theory of mind / personalization | Mind Modeling (ToM) frameworks | Keep revisable hypotheses separate from confirmed facts |
| How to help | Christensen Jobs-to-be-Done | Ask for a real stuck moment and what success looked like |
| Interview stopping | Guest et al. on thematic saturation | Stop on no new actionable facts + user halt, not “all buckets checked” |
| Culture (when relevant) | Hwang face / Chinese relationalism | Relationship roles, face-sensitive topics, neutral obligation questions |
| Human–AI interaction | Amershi et al. guidelines | Disclose, stay correctable, do not over-claim intimacy |

### References

1. McAdams, D. P. (2007). *The Life Story Interview – II*. Northwestern University Foley Center. https://cpb-us-e1.wpmucdn.com/sites.northwestern.edu/dist/4/3901/files/2020/11/The-Life-Story-Interview-II-2007.pdf
2. McAdams, D. P. (2001). The psychology of life stories. *Review of General Psychology*, 5(2), 100–122. https://doi.org/10.1037/1089-2680.5.2.100
3. Soto, C. J., & John, O. P. (2017). The next Big Five Inventory (BFI-2)…. *Journal of Personality and Social Psychology*, 113(1), 117–143. https://doi.org/10.1037/pspp0000096
4. Zhang, B., Li, Y. M., Li, J., et al. (2022). The Big Five Inventory–2 in China…. *Assessment*, 29(6), 1262–1284. https://doi.org/10.1177/10731911211008245
5. Schwartz, S. H., Cieciuch, J., Vecchione, M., et al. (2012). Refining the theory of basic individual values. *JPSP*, 103(4), 663–688. https://doi.org/10.1037/a0029393
6. Schwartz, S. H. (2021). A repository of Schwartz value scales…. *Online Readings in Psychology and Culture*. https://scholarworks.gvsu.edu/orpc/vol2/iss2/9/
7. Holland, J. L. (1997). *Making Vocational Choices* (3rd ed.). PAR. ISBN 0911907270
8. Packer, C., Wooders, S., Lin, K., et al. (2023). MemGPT: Towards LLMs as Operating Systems. arXiv:2310.08560. https://doi.org/10.48550/arXiv.2310.08560
9. Park, J. S., O’Brien, J. C., Cai, C. J., Morris, M. R., Liang, P., & Bernstein, M. S. (2023). Generative Agents: Interactive Simulacra of Human Behavior. *UIST ’23*. https://doi.org/10.1145/3586183.3606763 ; https://arxiv.org/abs/2304.03442
10. Gena, C. (2026). Mind Modeling: A ToM-Based Framework for Personalization. arXiv:2605.10306. https://doi.org/10.48550/arXiv.2605.10306
11. Tulving, E. (1972). Episodic and semantic memory. In E. Tulving & W. Donaldson (Eds.), *Organization of Memory* (pp. 381–403). Academic Press.
12. Christensen, C. M., Hall, T., Dillon, K., & Duncan, D. S. (2016). *Competing Against Luck*. HarperBusiness. ISBN 978-0062435613
13. Guest, G., Bunce, A., & Johnson, L. (2006). How many interviews are enough? *Field Methods*, 18(1), 59–82. https://doi.org/10.1177/1525822X05279903
14. Hwang, K.-K. (1987). Face and favor: The Chinese power game. *American Journal of Sociology*, 92(4), 944–974. https://doi.org/10.1086/228588
15. Hwang, K.-K. (2000). Chinese relationalism…. *Journal for the Theory of Social Behaviour*, 30(2), 155–178. https://doi.org/10.1111/1468-5914.00124
16. Amershi, S., Weld, D., Vorvoreanu, M., et al. (2019). Guidelines for human-AI interaction. *CHI ’19*. https://doi.org/10.1145/3290605.3300233
17. Matt Pocock. grill-me skill. https://github.com/mattpocock/skills

**Important:** Scales and interview protocols above are **scaffolds**. Know me must not administer full psychometric batteries or produce clinical personality diagnoses.

## License

MIT
