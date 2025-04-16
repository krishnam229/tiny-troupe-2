# Q1 tinytroupe Installation & Setup Guide

This guide will walk you through installing and configuring the tinytroupe package in a GitHub Codespace environment.

---

## 📦 Step 1: Install Packages

1. *Open a terminal* in your GitHub Codespace.

2. *Clone the repository*:
   bash
   git clone https://github.com/microsoft/tinytroupe
   

3. *Navigate to the project folder*:
   bash
   cd tinytroupe
   

4. *Install the package*:
   bash
   pip install .
   

---

## 🔐 Step 2: Setup OpenAI API Key

1. In the same terminal, set your OpenAI API Key:
   bash
   export OPENAI_API_KEY="your-openai-key-here"
   

2. (Optional) To make the API key persist between sessions, add the following line to your shell configuration file (e.g., ~/.bashrc, ~/.zshrc, or ~/.profile):

   bash
   echo 'export OPENAI_API_KEY="your-openai-key-here"' >> ~/.bashrc
   source ~/.bashrc
   

3. Verify the key is set:
   bash
   echo $OPENAI_API_KEY
   

---

## ✅ You're Ready!

Once setup is complete, you can begin using the tinytroupe framework to simulate multi-agent LLM interactions.

1.	For more usage examples, see the [official GitHub repo](https://github.com/microsoft/tinytroupe).


# Q2  What is Turing Test? In today's world with Large Language Models (LLMs), what is the definition of Turing Test?
The Turing Test was proposed in 1950 by Alan Turing, a pioneer of computer science. The goal of the test is to assess a machine's ability to exhibit intelligent behavior indistinguishable from that of a human.
In the Original Setup:
•	A human judge interacts with a machine and a human.
•	If the judge cannot reliably tell which is the machine, then the machine is said to have passed the Turing Test.
Today, the Turing Test has evolved beyond the basic “Can it fool a judge?” setup.
Modern Interpretation with LLMs:
•	Focuses on contextual coherence, empathy, humor, common sense reasoning, and factual correctness.
•	A new benchmark includes not just fooling a human, but also sustaining meaningful, goal-oriented, error-free dialogue.
•	There's growing debate on whether just being convincing is enough — especially with LLMs like GPT-4 passing casual Turing Tests easily.

# Q3 Create a simulation of your own topic and show me the transcript. This implies define at least two personas of your own choice with conflict built in and observe their conversation. You can simply copy/paste the conversation in a .md file. Please comment on the transcript whether you think the Turing Test is passed.

>>> world = TinyWorld("Classroom", [yiqiao, john])
>>> world.make_everyone_accessible()
>>> 
>>> yiqiao.listen("I want to extend my homework.")
USER --> Yiqiao: [CONVERSATION] 
          > I want to extend my homework.
TinyPerson(name='Yiqiao')
>>> world.run(3) # trigger the conversation with 3 rounds back-and-forth
──────────────────────────────────────────────────────────────────── Classroom step 1 of 3 ─────────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > The person wants to extend their homework. I should ask them why they need an
            > extension and if they need help with anything specific.
Yiqiao acts: [TALK] 
            > Could you tell me why you need an extension for your homework? Is there something
            > specific you're struggling with?
Yiqiao acts: [DONE] 

Yiqiao --> John: [CONVERSATION] 
            > My name is Yiqiao, I'm 35 years old, and I'm from China. I work as a professor at a
            > university. I enjoy teaching and sharing knowledge with my students.
Yiqiao --> John: [CONVERSATION] 
            > Could you tell me why you need an extension for your homework? Is there something
            > specific you're struggling with?
John acts: [TALK] 
          > I appreciate your concern, Yiqiao. I've been struggling to keep up with the workload
          > lately, and I could really use a bit more time to ensure I submit my best work. Would
          > that be possible?
John acts: [DONE] 

John --> Yiqiao: [CONVERSATION] 
          > I appreciate your concern, Yiqiao. I've been struggling to keep up with the workload
          > lately, and I could really use a bit more time to ensure I submit my best work. Would
          > that be possible?
──────────────────────────────────────────────────────────────────── Classroom step 2 of 3 ─────────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > John is struggling with his workload and needs more time for his homework. I should
            > consider granting him an extension and ask how much time he needs.
Yiqiao acts: [TALK] 
            > I understand that managing workload can be challenging. How much extra time do you
            > think you would need to complete your homework?
Yiqiao acts: [DONE] 

Yiqiao --> John: [CONVERSATION] 
            > I understand that managing workload can be challenging. How much extra time do you
            > think you would need to complete your homework?
John acts: [TALK] 
          > Thank you for understanding, Yiqiao. I think an extra week would really help me to
          > complete my homework to the best of my ability. Would that be acceptable?
John acts: [DONE] 

John --> Yiqiao: [CONVERSATION] 
          > Thank you for understanding, Yiqiao. I think an extra week would really help me to
          > complete my homework to the best of my ability. Would that be acceptable?
──────────────────────────────────────────────────────────────────── Classroom step 3 of 3 ─────────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > John is asking for an extra week to complete his homework. I think that's a reasonable
            > request, and I should agree to it.
Yiqiao acts: [TALK] 
            > Yes, an extra week sounds perfectly reasonable. I’m glad you feel that will help you
            > submit your best work. Just make sure to reach out if you need any further assistance
            > during that time.
Yiqiao acts: [DONE] 

Yiqiao --> John: [CONVERSATION] 
            > Yes, an extra week sounds perfectly reasonable. I’m glad you feel that will help you
            > submit your best work. Just make sure to reach out if you need any further assistance
            > during that time.
John acts: [TALK] 
          > Thank you so much, Yiqiao! I really appreciate your understanding and support. I will
          > definitely reach out if I need any help during the week.
John acts: [DONE] 

John --> Yiqiao: [CONVERSATION] 
          > Thank you so much, Yiqiao! I really appreciate your understanding and support. I will
          > definitely reach out if I need any help during the week.