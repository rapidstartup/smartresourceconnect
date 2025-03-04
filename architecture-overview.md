# Architecture Overview

Smart Resource Connect utilizes a modern, cloud-based architecture designed for scalability, ease of deployment, and global accessibility. It follows a decoupled Jamstack approach, separating frontend user interfaces from backend data services, ensuring fast performance and robust security.

## Key Technologies

- **Frontend:** Next.js (React)
- **Deployment & Hosting:** Netlify
- **Code Repository:** GitHub
- **Design System:** Tailwind CSS
- **HTTP Client:** Axios
- **Backend Database & Authentication:** Supabase
- **CDN and Security:** Cloudflare 

## Matching Algorithm Implementation

- **Option A**: SQL function in Supabase for filtering, scoring, and ordering.
- **Option B**: Serverless function (Node/TypeScript) to compute scores and return top matches. 