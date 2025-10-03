# Generative AI for creatives:
a suite of classes that prepares creatives to use GenAI tools in an informed and ethical manner.

---
## 4 semester-long classes
Idea: rather than one teacher per class of 15 students, two teachers for a class of 30+ students: team teaching with one faculty from 'arts' background + one faculty from a CS/mathematics background (Glen?)

Idea: each class has a primary question, and students respond to that question through a final project. Final project culminates in 2 outputs:
- a public exhibition
- each student's project code and output examples are archived in a public GitHub repo

### 1 - Under the Hood Lectures:
from mathematicians/cs that walks through
- main question: is it magic?
- glossary: introduce terms/concepts
- bestiary: survey types of genAI systems (pattern recognition vs generation, etc)
- for each, walk through the architectures and training processes
- explain the math/code to demystify the results
- introduce tool sets, local and online, compare exposed parameters
- big project: run run a prompt against 4 GAIs, assess differences in results (attrection to variations in prompt engineering towards a stated goal)
- multimodal AI
- agents
- compare encoding/decoding for text, images, audio, video, etc
- [Github for Poets](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV)

### 2 - The School Board Seminar:
- main question: how do we teach (train) our AI children?
- survey existing training sets
- build small training sets: what kinds of results do we get? can we go beyond style
- an assignment: run a prompt against 4 GAIs with known, different training sets. Print and analyse the results
- philosophy component in the readings?
- problems of antropomorphism/anthropocentrism
- big project: collect materials for a training corpus and build a custom model tailored to a specific type of output (forbidden: anime-styles); generate a body of work using that model (can be a suite of images, a collection of texts, a movie, a cycle of songs)

### 3 - GenAi manifest in the material world
using GAI tools to design/build things
- main question: how do we apply this tech to real problems/things? (get out of the computer)
- laser/vinyl cutting (GAI to create vectors)
- 3D printing (GAI to create meshes - possibly to solid models? Fusion 360?)
- basic: printing/large format printing (just to get sketches out)
- using GenAI as a research/idea generation/sketching tool for traditional media
- big project: identify a problem in the real world that requires a functional, mechanical part - usa AI to design the part, then fabricate and put into use. Assess usefulness. (is there an alternative to this that is more studio-friendly? product design?)

### 4 - GenAI to build novel workflows that support creative tasks.
- main question: how does AI enhance professional practice?
- ComfyUI and Python notebooks to customize creation workflows?
- GenAI and interaction?
- GenAI to do your bookkeeping?
- GenAI to build your web site?
- big project: clone oneslf as an AI

---
## James' roadmap for RTS (Research Technology Services, in GW IT)

### some data collection
- how long each generation takes? (performance)
- how much power was consumed? (environmental cost)
- side project: can we make RTS service carbon-nuetral? solar powered? geothermal, Chris Combs... build in Ashurn?

### a toolkit that includes
- txt (we've done this, but needs SSO and maybe a dedicated node)
- txt2img (we've done this, but needs SSO and maybe a dedicated node)
- txt2audio (we've done this, but needs SSO and maybe a dedicated node)
- txt2video (testing)
- txt23D (wish list)
- model creation (what can students do with small training sets?)
- logging for each user (google sheet or tab-delimited) that includes for each run:
  - time to complete
  - power consumption
  - job variables
  - output filename
- queue batches (current batch interface is goofy)
  - BOX for output?
- SSO login

### would a dedicated Grace Hopper node be sufficient for a class of 30 students? How do we test? Cost? (My recollection is about $40K)
- no...
- assume 32 concurrent users (espedcially during class, then assume 12 hours per week per 32 users.)
- automate usage tracking/reporting
- is there a cluster that can support that? Cerberus?
- talk to Glen: update the HPC website with current info, tutorials, etc - host on github rather than wordpress?
- potential teaching partners - JP? Robert Pless?

---
## Why run our own services locally?
- expose more parameters
- students don't bear cost of services like ChatGPT, RunwayML, etc
- students don't need powerful laptops or storage (processing on the HPC via OOD interface)
