1. Enable Google Workspace API:
- Go to https://console.cloud.google.com/apis/library/browse?filter=category:gsuite
+ enable Gmail API
+ Google Calendar API
+ Google Drive API
+ Google Drive MCP
+ Calendar MCP API
+ Google Slides API
+ Slides MCP API
+ Google Docs API
+ Docs MCP API
+ Google People API
+ Google Tasks API
+ Google Chat API
+ Chat MCP API
+ Google Workspace Events API
+ Google Meet REST API

https://www.librechat.ai/docs/mcp_servers/google_workspace#enable-the-google-workspace-apis

2. Config Auth Platform:
https://console.cloud.google.com/auth/overview

Email: thuydungpham019@gmail.com
External

If you choose External and keep the app in testing mode, add yourself and any other allowed users under Audience > Test users. (thuydungpham019@gmail.com)

Ref: https://www.librechat.ai/docs/mcp_servers/google_workspace#configure-the-google-auth-platform

- Add Data Access Scopes: https://www.librechat.ai/docs/mcp_servers/google_workspace#add-data-access-scopes

3. Create a Web application OAuth client
https://console.cloud.google.com/auth/overview

In Google Auth Platform > Clients, create an OAuth client:

Application type: Web application
Name: use a descriptive name, such as LibreChat Google Workspace 
Authorized redirect URIs:
http://localhost:3080/api/mcp/gmail/oauth/callback
http://localhost:3080/api/mcp/drive/oauth/callback
http://localhost:3080/api/mcp/calendar/oauth/callback
http://localhost:3080/api/mcp/people/oauth/callback
http://localhost:3080/api/mcp/chat/oauth/callback
http://localhost:3080/api/mcp/calendar-mcp/oauth/callback
http://localhost:18000/oauth2callback

Get CLient ID and set GOOGLE_OAUTH_CLIENT_ID in docker-compose.yml and GOOGLE_WORKSPACE_MCP_CLIENT_ID in .env file
GEt Client secret and set GOOGLE_OAUTH_CLIENT_SECRET in docker-compose.yml and GOOGLE_WORKSPACE_MCP_CLIENT_SECRET in .env file



Ref: https://www.librechat.ai/docs/mcp_servers/google_workspace#create-a-web-application-oauth-client

4. Create AI Studio API Key
https://aistudio.google.com/api-keys


5. Change permission folders
