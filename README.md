# OnlyHuman Forum

A forum application built with Next.js and Supabase, focused on providing a platform for verified human users.

## Features

- 🔐 User Authentication
  - Supabase Auth-based authentication
  - Access restricted to verified users only

- 📝 Post Features
  - Create new posts
  - View post list
  - View post details
  - Like functionality

- 💬 Comment System
  - Post comments on articles
  - Real-time comment display

- 🎨 Modern Interface
  - Responsive design
  - Clear navigation
  - Elegant typography

## Tech Stack

- **Frontend Framework**: Next.js 14
- **Styling Solution**: Tailwind CSS
- **Database**: Supabase (PostgreSQL)
- **Authentication**: Supabase Auth
- **Deployment**: Vercel

## Core Modules

### Home Page
- Display forum title and login button
- Show post list
- Each post shows title, publish time, and like count

### Post Detail Page
- Display full post content
- Like functionality
- Comment system
- Back to home button

### Create Post Page
- Post title input
- Post content editor
- Publish functionality

## Development Setup

1. Clone the project
```bash
git clone [repository-url]
```

2. Install dependencies
```bash
npm install
```

3. Environment Variables
Create `.env.local` file and add the following variables:
```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. Start development server
```bash
npm run dev
```

## Database Structure

### posts table
- id: UUID
- title: text
- content: text
- nullifier_hash: text
- created_at: timestamp
- likes: integer

### comments table
- id: UUID
- post_id: UUID (foreign key)
- content: text
- nullifier_hash: text
- created_at: timestamp

### likes table
- id: UUID
- post_id: UUID (foreign key)
- nullifier_hash: text
- created_at: timestamp

## Contributing

Pull requests and issues are welcome to help improve the project.

## License

MIT License
