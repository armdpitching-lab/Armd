# ARM’D — Deploy Guide

Everything is built and wired. Formspree is live.
Your only job: upload these files to GitHub and deploy on Vercel.

-----

## STEP 1 — Upload to GitHub (5 min)

1. Go to <https://github.com> and sign in
1. Click the **+** icon → **New repository**
1. Name it `armd` → click **Create repository**
1. Click **uploading an existing file**
1. Drag ALL files from this folder into the upload area
   (include: src/, public/, package.json, vercel.json, .gitignore, README.md, .env.example)
1. Click **Commit changes**

-----

## STEP 2 — Deploy on Vercel (3 min)

1. Go to <https://vercel.com/armdpitching-6330> (your account is ready)
1. Click **Add New Project**
1. Select your `armd` GitHub repository
1. Click **Deploy** — done

Your site is live at `armd.vercel.app` within 2 minutes.

-----

## STEP 3 — Add Stripe (when you’re ready)

Once you have a Stripe account:

1. Go to your Vercel project → **Settings → Environment Variables**
1. Add:
- `REACT_APP_STRIPE_PUBLISHABLE_KEY` → your `pk_live_...` key
- `REACT_APP_STRIPE_PRICE_ID` → your `price_...` ID from a Stripe Product
1. Redeploy — payments are now live

**Until then:** bookings still work. Every submission hits Formspree
and emails you instantly with the full booking details. No money lost.

-----

## STEP 4 — Custom Domain (optional, ~$12/year)

1. Buy your domain at <https://namecheap.com>
1. In Vercel → Settings → Domains → add your domain
1. Copy the DNS records Vercel gives you into Namecheap
1. Live within minutes

-----

## How it works right now

|What happens            |What you get                                                                |
|------------------------|----------------------------------------------------------------------------|
|Someone books           |Email to [getarmd@gmail.com](mailto:getarmd@gmail.com) with full details    |
|Someone applies to pitch|Email to [getarmd@gmail.com](mailto:getarmd@gmail.com) with full application|
|Stripe added later      |Payments wired in, zero code changes needed                                 |