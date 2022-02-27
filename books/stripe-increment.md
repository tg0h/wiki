---
title: Increment Magazine
tags: [development]
---

date read: 2022-01-13

# Increment

## 3 - Development

### What's it like to be a developer at ...

Lyft has a set of internal products named DevBox and OneBox, which let you run Lyft services in an environment that closely mimics a simple production deployment.

We built a tool called submitqueue, which manages the submission, revert, and testing of pull requests via a number of different emoji commands in the pull request comment section. For example, :rocket: to ship, :rocket: plus :praying hands: to ship without running tests, :loudly crying face: to revert, and :hammer: to rerun tests.

Deployment mistakes happen: Rolling back a set of changes is a single click, and often completes within one to two minutes.

One of the core values we really live by is “Make It Happen.” There’s so much work to do! Engineers are encouraged to take on big projects, propose new features, fix persistent bugs, and take risks.

Working remotely requires a certain amount of discipline; because the people you need might not be awake for another 12 hours, you have to plan ahead to make sure you don’t get stuck waiting for them, and [to ensure] that you don’t hold anyone else back. The flip side of this is that we’re really relaxed about what we consider a work “day” to be—as long as you meet the expectations of the team you can work however and whenever you want.

 As such, the most common tool used by developers at Slack (other than Slack itself) is Sublime Text—though there is a hearty contingent of people continuing the Emacs versus Vim debate.

 If the change goes awry, I figure out how to fix forward or revert my change.

So much of development is couched in metaphor; code review is a perfect time to talk concretely about code in context.

### Center stage: Best practices for staging environments

It’s not about eating your tech vegetables; it’s about showing respect for your users’ money and time.

### Interview with Isaac Z. Schlueter, CEO of npm

We’re not yet profitable, but we’ve been—there’s a term—default alive.

Some companies have made quite a lot of money by having interests that diverged with a majority of their users or the community that they’re in. I don’t know if it’s right to say that it’s bad or evil, [but] it’s certainly antisocial to be at odds with your user base.

They would disappear and go invent something else themselves. I have no doubt about that. We haven’t solved cold fusion or done something truly innovative. What we’ve done is we’ve developed a community platform that’s extremely useful to a given community, provided that we keep it that way.

### Ask an expert: Has adopting microservice architecture changed the way we develop software?

There is simply no easy way to fix abstraction mistakes without complex migrations that consume valuable engineering time.

### Home is where the work is

We’re adults—we know what we have to get done, so let us get it done and we will give you our best.

### The melting pot of javascript

While the standards committees spent years arguing about the future of a document-centric web, developers realized that the advantages of a cross-platform delivery mechanism for rich interactive apps is worth the pain of creating them with no SDK, module system, library, or compiler. After all, they could write their own. And they did.

People often joke about it, but the fact is that the npm registry is the largest code-sharing platform in the human history.

Since npm places the dependencies right under your project directory, you are always a click away from the code that makes your app tick

## 4 - Energy & Environment

### The secret energy impact of your phone

The American Council for an Energy-Efficient Economy estimated in a 2012 study that the energy impact of data in real terms is about 5.12 kilowatt hours per gigabyte of data consumed. It also uncovered where most of that cost is incurred: cloud providers.

According to that study, 48 percent of each gigabyte’s energy cost is incurred in data centers and point of presence networks, 38 percent at the end user, and just 14 percent in transit.

## 5 - Programming Languages


### A crash course in compilers

I love languages because, of everything I’ve encountered in computing, languages are by far the weirdest.

The decision to adopt or avoid a language is always a mix of their perceived formal power (“Does this language even have this particular feature?”), employability (“Will this language get me a job?”), and popularity (“Does anyone important use this language anymore?”).

You can think of source code as an extreme, Turing-complete configuration file that controls the interpreter’s behavior.

The job of a compiler is to take source code and translate it into a target code with the same meaning. Often that target code is in a lower-level language like machine code, but that isn’t always the case.

There are even cases where it is desirable to compile a lower-level language into a higher-level one. To run in the browser, the JSIL project compiles C# bytecode into JavaScript so it can run on the web

A scanner (also known as a lexical analyzer) reads source text and produces a linear stream of tokens; the parser reads the stream of tokens and recognizes patterns to transform into nodes in an abstract syntax tree 

Most package managers are specific to their languages, custom built, and require server infrastructure, though generic solutions like Gx and Nix are available as well. Gx is interesting because it operates over IPFS, a peer-to-peer protocol that requires no central server coordination.

Languages represent different ideas of how to capture human creativity on a machine

### Six questions on programming languages

We have customer support engineers who do write code and work with customers’ code. I’m pleased that we do support them moving into engineering.

nothing suits my natural way of thinking quite like C does. It’s like coming home

### It's COBOL all the way down

The oldest computer program still running is arguably the Department of Defense’s Mechanization of Contract Administration Services (MOCAS), which manages over a trillion dollars across hundreds of thousands of contracts. It’s written in COBOL, though because it was launched in 1958, it was likely first written in a similar predecessor language, Hopper’s FLOW-MATIC

### Julia: The Goldilocks language

When you decide to create a programming language from scratch, you come across countless key structural questions that have to be answered before you can progress, each with the potential to waylay the language if there’s a single misstep.

### The language of the workplace

Language is a powerful tool. It signals belonging, culture, values, place. In the tech industry, coding languages are worn as a badge of honor, and are used to create hierarchies. They’re indications of longevity, survival, sophistication.

However, for people who are the first in their family to go to college, to write a resume, to interview for a six-figure job, or who simply haven’t worked in the tech industry before, the norms and expectations are largely unlearned.

When, by the grace of their devastatingly hard work, their hustle, myriad mentors, the prayers of grandma, and some plain luck, they make it into a tech job, the language of the workplace is a foreign one.

their ignorance of the norm is often attributed to their race, gender, sexual orientation, disability, lack of innate intelligence, and so on.

On one hand, identity performance and the pressure to assimilate operationally is draining, and chips away at an individual’s sense of self

When configuring a system, you often just need some combination of dictionaries and lists, which allows you to use a format like YAML or JSON quite straightforwardly

The general situation where one configuration value depends on some others is very common, and frequently motivates the change to configuring systems with a programming language.

### The ABCs of language migration

 “It’s rare that you look back at this five-year journey and say, ‘Wow, that was the right choice.’ Everyone’s always like, ‘We thought it was going to be a year [to transition], but it was more like two years,’” Schenk said.

### Unplain text

Written language is one of the most intricate and complex technologies we’ve developed as a species. From the ideograms of East Asia to the cursive abjads of the Middle East to the syllabics of North America, the hundreds of living scripts in use today evolved organically and independently over millennia, and they are massively varied

## 9 - Open Source

### The rise of few-maintainer projects

You put at risk millions of people, and making something for free, but public, means you are responsible for the package

He emailed me and said he wanted to maintain the module, so I gave it to him

Instead of a community of developers looking after the entire Rube Goldberg machine, we’ve now got individual developers in charge of a pulley here, a marble there

As open source moves toward high-frequency, low-touch interactions, this level of downside protection starts to feel unrealistic. Instead, maintainers must find ways to manage support requests and casual contributions without substantial investments of their time.

## 13 - Frontend

### When frontend means full stack

Frontend development is at the intersection of art and logic, business and expression, left brain and right brain, design and nerdery.

### The rise of React

I’ve noticed React-driven websites tend to be pretty battery-draining on my mobile because there’s a lot of heavy lifting going on,

‘If a trillion-dollar company is using modularity, there must be something to it,’” says Meyer. “Even if it has nothing to do with how they became a trillion-dollar company.”

has been treated by Facebook as a way to solve Facebook’s problems, and few of us have websites that have Facebook’s problems.

React makes certain things easy and other things hard. We generally move toward the things that are easy and away from the things that are hard. It herds you in a certain direction

Mullenweg was torn. He could accept the patent clause, roll out the Gutenberg update, and opt in millions of people despite their protestations. Or he and his team could rewrite it from scratch without using React, a decision that would add anywhere from six to 12 months to the development timetable.

### A frontend of our own

Cegłowski attempted to lure those users to Pinboard for their bookmarking needs, hawking it as an alternative. But first, fans had a few suggestions.

Cegłowski created a Google doc and shared it on social media, then watched in wonder as dozens of anonymous fans worked together to map out features and improvements, such as the ability to choose between multiple accounts in the bookmarklet, or to subscribe to tags as well as user/tag and tag/tag combinations. “Having worked at large tech companies, where getting a spec written requires shedding tears of blood in a room full of people whose only goal seems to be to thwart you, and waiting weeks for them to finish, I could not believe what I was seeing,”

### Interview: Sarah Allen

One of the key innovations of After Effects was that we thought of time as going into the monitor, like the z-axis, when in math time is [usually] across the x-axis. Now you would call that human-centered design.

I’d had this idea that apps would allow people to do different things—grandparents [could] read their kids stories and make words come to life. But what the world actually “needed” was just Desperate Housewives and Lost.

Software is everywhere. That’s not an altogether good thing. Farmers now buy tractors which they are not permitted by law to repair themselves. We’re creating a very fragile society by allowing companies to sell machines that just stop working. Each of us needs to take responsibility for the software we write.

## 19 - Planning

### Planning for momentum 

suggested that people who work in complex domains shouldn’t try to solve entire problems in their heads and then implement the solution. Instead, they should write about them first.

### An IC's guide to roadmap planning

The best products are opinionated, built with distinct intention and a clear vision.

### Software development as a wicked problem

One group sees the problem as one of data standardization across the enterprise, while the other perceives it as one of addressing subsidiaries’ local reporting requirements. Which viewpoint stakeholders hold is ultimately a political matter rather than a technical one.

Robert Glass argues that the top two causes of late and over-budget software projects are poor estimation and unstable requirements. Both are related to wickedness. 

Complex projects are hard to estimate and requirements difficult to pin down due to internal or end users’ continually shifting perceptions of what they need.

essential truth: The success of complex software projects hinges on trust-based communication.

grows more challenging as projects become more complex and distributed—not only because of the number of people involved, but also because team members’ and other stakeholders’ views and beliefs may differ greatly. In other words, due to issues of wickedness.

the trick is to surface and reconcile diverse viewpoints, making multiple perspectives explicit so all parties can develop a shared understanding of contentious issues.

 “The problem is not truth, the problem is trust.”

### Just hire great people?

If we don’t give our people the resources they need to succeed—like fair expectations, room to grow, and a place in the company strategy—they may shoulder the blame for not living up to the culture’s expectations of “greatness.”
