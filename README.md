# [Christmas Conundrum]

> WEB-115 Final Project: an interactive, browser-based story built with HTML, CSS and JavaScript.

---

## Team Members and Roles

| Name | GitHub Username | Responsibilities |
|------|-----------------|------------------|
| [Kjai Hamblin] | [@khamwtcc] | [Flowchart, Storywriting, JavaScript] |
| [Parker Mozingo] | [@MrsMozingo] | [HTML, CSS] |
| [Jason Wendel] | [@jaswen2003] | [Flowchart, Storywriting, JavaScript] |

## Application Overview

### Story
[In this story you are a regular person with a hectic family doing your best to navigate a Christmas party that could potentially go wrong in the blink of an eye.]

### Gameplay
[In this story you have to navigate throughout the day by making your own decisions. The goal is to make it to gift giving time without anything going wrong so you can give a family member the perfect gift.]

### Rules and Navigation
- [In this game you have to click on one of two choice buttons provided depending on the situation you are currently in to progress through the day.]
- [Includes some randomized events for different ways the day can go.]

## Story Flowchart

```mermaid
flowchart LR
    %% ---------- Start ----------
    S1["Scene 1:<br>Holiday Gathering at Parents home"]
    S1 --> D1["Decision 1:<br>Invite Best Friend"]
    S1 --> D2["Decision 2:<br>Wait for Chaos to Unfold<br>(Random Event)"]

    %% ---------- Decision 1 branch ----------
    D1 --> S1A(["Scene 1A:<br>Brother gets furious as he doesnt like your best friend."])
    S1A --> D1A["Decision 1A:<br>Escalate the Situation"]
    S1A --> D1B["Decision 1B:<br>De-escalate the Situation"]
    D1A --> S1B(["Scene 1B:<br>You argue that your best friend is a cooler/better person. You argue but relatives resolve it by sending your best friend home."])
    D1B --> S1C(["Scene 1C:<br>You argue that you and your best friend have a close bond and its no big deal.<br>Brother deals with it."])

    %% ---------- Decision 2 branch: random events ----------
    D2 --> E1["Event 1:<br>Criminal Uncle Shows up to the Party"]
    D2 --> E2["Event 2:<br>Your Aunt Had too Much to Drink"]
    D2 --> E3["Event 3:<br>Your Sister Breaks an Expensive Vase"]

    %% Event 1
    E1 --> E1S2(["Event 1, Scene 2:<br>You open the door to your wanted uncle."])
    E1S2 --> E1DA["Event 1, Decision A:<br>Call the Cops"]
    E1S2 --> E1DB["Event 1, Decision B:<br>Take things into your own hands"]
    E1DA --> E1S3A(["Event 1, Scene 3A:<br>Cops arrive and remove him from the property.<br>Time for gift giving."])
    E1DB --> E1S3B(["Event 1, Scene 3B:<br>Brawl starts and cops get called.<br>(Story Ends)"])

    %% Event 2
    E2 --> E2S1(["Event 2, Scene 1:<br>Relative starts drunkenly screaming while pouring another glass."])
    E2S1 --> E2DA["Event 2, Decision A:<br>Join in on the Fun"]
    E2S1 --> E2DB["Event 2, Decision B:<br>Criticize Drunken Relative"]
    E2DA --> E2S3A(["Event 2, Scene 3A:<br>You and your aunt clink glasses and have another drink.<br>Time for gift giving."])
    E2DB --> E2S3B(["Event 2, Scene 3B:<br>Your aunt snaps back and criticizes your parents. She gets kicked out and the festivities finish early.(Story Ends)"])

    %% Event 3
    E3 --> E3S1(["Event 3, Scene 1:<br>Glass breaks and scatters across the floor"])
    E3S1 --> E3DA["Event 3. Decision A:<br>Clean the Mess"]
    E3S1 --> E3DB["Event 3, Decision B:<br>Yell at your Sibling"]
    E3DA --> E3S3A(["Event 3, Scene 3A:<br>Mother is frustrated, but thanks you for helping and cools down.<br>Time for gift giving."])
    E3DB --> E3S3B(["Event 3, Scene 3B:<br>Mother gets mad at you for yelling instead of helping. You are made to sit out of the gift giving.<br>(Story Ends)"])

    %% ---------- Paths that merge into Decision 3 (dashed in the original) ----------
    D3["Decision 3:<br>Give a gift to a Family Member"]
    S1B -.-> D3
    S1C -.-> D3
    E1S3A -.-> D3
    E2S3A -.-> D3
    E3S3A -.-> D3

    %% ---------- Decision 3 branch: gifts ----------
    D3 --> D3A["Decision 3A:<br>Give Gift to Parent"]
    D3 --> D3B["Decision 3B:<br>Give Gift to Sibling"]
    D3A --> D3AA["Decision 3AA:<br>Give Mom Tea Set. She is appreciative."]
    D3A --> D3AB["Decision 3AB:<br>Give Dad Grilling Tools. He is incredibly happy with the gift."]
    D3B --> D3BA["Decision 3BA:<br>Give Sister Makeup. She likes the gift and adds it to her makeup drawer"]
    D3B --> D3BB["Decision 3BB:<br>Give Brother Video Game. He says its one he isnt interested in and moves on."]
```
