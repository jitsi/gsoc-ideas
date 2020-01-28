# Videobridge Telemetry Dashboard

## Prerequisites
Prior knowledge in these areas will be an advantage for this project, but none of them
are strictly necessary:

* Git
* Javascript

## The project:
The Jitsi Videobridge currently accumulates lots of statistics, but currently
the only way to view it is in raw JSON via an HTTP request.  Since the
videobridge is the heart of most Jitsi calls, it's important we be able to
diagnose any problems quickly and easily.  What we need is a better visual
representation of the wealth of information we already collect.

* Implement a dashboard capable of pulling the data from the JVB and rendering
it in a usable way
* Allow for 'drilling' into the information: start with a high-level view
(e.g. some information for each conference) and add more information
(conference details, endpoint details, receive/send details) as the user clicks
through

## Pro tips for your application
Your GSoC application would be great if you included what frameworks you plan
on using and a rough design of how you intended to implement it.

If you have any questions, feel free to [create an issue](https://github.com/jitsi/gsoc-ideas/issues/new)!

## Mentors

@bbaldino
