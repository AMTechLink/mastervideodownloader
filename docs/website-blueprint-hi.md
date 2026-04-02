# AI-Powered Fusion Media Video Downloader — Blueprint (Hindi)

## 1) Product Vision
ऐसी वेब ऐप बनानी है जहाँ यूज़र अलग-अलग प्लेटफ़ॉर्म की **public videos** का लिंक पेस्ट करके अच्छी क्वालिटी में डाउनलोड कर सकें।
भविष्य में **Pro प्लान** और **AI टूल्स** जोड़ने हैं, और आपके पास पूरा कंट्रोल देने के लिए **Admin Panel** भी होना चाहिए।

---

## 2) User Roles
1. **Guest**
   - बिना अकाउंट के सीमित डाउनलोड
2. **User (Free)**
   - साइनअप/साइनइन के बाद अधिक फीचर्स
3. **User (Pro)**
   - हाई-स्पीड/बैच/AI फीचर्स
4. **Admin**
   - यूज़र, पेमेंट, फीचर्स, मॉडरेशन, एनालिटिक्स मैनेज

---

## 3) Core Features (MVP)

### A. Authentication
- Signup (Email + Password)
- Signin
- Forgot Password
- Email verification (optional but recommended)
- JWT/session based login

### B. Video Download Flow
- URL input box
- URL validation + platform support check
- Quality options (360p, 720p, 1080p, best)
- Audio-only (mp3/m4a) option
- Download progress indicator
- Download history (logged in users)

### C. Admin Panel
- Dashboard: total users, downloads/day, success/fail ratio
- User management: block/unblock, role change (free/pro/admin)
- Content moderation: suspicious URLs logs
- System settings: max file size, queue limit, rate limits
- Plans/pricing control (for future Pro)

### D. Basic Security
- Rate limiting
- Bot protection (CAPTCHA)
- Input validation/sanitization
- Logging + audit trail (admin actions)

---

## 4) Pro Version Roadmap

### Phase-2 (Monetization)
- Stripe/Razorpay integration
- Monthly/yearly plans
- Usage limits by plan
- Invoice + billing history

### Phase-3 (AI Tools)
- Auto title/description generation
- Smart tags/hashtags suggestion
- Language translation for captions
- Thumbnail enhancement suggestions
- Viral score / trend hints (advisory)

---

## 5) Suggested Tech Stack

### Frontend
- **Next.js (React + TypeScript)**
- TailwindCSS + shadcn/ui
- Zustand/Redux (optional)

### Backend API
- **Node.js (NestJS or Express + TypeScript)**
- yt-dlp worker service (isolated)
- Queue: Redis + BullMQ

### Database
- **PostgreSQL**
- Prisma ORM

### Auth
- NextAuth/Auth.js or custom JWT auth

### Storage
- S3-compatible object storage (Cloudflare R2 / AWS S3)

### Infra
- Docker
- Nginx reverse proxy
- CI/CD with GitHub Actions
- Monitoring: Sentry + Prometheus/Grafana (optional)

---

## 6) Compliance Notes (Important)
- केवल **publicly accessible** और legally permitted content ही allow करें
- Terms of Service + Privacy Policy + DMCA policy clearly publish करें
- Copyright takedown process रखें
- Platform-specific restrictions का सम्मान करें

---

## 7) Database Draft (High-level)
- `users`
- `roles`
- `subscriptions`
- `downloads`
- `download_jobs`
- `ai_usages`
- `admin_audit_logs`
- `settings`

---

## 8) API Draft (Sample)
- `POST /auth/signup`
- `POST /auth/signin`
- `POST /auth/forgot-password`
- `POST /downloads/create`
- `GET /downloads/history`
- `GET /admin/dashboard`
- `PATCH /admin/users/:id/role`
- `PATCH /admin/users/:id/status`
- `GET /admin/downloads/logs`

---

## 9) 30-Day Build Plan

### Week 1
- Auth + UI skeleton + DB schema

### Week 2
- Downloader worker + queue + progress tracking

### Week 3
- Admin panel + logs + role system

### Week 4
- Payments draft + polish + deployment + security hardening

---

## 10) Pricing Suggestion (Starter)
- **Free:** limited downloads/day, standard speed
- **Pro Lite:** higher limit + better quality options
- **Pro Plus:** fastest queue + batch + AI tool credits

---

## 11) Next Step for This Repo
अगर आप चाहें, अगले कमिट में मैं यह deliver कर सकता हूँ:
1. Next.js frontend scaffold
2. Auth pages (signup/signin/forgot password)
3. Downloader input UI + history page
4. Admin panel starter (dashboard + users table)
5. Backend starter with PostgreSQL + Prisma schema
