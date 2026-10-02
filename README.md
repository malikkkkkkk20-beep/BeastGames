# Beast Games – BSA College Mathura

Registration portal for the Beast Games sports event.

## Files
- `index.html` – the complete website (single file, deploy as is)
- `supabase-setup.sql` – database, security rules and storage (already applied to the "Beast Games BSA" project)

## Deploy (Vercel)
1. Put `index.html` in your project root (replace the old one).
2. Redeploy.

## Supabase checklist
1. Authentication > Providers > Email: turn **Confirm email OFF**.
2. Authentication > Users > Add user (admin email + strong password, auto-confirm).
3. Add the admin: `insert into public.admins(uid) select id from auth.users where email = 'ADMIN_EMAIL_HERE';`
4. Admin panel (small circle on the home page, bottom right): set UPI ID, fees, registration date and venue.

## Notes
- Games start date is set in `index.html` (`GS`, currently 5 Nov 2026, 8 days).
- Players never see admin options; admin sessions are not saved after refresh.
- Photos and ID proofs are stored in private buckets.
