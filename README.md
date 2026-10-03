# BNHS Wellness Leave Portal — GitHub Pages

This repository hosts the **teacher-facing BNHS Wellness Leave Portal**.

## Architecture

- **GitHub Pages** hosts the website (`index.html`).
- **Supabase Auth** provides one login account per teacher.
- **Supabase PostgreSQL** stores the shared Wellness Leave calendar.
- **Row Level Security (RLS)** prevents a teacher from creating or deleting another teacher's leave.

## Wellness Leave rules

- Maximum 5 Wellness Leave days per teacher.
- Maximum 3 consecutive school days.
- Maximum 2 teachers on the same school date.
- Saturday and Sunday are unavailable.
- All connected teachers see the same calendar slots.

## Setup

1. Run `SUPABASE_SETUP.sql` in the Supabase SQL Editor.
2. Create each teacher as a Supabase Auth user and link the Auth user UUID to a matching row in `public.profiles`.
3. Edit `online-config.js` with the Supabase URL and browser-safe publishable key.
4. In GitHub, enable **Settings → Pages → Deploy from a branch → main → /(root)**.

Do **not** put teacher passwords or a Supabase service-role/secret key in this public repository.
