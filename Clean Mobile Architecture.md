*May 3rd, 2023*  
Designing an application to be testable is crucial for its longevity.
#### Products vs. Projects
A **project** is temporary in that it has a defined beginning and end in time and thus defined scope and resources.  
A **product** is an object or system made available for consumer use; it is anything that can be offered to a market to satisfy a desire or need.
  
Software development nowadays is mainly about building products. It involves many unknowns that make it hard for us to have the certainties projects require upfront.   When we start working on a new app, we know the least about the software that we are building.  
Software evolves constantly. Think of the apps you use in your daily life. We are continually receiving updates, whether for bug-fixing, adding new features, or improving the UX. Take as an example your favorite social media or telecom app; how much has it changed over the past two years? Does this fit into the definition of a project? Do these applications have “a defined beginning and end in time”? And how about scope and resources? Do they seem to have been fixed upfront?  
Any piece of software with a fixed scope and time will become obsolete. Regardless of how innovative the idea is, evolving competition will eventually increase, eating up the market.  
  
#### How to determine the technical price of a software product?
We usually refer to the complexity of a product solely based on the technical complexity and the number of features. Are those the only factors that define its overall complexity? Definitely not! There is a process, organization, and people involved in building a product. On a high level, three major factors define the technical price of a software product:  
- The People.
- The amount and complexity of the features.
- The longevity of the product.  
  
All the above factors are key in making architectural decisions.  
  
*The architectural design is context-dependent. What works in a particular context does not work in another. Our own experience, when limited in variety, leads to biases that can harm the team’s productivity.*
  
*Software architecture is a communication medium. We communicate to other engineers the intention of the system.*

To define how elaborate an app’s architectural design should be, we must take into account its context, which includes:  
- The people involved.
- The technical complexity. 
- The intended lifespan.
  
A principle originating from Extreme Programming describes the above situation; it’s called YAGNI. “You ain’t gonna need it.” The principle states that a programmer should not be adding functionality to the software until deemed necessary. XP co-founder Ron Jeffries has said:  
Always implement things when you actually need them, never when you just foresee that you need them. —Ron Jeffries
  
##### The Mastery Path
Programmers generally pass through (at least) three stages of mastery —Junior, mid, and senior. At the junior level, we struggle to understand design patterns and apply them. Therefore, we just avoid them. At the mid-level, we are mainly able to understand and apply them. But in our excitement of acquiring this toolset, we tend to overuse it. Even in cases where they make the code more complex and harder to read. At the senior level, we have the experience and understanding to use them properly, in the right place and time. Complex code needs them; simple code does not benefit from them.

##### How much should I pay?
Time is money. —Benjamin Franklin
I purposefully used monetary terms to describe the terms under- engineering and over-engineering. First of all, as Benjamin Franklin stated, time is money. And engineering effort takes time. Secondly, as engineers, we often debate priorities with business people and product owners. Those people, before all, understand money. Therefore, it will help you make your case if you back it up with arguments closely tied to money. Speak their language. The next time you negotiate in favor of prioritizing a better dev-ops strategy, make sure to emphasize how much time and money the organization will save.
  
The rule of thumb is that: we refactor the code when it becomes hard to read. Usually, we notice it in the following moments of the development life-cycle:
1. While reviewing our own implementation, right before we commit it.
2. When a colleague complains that the code is hard to understand. This usually happens during code review or pair- programming.  
3. When we receive a new requirement that affects the code significantly. It’s more efficient if we perform the refactoring before adding the extra functionality.
  
From the above, I prefer point 3. In our example, I would refactor the function when the requirements included extra deciding factors. At the moment, the customer type and balance were added to the equation. At this moment it’s also easier to convince the business people. Avoid adding a task “Refactor function X.” Instead, add the refactoring effort inside the task: “Adjust text coloring based on customer type and balance.” A product owner can decide that something is not a priority. They can’t pressure you to deliver something they asked for in a very short time, though.

Over-engineering is writing code based on speculations or writing code that solves problems you don’t currently have. It’s as bad as under- engineering.  
The ideal moment for refactoring is right before introducing a new feature that our codebase is not ready to support. This way, it’s easier to convince other people as well as to motivate ourselves to do it.
