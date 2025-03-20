# **Empowering Businesses with AI: The Xmacna Story**

## **Introduction**

We are **Xmacna.ai**, a platform dedicated to facilitating the transition of businesses into an AI-centric perspective. Our roots trace back to **Plataforma Redigir**, a B2B EdTech company that aids schools in teaching writing skills to children.

## **The Challenge**

**Plataforma Redigir** has always been AI-focused, constantly researching innovative methods to assist in reviewing the essays submitted by students. This process, traditionally performed by human professionals, has been a significant growth bottleneck due to the scarcity of expertise required for the job.

## **The First Breakthrough**

Our first breakthrough came with the introduction of **"Bárbara"**, an AI bot designed to alleviate this bottleneck. **Bárbara** was programmed to generate a "Final Comment" based on all the reviewer's comments on an essay, providing the student with recommendations and guidance. This innovation resulted in a 30% time-saving per essay and improved the average student's star rating of the reviews from 4.2 to 4.5. However, the six-month development time from idea to production posed a challenge due to our small developer team and an already overwhelming backlog.

## **The Game Changer: Flowise**

Enter **Flowise**, a game-changer that revolutionized our approach to AI bot creation. **Flowise** was not just a tool; it was a catalyst that democratized the ability to create AI bots within our organization. It empowered all of our teams to create bots that automated and enhanced their tasks, effectively decentralizing the bot creation process from the IT department to the wider team. This led to a significant increase in our rate of innovation. Within the first week, we had two bots deployed and operational, many others brewing, neither of which were developed by IT.

![Amount of ChatFlows](https://staticredigir.azureedge.net/flowise-briefing/5_Flowise_ChatFlows.png)

_Amount of ChatFlows_

## **Introducing "Cléber"**

One of these was **"Cléber"**, a Data Science bot designed to bridge the gap between our data and the schools. Despite having a dashboard and offering data, we realized it wasn't sufficient. Hence, we had employees whose primary job was to interact with the school and provoke actions based on our data interpretation. With **Flowise**, our Customer Care team quickly created a bot that ingested raw data, analyzed it based on our criteria, and generated an interactive HTML with insights and calls to action. **Cléber** performed this task flawlessly.

![Cleber Flow](https://staticredigir.azureedge.net/flowise-briefing/3_Cleber_Flow.png)

_Cléber's ChatFlow_

### **How Cléber Works**

- It uses an `OpenAI Function Agent` that knows how to convert a _school_name_ and a _time_period_ into a full blown personalized Html analysis through tools.
- A `Custom Tool` connected to our business API that takes a _school_name_ and tries to return a _school_id_.
- A `Custom Tool` that takes a _school_id_ and a _time_period_ and returns the _raw_data_.
- A `Chain Tool` connected to a `Conversation Chain` that interprets the _raw_data_ according to our criteria and generates an _analysis_.
- Finally, a `Chain Tool` that takes an _analysis_ and generates an interactive _HTML_ based on examples (few-shot).

One example input that "Cléber" takes would be something like this:

- Give me the html for the engagement data for School X for the month of April

`OpenAI Function Agent` then understands that it needs an _analysis_ for the _HTML_, need _raw_data_ for the _analysis_, need a _school_id_ and _time_period_ for the _raw_data_ and a _school_name_ for the _school_id_.

If the user don't provide some of this information, it asks the user until it has all the data it needs.

If the school name is ambiguous, the agent present the options and asks the user to choose one.

Here is the final output:

![Cleber Output](https://staticredigir.azureedge.net/flowise-briefing/4_Cleber_Html.png)

_Cléber's Output_

## **Other Bots**

![Support Bot](https://staticredigir.azureedge.net/flowise-briefing/6_Super_bot_avr.png)

**Support Bot**

- Uses a `Multi Prompt Chain` with one `Prompt Retriever` per functionality on the app, the `Conversational Agent` at the front is given this `Multi Prompt Chain` as a `Chain Tool`, and is instructed on how to ask for a specific topic

![Assistant Bot](https://staticredigir.azureedge.net/flowise-briefing/7_Jarvis.png)

**Assistant Bot**

- An `OpenAI Function Agent`, with infinite memory using `Zep Memory`, and access to `Web Browser` and `Serp API`. Its prompt contains context specific to its user's workflow, and the `sessionId` is unique per user, as to preserve the full story.

## **The Future: Xmacna.ai**

While **Cléber** was being developed, other teams were simultaneously creating a **Support Bot**, a **Salesman Bot**, an **Executive Secretary Bot**, and more. This flurry of innovation was made possible by **Flowise**. Inspired by this, we founded **Xmacna.ai**. We aim to leverage our expertise in automating business processes using the tools and knowledge we developed for **Redigir**. We offer digital employees, intelligent and tireless workers operating 24/7, trained to handle your business operations efficiently.

_Rafael Reis_
_CTO - Xmacna_
*https://xmacna.ai*
