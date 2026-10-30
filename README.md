# Swapnil Chowdhury — academic portfolio

A build-free, single-page portfolio. All styling and behavior are in index.html. The supplied CV is included unchanged as assets/cv.pdf.

## Deploy on GitHub Pages

1. Extract this ZIP. Upload index.html, assets/, papers/, and this README to the root of a GitHub repository. Do not upload the ZIP itself or leave index.html inside an extra enclosing folder.
2. In the repository, open Settings → Pages. Under Build and deployment, select Deploy from a branch, then main and / (root), and save.
3. Open the URL displayed by GitHub after deployment finishes. Repository availability and Pages eligibility depend on your GitHub account and repository settings.
4. Test navigation, the mobile menu, and both CV actions on the live URL. View CV opens a normal PDF tab; Download CV uses the browser download attribute. Browser settings can affect PDF handling.

## Files

- index.html — complete website with inline CSS and JavaScript.
- assets/cv.pdf — original supplied CV.
- assets/profile.jpg — not supplied; add your real photograph here. The page currently displays an intentional initials design and automatically replaces it when this image loads. A missing image request is expected until you supply it; no broken image is displayed.
- papers/ — ready for your paper PDFs; none were supplied.

## Update through GitHub

Open index.html in the repository and choose Edit (pencil). Comments mark each section. Commit the changes and GitHub Pages republishes the site.

- Photo: upload a JPEG named assets/profile.jpg. A portrait-oriented crop is recommended. Its object-fit: cover style fills the arched frame; adjust object-position if necessary.
- CV: replace assets/cv.pdf using the same filename. Both viewing and download links will use the new file.
- Publications: copy an existing article.publication block. Update every author, title, venue, year, and status. Do not label accepted work as published until confirmed.
- Paper PDFs: upload an authorized copy to papers/ using a descriptive lowercase filename with hyphens, then add the following link inside its matching publication entry. Replace the sample filename with the exact uploaded filename, including case:

```html
<a class="button" href="papers/your-actual-paper-filename.pdf"
   target="_blank" rel="noopener"
   aria-label="View Paper (PDF, opens in a new tab)">View Paper ↗</a>
```

Only add that link after the PDF exists. Normal PDF links let visitors use their browser's viewer. No paper buttons are currently displayed because no paper PDFs were supplied.

## Content provenance and missing items

Content is based only on Swapnil_Chowdhury__CV.pdf. Research-interest summaries are synthesized from the documented work; no PhD admission, new affiliation, or future commitment has been invented. Research results are attributed to the CV because evaluation details are not supplied.

- Missing: real profile photograph and individual paper PDFs.
- Not supplied: project repository URLs, a Google Scholar or ORCID profile, a detailed contribution summary for the accepted humor paper, and specific future research plans. These were not invented.
- Email, phone, GitHub, LinkedIn, and three DOI URLs were extracted from the CV, including embedded PDF links. External ownership and live availability could not be independently verified. DOI URLs were retained exactly as supplied.
- Publication status follows the CV: three published entries and one accepted/to-appear MIET 2026 entry. Reconfirm status when updating the site.

## Verification

Passed static checks: unique section IDs, all section navigation targets, relative local CV paths, original CV byte integrity, PDF readability, explicit new-tab protections, download attribute, and JavaScript syntax. Mobile-menu event logic was exercised with a small DOM stub (open/close, Escape, link selection, outside click); active-section selection was exercised with simulated scroll positions.

Designed with responsive breakpoints, a no-JavaScript navigation fallback, a skip link, visible focus styles, semantic headings, and reduced-motion support. Core foreground/background color pairs meet WCAG AA normal-text contrast.

Browser QA remains unverified: the environment's preview relay was unavailable. Desktop/mobile rendering, actual keyboard focus behavior, PDF viewing, and download behavior need a final check in a browser after deployment. No external fonts, packages, build step, backend, or analytics are required.
