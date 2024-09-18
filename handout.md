# Workshop Handout: AI Augmented Web Development with Cursor

## 1. Introduction to AI-Augmented Development with Cursor

Welcome everybody to the Cursor workshop! If you're here, you've likely heard of Cursor, but if not, let me introduce you to this premium AI code editor. Cursor has rapidly become one of the most popular software tools in the AI space, experiencing a significant surge in popularity over the past year and a half.

The recent explosion in Cursor's user base is largely due to the increasing power and code aptitude of Large Language Models (LLMs). Developers are now realizing the substantial productivity gains that can be achieved with this tool. In this workshop, we'll explore how to integrate Cursor into your AI development workflow and your general software development process.

Cursor stands out as the best way to boost your productivity with AI tools. It seamlessly integrates AI features into an IDE, creating a natural and intuitive experience. The tool is designed to keep you in your workflow without disrupting your focus.

A word of advice: be patient as you learn these new workflows and features. It typically takes about one to two weeks to fully commit the hotkeys to memory and become familiar with all the available features. Once you overcome this initial learning curve, these tools will become second nature, and you'll find yourself writing high-quality code more efficiently than ever before.

Now, let's dive into the details of AI-augmented development with Cursor!

## 2. Setup

You can access Cursor specific settings via the settings gear in the bottom right corner or by pressing `Shift + Command + J` and selecting `Cursor Settings`.

### 2.1. Getting API keys for OpenAI and Anthropic

You can use Cursor with your personal OpenAI and Anthropic API keys, thus avoiding their subscription fees, but you'll get better throughput and reliability with their PRO plans.

### 2.2 Custom API keys on Cursor

You can also use other open source models on Cursor with your own API keys, but you'll need to make sure you're using a model that supports function calling and has a context window that's large enough to handle the code you're trying to generate. Check out the Open Router project for a list of models that support function calling, see this [blog post](https://medium.com/ai-creators/how-to-use-claude-3-on-cursor-ai-855edee19c6e) for a step by step guide on how to add them.

### 2.3 Recommended settings

Example of a good set of Rules for AI based on Ruby on rails projects, (customize for your needs and programming language):

```txt
 In ruby on rails projects: 
- Always suggest the latest Ruby On Rails conventions and code
- Use Hotwire (Stimulus JS, Turbo frames, Turbo Streams, etc)
- Always prefer the hotwire way when possible, avoid writing senseless javascript just because, use "sprinkles" and always prefer Stimulus JS code. 
- If you are adding a new stimulus controller, always add it to the index.js file too. 
- Always prefer double quotes unless the double quotes break the code
- Layout/SpaceInsideArrayLiteralBrackets: Use space inside array brackets. (RuboCopLayout/SpaceInsideArrayLiteralBrackets)
```

## 3. Cursor Features: Tab

- **Code Generation**: Cursor can generate code changes based on your request, allowing you to quickly implement new features or modify existing code.
- **Multi-Line Edits**: Cursor enables you to make multiple edits at once, saving time when refactoring or updating large sections of code.
- **Smart Rewrites**: Cursor can automatically fix your mistakes and improve your code quality by suggesting better implementations.
- **Cursor Prediction**: Cursor predicts your next cursor position, helping you navigate through your code more efficiently.
- **Autocomplete**: Cursor includes a powerful autocomplete feature that predicts your next edit, making coding faster and more accurate across multiple files.

## 4. Cursor Features: Chat

- **Chat**: Cursor offers a chat feature that allows you to interact with the AI assistant. You can ask questions, request explanations, or seek help with specific coding tasks. The chat interface supports natural language input, making it easy to communicate your needs and receive tailored assistance.
- **Codebase Awareness**: The chat feature is aware of your entire codebase, allowing you to ask questions about specific files or code sections without needing to manually provide context.
- **File and Symbol References**: You can reference specific files or symbols in your chat queries, enabling more precise and context-aware interactions with the AI assistant.
- **Web Search Integration**: Cursor's chat feature can perform web searches to gather additional information or resources related to your queries, enhancing its ability to provide comprehensive assistance.

## 5. Cursor Features: Command + K

- **Fast Edits**: Quickly edit code with AI assistance. Select some code, press Command + K, and describe how the code should be changed to generate new code.
- **Terminal Commands**: Use Command + K in the terminal to write terminal commands in plain English. Cursor will convert your instructions into the terminal syntax you need.
- **Quick Questions**: If you have questions about specific parts of your code, select the relevant section and use "Quick Question" to get instant answers.
- **AI-Powered Search**: Easily search and navigate through your codebase using natural language queries.
- **Code Generation**: Generate new code snippets or entire functions based on your descriptions.
- **Refactoring Assistance**: Get AI suggestions for refactoring your code to improve its structure and readability.

## 6. Cursor Features: Composer with "Notepads" (Previously called Projects)

- Composer is a coding agent that can create files, folders and code more directly instead of prompting it like the Chat feature.
- Composer has a "Notepads" feature that allows you to create different "projects" or "notepads" to help you organize your code and ideas and share them between composers

## 7. Core skills for working with AI

- Regenerate often. This will give you an idea of how "wide" the probabilistic spray of a model is.
- Start new conversations often. This helps make sure that your prompts are solid and helps maintain a clean and small context window.
- Don't be afraid to use many different system prompts or just straight out / commands in chat.openai.com etc.
- Experiment with new models coming out all the time. This doesn't mean just bigger models, but also smaller faster models. Get a feel for what they can or cannot do and how they behave (or misbehave).
- Practice solving the same problem multiple time as you learn more (something called "code katas" in agile literature).
- Don't hesitate to edit your or even the LLMs messages. "Gaslight" them your heart's content. Let them think they output the code you had to fix.
- Generate helper scripts to help you work (edit clipboard, store things in history, search transcripts, etc).
- Don't do anything tedious by hand anymore.

## 8. 10x Developer with AI skills

- **Deep practical and fundamental knowledge** - Knowing how to build something and do it repeatedly in light of changing circumstances helps recognize what patterns to apply to decompose a problem into steps within the reach of a specific LLM, and recognize when the LLM goes awry.
- **Constantly practicing** - This is more of a skill like playing the guitar or other crafts, and less something you can learn analytically and out of books. You have to develop your own style and intuition on how models behave. Practice solving every problem you encounter with LLMs, or at least think "how could I decompose this so that I can solve parts of it with an LLM"
- **User centric thinking** - This might sound paradoxical, but the output of an LLM only has value if it is "experienced" by a human. If you don't know what the target human wants (be it a working app, or some clear documentation or a great TPS report), you will not have a direction for decomposing the problem into "natural language translation steps".
- **Divergent thinking** - LLMs are a cultural technology. You have to think outside the box to actually explore the box. Thinking of "can I use greek tragedy to make the LLM create better code reviews" is a step that is not easy to make. Look at what non-programmers are prompting.
- **Abstract thinking / meta thinking** - For each thing you build, think about the implications on the overall problem you are solving. Can you build the thing that builds the thing that solves the problem? Can you write the software that does the thing you just had the LLM do? Can you write the software to help you write the software that builds the software that helps humans write software that writes software?
- **learning when to step away** - You can only go so fast. You can generate 80 versions of a piece of software, and even have it working: the temptation is big to continue. But often, the best engineering decision you can make is to go walk in the woods.
- **Learn when you should do something yourself** - LLMs can't really reason, they certainly can't reason creatively. They will not create new algorithms because they thought really hard about it until they had a eureka moment. In fact they can't often solve a simple programming task like a SQL query to compute YOY revenue. Instead of fighting the model and going against the grain, just write the query yourself. It's way more fun, and one of the reasons we became programmers in the first place.
- **Learn about DSL and language design** - Language is the alpha and omega of LLMs. There is nothing more. Learn about programming language design and philosophy of language and linguistics and mysticism (so much of mysticism is about words) and literature and foreign languages and grammar and knowledge representation and cognitive linguistics. They now are all "programming frameworks." Of special interest are self-referential languages like Common Lisp, ruby, forth or to a lesser degree Haskell.

## 9. Tips for using Cursor

### 9.1 Plan before coding

- Sketch out ideas (Figma, Excalidraw, tldraw, paper!)
- Brainstorm with AI using Cursor Chat. (Rubber duck debugging)
- Use V0 for mockups (10-15 prompts minimum)

### 9.2 Keep a "Prompt Album"

- Copy tech-specific prompts
- Create .cursor_rules file in project root (Drastically improves Cursor's output)
- Pro tip: Customize prompts for your exact tech stack

### 9.3 Tag relevant documentation

- Add official docs to Cursor (Ruby on Rails, Stimulus JS, Python Packages, etc.)
- Ensures up-to-date, accurate responses
- Cursor reads docs when answering queries

### 9.4 Ask other AI models when stuck

- Copy errors to Claude, GPT-4, etc.
- Include failed solutions for better context
- Different models can solve problems others can't.

### 9.5 Use AI to explain code

- Great for learning & documentation
- Ask to explain like you're a beginner
- Follow up on confusing concepts
- The more you do this, the more you learn patterns

### 9.6 Leverage existing code templates

- Start with boilerplate (auth, DB, payments)
- Build on top of proven foundations
- Saves time on repetitive tasks

### 9.7 Add comments to your code

- Ask AI to explain & document your code
- Improves readability & understanding
- Great for team collaboration

### 9.8 Duplicate & modify existing functionality

- Copy working code from other parts of your project
- Ask AI to adapt it for new use cases
- Provides context for better results
- Key takeaway: Give AI as much context as possible for best results!

## 10. Advanced Tips

- Create a "prompts" folder in your project root. Add different .txt files like "Add double quotes to all strings" then use @prompts/filename.txt in your cursor chat.
- Use a whisper based voice to text tool like https://superwhisper.com/ to prompt the AI.

## 11. Best Practices for AI-Augmented Development

- Verify AI-generated code
- Use AI as a brainstorming tool
- Combine AI suggestions with human expertise
- Regularly update your AI tools

## 12. Additional Resources

- Simon Willison's blog: [simonwillison.net](https://simonwillison.net/)
- "Computational Logic and Human Thinking" by Robert Kowalski
- [LLMs Will Fundamentally Change Software Engineering](https://the.scapegoat.dev/llms-will-fundamentally-change-software-engineering/)
- [Centaurs and Cyborgs on the Jagged Frontier](https://www.oneusefulthing.org/p/centaurs-and-cyborgs-on-the-jagged)
