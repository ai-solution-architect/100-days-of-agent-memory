### 𝐃𝐚𝐲 𝟏/𝟏𝟎𝟎 𝐨𝐟 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲
[post](https://www.linkedin.com/posts/richmondalake_architecting-agent-memory-activity-7345776758417186816-V3Yp?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAQRyLsBkSAisgCJmXavcznDzyDTxIecxnk)

Honestly, didn't know it would blow up like it did.
After just a couple of days, the talk I gave on Agent Memory at AI Engineer Conference has over 25k views in a few days. 

Not only that, but my little weekend side project on Agent Memory gained over 100 ⭐ last weekend.

So what's all the fuss about?
It turns out that many developers, practitioners, and founders are very interested in making AI Agents reliable, believable, and capable. And we all agree that memory is a core component in making this happen.

𝐖𝐡𝐚𝐭'𝐬 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲?
AI agent memory is the persistent cognitive architecture that allows agents to accumulate knowledge, maintain contextual awareness, and adapt their behavior based on historical interactions and learned experiences. Think of it as giving AI a working memory that persists beyond a single interaction.

𝐖𝐡𝐲 𝐝𝐨𝐞𝐬 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲 𝐦𝐚𝐭𝐭𝐞𝐫?
As I said earlier, memory makes an AI agent reliable, believable, and capable. 
→ Without memory, every conversation with an AI agent starts from scratch.
→ Without memory, AI agents can't adapt to new information
→ Without memory, AI agents can't be personalized
→ Without memory, AGI won't happen

To learn in public and share the journey, I'm conducting a hashtag#𝟏𝟎𝟎𝐃𝐚𝐲𝐬𝐎𝐟𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 challenge starting today.

I'll be documenting my deep dive into key definitions, memory management techniques, research findings, implementation strategies, and real-world applications - sharing both insights and mistakes along the way.

Join me on this learning journey if you want to understand the backbone of truly intelligent AI systems.

Day 1 starts now. 🧠

---

### 𝐃𝐚𝐲 𝟐/𝟏𝟎𝟎 𝐨𝐟 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲
[post](https://www.linkedin.com/posts/richmondalake_moving-beyond-context-engineering-activity-7346263709477969920-6-7r?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAQRyLsBkSAisgCJmXavcznDzyDTxIecxnk)
𝐅𝐫𝐨𝐦 𝐂𝐨𝐧𝐭𝐞𝐱𝐭 𝐭𝐨 𝐌𝐞𝐦𝐨𝐫𝐲 𝐄𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠
Context Engineering is the buzzword of the week in AI circles, and for good reason. We're finally getting closer to the real work that needs to be done, but we need to go one step further to build truly reliable, believable, and capable AI agents.

𝐖𝐡𝐚𝐭 𝐢𝐬 𝐂𝐨𝐧𝐭𝐞𝐱𝐭 𝐄𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠?
Philipp Schmid describes it as "the discipline of designing and building dynamic systems that provides the right information and tools, in the right format, at the right time, to give a LLM everything it needs to accomplish a task."

Tobias Lütke, CEO of Shopify, captures the essence even more succinctly: "the art of providing all the context for the task to be plausibly solvable by the LLM."

And Andrej Karpathy blessed it.
So you know it's going in the Oxford dictionary along with Vibe Coding.

𝐓𝐡𝐞 𝐋𝐢𝐦𝐢𝐭𝐚𝐭𝐢𝐨𝐧 𝐨𝐟 𝐂𝐨𝐧𝐭𝐞𝐱𝐭 𝐄𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠
𝐓𝐡𝐞 𝐟𝐮𝐧𝐝𝐚𝐦𝐞𝐧𝐭𝐚𝐥 𝐥𝐢𝐦𝐢𝐭𝐚𝐭𝐢𝐨𝐧: 𝐜𝐨𝐧𝐭𝐞𝐱𝐭 𝐞𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠 𝐨𝐩𝐭𝐢𝐦𝐢𝐳𝐞𝐬 𝐟𝐨𝐫 𝐢𝐧𝐝𝐢𝐯𝐢𝐝𝐮𝐚𝐥 𝐢𝐧𝐭𝐞𝐫𝐚𝐜𝐭𝐢𝐨𝐧𝐬, 𝐛𝐮𝐭 𝐢𝐭 𝐝𝐨𝐞𝐬𝐧'𝐭 𝐞𝐧𝐚𝐛𝐥𝐞 𝐬𝐲𝐬𝐭𝐞𝐦𝐬 𝐭𝐡𝐚𝐭 𝐥𝐞𝐚𝐫𝐧 𝐚𝐧𝐝 𝐞𝐯𝐨𝐥𝐯𝐞 𝐨𝐯𝐞𝐫 𝐭𝐢𝐦𝐞. Your AI agent handles a complex customer inquiry perfectly, but forgets everything about that interaction.

𝐄𝐧𝐭𝐞𝐫 𝐌𝐞𝐦𝐨𝐫𝐲 𝐄𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠
Memory engineering addresses this by moving AI systems from stateless optimization to persistent intelligence.

Instead of just asking: 
❌ What information does this system need right now?
Memory engineering asks: 
✅ How can this system accumulate understanding that makes it more reliable and capable over time?

Here's what it looks like in practice↴
A context-engineered customer service agent retrieves relevant policy documents and previous tickets to answer current questions. 
A memory-engineered system does all of that, plus remembers interaction patterns, learns which communication approaches work best with specific customers, and continuously refines its understanding of common problem resolution strategies.

𝐌𝐞𝐦𝐨𝐫𝐲 𝐞𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠 𝐢𝐬 𝐭𝐡𝐞 𝐝𝐢𝐬𝐜𝐢𝐩𝐥𝐢𝐧𝐞 𝐨𝐟 𝐜𝐫𝐞𝐚𝐭𝐢𝐧𝐠 𝐬𝐲𝐬𝐭𝐞𝐦𝐬 𝐭𝐡𝐚𝐭 𝐬𝐲𝐬𝐭𝐞𝐦𝐚𝐭𝐢𝐜𝐚𝐥𝐥𝐲 𝐩𝐫𝐨𝐜𝐞𝐬𝐬, 𝐬𝐭𝐨𝐫𝐞, 𝐫𝐞𝐭𝐫𝐢𝐞𝐯𝐞, 𝐚𝐧𝐝 𝐮𝐩𝐝𝐚𝐭𝐞 𝐢𝐧𝐟𝐨𝐫𝐦𝐚𝐭𝐢𝐨𝐧 𝐭𝐨 𝐭𝐫𝐚𝐧𝐬𝐟𝐨𝐫𝐦 𝐫𝐚𝐰 𝐝𝐚𝐭𝐚 𝐢𝐧𝐭𝐨 𝐩𝐞𝐫𝐬𝐢𝐬𝐭𝐞𝐧𝐭 𝐦𝐞𝐦𝐨𝐫𝐲 𝐜𝐨𝐦𝐩𝐨𝐧𝐞𝐧𝐭𝐬, 𝐭𝐡𝐞𝐧 𝐝𝐲𝐧𝐚𝐦𝐢𝐜𝐚𝐥𝐥𝐲 𝐫𝐞𝐭𝐫𝐢𝐞𝐯𝐞 𝐚𝐧𝐝 𝐚𝐬𝐬𝐞𝐦𝐛𝐥𝐞 𝐭𝐡𝐞 𝐦𝐨𝐬𝐭 𝐫𝐞𝐥𝐞𝐯𝐚𝐧𝐭 𝐦𝐞𝐦𝐨𝐫𝐲 𝐜𝐨𝐦𝐩𝐨𝐧𝐞𝐧𝐭𝐬 𝐭𝐨 𝐩𝐨𝐩𝐮𝐥𝐚𝐭𝐞 𝐚𝐧 𝐋𝐋𝐌'𝐬 𝐜𝐨𝐧𝐭𝐞𝐱𝐭 𝐰𝐢𝐧𝐝𝐨𝐰 𝐟𝐨𝐫 𝐞𝐚𝐜𝐡 𝐢𝐧𝐭𝐞𝐫𝐚𝐜𝐭𝐢𝐨𝐧 𝐨𝐫 𝐬𝐞𝐬𝐬𝐢𝐨𝐧.

To be clear, Memory engineering doesn't replace context engineering
It builds on it.

hashtag#𝟏𝟎𝟎𝐃𝐚𝐲𝐬𝐎𝐟𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐀𝐈 hashtag#𝐌𝐞𝐦𝐨𝐫𝐲𝐄𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠 hashtag#𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲

---

### 𝐃𝐚𝐲 𝟑/𝟏𝟎𝟎 𝐨𝐟 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲

[post](https://www.linkedin.com/posts/richmondalake_100daysofagentmemory-ai-agentmemory-activity-7346687979605647360-lRaR?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAQRyLsBkSAisgCJmXavcznDzyDTxIecxnk)
Let's get you explaining Agent Memory like a pro.

Before we dive deeper into Agent Memory
It helps to understand why it matters in the first place. 
Whenever I'm asked about the importance of memory in AI 

𝐈 𝐞𝐱𝐩𝐥𝐚𝐢𝐧 𝐢𝐭 𝐭𝐡𝐢𝐬 𝐰𝐚𝐲:
If the aim of artificial intelligence is to mimic human intelligence, and one of the core components of intelligence is the ability to retain, recall, and reuse information—which in humans is governed by memory—then you can make the argument that for AI to achieve its objective, it needs some form of augmented computational memory.

Today, the agreed-upon form factor of AI is predominantly AI Agents and agentic systems.

𝐖𝐡𝐲 𝐌𝐞𝐦𝐨𝐫𝐲 𝐢𝐬 𝐍𝐨𝐧-𝐍𝐞𝐠𝐨𝐭𝐢𝐚𝐛𝐥𝐞
The importance of memory becomes crystal clear when you understand that it's the core component that makes AI agents more Reliable, Believable, and Capable—I call this the RBCs of AI Agents.
1️⃣ Reliable through consistent access to relevant historical context and learned patterns
2️⃣ Believable through coherent behavior that reflects accumulated experiences
3️⃣ Capable through the ability to leverage past knowledge for complex reasoning

𝐌𝐞𝐦𝐨𝐫𝐲 𝐓𝐲𝐩𝐞𝐬 𝐏𝐨𝐰𝐞𝐫𝐢𝐧𝐠 𝐑𝐁𝐂 𝐀𝐠𝐞𝐧𝐭𝐬
Different memory types enable different aspects of RBC behavior:
1️⃣ Reliability is powered by Episodic Memory - storing specific interactions with timestamps and context, ensuring agents can consistently reference past events and maintain coherent decision-making patterns over time.
2️⃣ Believability emerges from Semantic Memory - accumulating general knowledge and relationships that enable agents to demonstrate understanding that feels natural and contextually appropriate, just like humans draw from learned concepts. Persona memory also plays a role here, more on this later.
3️⃣ Capability is enhanced by Procedural Memory - retaining learned skills, workflows, and problem-solving approaches that allow agents to execute complex tasks more effectively through accumulated experience.

𝐀 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐄𝐱𝐩𝐥𝐨𝐫𝐚𝐭𝐢𝐨𝐧 𝐢𝐧 𝐑𝐞𝐚𝐥 𝐓𝐢𝐦𝐞
Full transparency: I'm not an expert teaching unsettled science. 
I'm an engineer actively exploring and uncovering these concepts alongside the broader AI community. 

So far, I find that this journey is as much about asking the right questions as it is about finding answers.

hashtag#𝟏𝟎𝟎𝐃𝐚𝐲𝐬𝐎𝐟𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐀𝐈 hashtag#𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐀𝐈𝐀𝐠𝐞𝐧𝐭𝐬

---

### 𝐃𝐚𝐲 𝟒/𝟏𝟎𝟎 𝐨𝐟 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲

[post](https://www.linkedin.com/posts/richmondalake_agent-memory-application-mode-activity-7347050219009695744-jaVE?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAQRyLsBkSAisgCJmXavcznDzyDTxIecxnk)
Let's talk about Application mode 
Their importance and how they map to Memory Types.

I've been thinking a lot about how the application mode an agent is expected to run in fundamentally defines the memory architecture it needs.

𝐖𝐡𝐚𝐭 𝐢𝐬 𝐀𝐩𝐩𝐥𝐢𝐜𝐚𝐭𝐢𝐨𝐧 𝐌𝐨𝐝𝐞?
Application mode refers to the operational environment and interaction patterns an agent is designed for. It's not about the domain (legal vs. medical vs. coding) but about how the agent fundamentally operates.
The three core application modes I'm observing are:
1️⃣ Assistant - Task-oriented systems providing specialized help through interactive dialogue while maintaining user context
2️⃣ Workflow - Process-driven systems that orchestrate multi-step operations through structured execution paths and tool coordination
3️⃣ Deep Research - Multi-source investigation systems that gather, synthesize, and report findings over extended periods

𝐖𝐡𝐲 𝐀𝐩𝐩𝐥𝐢𝐜𝐚𝐭𝐢𝐨𝐧 𝐌𝐨𝐝𝐞 𝐌𝐚𝐭𝐭𝐞𝐫𝐬
Identifying the right application mode when designing agent memory affects downstream decision in your AI stack:
✅ Embedding models - General purpose vs. domain-specialized 
✅ Memory architecture - Which memory types your agent needs 
✅ Agentic architecture - Single agent vs. multi-agent orchestration
✅ Retrieval methods - How your memory provider should be optimized

For example, Deep Research mode typically requires multi-agent architecture due to long-running execution and query parallelization. You spawn multiple agents for different research aspects, consolidate findings in shared memory, and have an orchestrator synthesize the final report.

When exploring the topic of application mode in agent memory I made I mistake. I viewed Coding, as a mode, which is wrong, it's instead a subset of Assistant Mode. I realized this when I making some changes to MemoRizz and trying to consolidate patterns in how agents are initialized.

💡So, the insight here is coding assistants, legal assistants, and medical assistants are all domain-specific variants of Assistant mode—they share the same operational patterns and memory requirements, just with different specialized knowledge.

Check out the attached PDF for more info.
And let me know what you think of Application Mode.

hashtag#𝟏𝟎𝟎𝐃𝐚𝐲𝐬𝐎𝐟𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐀𝐈 hashtag#𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐀𝐈𝐀𝐠𝐞𝐧𝐭𝐬

---

### 𝐃𝐚𝐲 𝟓/𝟏𝟎𝟎 𝐨𝐟 𝐀𝐠𝐞𝐧𝐭 𝐌𝐞𝐦𝐨𝐫𝐲

[post](https://www.linkedin.com/posts/richmondalake_100daysofagentmemory-100daysofagentmemory-activity-7347420372973084672-BiSo?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAQRyLsBkSAisgCJmXavcznDzyDTxIecxnk)
The best way to learn is to build.
So I'm building MemoRizz.

Five days into this journey, and I'm already exploring some fascinating research about agent memory architectures. But reading papers, articles and theorizing only gets you so far. To truly understand how memory works in AI agents, you need to get your hands dirty and built

𝐈𝐧𝐭𝐫𝐨𝐝𝐮𝐜𝐢𝐧𝐠 𝐌𝐞𝐦𝐨𝐑𝐢𝐳𝐳
I'm building an open-source Python library that serves as a memory layer for AI applications. Think of it as the practical implementation of everything I'm learning in this hashtag#100DaysOfAgentMemory series.
I will probably get a lot of things(definitions, techniques and implementations) wrong, and I think that's fine.

𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠 𝐢𝐧 𝐏𝐮𝐛𝐥𝐢𝐜, 𝐁𝐮𝐢𝐥𝐝𝐢𝐧𝐠 𝐢𝐧 𝐎𝐩𝐞𝐧
The point is that most of the concept I explore in this series gets tested, implemented, and refined in MemoRizz. When I discover something interesting about how procedural memory should work in workflow agents, it goes straight into the codebase.

On day 5️⃣ I worked on a form of episodic memories that some refer to as summarisation or observations. This is where you consolidate logs of interactions within a session, and compress them into summaries that can be used in future execution of agents for broader context of a problem domain or environment. A question I asked myself is when do I trigger a summarisation? When the context window gets full ? At the end of the session or day?

Either way I will release this feature in a few days in MemoRizz.

𝐖𝐡𝐲 𝐎𝐩𝐞𝐧 𝐒𝐨𝐮𝐫𝐜𝐞?
Agent memory is still an emerging field, and I believe the breakthroughs will come from the community—researchers, engineers, and builders working together to solve these fundamental challenges.

𝐖𝐡𝐚𝐭'𝐬 𝐍𝐞𝐱𝐭?
Over the next 95 days, MemoRizz will evolve alongside my understanding. 
Each post in this series will likely spawn new features, optimizations, or architectural decisions in the library. 
It's going to be messy and iterative, but we will a lot along the way.

The library is already gaining traction
—322 stars and growing
—which tells me we're onto something important here.

Want to contribute? 
Check out the repo: https://lnkd.in/eNwAZRhf

hashtag#𝟏𝟎𝟎𝐃𝐚𝐲𝐬𝐎𝐟𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐎𝐩𝐞𝐧𝐒𝐨𝐮𝐫𝐜𝐞 hashtag#𝐀𝐈 hashtag#𝐀𝐠𝐞𝐧𝐭𝐌𝐞𝐦𝐨𝐫𝐲 hashtag#𝐏𝐲𝐭𝐡𝐨𝐧

---


