# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Aggiunto supporto per esecuzione manuale del workflow `sync_branches` tramite `workflow_dispatch`
- Parametri configurabili `source_branch` e `target_branch` per merge dinamico tra branch personalizzati

### Changed

- Parametrizzati i nomi dei branch nel workflow `sync_branches` (non più hardcoded su `main` e `preprod`)
- Il workflow ora utilizza variabili d'ambiente `SOURCE_BRANCH` e `TARGET_BRANCH` per maggiore flessibilità
- Tutti i messaggi e commenti ora utilizzano i nomi dei branch parametrizzati

### Deprecated

### Removed

### Fixed

### Security

## [0.0.6] - 2025-12-16

### Fixed

- Corregge action di creazione automatica del tag di una release

## [0.0.5] - 2025-12-16

### Added

- Aggiunta GitHub Action per la creazione automatica di tag al merge di branch `release/*` in `main`
- Il tag viene estratto dal nome del branch usando una regex per semver2, rimuovendo testo superfluo
- Prefisso del tag configurabile tramite variabile `TAG_PREFIX` (default: 'release_')
- Workflow triggered su evento `pull_request` con tipo `closed` per rilevare merge in modo affidabile

## [0.0.4] - 2025-12-16

### Fixed

- Aggiornato il comando fetch nel workflow `sync_branches` per recuperare tutti i branch.

## [0.0.3] - 2025-12-16

### Fixed

- Risolto errore di fetch nel workflow `sync_branches`.

## [0.0.2] - 2025-12-16

### Changed

- Aggiornati i nomi dei branch nella GitHub Action di sincronizzazione (`sync_branches`).

### Fixed

- Correzione nella configurazione dei branch per la sincronizzazione automatica.

## [0.0.1] - 2025-12-16

### Added

- Initial release
