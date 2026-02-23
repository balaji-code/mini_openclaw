📦 Mini OpenClaw – Minimal Tool-Augmented AI Agent (Telegram + CLI)

A minimal yet production-oriented AI agent framework built around Anthropic Claude.

This project demonstrates how to design and implement:
	•	Multi-agent architecture
	•	Tool-augmented LLM reasoning (ReAct loop)
	•	Persistent conversation memory
	•	Long-term memory storage
	•	Telegram bot integration
	•	Scheduled autonomous tasks
	•	Basic permission control for tool execution

This is not just a chatbot.
It is a compact agent architecture skeleton.

⸻

🚀 Features

🧠 Multi-Agent Support
	•	Jarvis – Personal AI assistant
	•	Scout – Research-focused agent
	•	Easy to extend with new agents

🔁 Tool-Augmented Reasoning (ReAct Loop)

The LLM can:
	•	Request tools
	•	Receive results
	•	Continue reasoning
	•	Produce final output

Tools implemented:
	•	run_command
	•	read_file
	•	write_file
	•	save_memory
	•	memory_search

⸻

💾 Persistent Memory

Session Memory
	•	Stored as JSONL files
	•	Maintains conversational context
	•	Includes automatic history compaction

Long-Term Memory
	•	Markdown-based knowledge storage
	•	Searchable across sessions

⸻

🤖 Telegram Bot Integration
	•	Each Telegram user gets an isolated session
	•	Async message handling
	•	Event-driven architecture
	•	Multi-user capable

⸻

⏰ Scheduled Tasks
	•	Built-in daily heartbeat example
	•	Demonstrates autonomous execution

🔐 Security Notice (Important)

This project includes powerful tools such as:
	•	Shell command execution
	•	File read/write access

⚠️ Do NOT deploy publicly without:
	•	Removing or sandboxing run_command
	•	Restricting file access to workspace only
	•	Adding user authentication / whitelist
	•	Adding rate limiting

This project is designed for learning and controlled environments.

⸻

🧩 Design Philosophy

This project demonstrates:
	•	Clear separation of concerns
	•	Tool execution outside LLM
	•	Persistent structured memory
	•	Event-driven Telegram architecture
	•	Minimal yet extensible agent loop

It is intentionally simple, but architecturally clean.

