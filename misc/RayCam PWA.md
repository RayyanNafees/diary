Rebuilt [shadowcam](https://shadowcam.netlify.app) in astro

## Functionality Improvements
- Astro Static site with Pocketbase saving
- PWA
	- offline via service workers
	- can or cannot access gallery
	- Faster Load time
- Gallery Sync & Auth with Pocketbase
	- Add google photos integration
	- or imgur or alternatives' integrations
- Store user images in Cloudflare R2 bucket in pocketbase then link
- Filter Creator
	- CSS filters
	- Canvas filters
	- SVG filters
	- WebGL shaders
- Filter directory, find and merge 2 or more filters, mark filters as favourite etc
- Support for Wide Caption, where a person can just hold the camera wide and it scans stuff up
- Sorts filters in order of user preferences, then after top-5 adds the most popular ones in the area etc
## UI improvements
- use css `scale` in capture button for making it big and in center
- Better loading & permissions screen
- Use [shoelace](https://shoelace.style) carousel for the gallery carousel

## Far-Fetched ideas
- AI based Augmented Reality filters
- GIF/small vids that can apply dog/cat filters based on face-detection
- AI LLM models RAG to describe the filter and it generates one for you
- 3D image generations based on AI and 360 deg scanning
- VR & 360 deg videos