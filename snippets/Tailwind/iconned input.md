
All these need to have the `@tailwindcss/forms` plguin enabled

- Forms with highlighted borders m& Account Icon. [Play](https://play.tailwindcss.com/shN5sv667M)
 ![[../../media/{7A227745-F66A-4F85-9A16-016A1779DF1E}.png|300]]
```css
<label class="block">
	<span class="text-gray-700">Full name</span>
	<div class="relative">
	  <div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3">
		<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400" viewBox="0 0 24 24"><path fill="currentColor" d="M12 4a4 4 0 0 1 4 4a4 4 0 0 1-4 4a4 4 0 0 1-4-4a4 4 0 0 1 4-4m0 2a2 2 0 0 0-2 2a2 2 0 0 0 2 2a2 2 0 0 0 2-2a2 2 0 0 0-2-2m0 7c2.67 0 8 1.33 8 4v3H4v-3c0-2.67 5.33-4 8-4m0 1.9c-2.97 0-6.1 1.46-6.1 2.1v1.1h12.2V17c0-.64-3.13-2.1-6.1-2.1" /></svg>
	  </div>
	  <input type="text" class="mt-1 block w-full rounded-md border-gray-300 pl-10 shadow-sm focus:border-indigo-300 focus:ring focus:ring-indigo-200 focus:ring-opacity-50" placeholder="Enter your name" />
	</div>
</label>
```