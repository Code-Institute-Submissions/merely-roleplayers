# Merely Roleplayers Podcast Website

## Module One Milestone Project: User-Centric Frontend Development - Code Institute

This is a website for Merely Roleplayers, a live play roleplaying game podcast. The website was built with the aim of providing a single online location for listeners and fans to subscribe, listen and find out more information about the podcast and the players involved in its production.

## UX

My goal in the design was to make it as easy as possible for users to access information about the podcast categorised into a small number of pages, while also creating a simple and stylish design that was in keeping with the existing brand identity of the podcast. This is the rationale behind using white and purple as the primary colour palette, as it matches the branding and graphics already used for promotion of the podcast.

As the website is designed to be the online home for a podcast, spotlighting the ability to listen and subscribe to the podcast was paramount, so I wanted to make sure there were prominent links to new and old episodes across the site. The 'Listen' button in the footer was inserted to ensure that users could easily access the latest episode of the podcast regardless of which page they were on at the time. Mobile responsiveness was also important as people are likely to be listening to the podcast on their phone, so allowing them to access a responsive and easy-to-use version of the website while on their mobile phone was vital to the overall design.

A series of user stories relating to the different types of possible users can be found [here](user-stories.md) and wireframes can be found [here](wireframes.pdf)

## Technologies

- [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
    * The project uses **HTML5** for the overall structure and content of the website.
- [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3)
    * The project uses **CSS3** for the style and format of the website.
- [Bootstrap v4.3](https://getbootstrap.com/docs/4.3/getting-started/introduction/)
    * The project uses **Bootstrap v4.3** for additional style and format options, particularly the grid system and mobile responsive elements.
- [FontAwesome Icons](https://fontawesome.com/)
    * The project uses **FontAwesome Icons** to include social icons.
- [Google Fonts - Arimo](https://fonts.google.com/specimen/Arimo)
    * The project uses **Google Fonts - Arimo** for formatting all text.

## Features

The features of this website are designed to allow users to carry out a variety of actions as part of the **User Stories** created before development.

### Existing Features

The website includes a sticky navbar on all pages to ensure the user is able to navigate around the website regardless of where on the page they have scrolled to. The navbar element is also collapsible when the website is viewed on a mobile device to ensure the appearance and functionality of the website remains in place across a variety of devices. The **Episodes Page** also uses cards with the collapse class triggered by buttons and a data-parent attribute to allow the cards to behave in the same way as an element with the accordion class.

### Features Left to Implement

In future I would like to connect the form on the *Contact Page* to an email service to allow a dialogue to be created between users and podcast staff.

## Testing

The intended outcomes of the user stories were achieved by creating a showcase for the podcast from the perspective of both fans and potential advertisers.

The **Home Page** provides a brief overview of the podcast including prominent links allowing users to quickly navigate to a variety of options for listening and subscribing to the podcast. The **Latest Episode** and **Current Season** are both spotlighted in dedicated sections of the homepage, and the **Reviews** section provides an indication of the quality and reception of the podcast.

The **About Page** includes more in-depth information about the podcast, providing users details about how the podcast works and how it is structured, particularly in the **Seasons** section. The gallery, built using the `.carouselExampleIndicators` class also showcases behind the scenes photos of the cast and crew during production of the podcast, and the **Systems Used** section includes embedded videos to provide greater context about how the games involved in the podcast are developed and played.

The **Episodes Page** includes a series of cards for each season displayed using the `.collapse` class and controlled by buttons. During testing the standard classes outlined in the [Bootstrap v4.3 documentation](https://getbootstrap.com/docs/4.3/components/collapse/) did not allow for toggling the cards to close when another button was clicked, meaning the new cards would show below those already showing, thus making straightforward navigation difficult. The `data-parent` attribute from the **accordion collapse** example in the documentation was used to allow toggling between cards and make sure that the overall user experience was fluid and simple.

Initially I embedded the HTML players for each episode of the podcast to the cards within a separate `div`. However, upon testing this slowed the load speed of the page significantly, so to reduce this I chose to embed a single player for the first episode of each season and a button which linked to the rest of the episodes, hosted on **Podbean**, a dedicated podcast hosting server.

The **Players Page** includes a photo and some information about each of the players involved in the recording and production of the podcast. Initially the layout was built using [Bootstrap media objects](https://getbootstrap.com/docs/4.3/components/media-object/), however upon testing these did not incorporate with the responsive layout in the way I was expecting. After investigating and discovering via [this Stack Overflow thread](https://stackoverflow.com/questions/21004570/bootstraps-media-object-image-is-not-responsive-inside-of-tab) that media objects are not responsive by design, I opted to create a series of rows using Bootstrap's grid system which would stack and reorder when viewed on a mobile device.

I originally built this using `.push` and `.pull` classes on alternate rows to create an alternating pattern of images and text which would still stack one on top of another when viewed on mobile. However after discovering that this did not work with Bootstrap v4.3 I utilised the `.order-` classes as outlined in the [Bootstrap v4.3 documentation](https://getbootstrap.com/docs/4.3/layout/grid/#order-classes).

The **Contact Page** includes a form which will submit information to an email server and uses the `required` attribute on all fields to ensure that these fields are filled in before the form can be submitted, and the `email` input type on the **Email** field to ensure that only valid email addresses are submitted. If any of these requirements are not fulfilled, the form will not submit successfully. If they are all fulfilled, the form will submit and the page will reload.

All links will open in a new tab using `target="_blank"` and the downloads on the **Contact Page** will download to your default folder for downloads on click using the `download` attribute. All links have been manually tested to ensure that they are pointed to the correct destination.

The site was tested across multiple browsers (Chrome, Internet Explorer, Firefox) and on multiple mobile devices using the **Google Chrome Developer Tools** to ensure compatibility and responsiveness. During testing on mobile devices, I realised that the `.navbar-toggler-icon` was being pushed onto a separate row by the `.navbar-brand`, and so I implemented a media query to reduce the `font-size` to allow the entire navbar to remain formatted into a single row.

## Deployment

The Merely Roleplayers website is hosted on GitHub Pages at [https://twelvepercenthero.github.io/merely-roleplayers/](https://twelvepercenthero.github.io/merely-roleplayers/) directly from the master branch.

To run locally, you can clone this repository directly into the editor of your choice by pasting `git clone https://github.com/TwelvePercentHero/merely-roleplayers.git` into your terminal. To cut ties with this GitHub repository, type `git remote rm origin` into the terminal.

## Credits

### Content

The information on the **Home Page**, **About Page** and **Episodes Page** were adapted from the [Merely Roleplayers section](https://www.mattboothman.com/merelyroleplayers) of host **Matt Boothman**'s personal website.

Information in the **Systems Used** section of the **About Page** was adapted from content found on the following websites:

- [Powered by the Apocalypse](http://apocalypse-world.com/)
- [Simple World](http://buriedwithoutceremony.com/little-games/simple-world)
- [Impulse Drive](https://adrian-thoen.itch.io/impulse-drive)

### Media

The main cover image was sourced from [PXHere](https://pxhere.com/en/photo/1087634), a stock image library.

Photos in the gallery on the **About Page** were sourced from the Press Pack provided on the [Merely Roleplayers section](https://www.mattboothman.com/merelyroleplayers) of host **Matt Boothman**'s personal website.

Images used on the **About Page** were sourced from the following websites:

- [Merely Roleplayers](https://www.mattboothman.com/merelyroleplayers)
- [Powered by the Apocalypse](http://apocalypse-world.com/)
- [Simple World](http://buriedwithoutceremony.com/little-games/simple-world)
- [Impulse Drive](https://adrian-thoen.itch.io/impulse-drive)

Videos on the **About Page** were embedded via YouTube from the following channels:

- [Roll20](https://www.youtube.com/channel/UCHC1kWACzA7G6D2fqkqsRDg)
- [Adam Koebel](https://www.youtube.com/channel/UCrQL02ilNwJ_MrB7w61f8iw)

All photos on the **Players Page** were sourced from [Pexels](https://www.pexels.com/), a stock image library and used as placeholders.

**This site is for educational use**