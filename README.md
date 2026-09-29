# ⚽ Convocado
 
![Status](https://img.shields.io/badge/status-planning-yellow?style=for-the-badge)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![.Net](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)
![Blazor](https://img.shields.io/badge/blazor-%235C2D91.svg?style=for-the-badge&logo=blazor&logoColor=white)
 
> 🚧 **This project is in its early planning stage.** No code yet. This README describes the goals and the initial plan, and it will evolve as development progresses.
 
**Convocado** is a web application to manage amateur football teams (7-a-side, futsal, 11-a-side). The idea came from my own experience playing in a 7-a-side league: everything from scheduling games to knowing who is coming and who paid for the pitch is handled in chat groups, and it quickly gets messy.
 
## 🎯 Goals
 
**Product goals**
 
- Replace chat-group chaos with one place to schedule training sessions and matches
- Let players confirm attendance with one click
- Keep track of results and player statistics over the season
- Generate balanced teams for training games
- Keep track of pitch fees and payments
**Learning goals**
 
- Design and build a **REST API** with ASP.NET Core
- Build a **Blazor WebAssembly** frontend that consumes that API
- Implement **authentication and authorization** (JWT, per-team roles)
- Integrate **external APIs** in a resilient way
- Write **unit and integration tests**
- Set up **Docker**, **CI/CD with GitHub Actions** and a public deployment
- Keep the project properly **documented** (OpenAPI, architecture diagrams, ADRs)
## 👥 Planned roles
 
| Role | Permissions |
|------|-------------|
| Team admin | Creates the team, invites players, schedules events, records results and payments |
| Player | Confirms attendance, views calendar and statistics, checks pending fees |
| Visitor *(maybe)* | Views a public team page with results, no login required |
 
## 📋 Planned features
 
| Feature | Description | Priority |
|---------|-------------|----------|
| Accounts | Register and log in with email and password | MVP |
| Teams | Create a team, join with an invite code, manage members | MVP |
| Calendar | Training sessions and matches with date, time and location | MVP |
| Attendance | Players answer *Going / Not going / Maybe*, with a player limit | MVP |
| Results | Record the result of each match | MVP |
| Statistics | Goals, assists, attendance, rankings and charts | High |
| Team generator | Split confirmed players into two balanced teams | High |
| Weather | Forecast for the match day and location | High |
| Reminders | Automatic email to players who haven't answered | High |
| Fees | Track who paid for the pitch | High |
| Real-time updates | Attendance list updates live | Nice to have |
| Google login | External authentication with OAuth | Nice to have |
| PWA | Install the app on a phone | Nice to have |
 
## 🛠️ Planned tech stack
 
| Layer | Technology |
|-------|------------|
| Backend | ASP.NET Core Web API (.NET) |
| Frontend | Blazor WebAssembly + MudBlazor |
| Database | PostgreSQL + Entity Framework Core |
| Authentication | ASP.NET Core Identity + JWT |
| API docs | OpenAPI (Scalar / Swagger UI) |
| External APIs | Open-Meteo (weather) |
| Background jobs | Hangfire or Quartz.NET |
| Real time | SignalR |
| Testing | xUnit, WebApplicationFactory, Testcontainers, bUnit |
| DevOps | Docker, GitHub Actions, Azure |
 
*The stack may change as the project evolves. Important decisions will be documented.*
 
## 🏗️ Planned architecture
 
```
Convocado/
├── src/
│   ├── Convocado.Api             → REST API
│   ├── Convocado.Application     → business logic
│   ├── Convocado.Domain          → entities and domain rules
│   ├── Convocado.Infrastructure  → database, external services
│   ├── Convocado.Shared          → DTOs shared by API and frontend
│   └── Convocado.Web             → Blazor WebAssembly frontend
├── tests/
└── docs/
```
 
## 🗺️ Roadmap
 
- [ ] Phase 0: Repository and solution setup
- [ ] Phase 1: Domain model and database
- [ ] Phase 2: Base REST API and OpenAPI docs
- [ ] Phase 3: Authentication and authorization
- [ ] Phase 4: Blazor frontend base
- [ ] Phase 5: Attendance system → **MVP**
- [ ] Phase 6: Results and statistics
- [ ] Phase 7: Balanced team generator
- [ ] Phase 8: External API integration
- [ ] Phase 9: Reminders and real-time updates
- [ ] Phase 10: Fees and payments
- [ ] Phase 11: Testing
- [ ] Phase 12: Docker, CI/CD and deployment
- [ ] Phase 13: Final documentation
## 📄 License
 
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
