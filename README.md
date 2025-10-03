Toko - Artist Website

This is the official source code for the personal artist website for Toko. It's a minimalist, single-page-focused portfolio designed to be clean, atmospheric, and easy to navigate. The site is built with simple HTML and styled with Tailwind CSS, making it lightweight and fully responsive.
Live Site: https://intokowetrust.dev/ (You can update this link to your final URL)
Features
	•	Featured Video: Prominently displays a YouTube video at the top of the page.
	•	Music Grid: A responsive 2x2 grid showcasing key musical projects with album art and external links.
	•	Playlist Music Player: An interactive audio player in the footer that cycles through a customizable playlist of MP3s.
	•	Blurred Background: Uses a custom, atmospheric background image with a blur effect and a dark overlay to ensure text is readable.
	•	External Links: Includes a clean footer with links to major streaming and social media platforms.
	•	Multiple Pages: Includes separate, linked pages for a Patreon embed and a contact form.
	•	GitHub Pages Ready: Designed to be easily deployed and hosted for free on GitHub Pages.
File Structure
The project is organized into a few key files. To ensure the site works correctly, all these files should be in the root of your GitHub repository.
/ ├── index.html       (The main landing page with all content) ├── contact.html     (The contact form page) ├── patreon.html     (The Patreon embed page) ├── IMG_1937.jpg     (The background image) └── *.mp3            (Your music files for the playlist, e.g., 'ocean paradise.mp3') 
How to Customize
You can easily update almost any part of the website by editing the index.html file.
1. Change the Featured YouTube Video
	1	Find the <!-- YouTube Video Embed --> section.
	2	Replace the video ID (NVy2BuU0rjY) in the src URL with the ID of your new video.
<!-- end list -->
<iframe class="w-full h-full" src="[https://www.youtube.com/embed/YOUR_VIDEO_ID_HERE](https://www.youtube.com/embed/YOUR_VIDEO_ID_HERE)" ...></iframe> 
2. Update the Music Grid (Links & Images)
	1	Find the <!-- Main Content: Album/Music Grid --> section.
	2	There are four grid items. To change one, edit its href attribute for the link and the src attribute of the <img> tag for the album art.
<!-- end list -->
<!-- Grid Item 1 --> <a href="YOUR_NEW_MUSIC_LINK" target="_blank" ...>     <div ...>         <img src="YOUR_NEW_ALBUM_ART_URL" ...>     </div>     <p ...>Latest Single</p> <!-- You can also change the title here --> </a> 
3. Customize the Music Playlist
This is the most important part for keeping your music player fresh.
	1	Scroll to the bottom of index.html and find the <script> section.
	2	Locate the const playlist = [...] array.
	3	You can add, remove, or edit the objects in this array. Each object represents one song.
	4	Important: Make sure the filename in src exactly matches the name of the MP3 file you upload to GitHub.
<!-- end list -->
const playlist = [     {         title: 'New Song Title',         artist: 'Toko',         artwork: 'URL_TO_YOUR_NEW_ARTWORK.jpg',         src: 'new_song.mp3' // This file must also be uploaded     },     // ... add more songs here ]; 
4. Change the Background Image
	1	Near the top of index.html, find the <style> section.
	2	Update the URL in the background-image property.
	3	Make sure you upload the new image file to your repository and that the filename matches.
<!-- end list -->
body::before {     ...     background-image: url('YOUR_NEW_IMAGE.jpg');     ... } 
Deployment
This site is ready to be deployed on GitHub Pages.
	1	Ensure all your files (index.html, contact.html, patreon.html, your image, and your MP3s) are in the main branch of your repository.
	2	In your repository settings, go to the "Pages" tab.
	3	Under "Build and deployment," select "Deploy from a branch".
	4	Choose the main branch and the /(root) folder, then save.
	5	Your website will be live in a few minutes at https://your-username.github.io/.
