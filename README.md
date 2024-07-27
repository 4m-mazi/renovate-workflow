# Renovate workflow

Run Renovate on GitHub Actions

## Usage

see [trigger-renovate.yml](.github/workflows/trigger-renovate.yml)

## 実行するために必要なもの

このワークフローを実行ためには二つのGitHub Appsが必要です。
(同じAppを使っていても動きますが、権限制限の観点から別にしたほうがよいでしょう。)

- Renovate実行用App\
  必要な権限:
  - [read-only]\
      repo: Administration, Dependabot alerts, Metadata, Packages\
      org:  Members
  - [read and write]\
      repo: Checks, Commit statuses, Contents, Issues, Pull requests, Workflows

  [renovate.yml](.github/workflows/renovate.yml)で使います。

- このワークフローを起動するためのApp\
  必要な権限:
  - [read and write]\
      repo: Contents

  [trigger-renovate.yml](.github/workflows/trigger-renovate.yml)で使います。
