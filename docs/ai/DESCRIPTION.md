# AI

This folder defines the AI agent behavior and context layer.

It covers how agents read documentation, load context, select relevant knowledge, and produce structured artifacts.
The project remains AI-provider independent, so the contents here should work with different models and execution backends.

Use this folder for:

- agent definitions
- context strategy
- retrieval rules
- tool usage
- evaluation
- system prompts

AI is not the source of business knowledge.
It consumes knowledge from the documentation, dictionaries, schemas, and templates.

See also:

- [Architecture](../ARCHITECTURE.md)
- [Glossary](../GLOSSARY.md)
- [Prompts](../prompts/DESCRIPTION.md)
- [Schemas](../schemas/DESCRIPTION.md)
- [Dictionaries](../dictionaries/DESCRIPTION.md)
