# GED Dinâmico — projeto ASP.NET Core + React + OCR

Bootstrap inicial do projeto de GED inteligente.

**Atenção:** este diretório está na branch isolada `ged-dinamico-bootstrap` do repositório de perfil `tognasca/tognasca`. Não é um repositório independente. A branch `main` não foi alterada.

## Objetivo

Permitir que clientes digitalizem cheques, contratos e formulários desconhecidos, reconheçam o conteúdo por OCR, configurem quais campos indexar e salvem modelos documentais dinâmicos. Documentos seguintes reutilizam o modelo, com revisão humana nos casos incertos. Há também gestão de lotes, caixas e localização física (unidade → corredor → fileira → estante → prateleira → caixa).

## Tecnologias

- C# / ASP.NET Core 10 LTS
- React + TypeScript + Vite
- PostgreSQL 16 + EF Core
- Tesseract OCR (por+eng) + Poppler (PDF)
- Storage local abstraído por IStorageProvider
- Docker Compose para API, banco e OCR

## Código da primeira entrega

Os arquivos executáveis da primeira entrega (backend, frontend, Docker, exemplos e documentação) foram gerados em um ZIP entregue na conversa do ChatGPT. Como a conexão atual do GitHub não permite criar repositórios novos nem fazer upload de ZIP diretamente, esta branch inicial contém o ponto de partida documental. Para ter um repositório independente, crie `tognasca/GED-Dinamico` como **privado** e publique o conteúdo do ZIP usando o Git.

## Uso da entrega local

1. Extraia o ZIP `GED-Dinamico-MVP.zip`.
2. Execute `docker compose up -d --build`.
3. Em `frontend`, execute `npm install` e `npm run dev`.
4. Abra http://localhost:5173 e http://localhost:5088/swagger.

**Somente ambiente local de desenvolvimento.** A base ainda não possui autenticação e autorização; não exponha em produção.

## Próximos marcos

1. Autenticação JWT e RBAC, tenant por claims, auditoria e migrations.
2. Editor visual de formulários, configuração de campos por área e extração semântica.
3. Processamento assíncrono, workers, fila e progresso.
4. Migração para S3/MinIO/Azure/SMB, com hashes e retentativas.
5. Gestão de custódia, QR Code, relatórios e pesquisa avançada.

Consulte `docs/ROADMAP.md`.
