# Security and Environment Management Guidelines for CUE Artist Agency

## 1. Move Secrets and Business Logic to Edge Functions
- **Locate all API keys, tokens and sensitive values** in your React front-end (e.g., `.env`, `/src` code). Any keys embedded in the client can be exposed.
- **Store sensitive values** in Lovable’s secret manager or environment variables. Reference them in edge functions rather than in client code.
- **Migrate business logic** (form validation, email notifications, database writes) into Supabase edge functions written in TypeScript. The client should only call these functions; it should not perform or trust validation alone.
- **Review third-party library usage** to ensure no credentials are exposed.

## 2. Implement Row-Level Security (RLS) and Proper Authentication
- **Enable RLS** on all Supabase tables, especially for bookings and roster submissions.
- **Define policies** so that only:
  - Admins (e.g., role = 'admin') can read and write bookings and join-roster applications.
  - Artists can read their own profile data (if editing is allowed).
  - Clients can only insert bookings; they should not read other clients’ data.
- **Add a `role` column** to your `users` table to differentiate admin, artist and client roles.
- **Use Supabase’s authentication** service; store JWT tokens securely. Validate tokens and roles within edge functions; never trust client-side checks.

## 3. Run the Security Checker
- In the Lovable project dashboard, locate the built-in **Security checker** tool.
- Run the tool and review each issue it reports, such as unused secrets, missing environment variables, or open RLS policies.
- Fix any flagged issues immediately. Document the changes you make for future reference.

## 4. Manage Environment Variables (Self-Hosting or Cloud)
- **Avoid hard-coded values** in your front-end. Use environment variables (via `.env` and `supabase/config.toml`) for Supabase API keys, URLs and other secrets.
- If migrating to your own Supabase instance:
  - Create a new Supabase project and note the `projectId`, `anon` key and `url`.
  - Update `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` in your `.env` file.
  - Update `supabase/config.toml` with the new `projectId` and `api_key`.
  - Re-deploy your app to ensure the new settings take effect.
- Use Lovable’s secret manager to store these variables rather than committing them to Git.

## 5. Pin Stable Versions and Manage Git
- Every time you finish a functional change (e.g., domain consolidation, Knowledge file update, security fix), create a **version tag or pin** in Lovable’s Git integration. Use descriptive commit messages to document the change.
- If an issue arises, use Lovable’s version comparison to diff between the last working version and the current one to locate the problem.
- Avoid creating branches unless you understand Git workflows; always switch back to `main` before deleting a branch in Lovable.

## 6. Test User Flows and Set Up Monitoring
- **Test as an anonymous user:** Navigate all public pages and submit the booking and join-roster forms. Ensure forms validate correctly and show success messages.
- **Test as an admin:** Log in, view submitted bookings and roster applications, and publish a blog post. Confirm that permissions restrict what each role can see/edit.
- **Fix any errors or UX issues** before deploying.
- **Set up uptime and performance monitoring** via Lovable’s built-in tools or a third-party service (e.g., UptimeRobot). Configure alerts for downtime and high response times.

## 7. Plan Content and Backlinks
- Develop a content calendar for your blog: topics might include event planning tips, artist features, DJ culture trends and behind-the-scenes stories.
- Aim to publish at least two high-quality posts per month. Use descriptive titles, meta descriptions and structured data for SEO.
- Pursue backlinks by reaching out to industry blogs, event organisers and music publications for guest posts or interviews. High-quality backlinks from authoritative sites boost search rankings.
