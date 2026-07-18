---
title: "Event 3"
date: 2026-06-13
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Event Reflection: “FCAJ Meetup (June 13, 2026)”

### Purpose of the Event

- To provide a realistic, unfiltered view of what Engineers (DevOps, Data Analytics) actually do at multinational corporations (MNCs) and enterprises, thereby dispelling common student misconceptions.
- To dive deep into corporate culture, global working standards, and orientation for a sustainable career path—from taking the first steps in the industry to becoming an expert.
- To inspire and guide attendees on how to leverage tech communities (like AWS) as a launchpad for career advancement and value sharing.

### List of Speakers

- **Mr. Trong H. Truong** (DevOps Engineer @ Endava Vietnam): “What does a DevOps Engineer really do?”
- **Mr. Dat Pham** (Data Analytics Engineer) & **Mr. Cuong Nguyen** (Process Engineer): “Real-world stories and culture at multinational corporations”
- **Mr. Danh Hoang Hieu Nghi** (AI Engineer): “From First Cloud AI Journey to AWS Partner”
- **Dinh Trung Kien & Nguyen Minh Tho**: “A scalable URL shortening service on AWS”

### Key Highlights

The event featured 4 highly practical presentations:

#### 1) Dinh Trung Kien & Nguyen Minh Tho — A scalable URL shortening service on AWS

- **Objective**: Solving a classic System Design problem by building a highly scalable, secure, and low-latency URL shortening service (rather than just a simple MVP).
- **Risks of the "Basic" Architecture**: The traditional model (Frontend → Backend → Database) faces numerous issues such as Single Points of Failure (SPOF), scaling difficulties, high read latency, and vulnerability to attacks due to the lack of edge-layer protection.
- **Real-world System Architecture on AWS**:
  - **Edge Layer**: Utilizing Amazon CloudFront integrated with AWS WAF to block malicious traffic and distribute static content via Amplify.
  - **App Layer**: A containerized backend running on Amazon ECS (Fargate), using an ALB to route traffic into Private Subnets.
- **Key Generation Service (KGS)**: Optimizing performance by utilizing a background service to pre-generate short codes and push them into a Redis queue (using the LPUSH command), instead of generating them on-demand.
- **Create Flow (Write)**: The backend simply fetches an available code from Redis (using the RPOP command), maps it to the original URL, and writes directly to DynamoDB, completely eliminating code generation latency.
- **Read Flow (Cache-aside)**: The system queries Amazon ElastiCache for Redis first. Only on a Cache miss does it query DynamoDB and then update the cache, drastically reducing the database load.

#### 2) Trong H. Truong — What does a DevOps Engineer really do?

- **Myth vs. Reality**: Many mistakenly believe DevOps is just writing CI/CD pipelines, typing Docker/K8s commands, or being the midnight server "firefighter". In reality, the scope is much more system-oriented: on-call duties, incident handling, permission management, cost investigation, and ownership clarification.
- **What to Learn First**: Don't chase tools because they constantly change. Master the Fundamentals: Linux, Networking, Git, Containers, and a programming language (Python/Golang).
- **Crucial Lessons**: Copy-pasting commands from the internet doesn't mean you understand them. Always ask "Why" before "How". Communication is a core DevOps skill. Use AI to enhance your skills, but don't let it turn off your own critical thinking.

#### 3) Dat Pham & Cuong Nguyen — Real-world Stories & MNC Culture

- **Survival Skills**: To survive and thrive in an MNC, beyond hard skills, you must possess Critical Thinking, Communication Skills, Problem Solving, and especially "Data Storytelling".
- **The 5 Career Levels**: Follower (Execution) → Learner (Proactive Learning) → Problem Solver (End-to-end resolution) → System Thinker (Seeing the big picture, long-term optimization) → Super Star (Strategic direction and leadership).
- **Decoding Corporate Culture**: In tech MNCs, a "No-Blame Post-Mortem" culture is highly emphasized: when an error occurs, the team focuses on finding the root cause to fix the system rather than pointing fingers at individuals.
- **The "Right Work" Philosophy**: Built on 3 pillars: Being a Good Person (inner management), Being a Professional (serving with expertise), and Being a Citizen (national responsibility, technological legacy).

#### 4) Danh Hoang Hieu Nghi — From First Cloud AI Journey to AWS Partner

- **The 8-step Roadmap**: Starts with Student Curiosity → Finding the right environment (First Cloud AI Journey) → Hands-on Labs → Showcasing capabilities (Portfolio) → Becoming an AWS Partner → Sharing Back to the community.
- **The Power of Community**: Getting a job is just the beginning. Immersing yourself in a community (like the AWS Student Builder Group or AWS Community Builder) provides an excellent network and practical support: certification vouchers, AWS Credits, and swags.

### Key Takeaways

- **Clear Understanding**: Tools change constantly; only solid Fundamentals and System Thinking will sustain an engineer's long-term career.
- **Stepping Stone to MNCs**: A mindset shift is required—from just "getting the job done" to "doing it to standard", combined with a "No-Blame" mentality to continuously improve both the self and the system.
- **The Importance of Contribution**: Technical expertise combined with support from tech communities creates a powerful launchpad for career development.
- **Architecture Optimization (System Design)**: Grasped concepts like Separation of Concerns (decoupling Read/Write flows), Defense at the Edge, and the Pre-computation over On-demand strategy to minimize latency.

### Practical Applications

- **Self-Study & Practice**: Break the habit of mindlessly copy-pasting code. When using AI to help write scripts or configurations, force myself to analyze and understand the purpose of every single line.
- **Upgrading Project Mindset**: Apply a "System Thinker" mindset to internship projects instead of just being a "Follower". It's not just about making the code run; it's about optimizing performance, anticipating risks, and practicing clear progress reporting.
- **Personal Branding**: Plan to actively participate in the AWS Student Builder Group to build projects for my Portfolio and orient toward community building in the future.
- **Applying the Cache-aside Pattern**: Implement Redis in personal or academic projects to optimize response times for APIs with high read frequencies.
- **Decoupling Heavy Tasks**: Learn how to isolate heavy tasks from the main execution thread using background workers, preparing data in advance so the main flow runs more smoothly.

#### Some pictures from the event
