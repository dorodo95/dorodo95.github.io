---
layout: post
title: "Exploring Style in Limitation: Part 1"
excerpt_separator:  <!--more-->
---

 I've been meaning to start a devblog for a long time now, and I got motivated to do it after watching [Masahiro Sakurai's pretty damn good gamedev series]. If the dude can make that on his spare time, I sure as hell don't have a good excuse to postpone writing this.

With that said, since we've recently launched Horizon Chase 2 on Apple Arcade, that seemed like a good moment to talk a bit about one of my favourite topics and biggest challenge on that game: using product limitations to guide your project's artstyle.

This first part will be more introductory, focused on discussing the concepts and effects on development.

<p class="frame"><img src="{{site.baseurl}}/assets/images/yakuza.webp" style="max-width:80%"></p>

<!--more-->
<br>
<h2>The Many-Faced Budget</h2>
<br>
Art direction is a very organic process, especially in such an iterative media as games. It is a fine balance of exploring and achieving a unique creative vision for the project, all while fitting said vision within the bounds of your budget, that can come in a series of different factors:

<h3>Time and Funding</h3>
While these two points aren't necessarily interchangeable, they have similar effects during production. A tight deadline or small funding for your project will require the team to be more careful with the scope of the game, as well as defining pipelines, tools and solutions that fit the team's capabilities without demanding incredulous man-hours. On an art level, this can have significant impacts:

<ul>
    <li><b>Quicker iteration</b>, especially on the pre-production phase. This means that visual prototyping and lookdev may be shortened, as the art team will have to rely more on simpler, streamlined ideas, possibly already battle-tested by the team members on other occasions. This doesn't mean that the team will have to follow on safe bets (after all, our goal is to make our games stand out and feel special), but it also requires...</li>
    <li><b>More commitment</b> on decisions you may not be yet comfortable with. The longer it takes for a pipeline to be defined, or a prototype to be tested, the less time you'll have to actually build your systems and tools, and less time for polish in the end! It's important to understand when you need to investigate something further, and when it's time to keep moving forward with development.</li>
    <li><b>Asset Recycling</b>, following the "make more with less" mindset. A single rock may be rotated, scaled, color-tinted and tweaked in several tiny different ways in order to allow the team to use it in different contexts, and create new compositions. While this may make decrease the uniqueness of that asset, it also give the team an ever-growing library of ready-to-use assets, while also allowing for unique assets to have some more extra crafting time.</li>
    <h4> A Case for Game Jams </h4>
    Game Jams are a great way of enforcing a limited scope and encouraging fresh solutions. On our GMTK entry, <a href= "https://matheuscunegato.itch.io/towerbag">Towerbag</a>, we completely threw sanity out of the window when we decided to add custom drawings for each player upgrade. A lot of time was sunk during production, and we weren't happy with the final results. When we decided to tackle a revamped version of the game, I took a step back and thought about what we originally had, and how we could combine design, tech and scalability all in one go.
    <figure>
    <p class="frame"><img src="{{site.baseurl}}/assets/images/towerbag_comparison.png"></p>
    <figcaption>now do the same for 100 other cards</figcaption></figure>
    <br>
    With that in mind, I thought the idea of making brands and encapsulating the visual identity of the cards onto different parts would fit nicely in a customizeable shader. From it, we started prototyping some ideas and see how would it fit into the art direction:
    <p class="frame"><img src="{{site.baseurl}}/assets/images/towerbag_customization.png"></p>
    <figcaption>parameterization allows us to combine different elements, create new palettes and experiment directly in-game</figcaption>
    <p class="framePixel"><img src="{{site.baseurl}}/assets/images/cardsExample.gif"></p>
    <figcaption>ready to make the next hearthstone clone</figcaption>
    Aligning the limits of what your team (and yourself) can make on a set timeframe is essential, so that everybody understands the road that will lead your game to completion and its length.<a href= "https://www.youtube.com/watch?v=GxvIkLsyCso"> Owlboy's Simon Andersen gave a great GDC talk regarding the development of the project</a> over the course of a decade and the implications it had on design and art.
    <br>

</ul>
<br>
<h3>Technical Limitations</h3>
Once concepts and ideas start evolving and the team starts to create a mental image of the project, they'll also wonder how to turn that into a reality. That, in turn, will brew many other questions. This is a natural part of game development, one that we as an industry have inherited with the advance of technology throughout the years.
<br>
<ul>
    <li><b>Understand the Technical Budget</b>, as it will tell you how your project runs on the hardware, and how the hardware will run your project. It's a non-linear process to evolve the art in your game, exploit the strengths and avoid the weaknesses of the target device.</li> 
    <li><b>Prioritize</b> which parts of the game's visuals will require more processing power and by how much, so that areas that have a bigger impact on the visuals receive the correct amount of care and processing power. This may also impact the way certain assets are developed.</li>
    <li><b>Utilize the Gameplay Experience</b> when structuring your technical decisions, as it will also have an impact on your rendering. It's a neverending rabbit hole of challenges, and it's important to walk hand in hand with Game Design and Art Direction in order to align expectations and develop a solution that works for all areas while fitting the creative vision of the product.</li>
    <h4> A Technical Legacy</h4>
    During the advent of 3D graphics in videogames, developers were dealt with the challenge of discovering new rendering techniques and testing the waters of what was possible within a three-dimensional scene. Hardware was still severely limited, and with the combination of 3D models and textures, memory was a very scarce resource, and graphics followed a fixed-pipeline with no support for shaders and other effects.
    <p class="frame"><img src="{{site.baseurl}}/assets/images/paper_mario.png"></p>
    <figcaption>from super to paper </figcaption>
    As such, developers would explore an art style that would suit the hardware. An interesting example of this evolution is the Paper Mario series, which embraced these pillars on the initial prototypes and eventually evolved into a paper-like aesthetic for the world, with environment assets being abstracted to their primitive shapes, and tileable, simple textures and patterns being used to further cement the art in that direction. The flatness of sprites was also used to enforce the idea of paper, 2D characters in a 3D space, allowing sprites to fully rotate in the world without feeling out of place, saving on texture memory as well. Over the course of several generations and technological advancements, the series no longer has the same limitations, and yet utilizes modern pipelines to further develop these pillars in all aspects, including Game Design and UI, offering a different take on physically-based rendering and standing out as a unique experience for the players:
    <p class="frame"><img src="{{site.baseurl}}/assets/images/paper-mario-the-origami-king.jpg"></p>
    <figcaption>from paper to paperer </figcaption>
    
    <h4>Evolution of the medium</h4>
    As hardwares evolve, certain techniques become available for developers to explore. This is especially interesting when you consider the other way around, as games used all sorts of smoke and mirrors to achieve a certain vision. On traditional IPs that had several entries over the years, the development team can utilize this as a way to showcase an evolution for the franchise, and give us a glimpse of new ideas and concepts that were previously impossible to be achieved due to said limitations. A good example of this is the Yakuza series, which had most of its games taking place in the Kamurocho district, which managed to keep a lot of its original structure intact over the years. As the idea of a big city with several light sources and pedestrians walking around, the RGG team chose certain technical and design limitations to work with the hardware. 
    <p class="frame"><img src="{{site.baseurl}}/assets/images/yakuzacomp.png"></p>
    <figcaption>kamurocho was portrayed on many different generations, each one bring it to life on its own way</figcaption>

    This meant that for older titles, certain areas had pre-rendered backgrounds or fixed camera angles, with multiple loading zones and 2D billboards used in areas distant from the camera. Over time, the team was able to create more fully 3D environments, seamless transtitions, more NPCs and each element being able to cast its own light source.

</ul>

<h3>Design Limitations</h3>
<ul>
    Achieving a vision for the game experience may also require limitations to be included as part of the Game Design. This can be typically seen in games where the visuals are directly tied in some way to the gameplay, as is the case of titles such as <b>Monument Valley</b> and <b>Echochrome</b>, where the game's camera perspective impacts on the player navigation and possible actions.
     <p class="frame"><img src="{{site.baseurl}}/assets/images/monument_valley.webp"></p>
     <br>
    There are also other parts of the visuals that can be utilized in different ways to allow for new gameplay experiences. In <b>The Unfinished Swan</b>, for example, the developers utilized a dual-tone aesthetic in order to play with the idea of exploration through manipulation of positive and negative space.
     <p class="frame"><img src="{{site.baseurl}}/assets/images/unifinishedSwan.webp"></p>
     <br>
    
    Of course, I couldn't not mention the original Horizon Chase as an example of embracing said limitations. As a homage to retro 2D racers, the original team worked on the entire track system with the objective of replicating the infinite vanishing point usually seen in 2D racers such as Outrun or Top Gear. As such, the entire environment is a pseudo-3D scene, with objects actually moving and changing their scale to simulate a 2D-like perspective.
    <p class="frame"><img src="{{site.baseurl}}/assets/images/hct.png"></p>
    <figcaption>don't believe his lies</figcaption>
    <br>
</ul>

While other limitations may be imposed on the team, design limitations are purposefully embraced as a way to explore and evolve the interactive medium in other ways not previously seen. These will usually mean that the project is developed in an unorthodox manner, with unique tools and pipelines created for a specific purpose. As such, it can also mean that these limitations can actually make development more expensive, as it will take longer to train the team and may require more time on iterating such tools, which may also need to be reworked if design pillars change on the project, which is more likely due to the unique nature of the project. While this is not inherently a bad thing, it requires a lot of caution and even better communication between different areas than usual.
<br>

And that's it for now! On the next part, I'll be talking a bit more in-depth about the sorts of limitations and challenges we had on developing Horizon Chase 2.


[Masahiro Sakurai's pretty damn good gamedev series]: https://www.youtube.com/c/sora_sakurai_en