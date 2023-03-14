[https://en.wikipedia.org/wiki/Story-driven_modeling](https://en.wikipedia.org/wiki/Story-driven_modeling)

On our team, since going agile, we've also been trying to narrow down and understand just how much documentation is actually required.

Before anything else, make sure to read this article on [Agile/Lean Documentation](http://www.agilemodeling.com/essays/agileDocumentation.htm). 

Secondly, reconsider producing design documents after preliminary work on stories. We've tried that before and it has proven to be a waste. Update the design docs ONLY AFTER the code for the story is delivered. 

**You need to ask yourself why you want to do design docs prior to coding.** 

- We as a team need to understand how the story will affect the design.
- Having design documents has proven useful when new (or temporary) members join the team or when returning to code that no one has worked on for over a year. So they are useful for organizational memory to help understand how the code works.
- Design documents are useful for maintenance engineers who may need to troubleshoot the code after the release.
- To satisfy (1) you do not need to produce an actual design document. Your team should still have a design phase prior to coding, but that phase can be as simple as a 15 minute session in front of a whiteboard or a napkin. You do not need to produce an actual document that will take hours (if not days) to write just to discuss the design changes.

(2) or (3) are not needed during development of the current story and more than likely they will not be needed for several subsequent iterations.

Every time a team member is writing/updating design docs, that's the time that code is not being written. When you write docs before actual code, there is almost 100% chance that they will require to be updated because once you start coding design always ends up being altered. And even if you write design docs after the code, as our team has learned, refactoring from subsequent stories still alters the design.

**Recommended:**

- Initially produce temporary designs/models enough so that your team can have an intelligent conversation prior to coding. Do not expect to keep these and do not waste time on formalizing them.
- Only produce official design documentation if someone will need it (i.e. your team has a real need for organizational memory)
- Only produce design documentation on code that has been stabilized. There's no point trying to document a module that keeps being changed in every iteration.
- Produce design documents which fully describe a module (or portion of the product). Design docs which document the changes that have to be made were completely worthless as soon as the release was done.
- Keep the document very high-level. If you write 20 pages covering architecture and very high-level design, that document will a) actually be read by other people and b) will help people get familiar with general layout of your code. For details people can go straight into the code. If you write 700 pages of detailed specification, they will almost always not match reality, it is too much for anyone to read and you will end up having to maintain and update 700 pages instead of 20 whenever future changes are made.