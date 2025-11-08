# Knowledge File for CUE Artist Agency

## Product Vision
CUE Artist Agency is a national DJ booking agency.  Our mission is to connect premier DJs with clubs, festivals, corporate events, and private functions across the United States.  We curate elite talent and provide bespoke booking services that elevate live experiences and deliver unforgettable music for audiences.

## User Journeys
### Client Journey (booker)
1. **Home → Artists → Booking form**
   - A visitor arrives on the home page, learns about the agency’s ethos, and sees highlighted DJs.
   - They navigate to the **Artists** page to explore the roster, read profiles and listen to sample mixes.
   - After choosing a DJ or narrowing down options, they click **Book Now**/booking form.
   - They fill out event details (date, venue, budget, contact info), submit the request, and receive confirmation that an agent will follow up.

### Artist Journey (applicant)
1. **Home → Join Roster**
   - A DJ visits the home page, understands the agency’s brand and sees successful artists.
   - They click on **Join Roster** to learn about requirements and benefits.
   - They fill out the **Join Roster** form, providing their stage name, genre, links to mixes, social profiles and experience.
   - An admin reviews the submission; if accepted, the DJ is added to the roster and receives onboarding instructions.

## Roles
- **Admin** – Manages site content, artists and bookings; approves roster applications; updates blog posts; configures settings and security; monitors analytics and site health.
- **Artist** – DJ or performer featured on the roster; may update their profile (bio, images, mixes) and respond to booking enquiries (depending on workflow).
- **Client** – Event organiser or booker who browses the site, submits booking requests, reads blog articles and may subscribe to a newsletter.

## Design System
- **Typography** – Use modern sans‑serif fonts (e.g., Montserrat or Lato) for headings and body text; maintain strong hierarchy with large H1 headlines and smaller H2/H3 sub‑headings.
- **Colour palette** – 
  - **Black** (#000000) for backgrounds and main sections.
  - **Gold** (#D4AF37) or similar metallic hue for accents, calls to action and highlights.
  - **White** (#FFFFFF) or off‑white for text on dark backgrounds and negative space.
- **Components & Layout** – 
  - A fixed navigation bar with clear links (Home, About, Artists, Blog, Contact, Join Roster) and a prominent **Book Now** button.
  - Hero section with large headline (“Book Elite Talent”) and background image/video, plus CTA button.
  - **Artist cards** featuring a DJ’s photo, name, genre and a brief description with links to book.
  - **Forms** for booking and joining the roster with validation (required fields, error states).
  - **Blog post layout** with featured image, title, date, author, categories and tag list.
  - **Footer** with social media links, newsletter signup and legal notices.

## Key Functionality
- **Booking Form Handling** – Collects event details, desired artist(s), date, venue, contact information and additional requirements.  Validation should occur server‑side via a Supabase edge function.  Upon submission, store the request in the database and optionally send email notifications to admins.
- **Artist Roster Management** – Displays a searchable and filterable list of artists.  Admins can add or edit artist profiles, including photos, genres, biographies and audio samples.  Prospective artists submit a **Join Roster** application through a form; submissions are stored in the database and require admin review.
- **Blog Posts** – The site includes a blog section to share event recaps, artist spotlights and industry news.  Admins can create, edit and publish posts.  Each post should include meta title and description, categories, tags, featured image and alt text.
- **Contact Page** – Provides contact details and a simple contact form for general enquiries.
