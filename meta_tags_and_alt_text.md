# Meta Tags & Alt Text Recommendations for CUE Artist Agency

Below are recommended HTML `<title>` and `<meta name="description">` tags for each public page on the CUE Artist Agency site, along with general guidance on heading structure and alt text.

## Home Page (`/`)
```html
<title>CUE Artist Agency | Book Elite DJ Talent for Clubs, Festivals & Events</title>
<meta name="description" content="CUE Artist Agency connects clubs, festivals and events with elite DJs across the U.S. Browse our artists and book top talent for your next event.">
```
- **Heading hierarchy:** Use a single `<h1>` element for the main tagline (e.g., “Book Elite DJ Talent”) and `<h2>`/`<h3>` for secondary sections.
- **Alt text:** Describe images clearly, e.g., `alt="DJ performing at a nightclub"` or `alt="CUE Artist Agency logo"`.

## Artists Page (`/artists`)
```html
<title>Our DJs | CUE Artist Agency – Elite DJ Roster</title>
<meta name="description" content="Explore our curated roster of elite DJs at CUE Artist Agency. Listen to mixes and book the perfect talent for your club, festival or corporate event.">
```
- **Headings:** `<h1>` could be “Our DJs” followed by `<h2>` elements for genres or categories.
- **Alt text:** Each artist’s photo should include alt text with their stage name and genre, e.g., `alt="DJ Luna – house music DJ"`.

## Blog Page (`/blog`)
```html
<title>Blog | CUE Artist Agency – News & DJ Culture</title>
<meta name="description" content="Read articles about DJ culture, music trends, event planning and CUE Artist Agency news. Stay informed and inspired.">
```
- **Headings:** Use `<h1>` for “Blog” and `<h2>` for individual post titles.
- **Alt text:** Featured images on the blog should describe the content, e.g., `alt="DJ mixing tracks at a festival"`.

## Contact Page (`/contact`)
```html
<title>Contact Us | CUE Artist Agency</title>
<meta name="description" content="Get in touch with CUE Artist Agency for bookings or general inquiries. Our team is ready to help you secure the perfect DJ for your event.">
```
- **Headings:** `<h1>` could be “Contact Us”; `<h2>` for “Booking Enquiries”, “General Questions”, etc.
- **Alt text:** If there are photos or icons, use alt text like `alt="phone icon"` or `alt="envelope icon"`.

## About Page (`/about`)
```html
<title>About CUE Artist Agency – National DJ Booking Agency</title>
<meta name="description" content="Learn more about CUE Artist Agency, our mission, and our commitment to connecting elite DJs with clubs, festivals, and events across the U.S.">
```
- **Headings:** `<h1>` could be “About Us” and `<h2>` for sub‑sections such as “Our Mission”, “Our Team”, and “Our Story”.
- **Alt text:** Use descriptive alt text for team photos or event images.

## Join Roster Page (`/join-roster`)
```html
<title>Join Our Roster | CUE Artist Agency</title>
<meta name="description" content="Are you an elite DJ looking for representation? Submit your application to join the CUE Artist Agency roster and perform at top events nationwide.">
```
- **Headings:** `<h1>` for “Join Our Roster” and `<h2>` for “Why Join?”, “Requirements”, “Application Form”.
- **Alt text:** For images of DJ equipment or performance shots, use text such as `alt="DJ equipment setup"`.

### General Guidelines
- **Robots & sitemap:** Keep the existing `robots.txt` and `sitemap.xml` configuration; they already reference your sitemap.
- **Social tags:** Consider adding Open Graph and Twitter Card tags to improve social sharing, for example:
  ```html
  <meta property="og:title" content="CUE Artist Agency – Elite DJ Talent">
  <meta property="og:description" content="Book elite DJs for your club, festival or corporate event.">
  <meta property="og:image" content="https://cueartistagency.com/assets/og-image.jpg">
  ```
- **Structured data:** Implement Schema.org `Organization` and `Event` markup to enhance search appearance.
