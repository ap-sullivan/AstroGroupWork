---
layout: ../layouts/BaseLayout.astro
title: "Astro Presentation"
---

# Astro Presentation



### Andrew Sullivan, Ben Spiers, Pedro Santos, Stephen Ward 

[Astro Website](https://astro.build/).
[Astro Docs Website](https://docs.astro.build/en/getting-started/).

<section>

![Slide1](./images/presentation/1.png)

Welcome slide.

</section>


<section>

![Slide2](./images/presentation/2.png)

Introduction and background.

</section>

<section>

![Slide3](./images/presentation/3.png)

At its core, Astro is a modern web framework specifically designed for building fast, content-focused websites. It’s a relatively new player in the field, having first been released in 2022.

The main philosophy behind Astro is simple but powerful: send as little JavaScript to the browser as possible. Instead of loading a large bundle of JavaScript to render the entire page, Astro does most of the work on the server. You then add interactivity only where you need it by embedding components from frameworks, like React, Vue, or Svelte or just vanilla JS. 

This process is known as partial hydration, and it feels like a bit of a game-changer for web performance.

</section>

<section>

![Slide4](/images/presentation/4.png)

Why choose Astro over something more established? To understand this, let's look at a traditional Single Page Application, or SPA, like one built with React. In a typical SPA, the entire page runs as a single, large JavaScript application. This means the user's browser must download, parse, and execute a large JavaScript bundle just to see the content, which can be slow.

With Astro, the entire page is rendered into static HTML at build time. This means when a user visits the site, they get a fully-formed HTML page almost instantly. The interactive parts of the page are treated as isolated 'islands' that load their necessary JavaScript only after the main page content has already been rendered. The result is a much smaller JavaScript bundle and significantly faster page loads.

This performance boost has a direct impact on Search Engine Optimization, or SEO. Search engines like Google can index the full HTML content immediately without waiting for JavaScript to run, which leads to better rankings.

</section>

<section>

![Slide5](/images/presentation/5.png)


One of Astro's most powerful and unique features is that it is 'Framework Agnostic' as Astro lets you embed interactive components from other JavaScript frameworks directly into your pages.

What this means in practice is that you are not locked into a single technology, web developers aren’t forced to use only React, Vue, Svelte SolidJS, alpine js, you can use them all  alongside Astro.  

It also works with all the major CSS frameworks such as Tailwind and bootstrap and there are many community driven integrations with even more frameworks such as Angular, Lit and Flow.

<section>

![Slide6](/images/presentation/6.png)


Astro’s magic lies in a concept called the Island Architecture. Imagine a webpage is a large sea of static, non-interactive HTML. This 'sea' is all your text, images, and basic layout and it can be rendered on the server and sent to the browser incredibly quickly because it's just simple HTML and CSS. Scattered within that are your interactive UI components like image carousels,  search bars, or a 'add to cart' button. These are your 'islands'.

Instead of treating the entire page as one large, complex JavaScript application like a traditional SPA does, Astro treats it as mostly static HTML with a few isolated islands of interactivity. Astro renders the static HTML for everything first, so the user sees content almost instantly.

Only after the static page has loaded does Astro begin to 'hydrate' these islands, loading the small, self-contained JavaScript required to make them functional. This means if a user never scrolls down to your image carousel, the JavaScript for it might never even load.

This approach is the key to Astro's philosophy of sending as little JavaScript as possible, resulting in faster page loads, better SEO, and a much smoother user experience.

</section>

<section>

  ![Slide7](/images/presentation/7.png)

  This flowchart provides a visualisation of the entire page load process showing how Astro delivers its speed of load.
  
  1.	A user lands on an Astro site and send initial request.
  
  2.	On the server, Astro fetches any necessary data and renders a complete, static HTML page. Unlike many other frameworks that send a JavaScript bundle to the user's browser to build the page, Astro does this work on the server before sending anything.
  
  3.	Because it's just plain HTML, the browser receives this file and can render the page instantly and the user sees text, images, and layout almost immediately. There's no blank screen while waiting for JavaScript to download and execute.
  
  4.	After  the static content is visible, the hydrated components, or 'Islands,' activate their client-side JavaScript. This is the 'hydration' step. The JavaScript needed for interactive elements like a carousel or form loads in the background, making them functional without delaying the initial content.
  

</section>

<section>

  ![Slide8](/images/presentation/8.png)
 
  
  Traditional frameworks are fundamentally client-side heavy. Entire pages often require a full JavaScript bundle to render in the user's browser, which can significantly increase initial load times. Astro, by contrast, does this work on the server, sending pre-built HTML for maximum speed.
  
  This client-side approach creates SEO challenges and SPAs need extra work like server-side rendering or pre-rendering just to make their content crawlable by Google and other search indexers. Astro avoids this problem entirely by serving static HTML by default.
  
  Because of these factors, frameworks like React and Vue can be less efficient for content-heavy sites, which is precisely the area where Astro excels. 
  
  A React or Vue project usually commits you to that single framework but Astro is uniquely different; it empowers developers to mix components freely, allowing them take the best bits of each technology and use them together on the same page.
  

</section>


<section>

  ![Slide9](/images/presentation/9.png)

  Of course, no technology perfect and these of the challenges of working with Astro.
  
  As a new framework, the ecosystem is still evolving. This means you might find fewer ready-made libraries, plugins, and community support compared to more established giants like React or Vue. While the community is growing incredibly fast, you might occasionally have to build a solution yourself that would be readily available in an older ecosystem.
  
  Secondly, the very feature that makes Astro so flexible can also add complexity. If using different frameworks is not managed properly, you could inadvertently increase the JavaScript bundle size sent to the client, which works against Astro's core philosophy. It requires a disciplined approach to ensure you're using 'islands' effectively.
  
  There can also be a steeper learning curve as developers, especially those used to traditional Single Page Applications, need to adjust their thinking to the "island architecture
  
  Astro is not ideal for highly dynamic apps, for those use cases, a traditional client-side framework might still be a better fit.
  
  Finally, sites that are very large may experience long build times. The process of pre-rendering every single page can take more time to deploy than frameworks that render pages on demand. This is a direct trade-off you make: a potentially longer wait for deployment in exchange for a superior and faster user experience at page load time.
  
</section>

<section>

  ![Slide10](/images/presentation/10.png)

</section>

<section>

  ![Slide11](/images/presentation/11.png)

  Although Astro is a new framework that was only released in 2022, its adoption has been pretty rapid. This graph, using data from BuiltWith.com, shows the number of websites across the entire internet that use Astro.
  
  As you can see, the line is practically vertical from 2023 onwards and the statistics indicate that there are now over a million sites that use this technology. 
  
  However this is still relatively small fry when you consider that there are 3m next.js sites and over 50m sites built with react.
  
</section>

<section>

  ![Slide12](/images/presentation/12.png)

  This chart comes from a 2024 Netlify developer survey, which highlights the change in framework usage between 2023 and 2024.
  
  Astro is at the very top, showing a 10.6% swing in usage among developers. 
  
</section>

<section>

  ![Slide13](/images/presentation/13.png)

  Astro really excels at content-heavy sites where performance is critical. This includes blogs, marketing pages, documentation sites, personal portfolios, and e-commerce front-ends.
  
  Naturally, it's a perfect choice for any project where SEO is a top priority, because Google and other search engines reward fast, accessible pages with better rankings. It's also a great solution if you need to support users on slower networks or mobile devices, where large JavaScript bundles from traditional SPAs can be a significant problem.
  
  Finally, Astro is an excellent tool for modernising an existing website. You can perform a partial or progressive migration from an older framework without needing a full, risky rebuild that could take months and remove functionality
  
</section>

<section>

  ![Slide14](/images/presentation/14.png)

Here are just a few of the major companies and brands that use Astro for their websites. 

Major media outlets like The Guardian and NBC News which obviously have large amounts of content and global brands like IKEA, Porsche, and Unilever which again will have a lot of content for products and want good SEO to be above competitors in google rankings.  

And major tech companies like Cloudflare, Firebase who will have lots of documentation on their sites, and therefore pretty heavy on load times without statically generated HTML.


</section>

<section>

  ![Slide15](/images/presentation/15.png)

  To make getting started with the framework even easier, Astro has a library of pre-built templates and themes.
  
  You can find starter kits for specific projects like a restaurant website , a job board , an e-commerce store , or a developer portfolio plus many more.
  
  These templates are perfect for quickly prototyping a new site idea. They can also serve as a solid starting block for a bigger project, saving you from having to build common features from scratch.
  
  They are fully customisable, allowing a developer to extend and modify the code as much as they please to meet the project's specific requirements.
  
</section>

<section>

  ![Slide16](/images/presentation/16.png)
</section>

<section>

  ![Slide17](/images/presentation/17.png)
</section>

<section>

  ![Slide18](/images/presentation/18.png)
</section>

<section>

  ![Slide19](/images/presentation/19.png)
</section>

<section>

  ![Slide20](/images/presentation/20.png)
</section>

<section>

  ![Slide21](/images/presentation/21.png)
</section>

<section>

  ![Slide22](/images/presentation/22.png)
</section>

<section>

  ![Slide23](/images/presentation/23.png)
</section>

<section>

  ![Slide24](/images/presentation/24.png)
</section>

<section>

  ![Slide25](/images/presentation/25.png)
</section>
