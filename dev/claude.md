# claude.md Template

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Session Logic
At the beginning of each session claude will be instructed to read this file. Claude should first identify the session number by counting existing sessions in claude-context.md and announce "Beginning Session #X" where X is the next session number. Upon reading this file claude will get an understanding of the current project and get context for the rest of the files in the directory. Once this file has been reviewed claude should use this context to read the rest of the files in the directory and give the user an indication that they have completed all the tasks by stating "up to date on dev contents" and then provide a summary of the project status and proposed next steps based on the progress.md or any other relevant files in this directory.

When told to "log session" claude will announce "Logging Session #X" where X is the current session number, then review this file again, followed by the rest of the files in this directory and update them as appropriate based on what has been done either since the session started, or since the last "log session" was executed. Sessions should be added to claude-context.md as separate numbered journal entries (Session 1, Session 2, etc.). Each session entry should be completely separate and independent. Previous sessions should be retained by default - never modify or combine previous session entries.

When told to "wrap up" the session claude will announce "Wrapping up Session #X" where X is the current session number, then review this file again, followed by the rest of the files in this directory and update them as appropriate based on what was done that session. Sessions should be added to claude-context.md as separate numbered journal entries (Session 1, Session 2, etc.). Each session entry should be completely separate and independent. Previous sessions should be retained by default - never modify or combine previous session entries. Claude will suggest adding, committing, and pushing if appropriate. Claude will let the user know this is done and that we are ready to end the session.

## Development Folder Structure

This `dev/` directory contains project management and documentation files to support development workflow:

### `claude-context.md`
- **Purpose**: Store session information between Claude Code sessions
- **Usage**: Update before closing each session with key progress, decisions, and context. Sessions should be added as separate numbered journal entries (Session 1, Session 2, etc.). Each session entry should be completely separate and independent. Previous sessions should be retained by default - never modify or combine previous session entries.
- **Benefits**: Provides continuity for future sessions, maintains development history

### `progress.md`
- **Purpose**: Comprehensive project status tracking and roadmap
- **Usage**: Regular updates to component completion status, milestones, and goals
- **Benefits**: Clear visibility into project state, structured progress tracking

### `error-log.md`
- **Purpose**: Centralized error tracking and debugging information
- **Usage**: Populated by developer when error logs are too large for chat interface
- **Benefits**: Persistent error context, easier debugging across sessions

### `app-framework.md`
- **Purpose**: Technical documentation of application architecture and logic
- **Usage**: Document key technical decisions, algorithms, and implementation details
- **Benefits**: Reference for complex logic, onboarding documentation

### `claude.md`
- **Purpose**: Development guidance and project overview for Claude Code
- **Usage**: Instructions for consistent development approach and project context
- **Benefits**: Ensures Claude follows project conventions and understands architecture

## Project Overview

Stateful Claude Framework - A documentation system that maintains context and continuity between Claude Code sessions for complex, long-term projects. Solves the problem of losing project context by providing structured templates and workflows.

## Architecture

### Core Technologies
- Markdown documentation system
- Git version control
- Template-based project structure
- Claude Code integration

### File Structure
```
stateful-claude/
├── dev/                     # Our own stateful instance
├── *-TEMPLATE.md           # Framework templates
├── framework-purpose.md    # Framework philosophy
├── setup.md               # Setup instructions
└── README.md              # Basic usage
```

### Key Components
- **Templates**: Reusable documentation structures
- **Session Management**: Workflow for maintaining context
- **Progress Tracking**: Structured roadmap and completion tracking
- **Context Preservation**: Historical session information

## Development Commands

- `git status` - Check repository status
- `git add .` - Stage changes
- `git commit -m "message"` - Commit changes
- `git push` - Push to remote

## Deployment

This is a documentation framework - no traditional deployment needed. Distribution via:
- GitHub repository
- Template file sharing
- Documentation and examples

## Roadmap Updates
- **ALWAYS** update the "Current Roadmap" section in progress.md in-place
- **NEVER** create duplicate roadmap sections
- Archive superseded roadmaps in "Roadmap History" when major changes occur
- Use clear timestamps and reasons when archiving old roadmaps

## Key Development Considerations

- Keep templates generic but useful
- Focus on Claude Code workflow optimization
- Maintain clear separation between template and instance files
- Prioritize session continuity and context preservation

## Common Tasks

- Update template files based on user feedback
- Test template effectiveness with real projects
- Improve roadmap management and session workflows
- Document best practices and usage patterns

---

**Instructions for Use:**
1. Replace all `{PLACEHOLDER}` sections with project-specific information
2. Update project overview with your specific application details
3. Customize development commands and deployment information
4. Add project-specific considerations and common tasks