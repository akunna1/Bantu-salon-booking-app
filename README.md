# Bantu African Hair Braiding Salon — Booking App 💇🏾‍♀️

A full-stack salon management web application built with Next.js 14, Drizzle ORM, Neon Database, and Kinde Auth to modernize and simplify the ticketing and customer management process for hair salons.

---

## Project Purpose

Replace traditional salon notebooks with a streamlined, role-based booking system that supports:

* Secure employee logins
* Ticket creation and assignment
* Customer tracking
* Role-based permissions (Employee, Manager, Admin)
* Light/dark mode toggle
* Responsive UI for desktop, tablet, and phone

---

## Built With

* Next.js 14 App Router
* TypeScript
* Tailwind CSS + ShadCN UI
* Drizzle ORM
* Neon HTTP Adapter
* Kinde (passwordless authentication & role-based permissions)

---

## Project Structure Highlights

* `/src/app` — Core routing and layout
* `/src/app/(salon)` — Salon-specific pages
* `/src/components` — Header, footer, reusable buttons, form elements
* `/src/lib/queries` — Drizzle ORM database queries
* `/src/zod-schemas` — Validation for customers and tickets
* `/src/db` — Schema definitions and migration scripts
* `/public/images` — Static assets

---

## Features Implemented (52.4% Complete) 🚧

* Public homepage with salon info
* Passwordless employee login via Kinde
* Open tickets page (in progress)
* CRUD for tickets and customers
* Ticket status (OPEN / COMPLETED)
* User roles: Admin, Manager, Employee
* Weekly login requirement via SSO timeout
* Kinde-based permission management
* Light/dark theme toggle
* Mobile-responsive layout

---

## Middleware & Access Control

* `middleware.ts` handles route protection
* Routes like `/tickets` are protected and role-restricted
* Kinde ensures suspended users lose access immediately

---

## Tech Highlights

* ShadCN UI — Component library for styling and accessibility
* Drizzle ORM — Database layer using SQL migrations
* Neon — Serverless PostgreSQL with HTTP adapter
* Kinde — Handles user authentication and permissions
* Zod — Schema validation for user input

---

## Common Dev Commands 🧑🏾‍💻

```bash
npm i drizzle-orm @neondatabase/serverless
npm i -D drizzle-kit tsx dotenv
npm run db:generate
npm run db:migrate
```

---

## Authentication Flow (Kinde)

* Passwordless login enabled
* Custom roles set: `admin`, `manager`, `employee`
* Self-signup disabled
* SSO timeout = 7 days
* Logout & redirect logic managed in `.env.local`

---

## Example Routes

* Booking form: `/booking/form?customerId=2`
* Ticket edit: `/tickets/form?ticketId=24`

---

## Status

Development is still ongoing. Upcoming tasks include:

* Ticket search and filters
* Locking unauthorized pages
* Role-based edit/delete permissions
* Improved mobile support
