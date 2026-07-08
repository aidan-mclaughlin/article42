# Article 42

A friendly field guide to your rights under the [UN Convention on the Rights of the Child](https://www.unicef.org.uk/what-we-do/un-convention-child-rights/), tailored for young people in Scotland. For ages 8 to 18.

The name comes from Article 42 itself, which says governments must make sure children and adults know about these rights. Scotland incorporated the UNCRC into domestic law via the UNCRC (Incorporation) (Scotland) Act 2024.

## What's inside

An age-picker landing routes visitors into one of three tracks:

**8–12, a playful paper-style zine** with a 21-tile board game, "what would you do" scenarios, and a library of 14 rights in kid-friendly language.

**13–18, an editorial guide** with 12 rights cards, scenarios covering real situations (partners, police stops, coming out, fake IDs), and a 14-question Scottish legal quiz.

**Any age, Ask Article 42**, ten worry-based entry points (feeling unsafe, trouble at home, mental health, discrimination, bullying, work, privacy, etc.) that link to real Scottish and UK-wide helplines with live phone numbers.

## Helplines referenced

Scotland-specific: Breathing Space (0800 83 85 87), SAMH, respectme (national anti-bullying), Parentline Scotland / Children 1st (08000 28 22 33), Scotland Domestic Abuse + Forced Marriage Helpline (0800 027 1234), Scottish Women's Aid, Who Cares? Scotland, LGBT Youth Scotland, Clan Childlaw, Enquire, Govan Law Centre Education Law Unit, the Children and Young People's Commissioner Scotland, the Scottish Public Services Ombudsman, the Police Investigations & Review Commissioner (PIRC), and Citizens Advice Scotland.

UK-wide: Childline (0800 1111), NSPCC (0808 800 5000), Samaritans (116 123), Shout (text 85258), Papyrus HOPELINE247, Runaway Helpline (116 000), ACAS, and the HMRC minimum wage line.

## Tech

Single `index.html` file. Tailwind via CDN, Nunito from Google Fonts, vanilla JS state machine. No build step. Deployed via Netlify.

## License

[MIT](./LICENSE)

## Development & making changes

Everything lives in **one file: `index.html`** — Tailwind via CDN, Nunito from
Google Fonts, and a vanilla-JS state machine that routes the three tracks. No
build step, no dependencies to install.

```bash
python3 -m http.server 8000   # or just open index.html
```

Guidance for editors (human or agent):

- **Content lives in the JS data structures** inside the `<script>` block
  (rights cards, scenarios, quiz questions, helpline entries) — edit data, not
  markup, where possible.
- **Helpline numbers are safety-critical content.** Verify any number against
  the operator's own website before changing it, and never remove a helpline
  without a replacement.
- **Audience-appropriate language is the product.** The 8–12 track stays
  playful and simple; the 13–18 track is frank but non-judgemental. Legal
  claims must hold **for Scotland specifically** (UNCRC (Incorporation)
  (Scotland) Act 2024 — not England/Wales law).
- Keep it accessible: semantic headings, alt text, visible focus, high
  contrast. Young people on old phones and screen readers are the audience.

## Deploy

Static host — currently Netlify; any static server works (`robots.txt` and
`site.webmanifest` included). No analytics, no cookies, no personal data
collected — keep it that way.

Maintained by the SoftCare team (SoftCare-UK) as a public-good resource.
