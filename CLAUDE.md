<!-- coord:start -->
## Team coordination

This repo is set up for team coordination between agents working in shared
sessions. Follow these rules:

- Before starting non-trivial work, publish a plan with `publish_plan`.
- Keep step status current as you go, using `update_step`.
- If the injected context shows an overlap warning, coordinate before you
  edit (spec Law 3, Rev 28) — never silently duplicate the work. If it is the
  same task and you have not started, join their session: register on their
  branch, or offer `propose_work_request` — the server auto-accepts only
  when every step is provably unstarted and unassigned, so a safe join needs
  no human. If the work is related, claim only unstarted, unassigned steps
  the same way. Never take started or assigned work. Stop and ask your human
  only when your permission mode requires approval or no safe action exists.
- When you discover something non-obvious (a gotcha, a decision, a fact
  someone else would need), write it down with `remember` so the team
  keeps it.
- When something is a teammate’s job rather than yours — their area, their
  decision, a question only they can answer — hand it to them with
  `assign_work` instead of asking your human to relay a message. Use
  `list_people` to turn a name into an assignee id, put the whole brief
  in the note, and tell your human who you handed it to. Their own agent is
  told at its next prompt. This is free: no model call, no sponsor, nothing
  to pay for.
- When you hit a bug, a blocker, or something that plainly wants a different
  specialist, open it with `report_opportunity` and close it with
  `resolve_opportunity` when it is handled. Nothing reads your transcript
  looking for these, so a problem you only describe in your answer reaches
  nobody; reporting it is what lets the team's Brain offer it to whoever fits.
  Reporting is not notifying — it may reach no one — so do not tell your human
  a teammate was alerted.
<!-- coord:end -->

# Regeln für Claude (gilt für beide Accounts)

Zwei Personen suchen hier gemeinsam ein Produkt für ein Business. Du arbeitest für die Person, die gerade mit dir schreibt, aber der Ordner gehört beiden.

- Lies zuerst `README.md`, `00-ausgangslage.md` und `03-aufgaben.md`.
- Ändere nie, was die andere Person geschrieben hat, ohne es zu sagen. Ergänze lieber und markiere mit Namen und Datum.
- Jede neue Idee kommt in `02-kandidaten.md`, bewertet nach `01-kriterien.md`. Details gehören nach `recherche/<produkt>.md`.
- Schreib Quellen zu jeder Zahl (Link, Datum). Ohne Quelle als «geschätzt» kennzeichnen.
- Sei ehrlich: Wenn eine Idee schlecht ist (zu kleine Marge, zu viel Konkurrenz, rechtliche Probleme), sag es klar.
- Mach kurze Vorschläge, was als Nächstes sinnvoll wäre.
- Nichts kaufen, bestellen, bezahlen oder Verträge abschliessen. Das entscheiden die beiden selbst.
- Sprache: Deutsch.
