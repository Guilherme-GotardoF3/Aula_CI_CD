# Aula CI/CD

App Expo com pipeline de CI/CD via EAS Workflows (`.eas/workflows/pipeline.yml`):
a cada push na `main` roda `npm test` e, se passar, dispara os builds Android e iOS.

## Passos para ativar
1. `npm install -g eas-cli && eas login`
2. `eas init` (vincula o projeto Expo e grava `extra.eas.projectId` no `app.json`)
3. `eas build:configure` / primeiro build manual para credenciais (Android e iOS)
4. No painel Expo: Project settings > GitHub > instalar o app e selecionar este repositório
5. Push na `main` (ou `eas workflow:run .eas/workflows/pipeline.yml`)
