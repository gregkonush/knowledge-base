---
id: bhtykxq723p3wv97lf8y1kb
title: Knowledge Base
desc: ''
updated: 1662244152614
created: 1662014858035
---

## Development notes

### Logstash

This utility is part of ElasticSearch/OpenSearch stack can help with real time processing of events

Can be using as part of ETL to accept denormalized events, process them and move events to data store or search index

### Quarkus

Set of technology, libraries, frameworks optimized for native kubernetes runtime

### Armeria

Java microservice framework developed by creator of Netty

### GraalVM

Polyglot JVM. Can execute other language with one compiler.
Nashorn JavaScript engine is not included in OpenJDK. Oracle and GraalVM have `ScriptEngineManager` class


Practical use cases:

- Safely evaluate JavaScript from Java
- There is an interop between languages
  - Execution context can be set before evaluation
  - Resulting values can be extracted after evalution

[JavaScript Evaluation Code Snippet](/root.java.graalvm.md)

### Liquibase

Framework for database migrations and schema upgrades. It has a plugin for MongoDB

### MongoDB

NoSQL database

### Dendron

Notes are stored with [Dendron](https://wiki.dendron.so/)

Install Dendron cli

```bash
npm install -g @dendronhq/dendron-cli@latest
```
