
in order to create MERN stack apps, there's no better option than to use remix if u are planning on doing SSR

SSR in React is a problem developers have been facing since the dawn of React. MERN stack apps were never meant to be rendered server side… But instead, Client Side routing with build output rendered as static HTML pages & express used as a REST API server was the conventional strategy.

The complexity behind the SSR technique in JS UI frameworks is so wide that it lead to creating entirely new meta frameworks for solving this issue like Next.js, Astro, Remix being the top choices

We may have implemented SSR from our side, but I see potential inefficiencies in the current architecture which will become very big as the project grows introducing potential bugs and more complexities for additional functionality

## Potential Problems
Like how u think we can solve these problems with the current architecture ?
- For e.g., How can we create different Meta Tags for different routes for showing into the search engines ?
- Different pages require different Keywords, descriptions & SMO tags/images so that user can be easily redirected to the particular page by just googling it… Also leads the search engine to index our site well
- Current pages load with an annoying `[Object object]` starter page which takes time to render even on the dev server… Imagine what will happen once deployed to production and visited by users …. Things will get worse with additional network latency
- There is no Error-Boundary for internal errors that may really tell what's the issue with logic in which part of the application… instead of just printing errors… If something worse happens..… in the worst case, we'll be left with `Undefined in not an object` at a line number in a file that doesn't even exist.
- Recently an issue with TypeScript happened and there was no way I could internally guess the issue if I hadn't deleted the `node_modules` folder and reinstalled deps

In the current model even I, the guy who handles the SSR is afraid to touch anything thinking it might break the things and to let things go the way they are… and seeing the SSR code, it does seem a smart approach considering the situation

With such a mindset, there is 0 possibility that any customization related to rendering on the client might be extended or utilized by us by tweaking the current SSR strategy

We need a better model that requires the least changes in our codebase while giving us an easier & customizable  SSR strategy
And also enables us to find help online at GitHub Issues or Stack Overflow forums in case something goes wrong, and we are stuck with no clue — Something, that is impossible to get if u create your custom functionality for SSR
## Introducing Remix

Remix is just a Vite plugin is created by the developers behind the popular library for handling Client Side Routing `react-router`

It really eases up the way SSR is handled in MERN stack apps without adding significant complexity that meta frameworks like Next.js come along with

Is an industry standard, comes with lots of resources & integrations online to aid.. and solves all of the Potential Problems listed above without adding significant changes to our codebase

Here I have ported the project to Remix & it simplified the project by a lot
The only difference is that `client` folder is now just renamed to `app` and everything works as it was

While it may seem that since the current code works with the current model & the same code works with remix so there is no need of adding additional complexity of Remix
Well, "additional complexity" was added the moment we decided doing SSR ourselves, remix only handles that for us.

The important thing to consider is not only that it worked with no changes required to our codebase.. But the fact that remix does provide us a path to avoid the potential risks easily that may come along the way during the development process of this project with its great community resources and wide adoption by the industry