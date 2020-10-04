+++
title = "This Month in Rust GameDev #14 - September 2020"
date = 2020-10-05
transparent = true
draft = true
+++

Welcome to the 14th issue of the Rust GameDev Workgroup's
monthly newsletter.
[Rust] is a systems language pursuing the trifecta:
safety, concurrency, and speed.
These goals are well-aligned with game development.
We hope to build an inviting ecosystem for anyone wishing
to use Rust in their development process!
Want to get involved? [Join the Rust GameDev working group!][join]

You can follow the newsletter creation process
by watching [the coordination issues][coordination].
Want something mentioned in the next newsletter?
[Send us a pull request][pr].
Feel free to send PRs about your own projects!

[Rust]: https://rust-lang.org
[join]: https://github.com/rust-gamedev/wg#join-the-fun
[pr]: https://github.com/rust-gamedev/rust-gamedev.github.io
[coordination]: https://github.com/rust-gamedev/rust-gamedev.github.io/issues?q=label%3Acoordination

Table of contents:

- [Game Updates](#game-updates)
- [Learning Material Updates](#learning-material-updates)
- [Library & Tooling Updates](#library-tooling-updates)
- [Popular Workgroup Issues in Github](#popular-workgroup-issues-in-github)
- [Requests for Contribution](#requests-for-contribution)
- [Jobs](#jobs)
- [Bonus](#bonus)

<!--
Ideal section structure is:

```
### [Title]

![image/GIF description](image link)
_image caption_

A paragraph or two with a summary and [useful links].

_Discussions:
[/r/rust](https://reddit.com/r/rust/todo),
[twitter](https://twitter.com/todo/status/123456)_

[Title]: https://first.link
[useful links]: https://other.link
```

Discussion links are added only if they contain
some actual interesting discussions.

If needed, a section can be split into subsections with a "------" delimiter.
-->

## Game Updates

### Oh no, Lava!

![shooting water into lava](ohnolava_troligtvis.gif)

"Oh no, Lava!" by [@captainfleppo] is the working title
of a platforming game which take inspiration
from an old iOS game created back in 2014. The game is running with [Bevy][bevy]
as its core. The gameplay isn't there yet, but you as a player need to jump on
furnitures, collect coins and fight lava/fire based enemies with your water gun.

[@captainfleppo]: https://twitter.com/captainfleppo
[bevy]: https://bevyengine.org

### [BUGOUT]

![Play Go against AI and friends on the web](BUGOUT.jpg)
_Playing KataGo AI in 9x9_

[BUGOUT] is a web application which allows you to play Go/Baduk/Weiqi
against a leading AI ([KataGo]).
It provides a multiplayer mode so that you can play other humans,
either by joining a public queue or sharing a private URL to your friend.

The user interface is lifted from [Sabaki].

The initial installation's AI is powered by an energy-efficient
[dev board][nv-devboard].

BUGOUT is marching actively toward production, at which point the
team will publish the website address and invite users.
The author anticipates being finished with the production release
prior to Jan 1, 2021.

[BUGOUT]: https://github.com/Terkwood/BUGOUT
[KataGo]: https://github.com/lightvector/KataGo
[Sabaki]: https://github.com/SabakiHQ/Sabaki
[nv-devboard]: https://developer.nvidia.com/embedded/jetson-nano-developer-kit

## Learning Material Updates

## Library & Tooling Updates

### [gfx-rs] and [gfx-portability]

![gfx-rs logo](gfx-logo.png)

[gfx-portability] is a Vulkan portability implementation based on [gfx-rs].
It's basically a drop-in implementation of Vulkan on top of Metal and D3D12,
useful on platforms that don't have native Vulkan support, or buggy drivers.

It released version [0.8.1](https://github.com/gfx-rs/portability/releases/tag/0.8.1)
with official support for the new [KHR portability extension][khr-portability],
as well as a few other extensions, plus a number of correctness fixes.

gfx-rs team asks Rust users of Vulkano, Ash, and other Vulkan-only wrappers to try
out the gfx-portability as a solution on macOS and relevant Windows 10 platforms.

In [gfx-rs] itself, the DX12 backend, and the descriptor indexing feature support
got improved. There has been a push to get DX11 backend in a solid shape,
and it can now run [vange-rs] pretty well 🎉.

[gfx-rs]: https://github.com/gfx-rs/gfx
[gfx-portability]: https://github.com/gfx-rs/portability
[khr-portability]: https://www.khronos.org/registry/vulkan/specs/1.2-extensions/man/html/VK_KHR_portability_subset.html
[vange-rs]: https://github.com/kvark/vange-rs

## Popular Workgroup Issues in Github

## Requests for Contribution

<!-- Links to "good first issue"-labels or direct links to specific tasks -->

- [Embark's open issues][embark-open-issues] ([embark.rs]).
- [winit's "Good first issue" and “help wanted” issues][winit-issues].
- [gfx-rs's "contributor-friendly" issues][gfx-issues].
- [wgpu's "help wanted" issues][wgpu-help-wanted].
- [luminance's "low hanging fruit" issues][luminance-fruits].
- [ggez's "good first issue" issues][ggez-issues].
- [Veloren's "beginner" issues][veloren-beginner].
- [Amethyst's "good first issue" issues][amethyst-issues].
- [A/B Street's "good first issue" issues][abstreet-issues].
- [Mun's "good first issue" issues][mun-issues].
- [SIMple Mechanic's good first issues][simm-issues].
- [Bevy's "good first issue" issues][bevy-issues].

[embark.rs]: https://embark.rs
[embark-open-issues]: https://github.com/search?q=user:EmbarkStudios+state:open
[winit-issues]: https://github.com/rust-windowing/winit/issues?utf8=✓&q=is%3Aissue+is%3Aopen+label%3A%22status%3A+help+wanted%22+label%3A%22Good+first+issue%22
[gfx-issues]: https://github.com/gfx-rs/gfx/issues?q=is%3Aissue+is%3Aopen+label%3Acontributor-friendly
[wgpu-help-wanted]: https://github.com/gfx-rs/wgpu-rs/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22
[luminance-fruits]: https://github.com/phaazon/luminance-rs/issues?q=is%3Aissue+is%3Aopen+label%3A%22low+hanging+fruit%22
[ggez-issues]: https://github.com/ggez/ggez/labels/%2AGOOD%20FIRST%20ISSUE%2A
[veloren-beginner]: https://gitlab.com/veloren/veloren/issues?label_name=beginner
[amethyst-issues]: https://github.com/amethyst/amethyst/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22
[abstreet-issues]: https://github.com/dabreegster/abstreet/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22
[mun-issues]: https://github.com/mun-lang/mun/labels/good%20first%20issue
[simm-issues]: https://github.com/mkhan45/SIMple-Mechanics/labels/good%20first%20issue
[bevy-issues]: https://github.com/bevyengine/bevy/labels/good%20first%20issue

## Jobs

<!-- An optional section for new jobs related to Rust gamedev -->

## Bonus

<!-- Bonus section to make the newsletter more interesting
and highlight events from the past. -->

------

That's all news for today, thanks for reading!

Subscribe to [@rust_gamedev on Twitter][@rust_gamedev]
or [/r/rust_gamedev subreddit][/r/rust_gamedev] if you want to receive fresh news!

<!--
TODO: Add real links and un-comment once this post is published
**Discussions of this post**:
[/r/rust](TODO),
[twitter](TODO).
-->

[/r/rust_gamedev]: https://reddit.com/r/rust_gamedev
[@rust_gamedev]: https://twitter.com/rust_gamedev