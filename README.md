# Simulação de Ataques Cibernéticos

> *O projeto está em desenvolvimento*

## Descrição
Projeto com ambientes simulados para demonstração de ataques cibernéticos em contexto controlado: **SQL Injection (SQLi)**, **Cross-Site Scripting (XSS)**, **Session Hijacking** e **Misconfiguration**.  
O objetivo é oferecer um laboratório prático e seguro para estudos e demonstrações acadêmicas.

> **Aviso legal e ético:** utilize este projeto somente em ambientes controlados e isolados (lab/VM/air-gapped). Nunca execute ataques contra sistemas reais sem autorização explícita.

## Relevância do projeto
Muitos cursos abordam os ataques apenas teoricamente. Este projeto demonstra, de forma didática e segura, como os ataques acontecem e como mitigá-los, permitindo práticas de defesa e detecção.

## Objetivos de aprendizagem por ambiente
- SQLi: identificar injeções com payloads básicos, usar prepared statements para mitigar.
- XSS: demonstrar XSS refletido e persistente; aplicar Content-Security-Policy e HttpOnly.
- Session Hijacking: mostrar captura de cookie via rede insegura (teoria), importância de Secure, HttpOnly, SameSite e HTTPS.
- Misconfiguration: identificar permissões incorretas, diretórios expostos, e corrigir via configurações seguras.

## Tecnologias utilizadas
- Docker / Docker Compose
- Python (para aplicações demo)
- Nginx (opcional, para reverse proxy nos cenários)
- SQLite / Postgres (opcional, para exemplo de SQLi)

## Pré-requisitos
- Docker
- Docker Compose
- Git (opcional, para clonar o repositório)

## Como executar
Há 4 ambientes disponíveis atualmente:

- `sqli` — SQL Injection
- `xss` — Cross-Site Scripting
- `session-hijacking` — Roubo de sessão
- `misconfiguration` — Misconfiguração intencional

Para subir um ambiente localmente (modo interativo):
```bash
# Exemplo: subir o ambiente de session-hijacking
docker compose up session-hijacking
# ou em background: usar a flag -d
docker compose up -d session-hijacking
```
