# Improvements & Upgrades — Pundit Studio

This document lists researched improvements and recommended features to enhance the portfolio/admin experience.

- Add server-backed storage for uploads
  - Use S3, Cloudinary, Supabase Storage, or similar for persistent hosting of images, PDFs and video files.
  - Keep client-side `dataUrl` as a temporary preview; save the uploaded file URL returned by the server to `resources[].url`.

- Authentication & access control
  - Replace the localStorage admin check with a secure backend authentication or integrate with OAuth (GitHub, Google) or a small username/password API.
  - Add admin roles (editor, viewer).

- Rich media handling
  - Auto-generate optimized image variants (webp, different sizes) via Cloudinary or an image CDN.
  - Transcode large videos or host on YouTube/Vimeo and embed links.
  - Allow drag-and-drop uploads, multiple-file uploads for projects.

- Structured project pages
  - Allow multiple gallery assets per project (ordered images, cover image, video), with captions and credit fields.
  - Add case-study metadata: client, year, deliverables, outcomes, links.

- Client intake improvements
  - Add required/optional fields, file attachments, and a simple intake workflow that produces a PDF summary.
  - Integrate with Notion/Google Drive or email notifications on new submissions.

- CMS-like editing & version history
  - Basic versioning for content changes (who changed what and when).
  - Preview changes before publishing.

- Performance & SEO
  - Pre-render project pages and add meta Open Graph tags for sharing.
  - Use lazy-loading images and video placeholders.

- UX improvements
  - Better validation on forms (emails, URLs, file types/sizes).
  - Inline image previews and lightbox for gallery items.
  - Bulk import/export of projects/resources (CSV/JSON).

- Analytics & contact management
  - Track submission counts and source pages.
  - Simple CRM view for leads collected via briefs.

- Suggested next steps for implementation
  1. Keep current local-first UX (dataUrl + localStorage) for quick setup and prototypes.
  2. Add a serverless endpoint for file uploads (e.g., Netlify Functions, Vercel, Supabase Edge) and swap local storage save to send resource metadata to the backend.
  3. Integrate light authentication to protect the admin route.

If you want, I can implement the drag-and-drop uploader, the multi-asset project model, or a simple serverless upload endpoint next—tell me which to start with.
