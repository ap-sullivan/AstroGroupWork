---
layout: ../layouts/BaseLayout.astro
title: "Astro Tutorial"
---

<div class="tutorial-content" id="astroLocal">


<div class="tutorial-headings">

# Astro Introduction Tutorial
</div>

<div class="tutorial-sub-headings" >

## Setting Up Astro Locally

</div>

<section class="tutorial-section">




![Image1](/AstroGroupWork/images/tutorial/1.png)

![Image2](/AstroGroupWork/images/tutorial/2.png)

Within the terminal in Visual Studio code run the command <strong>‘npm create astro@latest’</strong> to start a local install. Note that you need to have node installed on the local machine for this to work, if you don’t, or don’t want to skip to the section <a href="#astroContainer"> Setting Up Astro in a Container</a>. 

</section>

<section class="tutorial-section">

![Image3](/AstroGroupWork/images/tutorial/3.png)


You will then be prompted with a few setup questions such as what folder to create the project, whether you want a starter template (go with the recommended starter template), install dependencies and initiate a git repo. 

</section>

<section class="tutorial-section">

![Image4](/AstroGroupWork/images/tutorial/4.png)

Once you have confirmed all the config options your project is initialised and you can start working in it by moving into the folder where the project was created and running <strong>'npm run dev'</strong> to start the local server.


</section>

<section class="tutorial-section">

![Image16](/AstroGroupWork/images/tutorial/16.png)

You will then be able to open your project in a browser on the specified localhost.

</section>

<section class="tutorial-section">

![Image17](/AstroGroupWork/images/tutorial/17.png)

Its a good idea to install the Astro plugin for VS code. This provides language support for .astro files as well as intellisense and syntax highlighting.

</section>


<div class="tutorial-sub-headings" id="astroContainer">

## Setting Up Astro in a Container

If you want to set up Astro in a container so nothing is installed locally, you can easily do this in Visual Studio Code using a Node/Typescript dev container. Note that you will have to have <a href="https://www.docker.com/">docker</a> installed on the local machine.
</div>

<section class="tutorial-section">

![Image6](/AstroGroupWork/images/tutorial/25.jpg)

In the search bar at the top of VS Code go to 'Show and Run Commands'.

</section>

<section class="tutorial-section">

![Image6](/AstroGroupWork/images/tutorial/6.png)

Click into 'Dev Containers:  Open Folder in Container' and select the folder on your local machine that the container will live.

</section>

<section class="tutorial-section">

![Image8](/AstroGroupWork/images/tutorial/8.png)

Select Node and TypeScript (or JavaScript if you prefer) as the dev container environment.

</section>

<section class="tutorial-section">

![Image7](/AstroGroupWork/images/tutorial/7.png)

Then select the version of node.js and linux. The default is bookworm-22 which means Node.js version 22 running on Debian Bookworm a stable version of Linux that Node uses. 

It will also ask if you want to install any additional features, but you can skip for this tutorial.

</section>

<section class="tutorial-section">

![Image9](/AstroGroupWork/images/tutorial/27.jpg)

After going through the setup you should be able to see a new container in the Docker desktop app.

</section>

<section class="tutorial-section">

![Image10](/AstroGroupWork/images/tutorial/10.png)

Now within the virtual container workspace you have created you can run the Astro install as per the steps set out in the <a href="#astroLocal">Setting Up Astro Locally</a> section.

</section>


<section class="tutorial-section">

![Image15](/AstroGroupWork/images/tutorial/15.png)

Once you have the Astro project setup you need to run '<strong>npm run dev - - &nbsp; - -host 0.0.0.0</strong>', not just 'npm run dev', this ensures that the Astro files served from the container can be opened not just within the container but also on the local browser.

</section>


<section class="tutorial-section">

![Image18](/AstroGroupWork/images/tutorial/28.jpg)

We now have a basic folder structure to start working with Astro.

</section>

<section class="tutorial-section">

![Image18](/AstroGroupWork/images/tutorial/29.jpg)


 If you look into the astro.index file code (located in pages)  you can get a basic understanding of how components are served to pages within an Astro project and its very similar to React or other frameworks.  A layout file with some basic CSS and html structure is imported as well as a component called “Welcome”. By placing the layout component on the page with the welcome component nested within it, the home page is rendered. 
 
 Have a play around with changing styles in layout and content in the welcome page, or create a component and import it to index.astro and place on the page to see how it renders.

</section>


<div class="tutorial-sub-headings">

## Using React with Astro

One of Astro's main strengths is the ability to be able to use other franeworks within it. This section talks you through how to install react and create a component and map contents of a json file to a page.
</div>


<section class="tutorial-section">

![Image18](/AstroGroupWork/images/tutorial/30.jpg)

In the command line run '<strong>npx astro add react</strong>' to install the relevant packages and dependencies needed to run react, and update the Astro config file. Double check the below has been added to the astro.config.mjs file:

![Image18](/AstroGroupWork/images/tutorial/31.png)

</section>

<section class="tutorial-section">


![Image18](/AstroGroupWork/images/tutorial/32.png)

Now create a folder in the /src folder called data and within that a file called users.json, copy the below json into the file and save.


<pre id="code">
[
  { "id": 1, "name": "Joe Bloggs", "role": "Full Stack Developer" },
  { "id": 2, "name": "Jane Doe", "role": "Backend Engineer" },
  { "id": 3, "name": "John Doe", "role": "UI/UX Designer" },
  { "id": 4, "name": "Donald Trump", "role": "Frontend Developer" }
]
</pre>

</section>

<section class="tutorial-section">

![Image18](/AstroGroupWork/images/tutorial/33.jpg)


Next in components, create a file called UserList.jsx (or .tsx if using TypeScript). And copy the below code into the file which is the code for fetching the data contained in the user json file and then mapping the contents in a component that can be placed:

<pre id="code">
import { useEffect, useState } from "react";

export default function UserList() {
  const [users, setUsers] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() =&gt; {
    // Fetch data from the local JSON file to simulate an API call
    fetch("/src/data/users.json")
      .then((res) =&gt; res.json())
      .then((data) =&gt; {
        setUsers(data);
        setLoading(false);
      })
      .catch((error) =&gt; {
        console.error("Error loading users:", error);
        setLoading(false);
      });
  }, []);

  if (loading) {
    return &lt;p className="loading"&gt;Loading users...&lt;/p&gt;;
  }
  
  return (
    &lt;div className="user-list"&gt;
      &lt;h3&gt;Team Members&lt;/h3&gt;
      &lt;ul&gt;
        {users.map((user) =&gt; (
          &lt;li key={user.id} className="user-card"&gt;
            &lt;strong&gt;{user.name}&lt;/strong&gt; &lt;br /&gt;
            &lt;span&gt;{user.role}&lt;/span&gt;
          &lt;/li&gt;
        ))}
      &lt;/ul&gt;
    &lt;/div&gt;
  );
}
</pre>


</section>


<section class="tutorial-section">

![Image21](/AstroGroupWork/images/tutorial/34.jpg)

Now create in your index.astro file import the UserList component at the top of the file, and then place the component on the page where you want the data to be rendered. 

Putting client:load within the component means the JavaScript "island" will be rendered only on page load. This can be seen when you inspect the page using the dev tools. Have a look yourself and then try client:visible, which only loads when the component enters the viewport (you may need to clear cache or use a incognito browser window).

</section>

<section class="tutorial-section">



![Image21](/AstroGroupWork/images/tutorial/35.jpg)

The rendered page should look something like this (this screenshot has some CSS styling which is also imported to the index.astro file from a separate style sheet).

</section>


<div class="tutorial-sub-headings">

## Using Svelte with Astro to Fetch and External API


As mentioned before you can use multiple frameworks and libraries within a single Astro project. This next section will bring in a svelte component that will render external API data on the same page as the react component that we just created, highlighting its flexibility as a framework.

</div>


<section class="tutorial-section">

![Image21](/AstroGroupWork/images/tutorial/21.png)
![Image22](/AstroGroupWork/images/tutorial/22.png)

First of all you need to install svelte using the <strong>'npm install @astro/svelte svelte</strong> command and update the <strong>astro.config.mjs</strong> file as per above to import and integrate the framework to the project.

</section>


<section class="tutorial-section">

![Image22](/AstroGroupWork/images/tutorial/36.jpg)

Now create a component file (in the components folder) called Cocktails.svelte. and copy the code below into the component. This code sets up a fetch query to the cocktaildb API and maps the results as a list.

<pre id="code">
&lt;script&gt;
  import { onMount } from 'svelte';
  let q = 'margarita';    
  let drinks = [];
  let loading = true;
  let error = null;

  const base = 'https://www.thecocktaildb.com/api/json/v1/1';

  async function fetchDrinks(query) {
    loading = true;
    error = null;
    try {
      const res = await fetch(`${base}/search.php?s=${encodeURIComponent(query)}`);
      if (!res.ok) throw new Error(`HTTP ${res.status}`);
      const json = await res.json();
      drinks = json.drinks || [];
    } catch (e) {
      error = e.message;
      drinks = [];
    } finally {
      loading = false;
    }
  }

  onMount(() => {
    //  fetch
    fetchDrinks(q);
  });
&lt;/script&gt;

&lt;section&gt;
  {#if loading}
    &lt;p&gt;Loading…&lt;/p&gt;
  {:else if error}
    &lt;p&gt;Error: {error}&lt;/p&gt;
  {:else if drinks.length === 0}
    &lt;p&gt;No results&lt;/p&gt;
  {:else}
    &lt;ul&gt;
      {#each drinks as d}
        &lt;li style="margin-bottom:1rem;"&gt;
          &lt;strong&gt;{d.strDrink}&lt;/strong&gt; — {d.strAlcoholic} &lt;br /&gt;
          &lt;small&gt;{d.strCategory} • {d.strGlass}&lt;/small&gt;
          &lt;div style="max-width:85%;"&gt;{d.strInstructions}&lt;/div&gt;
          {#if d.strDrinkThumb}
            &lt;img src={d.strDrinkThumb} alt={d.strDrink} style="max-width:180px;margin-top:.5rem;" /&gt;
          {/if}
        &lt;/li&gt;
      {/each}
    &lt;/ul&gt;
  {/if}
&lt;/section&gt;
</pre>

</section>

<br>

<section class="tutorial-section">


![Image23](/AstroGroupWork/images/tutorial/37.jpg)
![Image23](/AstroGroupWork/images/tutorial/38.jpg)

Back in index.astro, import the component at the top of the page, and then place the component below the react one that we added earlier.

</section>

<section class="tutorial-section">

![Image24](/AstroGroupWork/images/tutorial/39.jpg)

Now when you reload the page both the react component pulling data from the local json file is rendered to the page, and below that the list of cocktails being fetched from an external API in a svelte component. Magic!



</section>


<div class="tutorial-sub-headings">


## Astro's File Routing System

The last thing covered in this tutorial is an example of Astro's file routing system which is one of the pros of using the framework. Instead of having a complex separate routing file, Astro using the file and folder structure of the project and mirrors this for the URL structure. This is great for blogs or websites that are heavily nested such as documentation and news sites.

</div>

<div class="tutorial-sub-headings">


### Basic File Routing System
</div>

<section class="tutorial-section">



![Image24](/AstroGroupWork/images/tutorial/41.jpg)

Create a folder in src/pages called about.astro and add the below code



<pre id="code">
const pageTitle = "About";
---
&lt;html lang="en"&gt;
&lt;head&gt;
  &lt;title&gt;{pageTitle}&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;{pageTitle}&lt;/h1&gt;
  &lt;p&gt;
    This is the about page....
  &lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>


</section>


<section class="tutorial-section">

![Image24](/AstroGroupWork/images/tutorial/40.jpg)

Now in the browser add /about to the end of the localhost URL and the page should load. No separate routing definition required.


</section>





<div class="tutorial-sub-headings">

### Dynamic File Routing System

Where Astro really comes in useful for blogs and other sites that have heavily nested pages is using its dynamic page routes. 
</div>

<section class="tutorial-section">

![Image24](/AstroGroupWork/images/tutorial/43.jpg)

In the pages folder create a folder called blog and inside that folder create a file called <strong>[slug].astro</strong>. 


</section>

<section class="tutorial-section">

![Image24](/AstroGroupWork/images/tutorial/44.jpg)

Within the [slug].astro add the below code. This defines the pages that you want to use as paths (slugs).

<pre id="code">
---
export async function getStaticPaths() {
  return [
    { params: { slug: 'post1' } },
    { params: { slug: 'post2' } },
    { params: { slug: 'whatever-slug-you-like' } },
  ];
}

const { slug } = Astro.params;
---
&lt;html lang=&quot;en&quot;&gt;
  &lt;head&gt;
    &lt;title&gt;Blog: {slug}&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Blog Post: {slug}&lt;/h1&gt;
    &lt;a href=&quot;/blog/post1&quot;&gt;Post 1&lt;/a&gt;&lt;br /&gt;
    &lt;a href=&quot;/blog/post2&quot;&gt;Post 2&lt;/a&gt;&lt;br /&gt;
    &lt;a href=&quot;/&quot;&gt;Home&lt;/a&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

</section>

<section class="tutorial-section">


![Image24](/AstroGroupWork/images/tutorial/42.jpg)

Now add the code below to your index.astro file and go to the home page and click each link and see what URL the browser uses for each link.
<pre id="code">
&lt;h1&gt;Routing Example&lt;/h1&gt;
&lt;p&gt;Go to blog posts:&lt;/p&gt;
&lt;ul&gt;
  &lt;li&gt;&lt;a href=&quot;/blog/post1&quot;&gt;Post 1&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;/blog/post2&quot;&gt;Post 2&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;/blog/whatever-slug-you-like&quot;&gt;Hello World&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
</pre>


</section>

<section class="tutorial-section">

![Image24](/AstroGroupWork/images/tutorial/45.jpg)

The URL's and titles should match the pre-defined parameters defined in the [slug].astro file (these parameters would come from a headless CMS or database and wouldn't be hardcoded in a real site with lots of content). 
</section>
<section class="tutorial-section">

## Last Words

This tutorial introduced the core concept of Astro's island architecture and also its file routing system. Hopefully after doing the tutorial you can see the benefits of using the framework for certain use cases (content-heavy sites, SEO performance).

</section>

</div>






