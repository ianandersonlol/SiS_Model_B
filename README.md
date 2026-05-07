# SiS Model B

**Swap It Smart (SiS)** — an AI-powered recipe creativity assistant with a Python/FastAPI backend and React/Vite frontend.

## Changelog

### 2026-03-17
- Fixed recipe share URL routing and consolidated public recipe routes
- Simplified navigation in recipe cards; added pepper variants to always-available ingredients
- Removed confirmation pattern from pantry tools; lint cleanup across backend
- Synced migration schema drift for CI

### 2026-03-16
- Rebranded to "SiS powered by PTFI" with updated icons and assistant display name
- Added user-level preferences system (dietary profiles, AI mode settings)
- Added kitchen profile workspace type picker with budget settings
- Added clear-all pantry action, prep item flag, and send-to-pantry for recipes
- Added public recipe sharing via share links with unauthenticated route support
- Added USDA weight references, price normalization, and ingredient cost rollup
- Improved ingredient fuzzy matching with token-based comparison
- Added keywords style bar with auto-expiry tracking
- Added GFM table rendering in chat messages
- Added Excel sheet metadata and multi-sheet selection for pantry import
- Added admin usage monitoring dashboard endpoint
- Parallelized context assembly in kitchen chat for performance
- Large dead-code cleanup: removed unused components, hooks, and feature stubs
- Persisted generated recipes in assistant message metadata

### 2026-03-15
- Added multi-source pantry import: clipboard paste, photo capture, Google Sheets link, and undo support
- Enhanced backend pantry import with import logs, batch undo, and file/photo parsing

### 2026-03-14
- Added security audit and migration drift detection CI workflows
- Fixed home feed flash on navigation; ensured account section always shows

### 2026-03-13
- Fixed Supabase JWT verification to accept ES256 algorithm
- Added PTFI proteomics tools for protein and amino acid analysis
- Redesigned recipe studio UI with copilot-first workflow
- Polished login page UX; added account section with logout to workspace settings
- Added PTFI badge with tooltip to recipe cards

### 2026-03-11
- Added mypy type checking and fixed type annotations across backend
- Added conversation branching support (backend + frontend)
- Added agent execution metrics and limit tracking
- Added tool auto-discovery for dev mode
- Added photo import tool and recipe image parsing endpoint
- Added Vitest testing infrastructure for frontend
- Added PWA support with service worker and install prompt
- Upgraded theme system with system-preference support
- Added branded login page with centered layout and real logo
- Added cost summary and recipe sharing features

### 2026-02-27
- Enhanced food atlas tool with disease search and attribution requirements

### 2026-02-26
- Added Supabase JWT auth service with user-scoped repositories and usage tracking
- Added AppUser model and dual-ownership schema migration
- Wired auth into API routes and middleware with REQUIRE_AUTH setting
- Integrated Supabase auth into frontend: AuthContext, Google OAuth, password reset, signup confirmation
- Added React error boundaries, 401 token recovery, and SSE inactivity timeout
- Added GitHub Actions CI workflows for both backend and frontend
- Added global focus-visible keyboard navigation styles
- Added security headers for static hosting
- Updated README with architectural overview and quickstart guide

### 2026-02-25
- Added food atlas integration and recipe-scrapers support for URL import
- Added spreadsheet import service for pantry items (SheetJS/PapaParse)
- Added pantry inventory fields, edit/depletion endpoints, and inventory-aware agent tools
- Built pantry edit UI with progressive badges and manager table
- Applied security fixes: IDOR protection, prompt injection guards, input validation, rate limiting
- Added conversation persistence via URL routing
- Compressed orchestrator system prompt; added in-memory LRU cache for ingredient categorization
- Added evaluation framework for orchestrator agent testing

### 2026-02-24
- Added save-imported endpoint for recipe import wizard
- Fixed recipe import API calls for wizard flow

### 2026-02-23
- Added drag-and-drop recipe selection to meal planner
- Replaced local chef mode state with URL-based studio routes
- Redesigned workspace navigation for studio modes

### 2026-02-22
- Added recipe R&D experiments with runs, comparison, and agent context
- Redesigned thinking display with indeterminate progress and detail transcript
- Enhanced activity panel with jump-to-message and virtualization
- Optimized chat streaming with index-based lookups and throttled scroll
- Unified message list components; improved mobile layout and accessibility

### 2026-02-20
- Added chat cancellation, message rewriting, and recipe variant merging
- Added recipe editing, import wizard, and cooking experience UI
- Added meal planner, templates, techniques, activity log, and workspace integration
- Added menu plans, voice routes, and recipe edit infrastructure on backend

### 2026-02-17
- Upgraded Claude Sonnet from 4.5 to 4.6
- Rebranded UI to match PTFI brand guide; consolidated activity display into inline thinking

### 2026-02-16
- Visual design overhaul: premium color palette, glass utilities, editorial chat messages, warm hero with time-aware greeting
- Added TTS audio endpoint for recipe step readout
- Added recipe cost estimation engine and budget settings
- Added cooking journal with notes, ratings, and cook tracking
- Added nutritional analysis engine and family/household profiles
- Added flavor profile radar chart and recipe comparison view
- Added cooking mode with step-by-step timer and audio readout
- Added mobile bottom tab bar with shopping list page
- Enhanced agent with proactive intelligence and workspace-type adaptation
- Added recipe sharing and creative engagement features
- Redesigned chat layout with smart auto-scroll and "Jump to latest" button
- Switched recipe search to server-side with abort support
- Added chef mode workspace toggle with manager dashboard
- Persisted tool activities in chat metadata; improved recipe search ranking

### 2026-02-15
- Major quality and performance sweep across backend and frontend
- Switched orchestrator from Opus to Sonnet 4.5 for cost/speed balance
- Added retry logic to provider methods; partial response display on stream errors
- Fixed N+1 queries in repositories with batch loading
- Added LRU bounds to caches; periodic rate limiter eviction
- Performance: staleTime/gcTime on React Query, memoized contexts, batched SSE updates, optimistic pantry mutations, Vite code splitting
- Refactored Message component into UserMessage/AssistantMessage sub-components
- Accessibility: tablist/tab roles, focusable recipe chips, keyboard navigation
- Styled PantryConfirmCard with amber theme and slide-in animation
- Added error banner with retry/dismiss to chat
- Replaced manual history.pushState with React Router navigation
- Security: SSRF protection, UUID typing, RequestValidationError handler
- Forwarded sub-agent progress events to frontend

### 2026-02-09
- Added recipe references and get_recipe tool for improved editing workflow
- Added auto-attach recipe reference when clicking context panel recipes

### 2026-02-08
- Added inline recipe expansion in workspace with responsive layouts
- Added all-recipes grid to recipe book; improved workspace panel layout
- Added delete conversation endpoint; upgraded orchestrator to Claude Opus 4.6
- UX improvements: correct new-chat navigation, fresh chat on load, delete with confirmation dialog
- Client-side recipe search fallback

### 2026-02-07
- Rebranded app to "Swap it Smart Creativity Agent"
- Added @recipe mentions in chat with inline recipe cards
- Added recipe collections (replacing bookmarks), shopping list components, home feed
- Replaced dashboard layout with workspace-first design
- Added onboarding components and conversation threads with auto-summarization
- Added recipe import service with multi-source support and model fallback
- Removed legacy chat and session endpoints

### 2026-02-06
- Introduced culinary design system: warm cream/terracotta/amber palette, DM Serif Display + Inter fonts, ingredient category colors
- Extracted shared tool display name utilities across frontend and backend
- Migrated data hooks to React Query
- Added Creative Studio workspace with responsive desktop/mobile layout
- Added multi-conversation support to kitchen chat
- Added onboarding endpoint and kitchen action dispatch improvements

### 2026-02-05
- Broadened topic guardrail to allow food-adjacent conversations
- Added sustainability infrastructure and dietary tools on backend
- Added sustainability UI, dietary profiles, recipe branching on frontend
- Implemented thinking stream fallback summaries

### 2026-02-03
- Added smart confirmation flow for kitchen tools based on user intent
- Fixed recipe validation errors by normalizing LLM field name variations
- Added thinking display, recipe import feature, and favicon
- Renamed "Keywords & Vibes" to "Areas of Inspiration"

### 2026-02-02
- Fixed invalid Claude model IDs and SSE parser for sse-starlette 3.x line endings
- Added full database layer: SQLAlchemy models, Alembic migrations, repository pattern
- Added kitchen tools for pantry, recipe, and keyword management
- Major frontend architecture expansion: React Router, React Query, kitchen domain types
- Added session/kitchen context providers, domain hooks, and page components
- Added pantry confirmation UI, live recipe generation status, and chat history loading
- Redesigned recipe detail page with digital cookbook layout and sectioned instructions
- Added light/dark mode toggle; removed default Vite favicon
- Added Dockerfile for containerized frontend builds

### 2026-01-30
- Fixed Docker build issues and CORS_ORIGINS environment variable parsing

### 2026-01-28
- Added multi-provider LLM abstraction layer (Anthropic, OpenAI, Google)
- Built tool system framework with core tools (math, unit converter, recipe scaling)
- Added LLM-powered tools: creative substitution, web search, present recipes
- Implemented agent executor with orchestrator agent definition
- Fixed frontend build configuration and added typed error handling system
- Added app initialization flow, keyboard shortcuts, skeleton loading states, and health status indicator

### 2026-01-13
- Phase 1 backend foundation with FastAPI setup
- Bootstrapped React frontend with chat interface and activity sidebar

### 2026-01-12
- Initial project scaffolding

---

*This changelog is updated from the commit histories of the backend and frontend repositories.*
