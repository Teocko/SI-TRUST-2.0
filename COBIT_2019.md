# COBIT 2019: Podprtost cilja BAI06 – Upravljane IT spremembe

Ta stran povzema, katere prakse cilja **BAI06** so podprte z orodji GitHuba in katere metrike lahko spremljamo samodejno.

## Podprtost praks BAI06 v GitHubu

| BAI06 praksa | Kaj pomeni | Podprtost v GitHubu |
|---|---|---|
| **BAI06.01** Ovrednoti, prioritiziraj in odobri spremembe | Formalen predlog, vpliv, odobritev | **Issues** (opis, predloga), **Projects** (prioritete), **Milestones**, **Pull Request approvals**, **CODEOWNERS** |
| **BAI06.02** Načrtuj spremembe | Plan, okna sprememb, rollback | **Projects timeline**, **Milestones**, PR opis (rollback), **GitHub Actions** za planirane deploye |
| **BAI06.03** Testiraj spremembe | Dokazila testov | **Actions CI**, obvezni **status checks**, test reporti kot artefakti |
| **BAI06.04** Uvedi spremembe | Nadzorovana uvedba | **Actions CD**, **Environments** (approval gates), **Secrets** |
| **BAI06.05** Preglej in zaključi | Post-implementation review | **Issue/PR templates**, *close issue on merge*, **Release notes** |
| **BAI06.06** Upravljaj nujne spremembe | Emergency change | `hotfix/*` branch, label **emergency**, hitri PR z obveznim pregledom |
| **BAI06.07** Vodi evidence | Sledljivost sprememb | Commit zgodovina, PR ↔ Issue povezave, **Protected branches**, **Audit log (org)** |

## Samodejno podprte metrike (primeri)

- **Lead time for change** – čas od PR *open* do *merge* (Insights / PR timestamps).  
- **% sprememb z odobritvijo** – “required reviews approved” (branch protection).  
- **Stopnja uspešnosti sprememb** – deploy brez rollbacka (Actions run status + release notes).  
- **Mean Time to Restore (MTRS)** – čas do revert/restore (PR + Actions časovnice).  
- **% sprememb s testnimi dokazi** – *required checks passed* (PR status).  
- **Št. emergency sprememb** – štetje PR/Issues z labelom `emergency`.
