# Project Context

Paste this at the top of a new AI chat so it knows what I'm working on.

## What I'm building

A stock screener website.

A user makes filter rules like "show me stocks where price is above 500
and volume is more than 1 million". They save those rules. When a stock
starts matching a rule, they get an email.

Users pay for a higher tier to get more saved rules and faster alerts.

## Why I'm building it

To learn Next.js properly and to have one real project I can show in job
interviews. I work on a stock market platform, so I understand this
subject and can tell when the output is wrong.

This is a learning project first. Shipping fast is not the goal.

## What I'm using

| Thing | What it does |
|---|---|
| Next.js 15 (App Router) | The framework. Pages, routing, server code. |
| TypeScript (strict mode on) | Catches mistakes while I type. No `any` allowed. |
| Tailwind CSS | Styling with classes in the HTML. |
| PostgreSQL | The database. |
| Drizzle | Lets me write database queries in TypeScript instead of raw SQL. |
| Auth.js | Handles login, signup and sessions. |
| Zod | Checks that data sent by a user is the right shape. |
| Docker | Runs a throwaway Postgres on my laptop for coding. |
| Vercel | Hosts the live site. |
| Neon | Hosts the cloud database the live site talks to. |

Live site: https://screener-saas.vercel.app/
Code: https://github.com/Vineet90x/screener-saas

## Decisions already made (please don't suggest changing these)

- **Auth.js, not Supabase Auth** — I want to build login myself. That's
  the point. A tool that does it for me removes the lesson.
- **Neon, not Supabase** — Supabase pauses a free project after 7 days
  of no activity, so the link would be dead when a recruiter clicks it.
  Neon's database sleeps but wakes itself in under a second.
- **Two databases** — a local one in Docker for coding, and Neon for the
  live site. The live site can't reach a database on my laptop.
- **Moving to AWS later** — around week 9 the database moves to AWS RDS
  and the app runs on EC2 in a Docker container. Neon is temporary.
- **No Kubernetes, no AWS certification.** Out of scope on purpose.

## Where I am now

Weekend 1 of 10. Started 19 Sep 2026.

Done:
- Project created, TypeScript strict mode on
- Pushed to GitHub
- Deployed live on Vercel (still showing the default page)

Next:
- Design the database tables (which tables, which columns)
- Replace the default homepage with a real page
- Week 2: login, Docker Postgres, connect Neon

## How I want help

I use AI to build, so these rules exist to make sure I actually learn:

1. **Explain in simple words.** Define any technical term the moment you
   use it. Don't assume I know it.
2. **I design, you review.** Let me try the data model, the structure,
   the approach first — even if I get it wrong. Correcting my version
   teaches me more than reading yours.
3. **Don't write big chunks of code for me.** I have to defend every
   line in an interview. Boilerplate and config are fine to generate.
   Auth logic, database queries, hooks and Dockerfiles are not.
4. **Explain why, not just what.** "Use X" is useless. "Use X instead of
   Y because Z" is the part I need.
5. **Be honest. Disagree with me.** If my idea is bad, say so directly
   and tell me why. Don't just agree to be agreeable.

## My experience level

About 2 years as a full stack developer. Comfortable with Angular,
FastAPI, SQL and Python. New to Next.js, Docker and AWS.

So: don't over-explain what a database or an API is. Do explain anything
specific to Next.js, Docker or cloud hosting.
