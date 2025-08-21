# Recovery — Known Good Restore (America/Regina)
Use when a bad commit slips into dev.

## Restore last Known Good snapshot locally
1) git fetch origin
2) git checkout v2b-dev
3) git log --oneline --decorate -n 20
4) git checkout <KNOWN_GOOD_COMMIT> -- BEAST_PhaseA_KnownGood_v2a_AUDITED.ipynb
5) git commit -m "recovery: restore Known Good notebook"
6) git push origin v2b-dev

Notes:
- Record absolute timestamps in PRs (TZ America/Regina).
- Never force-push `main`. Recovery happens on dev branch only.
