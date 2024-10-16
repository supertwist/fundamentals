# Generative AI for creatives:
a suite of classes that prepares creatives to use GenAI tools in an informed and ethical manner.

---
## 4 semester-long classes
Idea: rather than one teacher per class of 15 students, two teachers for a class of 30+ students: team teaching with one faculty from 'arts' background + one faculty from a CS/mathematics background (Glen?)

### 1
### Under the Hood Lectures:
from mathematicians/cs that walks through
- glossary: introduce terms/concepts
- bestiary: survey types of genAI systems
- for each, walk through the architectures and training processes
- explain the math/code to demystify the results
- introduce tool sets, local and online, compare exposed parameters
- an assignment: run run a prompt against 4 GAIs

### 2
### The School Board Seminar:
- survey existing training sets
- an assignment: run a prompt against 4 GAIs with known, different training sets. Print and analyse the results

### 3
## GenAi manifest in the material world

### 4
## GenAI to build novel workflows that support creative tasks.

---
## James' roadmap for RTS

# some data collection
- how long each generation takes? (performance)
- how much power was consumed? (environmental cost)
- side project: can we make RTS service carbon-nuetral? solar powered? geothermal, Chris Combs... build in Ashurn?

# a toolkit that includes
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

# would a dedicated Grace Hopper node be sufficient for a class of 30 students? How do we test? Cost? (My recollection is about $12-15K)

---
Why run our own services locally?
- expose more parameters
- students don't bear cost of services like ChatGPT, RunwayML, etc
- students don't need powerful laptops or storage (precessing on the HPS, and store to BOX)
