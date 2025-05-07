# spec
Esta é a especificação do Opsmind. Visite: https://opsminded.github.io/spec/

## Versionamento
A documentação da API segue o modelo de versão contínua (latest).
Toda nova mudança refletida no branch `main` representa a versão mais atual da API.

## Validação da especificação

```bash
docker run --rm -v $(pwd):/spec redocly/cli lint openapi.json
```

## Geração da documentação
```bash
docker run --rm -v $(pwd):/spec \
-v /etc/passwd:/etc/passwd:ro -v /etc/group:/etc/group:ro --user $(id -u) \
redocly/cli build-docs -o index.html --title Opsmind openapi.json
```

