# Master Video Downloader

यह रिपॉज़िटरी AI-enabled वीडियो डाउनलोडर SaaS के लिए planning + implementation की foundation के रूप में तैयार की जा रही है।

## Current Status
- Initial Hindi product blueprint added (MVP + Pro roadmap + Admin panel + Auth flow)
- Next step: frontend/backend scaffold implementation

## Product Blueprint
पूरा डॉक्यूमेंट यहाँ देखें:
- `docs/website-blueprint-hi.md`

## Proposed Stack
- Frontend: Next.js + TypeScript + Tailwind
- Backend: Node.js (NestJS/Express) + yt-dlp worker
- DB: PostgreSQL + Prisma
- Queue: Redis + BullMQ
- Auth: NextAuth/Auth.js (or JWT)
- Storage: S3-compatible storage

## Roadmap (Short)
1. Auth (Signup/Signin)
2. Video download flow + quality selection
3. Admin panel
4. Pro subscriptions
5. AI tools
