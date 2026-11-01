MALIK PROPERTIES website starter
=================================

Files:
- index.html: responsive BUY / SELL enquiry website with admin login/list.
- setup.sql: create the separate property_enquiries table and RLS policies.

Important setup before deployment:
1. In Supabase, open the project you want to use and run setup.sql in SQL Editor.
2. In index.html, replace:
   SUPABASE_URL = "PASTE_YOUR_SUPABASE_PROJECT_URL"
   SUPABASE_ANON_KEY = "PASTE_YOUR_SUPABASE_ANON_KEY"
   with the project's Project URL and anon/publishable key.
   Never put a service_role key in a public website.
3. In Supabase Authentication, create your admin user and disable public sign-ups.
4. Deploy index.html to a NEW Netlify site for MALIK PROPERTIES (keep the existing MALIK ONLINE SERVICES site unchanged).
5. Test one BUY enquiry, one SELL enquiry, and admin login.

Security note:
The SQL policy lets anonymous visitors INSERT only; anonymous users cannot SELECT enquiries.
The admin read/update/delete policies are for authenticated users. For a production setup with multiple users,
tighten these policies to a specific admin identity/email before inviting any other authenticated users.
