# Notes - Day 0

_<a href = "https://simpleprogrammer.com/solving-problems-breaking-it-down/">"How to Solve Programming Problems"</a>_

Common mistakes: improper allocation of time. Not thinking through problem before beginning coding. Solving problem on 1st iteration.

Simple set of steps to follow

1. Read the problem completely twice - You want to make sure you completely understand the problem. A good test of this is whether or not you can explain the problem to someone else.
2. Solve the problem manually with 3 sets of sample data - It’s very important that when you solve a problem manually, you recognize what your brain is actually doing to solve the problem. You may need to write out all the things you are normally storing in your head.
3. Optimize the manual steps - It is much easier to rearrange and reconstruct and idea or algorithm in your head than it is in code. What you want to do here is figure out if there is another way you can solve the problem easier, or if there are some steps you can cut our or simplify.
    -Up to 70% of time should be spent in steps 1-3
4. Write the manual steps as comments or pseudo-code - What we want to do here is capture all the steps we created and now either put them into our editor as comments or write them as psuedo-code that we can translate to real code. By doing this, we can know exactly what the structure of the code we are going to write is going to look like which makes the job of filling in the actual code later trivial.
5. Replace the comments or psuedo-code with real code - Take each comment and convert it into a real line of code.
6. Optimize the real code - Sometimes this step isn’t necessary, but it’s worth taking a look at your code and figuring out if you can cut out a few lines or do something simpler.

Any language you expect to be able to solve algorithm type problems in, you should know how to do the following things:

- Create a list
- Sort a list or array
- Create a map or dictionary
- Loop through a list, or dictionary
- Parse strings
- Convert from string to int, int to string, etc.

Many times you will find that a problem itself involves multiple large steps or is very complicated. In those instances, you will want to try and find a way to cut the problem directly in half and then following the process above for each half. This method of tackling a problem is called “divide and conquer”. A good way to know where to break a problem in half is to think about what part of the problem if already given to you would make solving the rest easy.

_<a href = "https://anthony-moore.medium.com/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-6ab2302b8e8c">"Act like you make $1000/hr"</a>_

Many people waste much of their time on pointless, low-quality activities that don’t help them reach their true goals — their mission. Truth is, most people value their time at far, far less than it’s worth. They say yes to things they have no business doing. They give away their talents, attention, and effort to others.

But what if you placed a high value on your time? How would that change you? Your life? Your family? Your future?

Imagine that an hour of your time is worth $1,000. What would your life look like? What people would you stop putting up with? What problems would you stop wasting time on? What things would you stop, and start doing? Your results would be incredible. You’d become exponentially more productive, focused, and effective.

If you let it, your world and the people around you will take all your time. Your time is not unlike your paycheck; if you don’t budget for things, you’ll have nothing left over by the end of the month. We’re all busy, with work, our families, our friends. It’s not bad to be “busy.” But in the words of best-selling author Jeff Goins: “The most successful people I know are not busy. They’re focused.”

Are you focused, making tangible action steps towards what truly matters? …Or are you just “busy?” When you’re busy, you are on autopilot. You can’t see the hours slipping away, time you’ll never get back. Who’s in charge of your time? You, or everyone else?

Extremely successful people don’t tolerate busywork or distraction. They have crystal clear vision on their goals, and do what they need to do to get there, every single day.

Deep work means absolutely not tolerating distractions and producing monumental quality and quantity in a very short time. This is how you can complete far more with focused efforts than unfocused efforts with far more time. If you don’t manage your time, it will manage you.

You teach people how to treat you. If you let people know your time is free and low-valued, people will treat it as such. But if you teach people that your time is expensive, important, and valuable, then people will respond in kind.

What you think is what you become. If you think your time is worth a few bucks an hour, that you’ll begin to act like it. You’ll find yourself saying “yes” to meaningless, pointless obligations. But if, in your heart, you know your time is valuable…People will recognize that. People will respect that. People will treat you differently.

If you don’t treat yourself and your time with respect, you will become unhappy, resentful, and tired. Your body and mind long for mastery and freedom; you can’t have those things if your time is cheap and easily taken. You become what you are. You attract what you look for.

Back in my early days of writing, I didn’t think I was much of a writer. So I spent a lot of time on low-quality activities, like begging other low-tier/no-name bloggers to let me write guest posts. No one responded to me. I rarely was invited to write. I think people could see how little I valued myself, and didn’t want to promote my message. I don’t even blame them. Years later, I finally began seeing my time as very important. I began saying “no” to almost everything. I had a mission, and I became unwilling to fill my valuable time with things that wouldn’t help me achieve my goal. I turned down high-paying, exciting, interesting opportunities…because they weren’t the right fit. In the end, they were all wasting time I needed to focus on my mission.

You probably need to say “no” more. Every time you say yes to something, it means you’re saying “no” to a dozen other opportunities. The world’s most successful and extraordinary people say no to almost everything, but yes to a few things. Really successful people say no to most things, because most things won’t get them to where they truly want to be.

This process of weeding out the merely “good” for the truly great opportunities is easier when you value your time at $1,000/hour. Anything you can honestly justify doing for $1,000/hour is probably a good thing.

_<a href = "https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/">"How to think like a programmer"</a>_

The best way involves a) having a framework and b) practicing it

So, what should you do when you encounter a new problem?

Here are the steps:

1. Understand: Know exactly what is being asked. Most hard problems are hard because you don’t understand them. How to know when you understand a problem? When you can explain it in plain English.

This is why you should write down your problem, doodle a diagram, or tell someone else about it (or thing… some people use a rubber duck).
2. Plan: Don’t dive right into solving without a plan. Plan your solution! Nothing can help you if you can’t write down the exact steps. In programming, this means don’t start hacking straight away. Give your brain time to analyze the problem and process the information.

To get a good plan, answer this question: “Given input X, what are the steps necessary to return output Y?”

Side note: Programmers have a great tool to help them with this… Comments!
3. Divide: Break it into sub-problems. These sub-problems are much easier to solve. Then, solve each sub-problem one by one. Begin with the simplest. Simplest means you know the answer (or are closer to that answer). After that, simplest means this sub-problem being solved doesn’t depend on others being solved. Once you solved every sub-problem, connect the dots. Connecting all your “sub-solutions” will give you the solution to the original problem.
4. Stuck?: The difference is the best programmers/problem-solvers are more curious about bugs/errors than irritated. In fact, here are three things to try when facing a whammy:
    - Debug: Go step by step through your solution trying to find where you went wrong. Programmers call this debugging.
    - Reassess: Take a step back. Look at the problem from another perspective. Is there anything that can be abstracted to a more general approach?
    - Research: No matter what problem you have, someone has probably solved it. Find that person/solution. In fact, do this even if you solved the problem!
5. Practice: Practice. Practice. Practice. It’ll only be a matter of time before you recognize that “this problem could easily be solved with <insert concept here>.”
6. Conclusion: Now, you know better what it means to “think like a programmer.”

_<a href = "https://www.mindtools.com/pages/article/newTMC_5W.htm">"The 5 Whys"</a>_

Sakichi Toyoda, the Japanese industrialist, inventor, and founder of Toyota Industries, developed the 5 Whys technique in the 1930s. It became popular in the 1970s, and Toyota still uses it to solve problems today. The method is remarkably simple: when a problem occurs, drill down to its root cause by asking "Why?" 5 times. Then, when a counter-measure becomes apparent, you follow it through to prevent the issue from recurring.

Can use 5 Whys for troubleshooting, quality improvement, and problem solving, but it is most effective when used to resolve simple or moderately difficult problems.

May not be suitable if you need to tackle a complex or critical problem. This is because 5 Whys can lead you to pursue a single track, or a limited number of tracks, of inquiry when, in fact, there could be multiple causes.

How to use the 5 whys:

1. Assemble a Team - Gather together people who are familiar with the specifics of the problem, and with the process that you're trying to fix. Include someone to act as a facilitator, who can keep the team focused on identifying effective counter-measures.
2. Define the Problem - If you can, observe the problem in action. Discuss it with your team and write a brief, clear problem statement that you all agree on. For example, "Team A isn't meeting its response time targets" or "Software release B resulted in too many rollback failures." Then, write your statement on a whiteboard or sticky note, leaving enough space around it to add your answers to the repeated question, "Why?"
3. Ask the First "Why?" - Ask your team why the problem is occurring. For example, "Why isn't Team A meeting its response time targets?" Asking "Why?" sounds simple, but answering it requires serious thought. Search for answers that are grounded in fact: they must be accounts of things that have actually happened, not guesses at what might have happened. This prevents 5 Whys from becoming just a process of deductive reasoning, which can generate a large number of possible causes and, sometimes, create more confusion as you chase down hypothetical problems.
4. Ask "Why?" Four More Times - For each of the answers that you generated in Step 3, ask four further "whys" in succession. Each time, frame the question in response to the answer you've just recorded.
5. Know When to Stop - You'll know that you've revealed the root cause of the problem when asking "why" produces no more useful responses, and you can go no further. An appropriate counter-measure or process change should then become evident. If you identified more than one reason in Step 3, repeat this process for each of the different branches of your analysis until you reach a root cause for each one.
6. Address the Root Cause(s) - Now that you've identified at least one root cause, you need to discuss and agree on the counter-measures that will prevent the problem from recurring.
7. Monitor Your Measures - Keep a close watch on how effectively your counter-measures eliminate or minimize the initial problem. You may need to amend them, or replace them entirely. If this happens, it's a good idea to repeat the 5 Whys process to ensure that you've identified the correct root cause.

Summary: The 5 Whys strategy is a simple, effective tool for uncovering the root of a problem. You can use it in troubleshooting, problem-solving, and quality-improvement initiatives. Start with a problem and ask why it is occurring. Make sure that your answer is grounded in fact, and then ask the question again. Continue the process until you reach the root cause of the problem, and you can identify a counter-measure that will prevent it from recurring. Bear in mind that this questioning process is best suited to simple or moderately difficult problems. Complex problems may benefit from a more detailed approach, although using 5 Whys will still give you useful insights.

**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**
