# Batac National High School — Wellness Leave Portal

This repository hosts the **online BNHS Wellness Leave Portal**.

## Status

The portal is already connected to the live Supabase backend. GitHub Pages is enabled for this repository.

## Teacher workflow

1. Open the GitHub Pages website.
2. On first use, choose the **Activate My Account** section.
3. Enter the teacher name exactly as issued by the administrator.
4. Enter a valid personal email address.
5. Create a password of at least 8 characters.
6. Enter the teacher's **one-time activation code**.
7. If email confirmation is requested, confirm the email, then return to the portal and sign in.

Each activation code can be used only once and binds the login account to that teacher.

## Wellness Leave rules

- Maximum **5 Wellness Leave days** per teacher.
- Maximum **3 consecutive school days**.
- Maximum **2 teachers on the same date**.
- **Saturday and Sunday are unavailable**.
- All logged-in teachers see the same shared calendar and available slots.
- A teacher can plot or remove only their own leave. Administrator access can manage all records.

## Security

Teacher activation codes and passwords are **not stored in this public GitHub repository**.

The browser uses only the Supabase project URL and browser-safe publishable key. Row Level Security and database validation enforce the leave and ownership rules on the server.

## Private administrator file

The school administrator should keep the separate activation-code CSV private and distribute each code only to its assigned teacher.
