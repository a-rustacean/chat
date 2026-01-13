# Chat 💬

A modern, real-time chat application built with Next.js, featuring guild/server systems, real-time messaging, and a beautiful user interface.

## ✨ Features

- **Real-time Messaging**: Instant message delivery powered by Pusher
- **Guild/Server System**: Create or join private chat servers with invite codes
- **Rich Message Types**:
  - Text messages with emoji support
  - File and image uploads
  - Interactive polls with real-time voting
- **User Authentication**: Secure authentication with Clerk
- **Presence System**: See who's online in real-time
- **Message Management**:
  - Edit your messages
  - Delete messages (owners can delete any message in their guild)
  - Message read receipts
- **Theme Support**: Light and dark mode toggle
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🚀 Tech Stack

- **Framework**: [Next.js 14](https://nextjs.org/) (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Database**: SQLite with [Drizzle ORM](https://orm.drizzle.team/)
- **Real-time**: [Pusher](https://pusher.com/)
- **Authentication**: [Clerk](https://clerk.com/)
- **State Management**: Zustand
- **UI Components**:
  - Heroicons
  - Lucide React
  - Emoji Picker React

## 📋 Prerequisites

- Node.js 18+
- npm or yarn or pnpm
- A Clerk account (for authentication)
- A Pusher account (for real-time features)

## 🛠️ Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/a-rustacean/chat.git
   cd chat
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Set up environment variables**:

   Create a `.env` file in the root directory with the following variables:

   ```env
   # Database
   DATABASE_URL="your_database_url_here"

   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key

   # Pusher (Real-time)
   PUSHER_APP_ID=your_pusher_app_id
   NEXT_PUBLIC_PUSHER_KEY=your_pusher_key
   PUSHER_SECRET=your_pusher_secret
   NEXT_PUBLIC_PUSHER_CLUSTER=your_pusher_cluster
   ```

4. **Set up the database**:
   ```bash
   npm run db:push
   ```

## 🏃‍♂️ Development

Run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## 📜 Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build the application for production
- `npm run start` - Start the production server
- `npm run lint` - Run ESLint
- `npm run db:push` - Push database schema changes
- `npm run db:studio` - Open Drizzle Studio (database GUI)
- `npm run db:generate` - Generate database migrations

## 📁 Project Structure

```
chat/
├── app/                    # Next.js App Router
│   ├── api/               # API routes
│   ├── chat/              # Chat page
│   ├── sign-in/           # Sign-in page
│   ├── sign-up/           # Sign-up page
│   └── page.tsx           # Landing page
├── components/            # React components
├── db/                    # Database schema and configuration
│   ├── schema.ts          # Drizzle schema definitions
│   └── index.ts           # Database instance
├── lib/                   # Utility functions
├── store/                 # Zustand state management
├── public/                # Static assets
└── middleware.ts          # Next.js middleware (auth protection)
```

## 🗄️ Database Schema

The application uses SQLite with the following main tables:

- **Messages**: Store all chat messages with support for different types
- **Guilds**: Server/guild information
- **GuildMembers**: User memberships in guilds
- **Rooms**: Chat rooms within guilds

## 🌐 Deployment

### Deploy on Vercel

The easiest way to deploy this application is using [Vercel](https://vercel.com):

1. Push your code to a GitHub repository
2. Import the project to Vercel
3. Add your environment variables in the Vercel dashboard
4. Deploy!

The `vercel-build` script will automatically push database changes and build the application.

## 🔐 Environment Setup Details

### Clerk Setup

1. Create an account at [clerk.com](https://clerk.com)
2. Create a new application
3. Copy your publishable key and secret key to `.env`

### Pusher Setup

1. Create an account at [pusher.com](https://pusher.com)
2. Create a new Channels app
3. Copy your app credentials to `.env`
4. Enable client events in your Pusher dashboard

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Dilshad**

- GitHub: [@a-rustacean](https://github.com/a-rustacean)

---

Built with ❤️ using Next.js and modern web technologies.
