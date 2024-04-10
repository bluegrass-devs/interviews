<!-- omit in toc -->
# Ruby on Rails example interview: Part 2, Rails

<!-- omit in toc -->
## Contents

- [Intro](#intro)
- [Question: What's your story?](#question-whats-your-story)
- [Question: Can you describe what happens to an HTTP request from start to finish in a Rails app?](#question-can-you-describe-what-happens-to-an-http-request-from-start-to-finish-in-a-rails-app)
- [Question: How would you troubleshoot a slow database query?](#question-how-would-you-troubleshoot-a-slow-database-query)
- [Question: Are there any cases where a database query can't be sped up with SQL?](#question-are-there-any-cases-where-a-database-query-cant-be-sped-up-with-sql)
- [Question: How would you refactor a fat model?](#question-how-would-you-refactor-a-fat-model)
- [Question: what does “clean code” look like to you?](#question-what-does-clean-code-look-like-to-you)
- [Question: Are you more comfortable on the front or back end?](#question-are-you-more-comfortable-on-the-front-or-back-end)
- [Conclusion](#conclusion)

## Intro

There was a 30-minute break between the first interview and this one.

There was one interviewer, the hiring manager.

The interviewer started by shared a bit of his story. I asked about resources for self-teaching UX, which he said he'd done earlier in his career.

I was also prepared with his LinkedIn bio copied into my notes, which told me a few things that are important to him.

## Question: What's your story?

The interviewer mentioned that he’d read my cover letter and was familiar with my story as I’d told it there.

So I added a twist to what he already knew: how my teaching background informs me as a developer.

## Question: Can you describe what happens to an HTTP request from start to finish in a Rails app?

*Gulp.* I’d read about this several times, and I’ve even gone through the book *Rebuilding Rails* which shows it in a hands-on way. But I still struggled to describe it in detail.

## Question: How would you troubleshoot a slow database query?

I said I’d check the SQL in the logs (often the problem is associations that need to be preloaded), check for missing indexes, and *maybe* write a custom SQL query but only if absolutely needed, because custom SQL is less maintainable.

Then he asked a follow-up question.

## Question: Are there any cases where a database query can't be sped up with SQL?

*Huh?* I mentioned bulk inserts/updates as a special case, and maybe the data modelling could be improved, but that a query very rarely can't be made sufficiently fast with SQL.

Then he put the cards on the table and described a recent real-world situation at Doximity where a table with millions of records became really slow in queries, after no change to the code. It turns out the indexes weren't being used anymore (because of reasons I didn't catch) and they had to force the DB to use the indexes.

His repeated questioning made it feel like he expected me to be familiar with this edge case or something like it. But on the other hand I’m not sure, because he said that he and several other engineers were stumped for a long time as they looked for what was causing the issue.

## Question: How would you refactor a fat model?

He referred to the README section that I added in the take-home assignment, *“Design choices by Felipe”*, specifically a point I made about how I don’t love service objects but I’m fine using them until a more suitable pattern emerges.

To answer the question, I used notes that I’d made on the book *Layered Design for Ruby on Rails Applications*, which (among other things) provides lots of design alternatives to fat models, some of which I’ve used myself. I had these notes ready among my interview notes. I mentioned the book and he made a note of it.

The interviewer's stance became clear in our discussion: he isn't a fan of breaking up a fat model only to separate the logic into lots of tiny isolated classes. He doesn't see fat models as too huge of a problem. So I tweaked my stance accordingly.

## Question: what does “clean code” look like to you?

I said I don’t love the “clean” terminology because it introduces too much of an aesthetic element, and I pointed to other aspects instead: clear names, and code that is easily changeable.

I said that paradoxically, long variable/method names are ugly but clearer. A fat model is easier to improve upon than a design pattern that is applied too early or too broadly. (I thought he would appreciate hearing that, given his above-mentioned opinions.)

He said those are the kinds of things he was looking to hear in my answer. He mentioned two other things: “no duplication” and something else that I can’t remember.

## Question: Are you more comfortable on the front or back end?

I said I enjoy full stack work and I'm comfortable with front-end JavaScript frameworks, but I'm more productive on the back end.

He said he saw my personal projects using Hotwire and asked how I like it.

I said I like Hotwire and it’s pretty easy. I said most parts of most apps could easily use Hotwire instead of a JS framework. Only highly interactive apps/pages/components really need a lot of JS.

He asked for examples of where that line could be drawn. I said mapping apps, online word processors, and in short, anything outside the typical CRUD app. It also depends on what your app looks like now, e.g. a Hotwire app where you need a fancy autocomplete field could just as well have it made in Hotwire too, rather than adding a JS framework just for that one component.

## Conclusion

At the one-hour mark, he said he could stay a few minutes if I had any questions.

I asked about a culture of learning (just as in the first interview), whether there were many early-career developers at Doximity and what mentorship looks like there, and whether Doximity’s position on the board of the Rails Foundation impacts the engineers’ day-to-day at all. (He said it doesn’t; it’s just a financial thing.)

My overall feeling: it was OK. I feel like I got stuck in the weeds of details too often, but maybe that’s because of the interviewer’s style of questions.
