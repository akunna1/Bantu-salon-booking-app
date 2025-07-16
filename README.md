# Bantu African Hair Braiding Salon Booking App 💇🏾‍♀️✨🖥️

This web application is designed to modernize how small salons manage customer records, service tickets, and staff roles. Built with Next.js, Drizzle ORM, Neon, and Kinde Auth, it replaces traditional notebooks with a streamlined, secure, and mobile-friendly booking system.

---

## Project Overview

**Bantu Salon App** simplifies salon operations through:

* Passwordless employee login
* Real-time service ticket tracking
* Customer data management
* Role-based access (Admin, Manager, Employee)
* Light/dark mode toggle
* Clean, responsive design optimized for desktop and mobile

---

## Technologies Used

* **Framework & Language**: Next.js 14 (App Router), TypeScript
* **UI Components**: Tailwind CSS, ShadCN UI
* **Database**: Drizzle ORM with Neon (serverless PostgreSQL)
* **Authentication**: Kinde (SSO, permissions, passwordless login)
* **Validation & Utilities**: Zod, custom middleware, reusable components

---

## Core Features

* ✅ Public landing page with contact info
* ✅ Secure passwordless login for employees
* ✅ Role management via Kinde (Admin, Manager, Employee)
* ✅ CRUD functionality for customers and service tickets
* ✅ Weekly login requirement (via SSO timeout)
* ✅ Toggleable light/dark mode
* ✅ Fully responsive UI for phones, tablets, and desktops
* 🔜 Upcoming: role-specific access control, ticket filters, page locking

---

## Folder Highlights

* `src/app/(salon)` – Routes for booking, tickets, users
* `src/components/ui` – ShadCN-based reusable elements
* `src/db` – Drizzle schema, migration scripts
* `src/lib/queries` – SQL queries for customers and tickets
* `middleware.ts` – Handles protected routes

---

## Dev Setup & Commands

```bash
npm install
npm run db:generate    # Generate types from schema
npm run db:migrate     # Run database migration
```

---

## Authentication & Permissions

* Kinde handles secure login and user roles
* Self-signup is disabled for security
* Permissions set in Kinde dashboard for Admin, Manager, Employee
* Session timeout: 7 days of inactivity
* Suspended users lose access immediately

---

## Status

The app is currently **52.4% complete**. In-progress features include:

* Ticket search and filtering
* Page locking by role
* Responsive refinements
