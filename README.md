# Sayso

An English-language presentation practice app. All HTML, CSS, JavaScript, and 36 topic briefs are embedded 
in `index.html`. The app uses no external services, dependencies, fonts, analytics, or API keys. Optional 
further-reading links open external websites only when clicked; the practice content works offline once 
loaded.

## Project idea and motivation

Sayso grew out of a personal need. I am an introverted person, and after moving to the US for college, 
I lived alone and did not go out very often. Over time, I had fewer opportunities to communicate with 
others. I began to feel that expressing myself was becoming harder: I often stumbled over my words and 
struggled to explain my opinions clearly. I also wanted to improve my spoken English, so I was looking 
for a way to practice speaking independently and without the pressure of a live audience.

I came across a practice method online: choose a random topic, spend ten minutes researching it, and then 
record a one- to two-minute speech explaining what I had learned. This seemed like a useful exercise for 
people who want to improve their ability to express ideas or speak English. However, choosing a topic, 
finding sources across different websites, and setting up a recording felt like unnecessary friction. 
I wanted to bring those steps together in one place. Sayso lets users choose a topic, read background 
information, and record and review a video presentation on the same page. The exercise inspired the project, 
but the website leaves the timing flexible rather than enforcing a ten-minute research period or a fixed 
speech length.

## AI tool and key prompts

I used Codex to help build this project. I provided the initial idea, described the features I wanted, 
and reviewed the results. Codex generated and revised the HTML, CSS, and JavaScript based on my instructions. 
I also used Codex to help organize my own project explanation and reflections for this README.

The following key prompts are condensed summaries of my requests:

1. **Initial concept:** Build a platform for practicing expression skills. When a user selects a topic, 
show relevant sources and information, then let them record a presentation explaining it. Keep the HTML, 
CSS, and JavaScript in one `index.html`, use no external services, open a local preview, and include run 
instructions in the README.
2. **Topic variety and discovery:** Add more topics and topic categories, with more choices within each 
category. Add a Refresh button so users can see another batch of topics.
3. **Content and language:** Keep the website entirely in English. Make each topic's information more 
detailed, and include more specialized concepts such as cognitive technology, neuroscience, and ecosystems.
4. **Video practice:** Replace audio-only recording with video recording, and let users watch their 
recorded presentations afterward.
5. **Control over recordings:** Add a Delete video button so users can remove an accidental or unwanted 
recording.

## Reflection

The website meets my expectations in terms of its overall purpose and functionality, but reaching that point 
required several rounds of feedback. The first version offered only a handful of topics, so I asked for more 
categories and more choices within them. It also lacked a way to refresh the topic list, which limited users 
to the options already on their screen. Another issue was the amount of background information: each topic 
initially had only two or three brief points. I felt that this did not give users enough material to understand, 
reorganize, and explain in their own words, so I requested richer information and more specific concepts. I also 
asked Codex to replace audio-only recording with video recording so I could watch my presentation afterward. 
Finally, I noticed that I could not delete an unwanted recording, including one started accidentally, and 
requested a delete button. These changes taught me that an initial version can capture an idea while still 
missing details that matter when someone actually uses it. I am satisfied with the result as a practice tool, 
although that is different from having evidence that it has already improved my speaking ability.

This process helped me understand the different roles that AI and I played. Codex could write the code, but 
I needed to provide the direction, specify the features, and identify what was missing. In this project, it 
did not independently anticipate several needs that became clear to me when reviewing the website. I had to 
turn those observations into concrete requests and check whether the revisions matched my intentions. The 
relationship felt somewhat like that between a client and a contractor: I defined the goal and evaluated 
the work, while Codex handled much of the implementation. At the same time, I learned that giving a broad 
instruction once was not enough. The quality of the result depended on an ongoing exchange in which I 
explained not only what I wanted changed, but why those changes would make the practice experience more 
useful.

## Run

From this folder:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000 in Codex's built-in Browser or a modern browser. Camera and microphone recording require a secure context (localhost or HTTPS), browser support for `getUserMedia` and `MediaRecorder`, and camera/microphone permissions.

## Explore and practice

- Browse 36 topics across Everyday life, Technology, Society, Learning, Cognitive technology, Neuroscience, and Ecosystems.
- Click **Refresh** to cycle through shuffled batches: six topics in All topics, or up to three within a category. Each topic appears before the cycle repeats. Changing the category starts a new shuffled cycle. Refresh preserves the open brief and ongoing recording.
- Each topic has a concept overview, two defined terms, a detailed illustrative scenario, a critical-thinking note, and a speaking prompt. Professional topics include optional reading links to NINDS/NIH, OpenStax, NASA, and Nielsen Norman Group. Original scenarios are illustrative, not reported research findings.
- Click **Start video recording**, then allow camera and microphone access. Recording starts when access is granted. The live preview is muted and mirrored to avoid feedback; the recorded video includes audio and is not mirrored by the app.
- Click **Stop recording**. Use the video player's controls to watch, pause, seek, change volume, or enter fullscreen where supported.
- Click **Delete video** in the playback area to remove an unwanted take from this tab and release its recording data. It does not delete copies already downloaded to your computer. Deletion is disabled while another recording is starting or in progress.
- Click **Download video** to save the recording. The browser chooses a supported WebM or MP4 format.

## Privacy and recording lifetime

Video and audio stay in memory in this tab and are never uploaded. Camera and microphone tracks stop when recording ends. Refreshing the topic list does not discard a take. A successfully completed new take replaces the previous playback; a failed attempt preserves it. Download anything you want to keep before completing another take, reloading the page, or closing the tab. Very long videos consume more memory; the suggested practice length is 2–3 minutes.

## Troubleshooting

- Allow **both** camera and microphone in browser and operating-system permissions.
- If either device is missing, connect it. If it is busy, close other applications using it.
- If the embedded browser does not support media capture, open the same localhost address in a current Chrome, Edge, Firefox, or Safari browser.
- The interface reports unsupported recording, denied permissions, missing devices, and capture errors. A device disconnect ends the current recording and attempts to make captured content available.

The app does not provide transcription, automated scoring, or persistent recording storage.
