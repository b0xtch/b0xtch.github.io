# Mahmoud Shehata (b0xtch)

Source for [b0xtch.com](https://b0xtch.com/), Mahmoud Shehata's personal website.
Plain HTML and CSS, hosted on GitHub Pages with the domain in `CNAME`.
No build or JavaScript is required to read the page or its structured data.

## Preview

Run `python3 -m http.server 8000` from the repo, then visit
<http://localhost:8000/>.

## Identity configuration

The visible bio, page title, metadata, and JSON-LD connect
**Mahmoud Shehata = b0xtch = Software Engineer**. The structured-data graph links
a `WebSite`, a `ProfilePage`, and one `Person` with the stable ID
`https://b0xtch.com/#person`. The person's `sameAs` profiles also appear as
visible links. Keep the markup and visible content consistent.

Sources checked for this update:

- The existing website and [GitHub profile](https://github.com/b0xtch) connect
  the real name, handle, website, and X profile. The owner confirmed the
  LinkedIn URL `https://www.linkedin.com/in/botch`.
- The public [Confidential AI team page](https://confidential.ai/team) lists
  Mahmoud Shehata as a Member of Technical Staff. Keep the bio and `worksFor`
  current if that changes.
- Recent Confidential AI articles credit the organization. This page does not
  claim personal authorship of those articles. The whitepaper's old year label
  conflicted with the archive timestamp, so it now says “archived PDF” without
  asserting an unverified publication date.

The canonical URL, Open Graph URL, sitemap, JSON-LD, and `CNAME` use
`https://b0xtch.com/`. The sitemap contains only the actual canonical homepage,
not fragments, assets, or social profiles. No artificial `lastmod` date is used.
The 1200 × 630 `social-card.png` is a title card for social previews, not a
portrait or a `Person.image`.

For a new article, add an internal link, a sitemap entry, its own title,
description and canonical URL, and accurate Article schema with an author
link to this profile. Use real publication/modification dates.

## Launch checklist

1. After deployment, check the homepage, `/style.css`, `/favicon.svg`,
   `/social-card.png`, `/robots.txt`, and `/sitemap.xml` return 200. Confirm HTTP
   and the GitHub Pages hostname redirect to the HTTPS custom domain. Check the
   `www` hostname if configured; the working environment could not verify it.
2. Check Cloudflare's **live** robots.txt output, bot settings, managed AI
   crawler rules, and security events. Cloudflare added a content-signals
   preamble before this update. Allow verified Googlebot, Bingbot, and
   OAI-SearchBot access without challenges. User-agent spoofing alone cannot
   verify access for real bots. A repo `Allow` cannot override CDN blocking or
   a more specific `Disallow` group.
3. Verify a Domain property for `b0xtch.com` in
   [Google Search Console](https://search.google.com/search-console/) with the
   DNS value Google supplies. Submit `https://b0xtch.com/sitemap.xml`. Test the
   homepage with URL Inspection and request indexing after deployment.
4. Add/import the site in [Bing Webmaster Tools](https://www.bing.com/webmasters/)
   and submit the same sitemap. Verification needs the owner's authenticated
   accounts and real verification values; this PR does not fabricate these.
5. Validate the deployed page with Google's
   [Rich Results Test](https://search.google.com/test/rich-results) and the
   [Schema.org validator](https://validator.schema.org/). Local JSON validation
   does not establish Google rich-result eligibility. Check the social preview
   too; platforms may cache the previous metadata.

## Profile alignment

Apply these in the respective account settings. This website change does not
edit social accounts or other repositories. Keep the `b0xtch` handle and link
each profile back to `https://b0xtch.com/`.

| Profile | Suggested fields |
| --- | --- |
| GitHub | Name: Mahmoud Shehata; bio: Software Engineer · AI · Distributed Systems |
| X | Display name: Mahmoud Shehata (b0xtch); describe the actual current work |
| LinkedIn | Name: Mahmoud Shehata; headline: Software Engineer · AI Infrastructure · Distributed Systems |

The GitHub profile already showed the real name and website when checked. A
profile README can start with:

> I'm Mahmoud Shehata (b0xtch), a software engineer focused on AI, distributed
> systems, blockchain, and confidential computing. My website: https://b0xtch.com/

## Authority and measurement

- Establish a baseline in Search Console. Compare impressions, clicks, CTR,
  and average position for `Mahmoud Shehata`, `b0xtch`, and relevant name + topic
  queries over comparable 28-day periods. This change does not provide access
  to private analytics or establish current rankings.
- Publish original engineering articles tied to real code: explain the problem,
  approach, tradeoffs, measured results, and a reproducible example. One useful
  article per month is a reasonable starting cadence.
- Where you actually contributed or wrote something, seek a named author bio
  linking to this website and GitHub. The Confidential AI organization bylines
  are a concrete attribution opportunity **if** personal authorship is confirmed.
  Prefer genuine project documentation, conference speaker pages, and technical
  references over bought links, fabricated credentials, or keyword pages.
- Check a consistent set of name/handle/topic questions in AI search occasionally
  and record which sources are cited. Answers vary by system, time, location,
  and personalization; there is no universal AI ranking score.

Google's [AI search guidance](https://developers.google.com/search/docs/appearance/ai-features)
uses the same SEO fundamentals as regular search; no special AI file or schema
is required. [OpenAI's crawler documentation](https://developers.openai.com/api/docs/bots)
distinguishes `OAI-SearchBot` (search) from `GPTBot` (potential training use).
The wildcard robots policy permits crawling; review any future training-policy
changes separately from search access. None of these changes guarantees
indexing, citations, first place, training inclusion, or a knowledge panel.
