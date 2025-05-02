MyRestro Website Documentation
Live Demo: https://agmarestorant.netlify.app/

**1. Code Structure Overview
 
Key Components:
1.	Header & Navigation:
o	Logo (<a href="#" class="logo"> with AgmaLogo.png).
o	Mobile-responsive menu toggle (data-nav-toggler attributes).
o	Navigation links (#home, #menu, #about anchored to sections).
2.	Hero Slider:
o	Auto-rotating image carousel (<ul class="hero-slider">).
o	Preloaded images (<link rel="preload" as="image" ...> in <head>).
3.	Sections:
o	Services: Breakfast/Appetizers/Drinks cards (<section class="service">).
o	About Us: Story section with parallax effects (data-parallax-item).
o	Menu: Grid of dishes with prices (<section class="menu" id="menu">).
o	Reservation: Interactive booking form (<section class="reservation">).
o	 
4.	Footer:
o	Newsletter subscription form.
o	Social media links .
 

________________________________________
2. Deployment (Netlify)
Step 1: Prepare Code
•	Ensure all assets (images, CSS, JS) are in the assets/ folder.
•	Update contact details in:
html
Copy
Download
Run
<!-- In Topbar -->
<a href="tel:+254743418889">+254 743418889</a>
<a href="mailto:booking@restaurant.com">booking@restaurant.com</a>
Step 2: Deploy via Netlify
1.	Drag-and-Drop:
o	Zip your project folder → Upload to Netlify.
2.	Git Deployment:
o	Connect your GitHub/GitLab repo → Set build settings:
	Build command: Leave empty.
	Publish directory: / (root).
Step 3: Configure Netlify Forms
Add these attributes to the reservation form (<form>):
html
Copy
Download
Run
<form action="/" method="POST" data-netlify="true">
  <input type="hidden" name="form-name" value="reservation"
</form>
•	Submissions will appear in Netlify’s Forms tab.
________________________________________
**3. Testing Guidelines
A. Functional Tests
1.	Navigation:
o	Test all anchor links (e.g., #home, #menu).
o	Verify mobile menu toggle (data-nav-toggler).
2.	Hero Slider:
o	Confirm auto-rotation and manual navigation (prev/next buttons).
3.	Reservation Form:
o	Submit test entries → Check Netlify Forms dashboard.
B. Performance Tests
1.	Lighthouse Audit:
o	Run in Chrome DevTools → Optimize images if score < 90.
2.	Responsiveness:
o	Test on mobile (e.g., iPhone SE) and tablet breakpoints.
________________________________________
**4. Customization Guide
A. Update Content
1.	Logo:
AgmaLogo.png in:
html
Copy
Download
Run
<img src="./assets/images/AgmaLogo.png" width="50" height="50" alt="...">
2.	Menu Items:
Edit dish cards in the <!-- #MENU --> section:
html
Copy
Download
Run
<li>
  <div class="menu-card">
    <img src="./assets/images/menu-1.png" alt="Greek Salad">
    <h3 class="title-3">Greek Salad</h3>
    <span class="span title-2">$25.50</span>
  </div>
</li>
B. Modify Styles
•	Override CSS variables in style.css:
css
Copy
Download
:root {
  --background: #0c0c0c; /* Example variable */
}
________________________________________
**5. Troubleshooting
Issue	Solution
Images not loading	Confirm paths (e.g., ./assets/images/...).
Form not submitting	Add data-netlify="true" to <form>.
Mobile menu not closing	Check data-nav-toggler JS logic in script.js.


6. Credits & License
•	Design Template: Adapted from codewithsadee.
•	Icons: IonIcons.
•	License: Free for personal use. Attribute the original author.
________________________________________
 My site is live at https://agmarestorant.netlify.app/

