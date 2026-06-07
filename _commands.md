## Create the project
```
npm create-next-app@latest --typescript --tailwind --eslint
```

## Install dependencies
```
npm install socket.io socket.io-client react-hot-toast bcryptjs jsonwebtoken cookie zod
npm install @types/bcryptjs @types/jsonwebtoken @types/cookie
```

## Project structure
```
realtime-chat/
├── .env.local
├── package.json
├── server.js                 # Custom Next server + Socket.io
├── next.config.mjs
├── tailwind.config.ts
├── postcss.config.mjs
├── tsconfig.json
├── middleware.ts
├── app/
│   ├── layout.tsx
│   ├── page.tsx              # Login page
│   ├── chat/
│   │   ├── page.tsx          # Chat lobby & room selector
│   │   └── [roomId]/
│   │       └── page.tsx      # Individual chat room
│   ├── api/
│   │   └── auth/
│   │       └── route.ts      # Login endpoint
│   └── globals.css
├── components/
│   ├── ChatRoom.tsx
│   ├── MessageList.tsx
│   ├── MessageInput.tsx
│   ├── Sidebar.tsx
│   ├── Navbar.tsx
│   └── OnlineUsers.tsx
├── lib/
│   ├── auth.ts
│   ├── db.ts                 # In‑memory store for messages
│   └── socket.ts             # Socket.io client singleton
├── hooks/
│   └── useSocket.ts
├── types/
│   └── index.ts
└── public/                   # (optional favicon)
```
