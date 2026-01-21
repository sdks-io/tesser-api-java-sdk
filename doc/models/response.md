
# Response

## Structure

`Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Status` | `String` | Optional | - | String getStatus() | setStatus(String status) |
| `GitSha` | `String` | Optional | - | String getGitSha() | setGitSha(String gitSha) |
| `Env` | `String` | Optional | - | String getEnv() | setEnv(String env) |

## Example (as JSON)

```json
{
  "status": "ok",
  "gitSha": "abc123def456",
  "env": "local"
}
```

