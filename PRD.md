# PRD — Whisper Money (self-hosted, fork DITAP)

> Describe el **producto/uso**. Para reglas de ingeniería del fork ver `CLAUDE.md`.

## 1. Qué es

Instancia self-hosted de **Whisper Money**, app open source (CC BY-NC 4.0) de finanzas
personales cuyo pitch es "la forma más segura de entender tus finanzas" — los datos
nunca se comparten con terceros. Este repo es un **fork** de
`whisper-money/whisper-money` (upstream) mantenido en `JRM-Global/whisper-money`
(origin).

## 2. Para quién

Uso personal/interno — herramienta de gestión financiera, no un producto que DITAP
venda. Encaja con el patrón de "self-host lo que ya existe en vez de reconstruirlo"
que también se ve en `saas/postiz-app`.

## 3. Stack técnico

Laravel 12 (PHP 8.4) en el backend, React 19 vía Inertia.js v2 en el frontend, Vite +
Bun. Testing con `php artisan test` (excluye suite Browser por defecto) y linters
(ESLint, Prettier, Pint para PHP).

## 4. Qué NO es

Al igual que `postiz-app`, no es IP propia de DITAP: es un fork de un proyecto open
source que se mantiene actualizado contra `upstream`. Lo específico de DITAP acá son
credenciales, configuración de deploy y datos propios — no features nuevas del
producto en sí, salvo que se decida divergir deliberadamente.

## 5. Estado

Deployado (hay `Dockerfile` y `Dockerfile.production`), con changelog propio
(`CHANGELOG.md`) y guía de onboarding (`ONBOARDING.md`) heredados del proyecto
upstream.
