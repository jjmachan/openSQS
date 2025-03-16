# Distributed Task Queue
A PostgreSQL-powered distributed task processing system built with Python and SQLModel/SQLAlchemy.
## Project Overview
This distributed task queue allows you to:

1. Submit asynchronous tasks for background processing
2. Distribute work across multiple worker processes
3. Track task progress and retrieve results
4. Handle failures gracefully with automatic retries
5. Schedule tasks for future execution
6. Manage task dependencies and priorities

## Why This Project?
This project explores the fascinating intersection of:

- Distributed systems concepts and challenges
- PostgreSQL's advanced features beyond basic CRUD operations
- Concurrency control in database systems
- Fault tolerance and recovery mechanisms

## Key Features

- Atomic task claiming using PostgreSQL's FOR UPDATE SKIP LOCKED
- Real-time notifications with LISTEN/NOTIFY
- Flexible task payloads with JSONB
- Distributed coordination with advisory locks
- Worker health monitoring with heartbeats
- Task scheduling with dependencies and priorities
- Resilient failure handling with automatic retries

## Technical Architecture
The system consists of four main components:

- Database Layer: PostgreSQL with specialized schema for task management
- Producer API: Client interface for submitting and managing tasks
- Worker Nodes: Independent processes that execute tasks
- Scheduler: Coordinates timing and dependencies