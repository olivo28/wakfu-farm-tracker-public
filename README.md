# 📘 Wakfu Tracker — User Manual / Manual de Uso

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.1.1w-blue.svg)](https://github.com/olivo28/wakfu-farm-tracker)

**Version:** `1.1.1w` | **Platforms:** Windows / Linux / Mobile

---

## 🌍 Language / Idioma

- [🇪🇸 Español (ES)](#es)
- [🇬🇧 English (EN)](#en)
- [🇫🇷 Français (FR)](#fr)
- [🇵🇹 Português (PT)](#pt)

---

<a name="es"></a>
## 🇪🇸 Español (ES)

### 💡 ¿Qué es?
**Wakfu Tracker** es una herramienta "companion" multiplataforma diseñada para optimizar tu experiencia de juego en Wakfu. No es solo una lista de tareas; es un ecosistema conectado entre tu PC y tu Móvil que rastrea recursos, recetas y oficios en tiempo real.

**Novedad v1.1.1w:** Esta versión se centra en la **precisión y limpieza**. Se introduce un **Filtro Inteligente de Drops** que ignora ítems irrelevantes, una lógica mejorada para nombres similares y un nuevo sistema de visualización de notas de parche en formato Markdown rico.

### 🏗️ Arquitectura del Proyecto
El sistema se compone de tres pilares conectados:
1.  **Cliente Desktop (Electron):** La aplicación principal con monitoreo de logs y notificaciones visuales.
2.  **Cliente Móvil (Expo):** Una versión compacta para consultar tu progreso en cualquier lugar.
3.  **Servidor API (Node.js):** El cerebro que gestiona la sincronización en tiempo real.

### ✨ Características Principales

- **🧠 Filtro Inteligente de Drops:** (NUEVO) El Tracker ahora es mucho más estricto. **Solo procesará ítems que formen parte de tus recetas activas**, eliminando notificaciones por semillas o recursos de bajo nivel que no buscas.
- **✨ Visualización Markdown:** (NUEVO) La ventana de "Nueva Versión" ahora muestra las notas del parche con formato rico (**negritas**, listas) para una lectura clara.
- **🛡️ Precisión de Nombres:** (MEJORADO) Lógica de comparación refinada para diferenciar ítems con nombres casi idénticos (ej. *Topinambo* vs. *Topinambo Mágico*) evitando conflictos falsos.
- **🚫 Lista Negra Interna:** (NUEVO) El sistema ignora automáticamente archivos de juego irrelevantes (NPCs, planos visuales) para evitar duplicados fantasmas.
- **📜 Selector Multi-Receta:** Para ítems que se pueden fabricar de varias formas, puedes intercambiar la receta activa con un solo clic.
- **🧮 Lógica de Crafteo Inteligente:**
    - **Crafteo en Cascada:** Distribución automática de cantidades entre tarjetas activas del mismo ítem.
    - **Cálculo "Auto" Dinámico:** Calcula solo lo que **te falta** en tiempo real.
- **☁️ Sincronización Cloud:** Tu progreso en el PC se refleja instantáneamente en tu móvil y viceversa.
- **📝 Monitoreo de Logs:** Detecta eventos del juego en tiempo real (ítems obtenidos/consumidos, recetas craftadas).
- **📦 Detalles Completos de Ítems:** Visualiza iconos, efectos, descripciones, niveles y fuentes de obtención.

### 🔒 Privacidad y Seguridad
*   **Datos Locales:** La información de tu inventario se guarda localmente en tu dispositivo.
*   **Sincronización Segura:** Comunicación en la nube vía **HTTPS/TLS** y autenticación **Discord OAuth2**.
*   **Cero Datos Sensibles:** No leemos archivos fuera de la carpeta de logs de Wakfu.

### 🛠️ Stack Tecnológico
*   **Frontend:** React Native 0.81.5 + React 19.1.0
*   **Framework:** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop:** Electron 39.2.6 + Electron Builder
*   **Backend:** Node.js, Express, Socket.io, MariaDB
*   **Lenguaje:** TypeScript 5.9.2
*   **Persistencia:** AsyncStorage (móvil/web) + Electron Store (desktop)

### 📖 Guía de Uso Rápido
1.  **Instalación:** Ejecuta `Setup.exe`. Elige "Solo para mí".
2.  **Configuración:** Verifica la ruta de `wakfu.log` en Ajustes.
3.  **Login:** Conecta tu cuenta de Discord para habilitar la nube.
4.  **Uso:** Busca ítems y añádelos con `(+)`. El tracker se actualizará solo al jugar.

### 🗑️ Desinstalación
Ejecuta el archivo `uninstall.bat` ubicado en la carpeta de instalación.

### 🗺️ Roadmap / Planes
*   **Corto Plazo:** Refinamiento de la UI móvil y optimización de WebSockets.
*   **Medio Plazo:** Notificaciones Push (Firebase) y Backups encriptados.
*   **Largo Plazo (Wakfu Hub):** Combat Meter, Gestor de Tareas Diarias y Chat Tracker.

### 🙏 Agradecimentos
Fuentes de datos: **[Wakfu Wiki](https://wakfu.wiki.gg/)**, **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**, **[CraftKBU](https://craftkbu.com/)**, **[MethodWakfu](https://methodwakfu.com/)** y **[Ankama](https://www.ankama.com/)**.

### 📄 Licencia
**MIT License** - Copyright (c) 2025 Antikux (Olivo28).

### ☕ Apoya el Proyecto
*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`

---

<a name="en"></a>
## 🇬🇧 English (EN)

### 💡 What is it?
**Wakfu Tracker** is a cross-platform companion tool designed to optimize your Wakfu gameplay. It is a connected ecosystem between your PC and Mobile that tracks resources, recipes, and professions in real-time.

**New in v1.1.1w:** This version focuses on **precision and cleanliness**. It introduces a **Smart Drop Filter** that ignores irrelevant items, improved logic for similar names, and a new Markdown patch notes viewer.

### 🏗️ Project Architecture
The system consists of three connected pillars:
1.  **Desktop Client (Electron):** The main application with log monitoring.
2.  **Mobile Client (Expo):** A compact version to check progress anywhere.
3.  **API Server (Node.js):** The brain managing real-time sync.

### ✨ Key Features

- **🧠 Smart Drop Filter:** (NEW) The Tracker is now much stricter. It will **only process items that are part of your active recipes**, eliminating notifications for seeds or low-level resources you aren't tracking.
- **✨ Markdown Rendering:** (NEW) The "New Version" dialog now displays patch notes with rich formatting (**bold**, lists) for clear reading.
- **🛡️ Name Precision:** (IMPROVED) Refined comparison logic to correctly distinguish items with nearly identical names (e.g., *Jerusalem Artichoke* vs. *Magic Jerusalem Artichoke*), preventing false conflicts.
- **🚫 Internal Blacklist:** (NEW) The system automatically ignores irrelevant game files (NPCs, visual blueprints) to prevent ghost duplicates.
- **📜 Multi-Recipe Selector:** Swap the active recipe with a single click for items with multiple crafting options.
- **🧮 Smart Crafting Logic:**
    - **Cascading Craft:** Automatic quantity distribution among active cards for the same item.
    - **Dynamic "Auto" Calculation:** Calculates only what is **missing** in real-time.
- **☁️ Cloud Sync:** Instant progress reflection between PC and mobile.
- **📝 Log Monitoring:** Detects game events in real-time preventing double counting.
- **📦 Complete Item Details:** View icons, effects, descriptions, levels, and sources.

### 🔒 Privacy & Security
*   **Local Data:** Inventory data is stored locally on your device.
*   **Secure Sync:** Cloud communication via **HTTPS/TLS** and **Discord OAuth2**.
*   **No Sensitive Data:** We do not read files outside the Wakfu log folder.

### 🛠️ Tech Stack
*   **Frontend:** React Native 0.81.5 + React 19.1.0
*   **Framework:** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop:** Electron 39.2.6 + Electron Builder
*   **Backend:** Node.js, Express, Socket.io, MariaDB
*   **Language:** TypeScript 5.9.2
*   **Persistence:** AsyncStorage (mobile/web) + Electron Store (desktop)

### 📖 Quick Start Guide
1.  **Installation:** Run `Setup.exe`. Choose "Only for me".
2.  **Setup:** Verify `wakfu.log` path.
3.  **Login:** Connect Discord account for cloud sync.
4.  **Play:** Add items and play; the tracker updates automatically.

### 🗑️ Uninstallation
Run the `uninstall.bat` file located in the installation folder.

### 🗺️ Roadmap
*   **Short Term:** Mobile UI refinement and WebSocket optimization.
*   **Medium Term:** Push Notifications (Firebase) and Encrypted Backups.
*   **Long Term (Wakfu Hub):** Combat Meter, Daily Tasks Manager, and Chat Tracker.

### 🙏 Acknowledgments
Data sources: **[Wakfu Wiki](https://wakfu.wiki.gg/)**, **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**, **[CraftKBU](https://craftkbu.com/)**, **[MethodWakfu](https://methodwakfu.com/)**, and **[Ankama](https://www.ankama.com/)**.

### 📄 License
**MIT License** - Copyright (c) 2025 Antikux (Olivo28).

### ☕ Support the Project
*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`

---

<a name="fr"></a>
## 🇫🇷 Français (FR)

### 💡 Qu'est-ce que c'est ?
**Wakfu Tracker** est un outil compagnon multiplateforme conçu pour optimiser votre expérience de jeu sur Wakfu. C'est un écosystème connecté entre votre PC et votre mobile qui suit les ressources et les recettes en temps réel.

**Nouveauté v1.1.1w :** Cette version se concentre sur la **précision et la propreté**. Elle introduit un **Filtre de Drop Intelligent** qui ignore les objets non pertinents, une logique améliorée pour les noms similaires et un nouveau visualiseur de notes de patch en Markdown.

### 🏗️ Architecture du Projet
Le système repose sur trois piliers :
1.  **Client Desktop (Electron) :** L'application principale avec surveillance des logs.
2.  **Client Mobile (Expo) :** Une version compacte pour suivre votre progression partout.
3.  **Serveur API (Node.js) :** Le cerveau qui gère la synchronisation.

### ✨ Fonctionnalités Principales

- **🧠 Filtre de Drop Intelligent :** (NOUVEAU) Le Tracker est désormais plus strict. Il ne traitera **que les objets faisant partie de vos recettes actives**, éliminant les notifications inutiles (semences, ressources bas niveau non suivies).
- **✨ Affichage Markdown :** (NOUVEAU) La fenêtre "Nouvelle Version" affiche désormais les notes avec un formatage riche (**gras**, listes) pour une lecture claire.
- **🛡️ Précision des Noms :** (AMÉLIORÉ) Logique de comparaison affinée pour distinguer correctement les objets aux noms quasi identiques (ex. *Topinambour* vs *Topinambour Magique*).
- **🚫 Liste Noire Interne :** (NOUVEAU) Le système ignore automatiquement les fichiers de jeu non pertinents (PNJ, plans visuels) pour éviter les doublons fantômes.
- **📜 Sélecteur Multi-Recettes :** Changez la recette active en un clic pour les objets à recettes multiples.
- **🧮 Logique d'Artisanat Intelligente :**
    - **Artisanat en Cascade :** Répartition automatique des quantités entre les cartes actives.
    - **Calcul "Auto" Dynamique :** Calcule uniquement ce qui **manque** en temps réel.
- **☁️ Cloud Sync :** Votre progression voyage instantanément entre PC et mobile.
- **📝 Surveillance des Logs :** Détecte les événements du jeu en temps réel.
- **📦 Détails Complets des Objets :** Visualisez icônes, effets, descriptions, niveaux et sources.

### 🔒 Confidentialité et Sécurité
*   **Données Locales :** Stockage local sur votre appareil.
*   **Sync Sécurisée :** **HTTPS/TLS** et **Discord OAuth2**.
*   **Pas de Données Sensibles :** Lecture exclusive du dossier de logs Wakfu.

### 🛠️ Stack Technique
*   **Frontend :** React Native 0.81.5 + React 19.1.0
*   **Framework :** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop :** Electron 39.2.6 + Electron Builder
*   **Backend :** Node.js, Express, Socket.io, MariaDB
*   **Langage :** TypeScript 5.9.2
*   **Persistance :** AsyncStorage (mobile/web) + Electron Store (desktop)

### 📖 Guide Rapide
1.  **Installation :** Exécutez `Setup.exe`.
2.  **Config :** Vérifiez le chemin des logs.
3.  **Connexion :** Connectez Discord pour la sync cloud.
4.  **Jouer :** Ajoutez des objets ; le tracker se met à jour tout seul.

### 🗑️ Désinstallation
Exécutez le fichier `uninstall.bat` dans le dossier d'installation.

### 🗺️ Roadmap
*   **Court Terme :** Optimisation UI mobile et WebSockets.
*   **Moyen Terme :** Notifications Push (Firebase) et Backups chiffrés.
*   **Long Terme (Wakfu Hub) :** Combat Meter, Tâches Quotidiennes et Chat Tracker.

### 🙏 Remerciements
Sources : **[Wakfu Wiki](https://wakfu.wiki.gg/)**, **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**, **[CraftKBU](https://craftkbu.com/)**, **[MethodWakfu](https://methodwakfu.com/)**, et **[Ankama](https://www.ankama.com/)**.

### 📄 Licence
**MIT License** - Copyright (c) 2025 Antikux (Olivo28).

### ☕ Soutenir le projet
*   **Ko-Fi :** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID :** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`

---

<a name="pt"></a>
## 🇵🇹 Português (PT)

### 💡 O que é?
**Wakfu Tracker** é uma ferramenta "companion" multiplataforma projetada para otimizar sua jogabilidade no Wakfu. É um ecossistema conectado entre seu PC e Celular que rastreia recursos e receitas em tempo real.

**Novidade v1.1.1w:** Esta versão foca na **precisão e limpeza**. Introduz um **Filtro Inteligente de Drops** que ignora itens irrelevantes, lógica melhorada para nomes semelhantes e um novo visualizador de notas de atualização em Markdown.

### 🏗️ Arquitetura do Projeto
O sistema é composto por três pilares conectados:
1.  **Cliente Desktop (Electron):** A aplicação principal com monitoramento de logs.
2.  **Cliente Mobile (Expo):** Uma versão compacta para verificar seu progresso em qualquer lugar.
3.  **Servidor API (Node.js):** O cérebro que gerencia a sincronização.

### ✨ Funcionalidades Principais

- **🧠 Filtro Inteligente de Drops:** (NOVO) O Tracker agora é muito mais rigoroso. Ele processará **apenas itens que fazem parte das suas receitas ativas**, eliminando notificações de sementes ou recursos de nível baixo que você não busca.
- **✨ Visualização Markdown:** (NOVO) A janela de "Nova Versão" exibe notas com formatação rica (**negrito**, listas) para melhor leitura.
- **🛡️ Precisão de Nomes:** (MELHORADO) Lógica de comparação refinada para distinguir itens com nomes quase idênticos (ex. *Topinambo* vs. *Topinambo Mágico*), evitando conflitos falsos.
- **🚫 Lista Negra Interna:** (NOVO) O sistema ignora automaticamente arquivos de jogo irrelevantes (NPCs, plantas visuais) para evitar duplicatas fantasmas.
- **📜 Seletor Multi-Receita:** Troque a receita ativa com um clique para itens com múltiplas opções de craft.
- **🧮 Lógica de Crafting Inteligente:**
    - **Crafting em Cascata:** Distribuição automática de quantidade entre cartões ativos.
    - **Cálculo "Auto" Dinâmico:** Calcula apenas o que **falta** em tempo real.
- **☁️ Sincronização Cloud:** Seu progresso viaja instantaneamente entre PC e celular.
- **📝 Monitoramento de Logs:** Detecta eventos do jogo em tempo real.
- **📦 Detalhes Completos de Itens**: Visualize ícones, efeitos, descrições, níveis e fontes.

### 🔒 Privacidade e Segurança
*   **Dados Locais:** Informações salvas localmente no dispositivo.
*   **Sincronização Segura:** **HTTPS/TLS** e **Discord OAuth2**.
*   **Sem Dados Sensíveis:** Não lemos arquivos fora da pasta de logs do Wakfu.

### 🛠️ Stack Tecnológico
*   **Frontend:** React Native 0.81.5 + React 19.1.0
*   **Framework:** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop:** Electron 39.2.6 + Electron Builder
*   **Backend:** Node.js, Express, Socket.io, MariaDB
*   **Linguagem:** TypeScript 5.9.2
*   **Persistência:** AsyncStorage (mobile/web) + Electron Store (desktop)

### 📖 Guia Rápido
1.  **Instalação:** Execute `Setup.exe`.
2.  **Configuração:** Verifique o caminho dos logs.
3.  **Login:** Conecte o Discord para habilitar a nuvem.
4.  **Jogar:** Adicione itens; o tracker atualiza sozinho.

### 🗑️ Desinstalação
Execute o arquivo `uninstall.bat` na pasta de instalação.

### 🗺️ Roadmap
*   **Curto Prazo:** Otimização de WebSocket e UI mobile.
*   **Médio Prazo:** Notificações Push (Firebase) e Backups criptografados.
*   **Longo Prazo (Wakfu Hub):** Combat Meter, Gerenciador de Tarefas Diárias e Chat Tracker.

### 🙏 Agradecimentos
Fontes de dados: **[Wakfu Wiki](https://wakfu.wiki.gg/)**, **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**, **[CraftKBU](https://craftkbu.com/)**, **[MethodWakfu](https://methodwakfu.com/)** e **[Ankama](https://www.ankama.com/)**.

### 📄 Licença
**MIT License** - Copyright (c) 2025 Antikux (Olivo28).

### ☕ Apoie o projeto
*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`
