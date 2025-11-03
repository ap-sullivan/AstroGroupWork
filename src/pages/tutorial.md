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

Once you have the Astro project setup you need to run '<strong>npm run dev -- --host 0.0.0.0</strong>', not just 'npm run dev', this ensures that the Astro files served from the container can be opened not just within the container but also on the local browser.

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

Now create a folder in the /src folder called data and within that a file called users.json.

</section>




<!-- 
<section class="tutorial-section">



![Image20](/AstroGroupWork/images/tutorial/20.png)


</section> -->

<section class="tutorial-section">

![Image21](/AstroGroupWork/images/tutorial/21.png)

</section>

<section class="tutorial-section">

![Image22](/AstroGroupWork/images/tutorial/22.png)

</section>

<section class="tutorial-section">

![Image23](/AstroGroupWork/images/tutorial/23.png)

</section>

<section class="tutorial-section">

![Image24](/AstroGroupWork/images/tutorial/24.png)

</section>

</div>









## How Astro's island Architecture Works With Other Frameworks

### React

Can lift the React example from presentation might need to make it more of a step by step though


### Another Framework

Worth having another basic one - maybe svelte



## How to use API's and Fetching Data from External Sources With Astro

Step by step of how to get it pulling data from the cocktail api example


## Astro's File Routing System

Show how Astro automatically creates routes based on your project’s folder and file structure inside the src/pages directory


## Anything else? Probably need to find a bit more to talk about possibly?


