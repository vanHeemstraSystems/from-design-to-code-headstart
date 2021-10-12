# 100 - Evaluating a Design

As a way to talk about this, let’s use an example design for a “marketing-style” web page and assume we have been asked to implement it. We can also assume this site is created in a context where marketing professionals may come in and edit the content via some content management system (CMS), re-order the sections, replace images, and make style changes. So we need to decide on the components of the page that will be the building blocks used in the CMS.

This gets at another reason that this can be missed in education: often in our own solo projects, we can have static content right there in the HTML, and component parts aren’t going to be Frankenstein-ed together by strangers to form whole new pages and sections. But once you step into more real-world dev situations, things are a lot more dynamic, and we are often working at the layer of “make things that a non-developer can use to make a web page.”

Let’s use this website for a clinical trial is example. As we can see there are a lot of familiar design elements. Marketing sites tend to share common patterns:

- a big hero section
- product images
- small separate sections of short-form content emphasizing one thing or another
- information about the company
- etc.
- 
On mobile, we can take it as a given that in each section, the left columns will stack on top of the right, and some other fairly typical reflow will happen. Nothing structural will change on mobile. So what we are looking at is the core of the design.

In this example, there is a header, then a lot of distinct sections, and a footer. At a glance, some of the sections look kind of similar—several have a two-column layout, for example. There are button and heading styles that seem to be consistent throughout. As soon as you take a look at something like this, your eye will start to notice repeated patterns like that.

This is where we start making notes. Before we do any coding, let’s understand the ideas contained in the design. These ideas can fall into a few buckets, and we want our final product—the web page itself—to correctly represent all these ideas. Here are the buckets I commonly use:

***1. Layout-level patterns*** — repeating layout ideas and the overall grid

***2. Element-level patterns*** — headings, text sizes, fonts, spacing, icons, button sizes

***3. Color palette***

***4. Structural ideas*** — the logical organization of sections, independent from the layout

***5. Everything else*** - ideas that are only present in one component

Documenting the patterns this way comes in handy for figuring out our CSS approach, but also for choosing what HTML elements to use and starting conversations with the designer or other stakeholders if something is unclear. If you have access to the source files for the design, sections and layers might be labelled in there that give you a good idea what the designer was thinking. This can be helpful when you want to talk about specific sections.

So let’s look at the ideas contained in our example design. We’re going to do several passes through the design, and in all of them, we’re going ***outside-in, top-to-bottom, and left-to-right*** to ensure we evaluate every element. In each of the five passes, we’re looking for stuff that goes into just one of the buckets.

We’re unconcerned with getting this list perfect; it can always be changed later—we just want to record our first impressions.

## Pass 1: Layout-level ideas

See [README.md](./100/README.md)

## Pass 2: Element-level ideas

See [README.md](./200/README.md)

## Pass 3: Color palette

See [README.md](./300/README.md)

## Pass 4: Structural ideas

See [README.md](./400/README.md)

## Pass 5: Everything else

See [README.md](./500/README.md)
