Version: NAFATH-V3
Track: Software

## Overview

When a citizen opens the government assistant app, Mobile security protects the connection by requiring HTTPS. Networking transfers the citizen’s question between the app and the government server. Software uses clear version numbers to show whether an API update may break compatibility with existing applications. Artificial Intelligence (AI) helps the assistant answer questions using official government documents through Retrieval-Augmented Generation (RAG). Cybersecurity protects the assistant from prompt injection attacks, where malicious instructions in user input or external documents may change its behavior. Data protects chat records and citizens’ personal information. Pseudonymisation replaces names with codes, while anonymisation removes identifying information so people cannot reasonably be identified. These six fields work together to make the assistant secure, reliable, and useful for citizens.

## Software

Semantic Versioning uses three numbers: MAJOR.MINOR.PATCH. MAJOR must increase when a backward incompatible change is made to the assistant’s public API. For example, removing a field used by existing applications requires a MAJOR release. MINOR increases when compatible features are added or a feature is marked as deprecated. For example, adding a new language requires a MINOR release. PATCH increases when backward-compatible bug fixes are made, such as correcting a wrong appointment time in the assistant’s answer.

Resource: Semantic Versioning 2.0.0 - https://semver.org

## AI

Retrieval-Augmented Generation (RAG) helps AI systems answer questions using external information. It searches relevant documents and retrieves passages. The model uses these passages to generate an answer. This reduces errors because answers are based on retrieved documents, not only the model’s stored knowledge. Documents can be updated without retraining the model. For example, a government assistant can use official documents to answer questions about service fees. However, RAG may still make mistakes if it retrieves irrelevant information.

Resource: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks - https://arxiv.org/abs/2005.11401

## Mobile

App Transport Security (ATS) protects iOS apps. It requires HTTPS for connections using URL Loading System, such as URLSession. It checks TLS security and server certificates. If an app connects to a normal HTTP address, ATS blocks the connection by default unless an exception is configured. For example, a government assistant app should use HTTPS to protect citizens’ information when connecting to its server. Exceptions should be limited because they reduce security.

Resource: NSAppTransportSecurity - https://developer.apple.com/documentation/bundleresources/information-property-list/nsapptransportsecurity

## Networking

IPv6 is the successor to IPv4. IPv4 addresses are 32 bits, while IPv6 addresses are 128 bits. IPv6 simplifies the packet header by removing some IPv4 fields or making them optional. Its larger address space supports many more devices. IPv4 provides about 4.3 billion addresses, which is not enough for growing demand. For a government assistant serving millions of citizens, IPv6 helps support more connected devices.

Resource: RFC 8200: Internet Protocol, Version 6 (IPv6) Specification - https://www.rfc-editor.org/rfc/rfc8200

## Cybersecurity

Prompt injection happens when input changes an AI assistant’s behavior unexpectedly. Direct injection comes from user input, intentionally or accidentally. Indirect injection comes from external sources, such as websites or files. For example, a government assistant may read a document with hidden instructions to reveal citizens’ private data. To reduce risk, developers should separate untrusted content from trusted instructions and limit the assistant’s permissions. These methods reduce risk but cannot eliminate it.

Resource: LLM01:2025 Prompt Injection - https://genai.owasp.org/llmrisk/llm01-prompt-injection/

## Data

Pseudonymisation replaces names with codes, while keeping the extra identifying information separately and securely. The data remains personal data, so GDPR still applies. For example, a government chatbot may replace a citizen’s name with “User123”, but messages may still reveal their identity through an address or ID number. Anonymisation removes identifying details so people cannot reasonably be identified. Truly anonymous data falls outside GDPR.

Resource: Regulation (EU) 2016/679 - https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32016R0679

## Misconception in My Track

A common misconception about Semantic Versioning is that marking a feature as deprecated requires a MAJOR version increase. However, item 7 under “Semantic Versioning Specification (SemVer)” states that marking public API functionality as deprecated requires a MINOR version increase. Item 8 says MAJOR must increase when a change breaks backward compatibility. For example, a government assistant can announce that an old API endpoint is deprecated in a MINOR release before removing it in a future MAJOR release. The FAQ entry “How should I handle deprecating functionality?” supports this.

## Open Question

How should a government entity inform application developers that an API endpoint is deprecated, and how much time should it give them to update their applications before the endpoint is removed?
