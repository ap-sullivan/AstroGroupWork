---
layout: ../layouts/BaseLayout.astro
title: "Astro Presentation"
---


<div class="content">

  
<div class="headings">

# Astro Presentation


### Andrew Sullivan, Ben Spiers, Pedro Santos, Stephen Ward 

### [Astro Website](https://astro.build/)
### [Astro Docs Website](https://docs.astro.build/en/getting-started/)

</div>

<section class="presentation-section">

![Slide1](/AstroGroupWork/images/presentation/1.png)

Welcome slide.

</section>


<section class="presentation-section">

![Slide2](/AstroGroupWork/images/presentation/2.png)

Introduction and background.

</section>

<section class="presentation-section">

![Slide3](/AstroGroupWork/images/presentation/3.png)

At its core, Astro is a modern web framework specifically designed for building fast, content-focused websites. It’s a relatively new player in the field, having first been released in 2022.

The main philosophy behind Astro is simple but powerful: send as little JavaScript to the browser as possible. Instead of loading a large bundle of JavaScript to render the entire page, Astro does most of the work on the server. You then add interactivity only where you need it by embedding components from frameworks, like React, Vue, or Svelte or just vanilla JS. 

This process is known as partial hydration, and it feels like a bit of a game-changer for web performance.

</section>

<section class="presentation-section">

![Slide4](/AstroGroupWork/images/presentation/4.png)

Why choose Astro over something more established? To understand this, let's look at a traditional Single Page Application, or SPA, like one built with React. In a typical SPA, the entire page runs as a single, large JavaScript application. This means the user's browser must download, parse, and execute a large JavaScript bundle just to see the content, which can be slow.

With Astro, the entire page is rendered into static HTML at build time. This means when a user visits the site, they get a fully-formed HTML page almost instantly. The interactive parts of the page are treated as isolated 'islands' that load their necessary JavaScript only after the main page content has already been rendered. The result is a much smaller JavaScript bundle and significantly faster page loads.

This performance boost has a direct impact on Search Engine Optimization, or SEO. Search engines like Google can index the full HTML content immediately without waiting for JavaScript to run, which leads to better rankings.

</section>

<section class="presentation-section">

![Slide5](/AstroGroupWork/images/presentation/5.png)


One of Astro's most powerful and unique features is that it is 'Framework Agnostic' as Astro lets you embed interactive components from other JavaScript frameworks directly into your pages.

What this means in practice is that you are not locked into a single technology, web developers aren’t forced to use only React, Vue, Svelte SolidJS, alpine js, you can use them all  alongside Astro.  

It also works with all the major CSS frameworks such as Tailwind and bootstrap and there are many community driven integrations with even more frameworks such as Angular, Lit and Flow.

</section>

<section class="presentation-section">

![Slide6](/AstroGroupWork/images/presentation/6.png)


Astro’s magic lies in a concept called the Island Architecture. Imagine a webpage is a large sea of static, non-interactive HTML. This 'sea' is all your text, images, and basic layout and it can be rendered on the server and sent to the browser incredibly quickly because it's just simple HTML and CSS. Scattered within that are your interactive UI components like image carousels,  search bars, or a 'add to cart' button. These are your 'islands'.

Instead of treating the entire page as one large, complex JavaScript application like a traditional SPA does, Astro treats it as mostly static HTML with a few isolated islands of interactivity. Astro renders the static HTML for everything first, so the user sees content almost instantly.

Only after the static page has loaded does Astro begin to 'hydrate' these islands, loading the small, self-contained JavaScript required to make them functional. This means if a user never scrolls down to your image carousel, the JavaScript for it might never even load.

This approach is the key to Astro's philosophy of sending as little JavaScript as possible, resulting in faster page loads, better SEO, and a much smoother user experience.

</section>

<section class="presentation-section">

  ![Slide7](/AstroGroupWork/images/presentation/7.png)

  This flowchart provides a visualisation of the entire page load process showing how Astro delivers its speed of load.
  
  1.	A user lands on an Astro site and send initial request.
  
  2.	On the server, Astro fetches any necessary data and renders a complete, static HTML page. Unlike many other frameworks that send a JavaScript bundle to the user's browser to build the page, Astro does this work on the server before sending anything.
  
  3.	Because it's just plain HTML, the browser receives this file and can render the page instantly and the user sees text, images, and layout almost immediately. There's no blank screen while waiting for JavaScript to download and execute.
  
  4.	After  the static content is visible, the hydrated components, or 'Islands,' activate their client-side JavaScript. This is the 'hydration' step. The JavaScript needed for interactive elements like a carousel or form loads in the background, making them functional without delaying the initial content.
  

</section>

<section class="presentation-section">

  ![Slide8](/AstroGroupWork/images/presentation/8.png)
 
  
  Traditional frameworks are fundamentally client-side heavy. Entire pages often require a full JavaScript bundle to render in the user's browser, which can significantly increase initial load times. Astro, by contrast, does this work on the server, sending pre-built HTML for maximum speed.
  
  This client-side approach creates SEO challenges and SPAs need extra work like server-side rendering or pre-rendering just to make their content crawlable by Google and other search indexers. Astro avoids this problem entirely by serving static HTML by default.
  
  Because of these factors, frameworks like React and Vue can be less efficient for content-heavy sites, which is precisely the area where Astro excels. 
  
  A React or Vue project usually commits you to that single framework but Astro is uniquely different; it empowers developers to mix components freely, allowing them take the best bits of each technology and use them together on the same page.
  

</section>


<section class="presentation-section">

  ![Slide9](/AstroGroupWork/images/presentation/9.png)

  Of course, no technology perfect and these of the challenges of working with Astro.
  
  As a new framework, the ecosystem is still evolving. This means you might find fewer ready-made libraries, plugins, and community support compared to more established giants like React or Vue. While the community is growing incredibly fast, you might occasionally have to build a solution yourself that would be readily available in an older ecosystem.
  
  Secondly, the very feature that makes Astro so flexible can also add complexity. If using different frameworks is not managed properly, you could inadvertently increase the JavaScript bundle size sent to the client, which works against Astro's core philosophy. It requires a disciplined approach to ensure you're using 'islands' effectively.
  
  There can also be a steeper learning curve as developers, especially those used to traditional Single Page Applications, need to adjust their thinking to the "island architecture
  
  Astro is not ideal for highly dynamic apps, for those use cases, a traditional client-side framework might still be a better fit.
  
  Finally, sites that are very large may experience long build times. The process of pre-rendering every single page can take more time to deploy than frameworks that render pages on demand. This is a direct trade-off you make: a potentially longer wait for deployment in exchange for a superior and faster user experience at page load time.
  
</section>

<section class="presentation-section">

  ![Slide10](/AstroGroupWork/images/presentation/10.png)

</section>

<section class="presentation-section">

  ![Slide11](/AstroGroupWork/images/presentation/11.png)

  Although Astro is a new framework that was only released in 2022, its adoption has been pretty rapid. This graph, using data from BuiltWith.com, shows the number of websites across the entire internet that use Astro.
  
  As you can see, the line is practically vertical from 2023 onwards and the statistics indicate that there are now over a million sites that use this technology. 
  
  However this is still relatively small fry when you consider that there are 3m next.js sites and over 50m sites built with react.
  
</section>

<section class="presentation-section">

  ![Slide12](/AstroGroupWork/images/presentation/12.png)

  This chart comes from a 2024 Netlify developer survey, which highlights the change in framework usage between 2023 and 2024.
  
  Astro is at the very top, showing a 10.6% swing in usage among developers. 
  
</section>

<section class="presentation-section">

  ![Slide13](/AstroGroupWork/images/presentation/13.png)

  Astro really excels at content-heavy sites where performance is critical. This includes blogs, marketing pages, documentation sites, personal portfolios, and e-commerce front-ends.
  
  Naturally, it's a perfect choice for any project where SEO is a top priority, because Google and other search engines reward fast, accessible pages with better rankings. It's also a great solution if you need to support users on slower networks or mobile devices, where large JavaScript bundles from traditional SPAs can be a significant problem.
  
  Finally, Astro is an excellent tool for modernising an existing website. You can perform a partial or progressive migration from an older framework without needing a full, risky rebuild that could take months and remove functionality
  
</section>

<section class="presentation-section">

  ![Slide14](/AstroGroupWork/images/presentation/14.png)

Here are just a few of the major companies and brands that use Astro for their websites. 

Major media outlets like The Guardian and NBC News which obviously have large amounts of content and global brands like IKEA, Porsche, and Unilever which again will have a lot of content for products and want good SEO to be above competitors in google rankings.  

And major tech companies like Cloudflare, Firebase who will have lots of documentation on their sites, and therefore pretty heavy on load times without statically generated HTML.


</section>

<section class="presentation-section">

  ![Slide15](/AstroGroupWork/images/presentation/15.png)

  To make getting started with the framework even easier, Astro has a library of pre-built templates and themes.
  
  You can find starter kits for specific projects like a restaurant website , a job board , an e-commerce store , or a developer portfolio plus many more.
  
  These templates are perfect for quickly prototyping a new site idea. They can also serve as a solid starting block for a bigger project, saving you from having to build common features from scratch.
  
  They are fully customisable, allowing a developer to extend and modify the code as much as they please to meet the project's specific requirements.
  
</section>

<section class="presentation-section">

  ![Slide16](/AstroGroupWork/images/presentation/16.png)

  So how does Astro fit in with other web technologies?

</section>

<section class="presentation-section">

  ![Slide17](/AstroGroupWork/images/presentation/17.png)

  Astro slots in well in the modern web ecosystem with its flexibility and compatibility with so many new and old technologies.
  
  You can use components from React, Vue, Svelte, and others seamlessly within the same project
  
  Since Astro runs on Node.js for its backend features, it can connect to any database that works with this technology. This includes traditional SQL databases like MySQL or PostgreSQL and NoSQL databases like MongoDB or Firebase,  and Cloud-hosted databases such as Firebase and Supabase.
  
  Astro is built to consume data from anywhere so working with API’s is seamles. It works with both REST and GraphQL APIs and can fetch data at different times: during the site build at deployment for static content, on the server for dynamic pages, or on the client-side within interactive islands.
  
</section>

<section class="presentation-section">

  ![Slide18](/AstroGroupWork/images/presentation/18.png)

  It integrates smoothly with popular headless content management systems like Contentful, Sanity, and Strapi which let you store text, images, and other content online and then fetch it via an API, this technique would be used heavily for e-commerce front ends or documentation sites which Astro works best for. 
  
  It integrates perfectly with styling tools like Tailwind, Sass, and PostCSS, and it supports TypeScript out of the box.
  
  Finally Astro can be deployed in many different environments, depending on the project’s needs:
  
  Static CDN: If your site is static (no backend), you can host it directly on a CDN like GitHub Pages or Cloudflare Pages for ultra-fast performance.
  
  Serverless platforms: For dynamic apps or APIs, you can deploy on Vercel, Netlify, or Render — they automatically scale and manage servers for you.
  
  You can also run Astro on your own Node.js server.
  
  
  Essentially, you can use Astro to build anything from a simple static site to a full-stack web app with live data.
  
</section>

<section class="presentation-section">

  ![Slide19](/AstroGroupWork/images/presentation/19.png)

  Leading on from the last slide, while Astro excels at static sites, it's also a capable full-stack framework as evidenced by the number of technologies you can work with. 
  
  The front-end would be handled by its static-site generation (SSG) capabilities and the concept of hydrating JavaScript 'islands.
  
  On the back-end, Astro lets you create server-side API routes directly inside your project, inside a folder like /src/pages/api/ similar to how express.js or Nextjs apps work.
  
  That means you can handle things like fetching data, posting forms, or even authentication — without needing a separate Express or Node.js app.
  
  You can also integrate any kind of database supported by Node.js — whether it’s SQL, NoSQL, or a cloud-based service like Supabase or Firebase.
  
  For security, Astro supports popular authentication libraries like JWT or OAuth — which means it’s capable of handling login systems and protected routes.
  
  As a framework Astro gives you the best of both worlds — static speed on the front end, with dynamic power and flexibility on the back end.
  
</section>

<section class="presentation-section">

  ![Slide20](/AstroGroupWork/images/presentation/20.png)

  Lets look at how to set Astro up and an example of how easy it is to incorporate react components or "islands" into a Astro project.
</section>

<section class="presentation-section">

  ![Slide21](/AstroGroupWork/images/presentation/21.png)

  Getting started with Astro very simple and takes only a few minutes.
  
  The most direct way is a local setup. As long as you have Node.js installed, you can just open your command line and run npm create astro@latest. The installer will then guide you through a few simple prompts, like naming your project and whether to install dependencies or initialize a Git repository. Once it’s finished, you just cd into the new folder and run npm run dev to start a local development server with live updates.
  
  Of course, if you prefer a containerised approach, you can also set up your project using Docker by installing the package within a Node.js container.
  
  To enhance the development experience there is an official plugin for VS Code. This is incredibly useful, providing features like syntax highlighting, IntelliSense, code formatting, and much more, which generally makes life a lot easier when writing Astro code.
  
</section>

<section class="presentation-section">

  ![Slide22](/AstroGroupWork/images/presentation/22.png)

  The next two slides show a practical example of how Astro works in conjunction with React.
  
  Adding React to an existing Astro project is easy, you just run a single command in your terminal “npx astro add react”.
  
  As you can see from the command line output, this command does two main things:
  
  1.	First, it installs all the necessary dependencies, like the Astro React integration package and the React libraries themselves.
  
  2.	Second, it automatically updates your Astro configuration file to import and use the new React integration.
  
</section>

<section class="presentation-section">

  ![Slide23](/AstroGroupWork/images/presentation/23.png)

  Once React is added, you can start using components. This slide shows the two key files.
  
  On the left, we have a standard React component called UserList.jsx. It uses familiar React hooks like useState to fetch data from a local JSON file and manage a loading state. 
  
  On the right is our index.astro page. At the top, we are importing the UserList component just like you would in a regular React project. This is where Astro comes in as when we use the component in our HTML, we add the directive <strong>client:load</strong>. 
  
  This is a command that tells Astro, 'This component is an interactive island.'  And  should not be rendered to static HTML at build time; instead, its JavaScript should be sent to the browser and rendered only when the page loads. This is how we create our islands of interactivity.
  
</section>

<section class="presentation-section">

  ![Slide24](/AstroGroupWork/images/presentation/24.png)

  And here is the final result. On the top left, you can see the fully rendered page in the browser. The React component has successfully fetched the data from the JSON file and mapped it to a list of team members, just as it would in any normal react project.
  
  The interesting part is what's happening in the browser. If you look at the screenshot of the browser's developer tools, you'll notice there isn't one large JavaScript bundle for the entire page. Instead, Astro has only shipped the UserList.jsx component as its own as individual JavaScript file.
  
  This demonstrates the 'island architecture' in action. The static content was delivered as fast HTML, and only the small, isolated JavaScript needed for this one interactive component was sent to the client. This is the core of how Astro works.
  
</section>

<section class="presentation-section">

  ![Slide25](/AstroGroupWork/images/presentation/25.png)


  At its heart, Astro is a performance-first framework. Its core principles are pre-rendering pages to static HTML and using the innovative 'island architecture' to handle interactivity.

It's important to note that Astro isn't a framework that will work for every single use case. However, when SEO and user experience are critical, it is an ideal choice, providing fast page loads and fully indexable HTML for better search engine rankings.

Since its launch, Astro has grown in popularity with developers at an incredible speed. This is likely due to its great flexibility, its framework-agnostic nature, and its full-stack capabilities.

Finally, while Astro has a rapidly growing ecosystem, it is still young. It remains to be seen whether it is a short-term trend or if it will become a long-term fixture in the future of web development.

</section>
</div>