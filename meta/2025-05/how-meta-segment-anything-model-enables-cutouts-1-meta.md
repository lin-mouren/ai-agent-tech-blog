---
title: "How Meta Segment Anything Model enables Cutouts in the Instagram Edits app"
vendor: meta
source_url: https://ai.meta.com/blog/instagram-edits-cutouts-segment-anything/
published_at: 2025-05-01T00:00:00.000Z
crawled_at: 2026-05-23T13:58:13.000Z
word_count: 800
reading_time_minutes: 4
tags: [segment-anything, sam, computer-vision, instagram, video-editing]
---

# How Meta Segment Anything Model enables Cutouts in the Instagram Edits app

May 1, 2025 | 4 minute read

We recently launched Edits, a new video creation app by Instagram designed for creators. One of the standout features of our new app is Cutouts, which is enabled by Meta Segment Anything Model (SAM) 2.1, the popular open source segmentation model created by the Meta Fundamental AI Research (FAIR) team.

"In 2024, we built a demo as part of our research and as a way to showcase SAM 2 externally to a research audience, independent developers, and the general population," says Nikhila Ravi, Research Engineering Manager, Meta. "We developed the demo from our perspective, but it was also clear that this could have a lot of practical value for the people who use Meta technologies."

Less than a year later, the research developed as Segment Anything Model 2.1 is now an important part of Edits. People can use Cutouts to edit across several layers of video, apply filters to specific parts of videos, and easily place elements like text and stickers behind objects.

While the experience feels seamless in the app, the Meta FAIR team worked behind the scenes to make sure the Segment Anything Model was ready to be shipped into Edits.

The Cutouts feature in Edits uses an object detection pipeline to automatically suggest an object in a frame of a video that someone might want to turn into a cutout. A user can also switch to manual mode, which allows interactively adding positive and negative clicks.

While Segment Anything Model 2 introduced real-time, promptable segmentation for video, the FAIR team improved upon its capabilities with the release of SAM 2.1 in fall 2024. The update included additional data augmentation techniques and improved occlusion handling.

Working with PyTorch and production partners, we made several performance improvements. On an NVIDIA H100 GPU, we increased model throughput by 1.8x and reduced end-to-end first frame preview latency by 3x.

With more people than ever now using the Segment Anything Model, the team is focused on their next big release: SAM 3.
