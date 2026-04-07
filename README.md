# 🔬 WOOD Lab Website - Maintenance Guide

This website is a single-page HTML/CSS site hosted on GitHub Pages. Use this guide to update your content.

---

## 1. Edit Research Summary
* **Location**: Find `<section id="research-summary">`.
* **Action**: Edit the text inside the `<p>` tags. 
* **Tip**: If you want to add a photo here, use: `<img src="filename.jpg" style="width:100%; border-radius:8px; margin-bottom:20px;">`.

## 2. Add a New Lab Member
* **Location**: Find `<section id="members">`.
* **Action**: Copy an existing `<div class="member-card">` block and paste it below the others.
* **Update**: 
    - `src="your-photo.jpg"`: Ensure the image is uploaded to your GitHub folder.
    - `href="URL"`: Update the Google Scholar link.
    - `target="_blank"`: Ensure this is kept so links open in new tabs.

## 3. Add New Publications (DOIs)
The list is automated. You do not need to write HTML for each paper.
* **Location**: Scroll to the bottom of `index.html` to the `<script>` section.
* **Action**: Add your new DOI string to the `doiArray` inside quotes, followed by a comma.
* **Example**: `"10.1038/s41467-022-28784-w",`

## 4. Move Members to Alumni
When a member leaves, move them to the "Previous Members" list:
1. **Delete** their `<div class="member-card">` from the main Members section.
2. **Location**: Find `<section id="previous-members">`.
3. **Action**: Add a new list item: 
   `<li><strong>Name</strong> - Role (Years) - Current Position</li>`

## 5. Add New AOB Cards
To keep the "Any Other Business" section organized, use the "Card" format:
* **Location**: Find `<section id="aob">`.
* **Action**: Paste this block for each news item:
```html
<div class="aob-card">
    <h3>News Title</h3>
    <p>Description of the event. You can add <a href="URL" target="_blank" class="perm-link">links</a> here.</p>
</div>