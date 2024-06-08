---
layout: posts
title: Sandboxing Scanners - A Leap into the Driverless Realm (GSoC '23 Report)🦘🔮
date: 2023-10-30
tags: [GSoC, Report]
excerpt: Final report for GSoC 2023
---

## A Brief Summary

1. [Link to PR in PAPPL](https://github.com/michaelrsweet/pappl/pull/249), which starts the scan journey by integrating PAPPL for Scanners.
2. [Link to MetaScan repository](https://github.com/Kappuccino111/MetaScan), which comprises the ScaniVerse.
3. [Link to SaneScanner-PapplRetrofit repository](https://github.com/Kappuccino111/SaneScanner-PapplRetrofit), the retrofit implementation for scanning drivers.

**_What are we waiting for? Let's dive into the dream!_**

## Unveiling the Enigma: Sand-Boxed Scanner Application Framework 🎭
In the ever-evolving landscape of technology, an immense void has been begging for attention – scanning devices. While printers, our desktop buddies, have soared into the future, the scanners often felt left in the past. However, with the Sand-Boxed Scanner Application Framework, the tides are turning.

## Genesis of the Idea 💡
The mission of this project was straightforward: enable devices without driverless scanning capabilities to masquerade as driverless wonders using PAPPL's Scanner Application Framework. Beyond mere emulation, this application also sets the stage for a new generation of sandboxed Scanner Applications.

## Community Bonding & the Code Dive 🤝📖

The adventure began with a thorough exploration of the PAPPL codebase, which felt like deciphering an ancient script where each line told a story. Fortunately, the code's API can be better understood through this [documentation](https://www.msweet.org/pappl/pappl.html). Initial documentation changes were made using [CodeDoc](https://www.msweet.org/codedoc/).

## The PAPPL Blueprint 🗺️

![PAPPL Blueprint](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/phk21dilskhh1c99wvjz.png)

As evident, the essence of PAPPL was clearly aligned with printers. My challenge? To weave together the stories of printers and scanners, particularly for multifunctional devices.

### Chiseling the Sculpture 🛠️

The foundation stone was laid by sketching the architecture of multifunction device scanning.

#### Client's Odyssey 🧭


![Client Flowchart](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/usk9y5f14zj0t3fzq97q.png)


#### Server's Dance 🎻

![Server Flowchart](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kgzu0z707bun5z24p9ur.png)


I adopted the MOPRIA Scan Specifications, initiating a series of requests and responses. Most of these interactions were in the eSCL format, encompassing areas such as Scan Capabilities, Scanner Status, Scan Jobs, URI Generation, and Document Retrieval.

To make this work, I had to carefully design data structures. This involved translating XML and making sure the information flowed smoothly to and from the scanner drivers.

#### Mimicking the Scanner: The Dummy Driver ✨

To test the waters, a facsimile of the scanner driver was created. From capturing the request format to simulating the , it was all about shadowing the scanner every move.


The work on the above can be checked [here](https://github.com/michaelrsweet/pappl/pull/249).

### Bridging the Old and New 🌉

While the first phase above laid the foundation, the sequel was about blending SANE (Scanner Access Now Easy) into our potion. With PAPPL-RETROFIT acting as the crucible, the old met the new, with SANE API's magic dust sprinkled generously. But the enchantment doesn’t end here; it's an ongoing saga. Dive into the SANE implementation [here](https://github.com/Kappuccino111/SaneScanner-PapplRetrofit).


### The Path Ahead: Uncharted Territories 🛤️

While we have set the stage and choreographed the initial dance, the performance is far from over. Here's a glance at what lies on the horizon:

**Compatibility Checkpoints**: Testing is the mirror that reflects an application's true potential. Testing the system with multiple scan clients is currently on the to-do list, ensuring the smooth waltz of every byte and bit.

**Merging of Realms**: At present, the pappl-retrofit application stands in its own independent domain. However, in the near future, it is set to merge with the main PAPPL retrofit repository, bringing together the old and new worlds.

### Dreaming Beyond the Horizon: ScaniVerse 🌌


![ScaniVerse](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gysl4gjijdpxhyq0oqgq.png)


During this journey, an epiphany struck. Why restrict ourselves to mere scanning? Why not a universe – a Scaniverse! A cosmos where scanning coalesces with metadata archival, creating a self-contained realm. Dive into this expansive universe, [here](https://github.com/Kappuccino111/MetaScan). And if curiosity still tugs at your heartstrings, join me as I unfold the ScaniVerse tale at the Ubuntu Summit 2023 in Riga. [Explore more about my talk](https://events.canonical.com/event/31/contributions/192/).



### A Bow to the Maestros 🙏

My gratitude to the guiding stars on this journey - [Till Kamppeter](https://at.linkedin.com/in/kamppetertill), [Aveek Basu](https://www.linkedin.com/in/basuaveek/), [Rishabh Maheshwari](https://in.linkedin.com/in/rishabh-maheshwari-41189a224), and [Deepak Patankar](https://in.linkedin.com/in/deepak-patankar-797622148?trk=public_post_feed-actor-name).

A symphony of appreciation is dedicated to **Till Kamppeter**. Without his baton orchestrating the path, this musical journey through code would have been silent.




