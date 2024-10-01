# promptql-graphql-workshop


1. Install Docker with compose, install psql
2. docker compose -f postgres-compose.yaml up -d
3. Load data: psql postgres://postgres:postgres@local.hasura.dev:5432/postgres < db.sql
4. Bring DDN locally: cd ddn_project; docker compose --env-file .env up --build -d
5. Start Pacha after cloning pacha repo: PORT=5000 CORS_ORIGINS="https://console.hasura.io" poetry run chat_server -d ddn -u http://localhost:3000/v1/sql -H "x-hasura-role: admin"

