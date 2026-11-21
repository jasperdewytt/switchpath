# Switchpath

Describe what's going on in your life, like a first graduate job or a plan to buy an investment property, and Switchpath tells you which financial professionals to see, in what order and why. It asks one follow-up question, builds the pathway, then matches you with professionals you can request a consultation with.

Built for Weekend of Startups 2026, where it reached the semi-finals. The professionals and the demo user are fictional.

## How it works

An Astro site in `frontend/` with two serverless endpoints, `/api/clarify` and `/api/generate`, deployed on Vercel. Both call Groq with a strict JSON schema. The output is then checked again before it reaches the page, and anything that claims a professional is licensed, accredited, "the best" and so on is rejected.

## Run it

```sh
cd frontend
npm install
cp .env.example .env   # add GROQ_API_KEY
npm run dev:ai         # with the live model
npm run dev:demo       # scripted demo, no key needed
npm test
```

Built by Jasper de Wolfe de Wytt. John Kong set up the original Astro site.
