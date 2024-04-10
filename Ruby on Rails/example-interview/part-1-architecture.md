<!-- omit in toc -->
# Ruby on Rails example interview: Part 1, Architecture

<!-- omit in toc -->
## Contents

- [Intro](#intro)
- [Question: What’s your story?](#question-whats-your-story)
- [Question: Are you familiar with the SOLID principles?](#question-are-you-familiar-with-the-solid-principles)
- [Question: Are you familiar with *dependency inversion*? Can you give an example?](#question-are-you-familiar-with-dependency-inversion-can-you-give-an-example)
- [Question: Sometimes it’s best to avoid long chains of method calls. Can you think of an example?](#question-sometimes-its-best-to-avoid-long-chains-of-method-calls-can-you-think-of-an-example)
- [Question: Do you generally prefer inheritance, or composition?](#question-do-you-generally-prefer-inheritance-or-composition)
- [Question: What is an example of polymorphism?](#question-what-is-an-example-of-polymorphism)
- [Question: What are microservices?](#question-what-are-microservices)
- [Conclusion](#conclusion)

## Intro

There were two interviewers, both senior engineers.

To start off, they said they like my blog because it gave them “a wealth of information to work with.” They mentioned a post about server-sent events, which they just recently had a use case for.

## Question: What’s your story?

## Question: Are you familiar with the SOLID principles?

I couldn’t remember the exact meaning of the acronym, but I said I was familiar and gave a general definition. They said that’s what they were looking for.

## Question: Are you familiar with *dependency inversion*? Can you give an example?

I gave the example of a logger injected into an object at instantiation, rather than being instantiated by the object being logged. They noted that this is a type of dependency inversion called *dependency injection*.

## Question: Sometimes it’s best to avoid long chains of method calls. Can you think of an example?

I gave the example of a wrapper/adapter class for an external API. This can prevent long chaining wherever the API is used in the code base, but more importantly it hides the details of the API to objects that don’t need to know them, and exposes only a simplified API, nothing more than is actually needed.

## Question: Do you generally prefer inheritance, or composition?

I said I generally prefer composition unless the problem clearly lends itself to inheritance and is limited in scope, depth, or possibility of future change. I mentioned POODR by Sandi Metz, where I was first introduced to this idea.

## Question: What is an example of polymorphism?

I fumbled with an example that’s more related to duck typing than polymorphism (the Gilded Rose Kata), but then I recovered by talking about polymorphic associations in Rails, and how we tried to avoid them at my last job. They said that’s what they were looking for.

The fumble wasn’t too bad, because I was buying myself time to give a better answer, and in doing so I showed off a little achievement of mine, a contribution I’d made to Exercism with an adaptation of the Gilded Rose Kata. Also, later in the interview when I asked about a culture of learning, my interest in katas came up again when the interviewers said the company has a group dedicated to coding challenges.

## Question: What are microservices?

The interviewers started by saying I probably didn't have experience with them and this is a question for more senior devs, but I chimed in when he mentioned “drawing app boundaries” and I described domain refactoring (Packwerk) at my last job. I continued, saying that's not microservices according to my understanding (and I described what microservices are technically), and they approved and described their microservices setup a bit.

Then I asked questions about their microservices, which showed my curiosity.

## Conclusion

At the 30-minute mark, they stopped and asked if I had any questions.

I asked about a culture of learning at the company (mentioning what I’d learned in my research), whether there’s freedom to change to different teams, and what advancement/growth opportunities look like.

The interview ended at 40 minutes.

My overall feeling: I fumbled a couple times but recovered well.
