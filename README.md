> **Celaya Solutions Research Course Edition. Challenge project.** Read [COURSE_EDITION.md](COURSE_EDITION.md) and [UPSTREAM.md](UPSTREAM.md) before you pick it. An instructor has to approve this one. Use fake data only.

<div align="center">
  <img src="assets/invidious-colored-vector.svg" width="140" height="140" alt="Invidious logo">
</div>

# Invidious

Project 08 on the [Zero to Agent project shelf](https://zerotoagent.org/course/landing.html#projects). Second of the four Challenge projects.

Invidious is a different front door for a video site. You watch the videos through it instead of through the site itself: no ads, no tracking, no account, and it works with JavaScript turned off. You can follow channels without an account anywhere else.

This is a copy of the real Invidious project, kept for the course. The name, the logo, and its license are its own, and they stay.

## Why this one is a Challenge

The language is Crystal, and the database is PostgreSQL. The course teaches neither, and the six Core projects are the same amount of work in a language the class shares.

But the real reason it is a Challenge is worth reading twice, because it is the whole lesson of this project.

**Invidious works by reading a website nobody promised it could read.** The video service it depends on can change its pages any morning, without telling anyone, and when that happens Invidious stops working. Not because someone wrote a bug. Because something outside the code moved. Public copies of Invidious break this way regularly, and the people running them find out from users.

That is a thing worth building on purpose, once, while it is safe to. Most software you will write depends on something you do not control, and the difference between a good build and a bad one is whether it tells you clearly when the thing it depends on has moved. Take this one if that is the problem you want.

Do not take it if you need the demo to work on a specific night. It might not, and that will not be your fault, and it will still be your demo.

## What you owe before an instructor will approve it

This project does not get the shared course setup, so bring a written plan first:

- Where it will run, and how you will get PostgreSQL for it.
- What you will change, given that you do not know Crystal yet.
- What you will show if the outside service is broken that night.

Then the same five things every project on the shelf has to hit:

1. A change you can see on the screen.
2. A change to the server or to what gets stored.
3. The frontend live on Vercel.
4. The backend running on Railway, still running tomorrow.
5. A three minute demo: the problem, the before, the after.

Note that this one is a single program that serves its own pages, so the Vercel and Railway split the Core projects use does not apply to it as written. Sorting that out is part of your plan.

## What is in here

| Path | What it is |
| --- | --- |
| `src/invidious/` | The whole application, in Crystal |
| `src/invidious/views/` | The pages, as templates |
| `config/` | Configuration, including the database connection |
| `locales/` | Translations |
| `spec/` | Tests |
| `docker/`, `kubernetes/`, `nix/` | Ways to run it |

## Running it

Running it needs Crystal and a PostgreSQL database, and it is not a `pnpm install` away. The project keeps its own installation guide at <https://docs.invidious.io/installation/>, and its full documentation at <https://docs.invidious.io/>. Use those; the course does not have its own version.

## Liability

The upstream project's own words on this, kept because they still apply:

> We take no responsibility for the use of our tool, or external instances provided by third parties. We strongly recommend you abide by the valid official regulations in your country. Furthermore, we refuse liability for any inappropriate use of Invidious, such as illegal downloading. This tool is provided to you in the spirit of free, open software.

## Source and license

Invidious is licensed under the GNU Affero General Public License version 3. The full license is in [LICENSE](LICENSE) and it applies to this copy, including the part that says if you run a modified version where other people can reach it, you have to offer them your source.

The source project, the exact commit, and the course status are recorded in [UPSTREAM.md](UPSTREAM.md). The Invidious name, logo, and copyright are the upstream project's and stay exactly as they are. This copy is frozen: it has no link back to the source project and does not take its updates, so do not open pull requests upstream from here.

This is a course edition, not a product, and it does not claim to be Invidious. It is free and noncommercial, and the Celaya Solutions Research Course Edition notice stays on it.
