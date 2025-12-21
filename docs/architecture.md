Greetings everypne this is the folder structue and file names you are supposed to follow 

CampusOr/
│
├── README.md
├── .gitignore
├── package.json                # root scripts (lint, format, etc.)
├── contributors/
│   └── vaidik.md               # contributor profiles
│
├── frontend/                   # Next.js PWA client
│   ├── package.json
│   ├── next.config.js
│   ├── public/
│   │   ├── icons/
│   │   └── images/
│   │
│   └── src/
│       ├── app/                # Next.js App Router
│       │   ├── layout.tsx
│       │   ├── globals.css
│       │   │
│       │   ├── (routes)/
│       │   │   ├── landing/
│       │   │   │   └── page.tsx
│       │   │   ├── login/
│       │   │   │   └── page.tsx
│       │   │   ├── dashboard/
│       │   │   │   └── page.tsx
│       │   │   ├── queues/
│       │   │   │   └── page.tsx
│       │   │   └── kiosk/
│       │   │       └── page.tsx
│       │
│       ├── components/
│       │   ├── ui/              # buttons, modals, inputs
│       │   ├── queue/           # queue list, token cards
│       │   ├── charts/          # admin analytics
│       │   └── navbar/
│       │
│       ├── context/
│       │   └── AuthContext.tsx
│       │
│       ├── hooks/
│       │   └── useAuth.ts
│       │
│       ├── lib/
│       │   ├── api.ts           # fetch / axios wrapper
│       │   └── websocket.ts
│       │
│       ├── service-workers/
│       │   └── sw.js            # PWA offline support
│       │
│       └── types/
│           └── frontend.d.ts
│
├── backend/                    # Express + MongoDB API
│   ├── package.json
│   ├── tsconfig.json
│   └── src/
│       ├── app.ts              # express app
│       ├── server.ts           # server bootstrap
│       │
│       ├── config/
│       │   ├── db.ts           # MongoDB connection
│       │   └── env.ts
│       │
│       ├── middlewares/
│       │   ├── auth.middleware.ts
│       │   ├── error.middleware.ts
│       │   └── rateLimit.middleware.ts
│       │
│       ├── routes/
│       │   └── index.ts
│       │
│       ├── modules/
│       │   ├── auth/
│       │   │   ├── auth.routes.ts
│       │   │   ├── auth.controller.ts
│       │   │   └── auth.service.ts
│       │   │
│       │   ├── queue/
│       │   │   ├── queue.model.ts
│       │   │   ├── queue.routes.ts
│       │   │   ├── queue.controller.ts
│       │   │   └── services/
│       │   │       └── token.service.ts
│       │   │
│       │   ├── admin/
│       │   │   ├── admin.routes.ts
│       │   │   └── admin.controller.ts
│       │   │
│       │   └── notifications/
│       │       ├── email.service.ts
│       │       └── whatsapp.service.ts
│       │
│       ├── server/
│       │   └── socket.ts       # Socket.IO handlers
│       │
│       └── utils/
│           ├── jwt.ts
│           └── logger.ts
│
├── ml-service/                 # FastAPI ML service
│   ├── requirements.txt
│   └── app/
│       ├── main.py
│       ├── schemas.py
│       └── services/
│           └── predictor.py
│
├── shared/                     # shared contracts
│   ├── types/
│   │   ├── user.ts
│   │   ├── queue.ts
│   │   └── token.ts
│   └── schemas/
│       └── zod.ts
│
├── infra/
│   ├── docker-compose.yml
│   ├── docker/
│   │   ├── backend.Dockerfile
│   │   ├── frontend.Dockerfile
│   │   └── ml.Dockerfile
│   │
│   └── scripts/
│       └── seed.ts
│
└── docs/
    ├── architecture.md
    ├── api.md
    └── websocket-events.md
