# Thoughts

## How do i semantically structure this content so it makes sense?
#### my implementation
```html
<main>
<figure>
  <img src="./assets/images/avatar-jessica.jpeg">
</figure>
<section>
  <h2>Ganesh Reddy Chimmula</h2>
  <h3>New Jersey, United States</h3>
</section>
<p>
  Front-end developer and a avid reader
</p>
<nav>
<button>GitHub</button>
<button>Frontend Mentor</button>
<button>linkedIn</button>
<button>Twitter</button>
<button>Instagram</button>
</nav>
</main>
```
#### thoughts
-Figure is used as there is image
-seperate Section is used for name and location, profile pic, description, links as there was significant space between profile them.
-nav is used because There are multiple navigation links. made sense to use nav

#### Suggestions from chatgpt and reasons
-Add alt to the image – important for accessibility.

-Use <figcaption> if you want to describe the image (optional).

-Use <article> to wrap the entire profile card – it’s self-contained content.
profile card is a self-contained piece of content:
It has a heading, image, location, description, and navigation.
It could stand on its own, be shared, reused, or repeated (like in a list of profiles).
So wrapping it in an <article> makes the meaning clearer

-Use <ul> inside <nav> instead of buttons — because those are actual links, not actions.
A navigation menu is a list of links.
So semantically, a list (<ul>) is the right choice.
Screen readers expect navigation to be a list of choices.
Using <ul> makes it easier for screen readers to:
Announce “list with 5 items”
Allow users to skip through links quickly
When the design looks like buttons but the elements are actually links (navigating to other pages or profiles), you should prioritize semantic meaning over appearance.

-Consider <address> for location if you want to be extra semantic.

-Heading levels: Don’t skip from <h2> to <h3> unless inside a nested section.

-Header instead of section
Use <header> when you're grouping introductory content (like a heading, subheading, or metadata) — especially at the top of a page, article, or section.

Use <section> when you're creating a thematic chunk of content that forms part of the document structure and includes its own heading.