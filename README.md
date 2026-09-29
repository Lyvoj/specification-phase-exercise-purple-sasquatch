# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

See instructions. Delete this line and replace with a list of the names of your team members, including links to each one's GitHub profile.

## Review of the Current Application

1. **Strength — Spoken mathematical expressions are recognized accurately.**  
   During testing with mathematical expressions and Fourier-transform terminology, Slide Machine converted orally described formulas into readable mathematical notation.  
   **Observed in:** (https://theslidemachine.com/d/untitled-f33dde17)  

2. **Strength — Spoken descriptions of plots can be converted into generated visualizations.**  
   Across multiple trials, the presenter described plots verbally and Slide Machine generated corresponding plot visuals rather than limiting the output to text. This behavior was observed more than once, indicating that the system can interpret some spoken quantitative relationships and represent them visually.  
   **Observed in:**  
   - [Trial 1](https://theslidemachine.com/d/untitled-7f6f21cf)  
   - [Trial 2](https://theslidemachine.com/d/untitled-29d9be49)  

3. **Strength — The generated exit-ticket quiz can closely reflect the lecture content.**  
   In one trial, the quiz generated from the lecture produced clear questions that matched the material covered in the generated deck, showing that the post-lecture quiz workflow can create a useful assessment from the lecture content.  
   **Observed in:** (https://theslidemachine.com/d/untitled-38535455)  
   **Quiz:** (https://docs.google.com/forms/d/e/1FAIpQLSezT_elEfOEK4csWcESoTvbmaEW3_zskjtXY5espOhSVLZIug/viewform)  

4. **Strength — Verbal corrections are reflected in the generated slide content.**  
   In one trial, the presenter intentionally stated an incorrect value and then corrected it verbally. Slide Machine reflected the corrected information rather than preserving only the original mistake, showing that it can respond appropriately to spoken self-corrections.  
   **Observed in:** (https://theslidemachine.com/d/untitled-ad83c51c)

5. **Strength — Clear topic transitions are recognized and separated appropriately.**  
   In one trial, the presenter moved from one unrelated topic to another, and Slide Machine handled the transition well by keeping the topics organized rather than blending them into the same slide content.  
   **Observed in:** (https://theslidemachine.com/d/untitled-7416ce41)

6. **Weakness — Seeded images are not always used when explicitly referenced during a lecture.**  
   In one test, an image of a matrix had already been uploaded as seed material, but when the presenter referred to the matrix while speaking, the generated slide did not use the uploaded image.  
   **Observed in:** (https://theslidemachine.com/d/untitled-38535455) 
   


7. **Weakness — Generated plots can have poor visual readability.**  
   Although Slide Machine successfully generated plots from spoken descriptions, the resulting plots in multiple trials used dark visual styling that made axis labels, annotations, or other text difficult to read. The generated figures also consistently included gray bands above and below the plot, reducing the amount of slide space available for the visualization and making the figure appear smaller.
   **Observed in:**  
   - [Trial 1](https://theslidemachine.com/d/untitled-7f6f21cf)  
   - [Trial 2](https://theslidemachine.com/d/untitled-29d9be49)  
   - [Trial 3](https://theslidemachine.com/d/untitled-e0f37daa) 


8. **Weakness — Some generated decks contain blank or nearly blank slides during generation.**  
   In multiple trials, Slide Machine produced slides with little or no visible content before later AI refinement improved the deck. Even if the content is eventually corrected, the temporary blank slides can make the live presentation feel incomplete or confusing while the lecture is still in progress.  
   **Observed in:**  
   - [Trial 1](https://theslidemachine.com/d/untitled-d0b1ef47)  
   - [Trial 2](https://theslidemachine.com/d/untitled-29d9be49)

9. **Weakness — A generated lecture may not include an introductory or title slide.**  
   In one trial, the generated deck began without a clear front/title slide, so the presentation opened directly into lecture content instead of first establishing the topic or lecture context.  
   **Observed in:** (https://theslidemachine.com/d/untitled-d0b1ef47)  

10. **Weakness — Changing the slide design can reduce formula readability.**  
After switching the slide design, the mathematical formula became oversized and partially cut off, so the full expression was no longer visible.  
**Observed in:** [Design-change formula trial](https://theslidemachine.com/d/untitled-2aadc2e4)

11. **Gap — Concept slides do not always include supporting visuals or process diagrams when those would help explain the topic.**  
   In a concept-based lecture such as one explaining photosynthesis, the generated slide may present the topic in text form without adding a relevant illustrative image or a simple visual overview of the process.  
   **Observed in:** (https://theslidemachine.com/d/untitled-7416ce41)


## Prior Art & Originality

Before committing to our proposal, our team reviewed the existing Slide Machine documentation and development activity identified in the project background materials. We have checked the Future Work and Open Questions sections, the delivery roadmap, and the repository's open issues and pull requests. 
 
The purpose of this review was to determine whether our proposed onboarding and tutorial functionality had already been specified, scheduled, or proposed.

We initially considered ideas such as improved mathematical formula support, but found that mathematical content and LaTeX rendering are already supported. We also found that features such as whiteboard annotation, voice interaction, preflight lecture preparation, template versioning, editing, sharing, translation, and quiz-related functionality are already implemented, specified, or planned.

We searched the repository for existing proposals related to tutorials, onboarding, walkthroughs, getting started, help, and first-time users. At the time of our review, we did not find an existing issue or pull request proposing the same guided first-time onboarding experience as our prototype.

Our proposed original contribution is a first-time onboarding and tutorial experience that introduces new users to the main Slide Machine workflow and remains accessible later as reusable help content.

So the prototype has two tuotorial paths:

**an Instructor Guide**, focused on learning how to prepare projects, seed lecture material, deliver a live lecture, review generated slides, share the resulting deck, and work with the exit-ticket quiz; and

**a Student Guide**, focused on learning how to access shared lecture material, navigate generated decks, use available viewing features, and locate the exit-ticket quiz.

The tutorial is intended to appear during the first-time-user experience while also remaining accessible later from the application so that users can revisit the guidance when needed.

This proposal does not introduce a replacement workflow or duplicate existing Slide Machine functionality. Its purpose is to make the application's existing features easier for first-time students and instructors to discover and understand.

## Stakeholders

### Interview Method and Privacy

We interviewed and observed four people representing the two primary user
types affected by our proposal: two instructor-type users and two student-type
users. The interviews were conducted on **September 26, 2026**, using a
**hybrid** format.

Each participant was asked about their lecture-related goals, needs, and
frustrations. We also observed each participant attempting relevant tasks in
the live Slide Machine application. After the observation, we explained our
proposed reusable, role-specific tutorial system and asked how they would want
to access and use that guidance.

The public names below use each participant's first name and last initial to
protect their privacy. Their full names and email addresses will be shared
privately with the course administrators for verification and will not be
published in this repository.

Our proposal is a reusable, role-specific onboarding and tutorial system. It
does **not** include an AI assistant. First-login onboarding, tutorial
categories, tutorial search, and a persistent tutorial entry are proposed
additions rather than features of the current application.

### Annie Q. — First-Time Instructor

**User type:** Instructor  
**Experience with Slide Machine:** First-time user

#### Background

Annie Q. is an assistant teacher at a local school who regularly prepares
PowerPoint slides and other visual materials before class. They were interested
in using Slide Machine to reduce preparation time, but they were concerned that
an unfamiliar workflow could interrupt a live lesson.

#### Goals and Needs

- Reduce the time required to prepare lecture slides.
- Understand what must be prepared before starting a live lecture.
- Understand the purpose of seed materials and how they affect generation.
- Know whether Slide Machine is still processing or has encountered an error.
- Review generated slides before sharing them with students.
- Generate and publish an exit-ticket quiz after a lecture.
- Reopen guidance later for tasks that are not performed frequently.

#### Problems and Frustrations

- The relationship between projects, seed materials, live sessions, generated
  decks, and quizzes was not immediately clear.
- The participant did not know whether seed materials were required before
  recording.
- Blank or incomplete slides made it difficult to determine whether generation
  was still in progress.
- The next step after stopping a live session was not obvious.
- Uncertainty during a live lecture created a risk of disrupting the class.
- When no guidance was available, the participant relied on trial and error.

#### Observed Behavior

- The participant paused at the seed-material area and asked what it was for.
- Without additional explanation, the participant skipped the seed-material
  step and looked for an import control similar to one in conventional
  presentation software.
- When a blank slide appeared during generation, the participant moved between
  the stop, refresh, and other nearby controls and asked whether the system was
  still processing.
- After stopping the live session, the participant remained on the current
  screen and waited for the application to present the next step.
- Without guidance, the participant did not immediately proceed to deck review
  or quiz generation.

#### Response to the Proposed Tutorial System

Annie Q. wanted a short, skippable getting-started tutorial that explains
the overall instructor workflow. On a first visit, they preferred a recommended
sequence or browsable overview. For later visits, they preferred searching for
a specific task, such as publishing a quiz. They also wanted tutorials to
remain accessible after the first login.

### Alice L. — Assistant Teacher with AI-Assisted Material Experience

**User type:** Instructor  
**Experience with Slide Machine:** Familiar with AI-assisted teaching-material
workflows

#### Background

Alice L. is an assistant teacher at a local school who has experience using
AI-assisted tools to prepare lesson materials. They review presentation content
before it is shown or distributed to students. Their priority is efficient
review and recovery rather than basic introductory instruction.

#### Goals and Needs

- Review generated slides quickly before they are shared.
- Identify and correct unreadable formulas, plots, images, or layouts.
- Add or replace a slide when generated content is unsuitable.
- Find instructions for a specific task without repeating the entire onboarding
  flow.
- Keep the current deck visible while consulting guidance.
- Learn how to use new functionality after an application update.

#### Problems and Frustrations

- Generated content may require manual review before distribution.
- The fastest recovery action is not always apparent when generated content is
  unsuitable.
- A long general tutorial would slow down a time-sensitive review task.
- Leaving the current deck to search for help would interrupt the review
  workflow.
- Browsing a large set of unrelated tutorials would be inefficient when the
  user already knows the problem.
- Guidance that covers only the ideal workflow would not help with recovery
  from an unsuccessful result.

#### Observed Behavior

- The participant immediately inspected formulas, plots, images, and layout
  after content was generated.
- When a displayed item appeared unsuitable, the participant first tried
  direct editing actions, including double-clicking, right-clicking, and
  looking for an edit control.
- When the correct recovery action was unclear, the participant looked for a
  search entry, documentation, or instructions related to the current task.
- The participant attempted to keep the current deck visible while looking for
  guidance.
- The participant showed greater interest in short, task-specific instructions
  than in repeating the complete lecture workflow.

#### Response to the Proposed Tutorial System

Alice L. would normally skip basic onboarding and search for a specific
tutorial. They preferred short tutorials such as “Insert a New Slide,” “Review
Generated Slides,” or “Recover from an Unreadable Slide.” They wanted guidance
that could be opened and closed without losing the current working context.

### Jefferson C. — First-Time Student

**User type:** Student  
**Experience with Slide Machine:** First-time user

#### Background

Jefferson C. is an undergraduate student who normally follows the
instructor's projected slides, opens shared lecture material on a personal
device, and completes a short quiz near the end of class.

#### Goals and Needs

- Open the correct shared lecture deck quickly.
- Understand which Slide Machine features are relevant to students.
- Locate and complete the exit-ticket quiz on time.
- Discover viewing features such as translation and narration.
- Receive guidance that does not include irrelevant instructor workflows.
- Reopen a tutorial later while reviewing lecture material.

#### Problems and Frustrations

- The participant initially understood Slide Machine mainly as an online slide
  viewer.
- Student-facing features were not immediately discoverable without
  explanation.
- The location of the exit-ticket quiz was not immediately clear.
- Missing a quiz or lecture link could affect participation in class.
- The participant depended on classmates or the instructor when unsure how to
  continue.
- Instructor-focused guidance would add irrelevant information and increase
  cognitive load.

#### Observed Behavior

- After opening a shared deck, the participant focused primarily on the central
  slide area.
- Without prompting, the participant did not open the translation or narration
  controls.
- When unsure how to access a student-facing feature, the participant looked to
  another person for guidance rather than finding instructions in the
  application.
- While looking for the exit-ticket quiz, the participant checked multiple
  interface areas before identifying where it could be accessed and submitted.

#### Response to the Proposed Tutorial System

Jefferson C. preferred a short Student getting-started path containing only
common student tasks. They preferred browsing a small Student category on the
first visit and wanted the ability to reopen a specific tutorial later, such
as a narration tutorial during exam review.

### Zixuan G. — International Student with Language-Support Needs

**User type:** Student  
**Experience with Slide Machine:** Uses translation and playback support when
reviewing lectures

#### Background

Zixuan G. is an international student who sometimes needs to review
lecture material more than once or use translation support to understand
unfamiliar technical terms.

#### Goals and Needs

- Locate translation controls without leaving the lecture deck.
- View translated lecture material while retaining access to the original
  content.
- Return to the original language after viewing a translation.
- Start, pause, and resume narration during lecture review.
- Keep the current slide visible while consulting instructions.
- Reopen language or narration tutorials when a feature has been forgotten.

#### Problems and Frustrations

- Language-related controls were not immediately discoverable.
- An inaccurate translation could make a technical concept more difficult to
  understand.
- Switching between translated and original content was not immediately clear.
- Narration controls required exploration before the participant understood
  them.
- Leaving the lecture deck to search for help would interrupt learning.
- The participant also wanted finer playback controls; this need is outside the
  current tutorial-system proposal.

#### Observed Behavior

- The participant examined several interface areas while looking for
  translation or language controls.
- After encountering an unnatural translation of a technical term, the
  participant looked for a way to restore or compare the original text.
- During narration playback, the participant searched around the playback area
  for pause, resume, and progress controls.
- When the expected control was not found, the participant returned to the
  original lecture material and postponed the task.
- The participant tried to keep the current lecture content visible while
  looking for guidance.

#### Response to the Proposed Tutorial System

Zixuan G. preferred a searchable Student tutorial catalog with a small
language and viewing category. They wanted task-specific tutorials such as
“Translate a Slide,” “Return to the Original Language,” and “Start and Pause
Narration.” They also wanted these tutorials to remain available from the deck
after the first login.

### Synthesized Interview Findings

#### Finding 1 — First-time users lack a clear mental model of the complete workflow

First-time users could understand the general purpose of Slide Machine without
understanding how projects, preparation, live sessions, generated decks, and
quizzes fit together. Annie Q. hesitated at seed materials and did not
naturally continue from recording to deck review and quiz generation.
Jefferson C. initially understood the application primarily as a slide-viewing
website.

**Design implication:** Provide short, role-specific getting-started paths that
explain the overall sequence without requiring users to learn every feature at
once.

#### Finding 2 — Important existing features are not always discoverable

The instructor did not immediately understand seed materials or the
post-recording workflow. Student participants did not immediately discover
translation, narration, or quiz access without additional guidance.

**Design implication:** Organize tutorials by role and task, and introduce the
most important features during a short first-login experience.

#### Finding 3 — Instructor and student guidance must be separated

Instructors need guidance about preparation, live sessions, generated content,
editing, and quizzes. Students need guidance about shared decks, quizzes,
translation, narration, and other viewing features. Combining both groups into
one undifferentiated tutorial would expose users to irrelevant instructions.

**Design implication:** Provide separate Instructor and Student tutorial
catalogs while using the same underlying tutorial structure.

#### Finding 4 — Users need clearer status and recovery guidance

Blank or incomplete generated content made it difficult for the first-time
instructor to determine whether the application was still working. The
experienced instructor-type participant also needed guidance for recovering
from unsuitable generated content.

**Design implication:** Tutorials should cover both successful workflows and
recovery situations, including how to recognize processing states and what to
do when a result is incomplete or unsuitable.

#### Finding 5 — First-time and experienced users need different ways to access help

First-time users preferred a short recommended path or a small browsable
catalog. The experienced participant preferred direct search for a known task
or problem.

**Design implication:** Support both browsing and search. Onboarding should be
optional and skippable, while individual tutorials should remain searchable
later.

#### Finding 6 — Tutorials must be available after the first login

Participants expected that they might forget infrequent tasks, encounter a new
feature, or need guidance while reviewing a lecture later.

**Design implication:** Do not limit tutorials to the first-login experience.
Provide a persistent way to reopen the tutorial catalog from the user's current
workflow.

#### Finding 7 — Guidance should preserve the user's current context

Instructor and student participants wanted to keep the current deck or lecture
visible while looking for instructions. Leaving the current task would increase
interruption and cognitive load.

**Design implication:** Use concise, dismissible guidance that can be opened
from the relevant screen and closed without losing the user's place.

#### Finding 8 — The tutorial system must be reusable and extensible

The set of relevant help topics will grow as Slide Machine adds features and as
users encounter new tasks. Building a separate navigation pattern for every
tutorial would not scale.

**Design implication:** Use one shared catalog and tutorial-runner structure.
Adding a topic such as “Insert a New Slide” should require adding a new tutorial
item and its steps, not redesigning the overall interaction.

### Scope Decision

Our proposal focuses on onboarding, feature discovery, and reusable
step-by-step tutorials. Requests for new application capabilities, such as
additional narration-speed controls, are valuable stakeholder findings but
remain outside the scope of this proposal.


## Product Vision Statement

See instructions. Delete this line and place your Product Vision Statement here — one sentence describing the improvements and new features your team is proposing for The Slide Machine.

## User Requirements

See instructions. Delete this line and place a list of your User Stories here, grouped by type of user. These should describe functionality that is new or changed, not functionality the app already has.

## Activity Diagrams

The tutorial system uses one shared Tutorial Portal. Users can enter from the first-use prompt or Help, choose a topic, follow its steps, and return to the Portal. New topics reuse the same navigation and guidance structure.

### 1. Enter the Tutorial Portal

![Enter the Tutorial Portal activity diagram](images/activity-diagrams/01-enter-tutorial-portal.png)

From Projects or a shared deck, first-time users can start tutorials or select **Not now** to stay on the current page. **Help → Tutorials** opens the same Portal later.

### 2. Choose and complete a tutorial

![Choose and complete a tutorial activity diagram](images/activity-diagrams/02-choose-and-complete.png)

Select a topic and follow its guidance. **Next** advances to the following step. At the last step, **Finish** opens the completion screen; **Back to Tutorials** returns to the Portal.

### 3. Exit a tutorial

![Exit a tutorial activity diagram](images/activity-diagrams/03-exit-tutorial.png)

**Exit tutorial** opens a confirmation dialog. **Continue tutorial** returns to the current step; **Exit to Tutorials** returns to the Portal without marking the tutorial complete. Lecture content is unchanged.

### 4. Replay or switch tutorials

![Replay or switch tutorials activity diagram](images/activity-diagrams/04-replay-or-switch.png)

From the Portal, choose the same topic to replay it or a different topic to learn something else. Either choice starts at Step 1 and uses the shared tutorial flow.

## Wireframes

The four grayscale sheets cover the Portal entry, topic list, shared guidance, and completion and exit states. Users choose a topic without a separate role-selection screen.

### 1. Entry and Help

![First-use prompt and Help entry wireframes](images/wireframes/01-entry-and-help.png)

**Start tutorials** opens the Portal. **Not now** dismisses the first-use prompt. **Help → Tutorials** remains available for reopening it.

### 2. Tutorial Portal

![Tutorial Portal wireframe](images/wireframes/02-tutorial-portal.png)

A single list offers topics such as recording, quiz generation, translation, and narration. **Start** opens the selected topic at Step 1, including when replaying it. **Back to application** returns to the application context from which the Portal was opened.

Adding a topic such as “Insert a New Slide” means adding another list item and its steps, using the same guide layout.

### 3. Shared tutorial guide

![Shared tutorial guide wireframes](images/wireframes/03-shared-tutorial-guide.png)

Each topic uses a title, step counter, short instruction, and highlighted target with an arrow. Ordinary steps offer **Next**; the last step offers **Finish**. **Exit tutorial** is available in both states.

Quiz generation illustrates the shared layout, not a complete topic walkthrough. The application background is schematic; the final prototype should use the actual application's navigation and control locations.

### 4. Completion and exit

![Tutorial completion and exit confirmation wireframes](images/wireframes/04-completion-and-exit.png)

After completion, **Back to Tutorials** returns to the Portal. In the exit dialog, **Continue tutorial** keeps the current step and **Exit to Tutorials** returns to the Portal. Restarting an exited tutorial begins at Step 1. Replaying and switching topics reuse the Portal rather than adding another screen.

## Clickable Prototype

[Open the Slide Machine Tutorials clickable prototype in Figma](https://www.figma.com/proto/SroFcNH2UkFln43ed1xbZZ/Purple-Sasquatch-%E2%80%94-Slide-Machine-Tutorials-Clickable-Prototype?node-id=3-2&starting-point-node-id=3%3A2)

Choose **Instructor** to explore the recording and quiz tutorials, or **Student** to explore the translation and narration tutorials. Follow the highlighted controls and arrow prompts; **Back to Tutorials** returns to the role-selection page.

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
