---
description: Blazor WebAssembly development practices and patterns for the SocOps bingo game project.
---

# Mandatory Development Checklist
- [ ] **Lint**: Run `dotnet format` to ensure code style consistency
- [ ] **Build**: Execute `dotnet build` to verify compilation
- [ ] **Test**: Run `dotnet test` to validate functionality

# Blazor Development Guidelines

## Project Structure
Blazor WebAssembly app with key folders: `Components/` (UI), `Pages/` (routing), `Services/` (logic), `Data/` (content), `Models/` (DTOs).

## Component Patterns
- `@inject` for dependencies
- `IDisposable` for event subscriptions
- `EventCallback<T>` for parent-child comms
- Async methods for I/O
- Minimize `StateHasChanged()` calls

## State & Logic
- State via `BingoGameService` and DI
- Avoid DOM manipulation; use data binding
- Bingo logic in `BingoLogicService`
- Questions from `Questions.cs`; support themes/levels

## Best Practices
- Small, focused components with single responsibility
- CSS isolation for styles
- Async/await for operations
- Thorough testing of components/services
- Meaningful event/callback names

## Workflow
- Build: `dotnet build`
- Run: `dotnet run --project SocOps.csproj`
- Debug in browser tools
- Use Hot Reload for iteration</content>
<parameter name="filePath">/workspaces/agent-lab-dotnet/.github/instructions/blazor-development.instructions.md