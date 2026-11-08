# brabo-ci-exemplo

Repositório-exemplo (público, fora da org `viralabs-dev`) que prova o [guia de adoção da política do brabo-ci](https://github.com/viralabs-dev/brabo-ci/blob/dev/scripts/ci/docs/tutorials/adotar.md) (AT-827). Comece pelo guia; este repo é o resultado de segui-lo.

## O que tem aqui

- `main` e `dev`: as duas branches permanentes (a esteira é `dev -> main`).
- `.github/workflows/politica.yml`: o kit mínimo. Chama o `pr-police` ("Política de branches") e a `escada` ("Escada de aprovação") do `viralabs-dev/brabo-ci`, pinados por SHA, com o `ci_ref` igual ao SHA do `uses:`.
- A variável de repositório `OWNER_HANDLE=daneiel`, sem a qual a escada reprova no modo `solo`.

Não há segredo nem GitHub App: o kit mínimo roda só com o `GITHUB_TOKEN`.

## Ver funcionando

Abra uma PR de uma branch `feature/...` para `dev`: os dois checks aparecem na PR. A PR de exemplo está nas PRs fechadas ou abertas deste repo.
