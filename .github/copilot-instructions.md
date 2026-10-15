# Soc Ops Workspace Instructions

## Required Development Checklist

Before completing a code change, work from `socops/` and complete:

- [ ] **Lint:** Run the configured lint or formatter command. This project currently has none; state that explicitly in the result.
- [ ] **Build:** Run `.\mvnw clean package`.
- [ ] **Test:** Run `.\mvnw test` and add focused JUnit 5 tests for changed board rules.

## Conventions

- This is a Java 21 Spring Boot/Thymeleaf social-bingo application built with Maven.
- Keep HTTP code in `com.socops.web`, game logic in `com.socops.service`, domain records/enums in `com.socops.model`, and static prompts in `com.socops.data`. Keep controllers thin.
- Keep `BoardAssembler` pure and stateless; use immutable records and return updated board lists rather than mutating shared state.
- Keep browser state and interaction in `socops/src/main/resources/templates/game.html` unless backend work is required.
- Reuse utilities in `socops/src/main/resources/static/css/app.css`; preserve semantic, keyboard-accessible controls and labels.
- Follow `.github/instructions/frontend-design.instructions.md` and `.github/instructions/css-utilities.instructions.md` for UI work.
- Update `README.md` or the relevant `workshop/` guide when setup, commands, or visible behavior changes. Do not alter generated output or Maven wrapper files unless required.
