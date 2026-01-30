# AI Content Generation Service - Backend

## Setup

1. Install dependencies:
```bash
npm install
```

2. Configure environment variables:
```bash
cp .env.example .env
# Edit .env with your actual values
```

3. Build and run:
```bash
# Development
npm run dev

# Production
npm run build
npm start
```

## Environment Variables

- `PORT`: Server port (default: 3001)
- `FIREBASE_PROJECT_ID`: Firebase project ID
- `FIREBASE_PRIVATE_KEY`: Firebase service account private key
- `FIREBASE_CLIENT_EMAIL`: Firebase service account email
- `ZAI_API_KEY`: Z.ai API key
- `JWT_SECRET`: JWT secret key
- `FRONTEND_URL`: Frontend URL for CORS

## API Endpoints

### Auth
- POST /api/auth/register
- POST /api/auth/login

### Content
- POST /api/content/generate
- GET /api/content/history
- GET /api/content/:id

### Templates
- GET /api/templates
- POST /api/templates

### Export
- POST /api/export/blog
- POST /api/export/social

## Deployment to Production

### Firebase Setup
1. Create a Firebase project
2. Enable Firestore Database
3. Create a service account and download JSON key
4. Set environment variables from the service account

### Vercel Deployment
1. Push code to GitHub
2. Import project in Vercel
3. Set environment variables in Vercel dashboard
4. Deploy

### Environment Variables for Production
```
NODE_ENV=production
PORT=3001
FIREBASE_PROJECT_ID=your-production-project-id
FIREBASE_PRIVATE_KEY=your-production-private-key
FIREBASE_CLIENT_EMAIL=your-production-client-email
ZAI_API_KEY=your-production-api-key
JWT_SECRET=your-production-jwt-secret
FRONTEND_URL=https://your-domain.vercel.app
```
