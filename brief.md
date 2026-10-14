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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
