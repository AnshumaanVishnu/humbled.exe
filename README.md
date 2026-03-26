# humbled.exe

Honest user feedback for founders, indie hackers, and solo devs.

## Deploy to Vercel

1. Push this folder to a GitHub repo
2. Go to vercel.com → New Project → import your repo
3. Deploy (zero config needed — vercel.json handles it)
4. Add custom domain: `humbled.dropoutdudes.com`
   - Vercel gives you a CNAME value
   - Add it in cPanel → Zone Editor

## Adding new feedback to the wall

Open `index.html` and find the `<!-- CARD -->` blocks in the feedback wall section.
Copy an existing card block and update:
- Product name
- #HMB-ID (increment the number)
- Feedback text (bold the key lines with `<strong>`)
- Starting reaction counts
- Time ago

Also add the entry to the `wallData` array in the script at the bottom so the lookup works.

Then push to GitHub → Vercel auto-deploys in ~30 seconds.

## Form
Submissions go to: https://forms.gle/ivKyPFE6XcUiagsE6
Check responses in Google Sheets linked to the form.

## Reactions
Reactions are stored in localStorage per visitor browser.
They reset on clearing browser data — this is fine for now.
When you want persistent counts, add Supabase free tier.
