# Roadmap GED Dinâmico

## Núcleo / primeira entrega local (ZIP)
- API .NET + React + PostgreSQL
- OCR imagem/PDF com Tesseract e Poppler
- Modelo documental configurável com campos JSONB
- Primeira leitura sugere campos, depois o modelo é reutilizado
- Indexação confirmada por operador
- Storage local por ID lógico e SHA-256
- Lotes e endereçamento físico hierárquico

## Antes de produzir ou usar documentos reais
- JWT/OIDC, RBAC, tenancy por identidade verificada (não por header livre)
- Auditoria e logs protegidos
- Migrations EF Core, testes e backups
- Segurança de upload, validação de arquivo, antivírus, HTTPS, políticas LGPD
- Job queue para OCR assíncrono e retentativas

## Evolução
- Editor visual de regiões OCR
- Classificação semântica por IA e regras de validação por tipo
- Versionamento de templates e revisão dupla
- Scanner Windows e câmera mobile
- Localização física com QR Code, movimentações, cadeia de custódia
- Full Text Search e índices dinâmicos
- Storages alternativos, migração verificável e gestão multicliente
