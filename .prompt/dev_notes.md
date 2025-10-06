**Prompt 1:**
"Requests to unify navbar/footer across pages (make resume nav match index/about, single-line footer)."

**AI output:**
HTML: unified navbar markup across pages — replaced differing nav blocks so index.html, about.html, and resume.html use the same structure and classes (Home, Projects, About, Resume, Contact). Each page keeps a manual class="active" on its matching link so the current page is highlighted.

CSS: added/updated styles in styles.css to make the navbar and footer consistent: .site-nav { display:flex; gap:1rem; align-items:center; } (consistent horizontal nav)
.site-nav .active { font-weight:600; border-bottom:2px solid var(--accent); }
.site-footer { display:flex; justify-content:space-between; align-items:center; gap:1rem; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; } (single-line footer on wide screens)
@media (max-width:600px) { .site-footer { flex-direction:column; white-space:normal; } } (wraps on small devices)

**Note on whether you accpected, modified, or rejected:**
I did accept the AI ouput for this prompt, but I also had to go in and modify the order of my footer to make my email display right after my phone number.

Prompt 2:
"I prefer that i can scroll down to see the full expand size of the project screenshot and add both images in for the first project."

AI output:
HTML: moved Project 1 description above images and added two images: project.png and images/project2.png (kept alt attributes).
CSS: added .project-full { object-fit: contain; max-height: 70vh; width: 100%; } so the image shows whole content and can be scrolled if tall.
Added slight bottom spacing between stacked images: .card img { margin-bottom: 0.75rem; }.
Files touched:
projects.html — reorder and add images for Project 1.
styles.css — .project-full and spacing rules.

**Note on whether you accpected, modified, or rejected:**
I accpted this AI output to change the size of my project screenshots to make sure it is fully visible for different window size. AI did a great job on answering my prompt and give me proper output that fulfills my request.

Prompt 3:
"Delete the repository but in the live demo place this link "https://r8rqdg.csb.app/index.html\" of my project to project 2."

AI output:
HTML: removed the repo button for the requested project card and updated the Live Demo anchor href to the supplied URL.
Accessibility: added rel="noopener noreferrer" and target="_blank" to external demo links.
Files touched
projects.html — removed repo link and updated Live Demo href.

**Note on whether you accpected, modified, or rejected:**
I also accepted this AI output, however, I need to modify the link myself becuase it was not able to redirect when I tested it out on the browsers.

**Overall Reflection (150-word):** 
Using AI saved me significant time on repetitive HTML/CSS edits, quick layout ideas, and generating accessible patterns (nav/footer unification, responsive gallery rules), allowing me to focus on content decisions and testing. AI made helpful, fast suggestions but occasionally produced inaccurate links, minor markup inconsistencies, and CSS comment/format issues that I caught and modified manually. To balance implementations and suggestions I treated AI as a coding partner: I validated every change and only accepted edits after verifying behavior and accessibility. When AI suggested structure or styles I adapted them to my site conventions and image urls, and I wrote final copy and link tests myself. This workflow kept development efficient while maintaining control over correctness, accessibility, and design originality. Overall, AI accelerated routine tasks and brainstorming but did not replace my own ideas and edits that ensure the final site was functional, visually appealing, and easy to navigate.
