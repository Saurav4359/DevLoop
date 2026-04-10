# DevEvent

DevEvent is a Next.js event listing app for developer meetups, conferences, and workshops. It shows featured events on the homepage and lets users open a detailed event page with the agenda, organizer info, and booking form.

## What it does

- Lists featured events on the home page
- Shows full event details on a dedicated event page
- Uses Route Handlers for fetching event records
- Includes a booking form UI on event pages
- Tracks a few user interactions with PostHog
- Anyone can create a new event
- Anyone can register for an event

## Stack

- Next.js 16
- React 19
- MongoDB with Mongoose
- Tailwind CSS
- Cloudinary for event images
- PostHog for analytics

## Project Structure

- `app/page.tsx` - homepage event list
- `app/events/[slug]/page.tsx` - event details page
- `app/api/events/route.ts` - event list and event creation route
- `app/api/events/[slug]/route.ts` - fetch one event by slug
- `database/event.model.ts` - event schema
- `database/booking.model.ts` - booking schema
- `lib/mongodb.ts` - MongoDB connection helper

## Local Setup

1. Install dependencies:

```bash
npm install
```

2. Add environment variables in `.env.local`:

```bash
MONGODB_URL=your_mongodb_connection_string
NEXT_PUBLIC_BASE_URL=http://localhost:3000
CLOUDINARY_URL=your_cloudinary_url
```

3. Start the dev server:

```bash
npm run dev
```

4. Open:

```bash
http://localhost:3000
```

## Useful Scripts

```bash
npm run dev
npm run build
npm run start
npm run lint
```

## Notes
- Event create and delete flows are planned for a later update
- Event creation and registration are open to all users
