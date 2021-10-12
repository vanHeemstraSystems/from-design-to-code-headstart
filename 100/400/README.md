# Pass 4: Structural ideas

This is where we might actually name the regions of the page in ways that make sense to us, and identify the hierarchy of the content. We can start to understand the accessibility needs of our implementation by documenting in plain language what we see as the ***nature*** and ***structure*** of the content in the page. As always, going outside-in, top-to bottom, left-to-right as we make our evaluations.

Focusing on structure helps us figure out the underlying patterns that eventually become our components, and also helps us understand the way we want people who use assistive technology to perceive the content. In turn, that guides us as far as what HTML elements we need to use to write ***semantic HTML***. Semantic HTML speaks to the nature and structure of the content so that it can be perceived correctly by browsers. Browsers use our HTML to create the [accessibility tree](https://developer.mozilla.org/en-US/docs/Glossary/Accessibility_tree) that assistive tech, like screen readers, uses to present the page. They need a strong outline for that to succeed and semantic HTML provides that solid structure.

This means we need to understand the nature of what’s on the page well enough that we could explain it verbally with no visual support if we had to. From that understanding, we can work backwards to figure out the correct HTML that expresses this understanding via the accessibility tree, which can be inspected in you browser’s developer tools.

Here’s a quick example of the accessibility tree in Chrome if everything on the page is a div, and if elements are correctly chosen to match the nature of the content. Determining the best element choice in a given situation is outside the scope of this post, but suffice it to say that the expressive, non-”generic generic generic” accessibility tree below is entirely created with HTML elements and attributes, and makes the content and its organization much easier for somebody to perceive using assistive technology.

Three screenshots of an accessibility tree. One is made up only of generic containers, the text beside it reads. “Div soup - ignores the nature of the content.” The next is all generic but has a main parent element and one article element with a title, “What is Cyclic Vomiting Syndrome (CVS)?” The text beside it says the article is the odd one out and that we will look closer. The final image is the article element expanded in the accessibility tree, showing that it contains headings, paragraphs, and other semantically appropriate HTML elements. The text beside that one reads “Semantic markup! Stuff knows what it is!”

![example_web_site_design_pass_004](https://user-images.githubusercontent.com/12828104/136927744-5912ca8d-7de0-40b1-b269-6aedf292546b.png)

So, in this fourth pass, here are notes we might make:

- Top-level structure:
- -- Header
- -- Main Content
- -- Footer

Not so bad for the first top-to-bottom pass. Let’s go a level deeper. We’re still unconcerned with the child inside elements of the sections themselves yet—we want just enough info to label the top level items inside each sections.

Within Header there is:
Home link
Navigation section
Within Main Content there is:
Hero section
Short explainer about the disease itself
Explainer about the treatment
Intro to the trial
Explainer with more details about the trial
Statement about who can join the study
Call-to-action to participate
Short explainer about the company
Within Footer there is:
Logo
Summary Sentence
Some lists of links with titles
Divider
Copyright notice
This pass reveals a few things. First, the Header and Footer sections are pretty shallow and are already revealing raw elements like links and text. Second, the Main section has eight distinct subsections, each with its own topic.

We’re going to do one more pass here and get at some of the deeper details in those sections.

Header home link—Woohoo, it’s just a link and we’re done.
Header nav—This is an expanding hover nav that needs JavaScript to work correctly. There are probably lots of accessible examples to follow, but still will take more time to develop and test than if we were working with raw links.
Hero
Title
Column 1
Subtitle (we missed this in the first element-level pass)
Paragraph
Primary button link
Secondary button link
Column 2
Hero image
Disease Explainer
Title
Paragraph
Unordered list
Large text
Unordered list
Image and caption (figure and figcaption)
List of links
Treatment Explainer
Title
Column 1
Paragraphs
Column 2
Image and caption (figure and figcaption)
Trial—Intro
Title
Column 1
YouTube Video Player
Column 2
Paragraphs
Trial—More Details
Title
Subtitle
Cards (with Icon, Title, and List)
“Who Can Join” statement
Title
Column 1
Paragraph
Unordered list
Column 2
Paragraph
Unordered list
Call-to-Action
Title
Paragraph
Secondary button link
About the Company
Title
Paragraph
Yowza, that got long fast! But now we understand pretty well the kinds of things we need to build, and what parts might be tricky. We also see that there may be some helper components to be built that aren’t quite represented by any one of these sections, for example, a two-column layout component that stacks to one column on mobile and has a title on top, or a generic “section container” component that takes a background and foreground color and provides the right styles plus standardized internal padding.

Incidentally, with this breakdown we’ve done a pretty good job expressing the final accessibility tree we want our HTML to create, so we are well on our way to having the implementation be a smooth experience without a lot of re-work to get accessibility right.
