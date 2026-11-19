# cohort-10-dotnet-22306-muhammad
Cohort 10 — .NET Fullstack (.NET+ReactJS) assignment for Muhammad Ali Ansari

## Initial Admin Provisioning
Public self-registration (`POST /api/auth/register`) always assigns the `RegularUser` role. On a fresh deployment, supply initial administrator credentials via environment variables or .NET User Secrets before starting the API:
- `SeedAdmin__Email` (e.g., `admin@taskmanagement.local`)
- `SeedAdmin__Password`

On startup, if no user with the `Admin` role exists, the API creates the initial Admin account. Existing Admins can subsequently promote other users via `PATCH /api/auth/users/{userId}/promote`.
