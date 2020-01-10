[Princiya and Stephen's issue](https://github.com/nodejs/mentorship/issues/85)

#[Mentorship Diary] Princiya and Stephen
(Mentorship Round 1) Stephen will be mentoring Princiya on diagnostics.

#Kickoff meeting (5 August 2018)
---
[Youtube meeting recording](https://youtu.be/FmAcQiqKp1A)

#Scope Introduction
---
Stephen will be mentoring about diagnostics, with focus on time-travel debugging and tooling around the CPU profiler.

>The Diagnostics Working Group leads various initiatives to improve the facilities for
understanding what goes on within a Node.js application. They maintain several tools
and parts of Node.js core code to support those needs.

#Goals & Expectations
---
- Learn about CPU Profiler output and identify useful ways to visualize the output data
- Learn about [Time-Travel Debugging](https://github.com/nodejs/diagnostics/issues/164) and how to get involved in moving that forward

#Availability
---
Meeting times will be coordinated through Slack. Stephen is available mostly any time except Tuesday and Wednesday mornings. The meetings will (probably) be on Zoom.

#Privacy & CoC
---
We are both comfortable recording sessions and will record sessions and link to them on github.

#Meeting 2 (August 8, 2018)
---
Forgot to record the meeting, sadly. I'll remember next time. sweat

- Discussed `node --inspect` and using Chrome Dev Tools
- Introduced the [v8-profiler](https://www.npmjs.com/package/v8-profiler) module
- Introduced [async_hooks](https://nodejs.org/api/async_hooks.html)

Princiya will experiment with `v8-profiler` and `async_hooks` and consider novel ways to connect the two to capture multiple profiles and connect them together.

#Meeting 3 (August 23, 2018)
---
Discussed:

- How sampling profilers work
- How garbage collectors track memory
- How async_hooks correlates callbacks of async tasks to the point at which it was called, and the benefits

Princiya has decided to write a blog post about things that might not be as clear to someone outside of the diagnostics bubble. It should be a big help for introducing people to the subject of diagnostics. 

#Meeting 4 (September 12, 2018)
---
Discussed:

- Currently active development (trace_events, async_hooks destroy/resource ideas)
- Differences with Firefox dev tools
- Needs of Diagnostics WG in terms of documentation, outreach, etc.

I will continue to work with Princiya to make the Diag WG more approachable and to encourage more community involvement.

[Here is my first blog post](https://princiya777.wordpress.com/2018/09/09/node-js-diagnostics/)


