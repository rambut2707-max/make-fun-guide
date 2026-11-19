# Submit notes — bring-the-humans-02 (do NOT ship this file's contents as the entry; it is the operator's checklist)

## Verified referral link (live, 2026-11-19 ~13:17 WIB)
- Link: https://make.fun/r/723bx7wm
- Code: 723bx7wm
- Source: GET /api/me/referrals (code + link + share_message all agree; pinned payout 7K1GPmaEsriWB45uzKgiGGXdMQD2oqJZnYyM4Uf1n7Uq).
- Referral terms on this account: $0.25 per verified signup (limit 20, 0 counted so far),
  $1.00 on a referred account's first submission, 10% prize share for 90 days.
- The README already carries the link and the bare code in several places. DO NOT change them.

## Placeholders still in README.md — fill before submit
- `{{GITHUB_OWNER}}` and `{{REPOSITORY}}` appear ONLY in the two per-repo badge lines
  (rank.svg / reward.svg). The GitHub repo does not exist yet (user has no GitHub account
  as of 2026-11-19; they are creating one and linking it to make.fun).
- Once the repo exists: replace both placeholders with the real owner and repo name,
  commit, and verify the badge URLs resolve. Do NOT touch the referral link/code.
- Repo About on GitHub must carry: website https://make.fun/bounty/bring-the-humans-02
  and topic `makefun` (check repo_about).

## screenshot.png — CANNOT be made yet
- It must be a screenshot of the repo's page ON GITHUB with this README showing, taken
  AFTER the repo is public. Top of the image should show the repo name + start of the README
  (board/Feed show the top square).
- Constraints: PNG/JPEG/WebP, at most 8 MB and 16,000,000 pixels (a full-page capture at
  normal scale fits; double-scale of a long page may not).
- Commit it as screenshot.png at the repo root, then submit that commit.

## Entry facts
- Competition: bring-the-humans-02 ("Bring the humans again"), Growth, $1,000 top 50
  (1st $150, 2nd $80, 3rd $50, 4th–10th $20, 11th–25th $17, 26th–50th $13).
- Deadline: 2026-11-21T10:30:00Z (17:30 WIB). Final check ends 30h after deadline.
- Ranking: verified human signups through the referral link in the window. Fake/bot/self/
  same-network/IP-cluster/idle signups never count. Tie goes to the earlier receipt.
- Quota verified 2026-11-19: can_submit TRUE, entries_made 0, day cap left 3.
- Repo requirements: public, owned by the GitHub account LINKED to the make.fun account,
  created AFTER the competition opens, OSI license (MIT here), README.md exact case at root,
  no .github/README.md shadowing it. Final re-check reads the repo again — it must stay
  public, same repo, same owner, README still carrying the referral code.
- The kit starter was READ for the three badge lines and the rules, but the README was
  written fresh in-session (draft + append + revision across 3 messages); nothing was copied.

## Submit pattern (GitHub-repo entry — NOT a source bundle)
From the kit root (~/workspace/makefun/bring-the-humans-02-work/kit-extract/bring-the-humans-02-kit/):

1. Bundle the transcripts (level-20 kit: --system-prompt required; agent-fact flags required):
   node cli/makefun.mjs bundle --repo ~/workspace/makefun/bring-the-humans-02-entry \
     --out ~/workspace/makefun/bring-the-humans-02-work/transcripts.tar.gz \
     --muse-usage ~/workspace/makefun/bring-the-humans-02-work/usage.jsonl \
     --system-prompt ~/workspace/makefun/bring-the-humans-02-work/system-prompt.txt \
     --mcp none --harness Muse --harness-version 1.3 \
     --provider meta --model muse-spark-1.3 --effort default
   NOTE: usage rows for the builder session attach only once its run completes — the parent
   must re-run the usage SELECT (parent id + builder session id) and re-bundle before submit.
2. Check from the kit root, NO --kit flag:
   node cli/makefun.mjs check --repo ~/workspace/makefun/bring-the-humans-02-entry \
     --transcripts ~/workspace/makefun/bring-the-humans-02-work/transcripts.tar.gz
3. Submit (GitHub URL + full 40-char commit sha; the repo must be public on GitHub first):
   node cli/makefun.mjs submit --competition bring-the-humans-02 \
     --repo-url https://github.com/<owner>/<repo> --commit <full-40-char-sha> \
     --bundle ~/workspace/makefun/bring-the-humans-02-work/transcripts.tar.gz \
     --keypair ~/.makefun/keypairs/make.fun.json
   The entry is signed by a Solana wallet linked to the account (the agent keypair's wallet
   7Cw8E4AHwuGK2PueqfvFbhMco4ct5dw7feyLuKJoZzNE signs under the payout delegation to
   7K1GPmaEsriWB45uzKgiGGXdMQD2oqJZnYyM4Uf1n7Uq).

## Remaining steps (in order)
1. User: create GitHub account + link it to make.fun (profile) + create the public repo
   (name it something like make-fun-guide), set About website + `makefun` topic.
2. Parent: replace {{GITHUB_OWNER}}/{{REPOSITORY}} in README.md, commit to the GitHub repo.
3. Parent/user: take screenshot.png of the GitHub repo page, commit it at the root.
4. Parent: re-run usage SELECT, re-bundle, re-check, verify quota, submit.
5. User: share the GitHub repo link (which carries the referral link) wherever real humans
   who might join make.fun will see it — the score is verified signups, not the guide alone.
