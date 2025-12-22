# 📘 Wakfu Tracker — User Manual / Manual de Uso

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.1.0w-blue.svg)](https://github.com/olivo28/wakfu-farm-tracker)

**Version:** `1.1.0w` | **Platforms:** Windows / Linux / Mobile

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

**Novedad v1.1.0w:** Esta versión introduce una **inteligencia de inventario avanzada**. Ahora el sistema detecta conflictos de rareza (nombres duplicados), permite elegir entre múltiples recetas para un mismo ítem y utiliza una lógica de "crafteo en cascada" para mantener tus cuentas perfectas.

### 🏗️ Arquitectura del Proyecto
El sistema se compone de tres pilares conectados:
1.  **Cliente Desktop (Electron):** La aplicación principal con monitoreo de logs y notificaciones visuales.
2.  **Cliente Móvil (Expo):** Una versión compacta para consultar tu progreso en cualquier lugar.
3.  **Servidor API (Node.js):** El cerebro que gestiona la sincronización en tiempo real y alerta sobre nuevas actualizaciones al instante.

### ✨ Características Principales

- **🛡️ Resolución de Conflictos de Rareza:** (NUEVO) Sistema inteligente que detecta cuando el juego entrega un ítem con nombre ambiguo (ej. *Equipo Raro vs Mítico*) y te permite elegir visualmente la versión correcta.
- **📜 Selector Multi-Receta:** (NUEVO) Para ítems que se pueden fabricar de varias formas (ej. *Cuero Eterno*), ahora puedes intercambiar la receta activa con un solo clic.
- **🧮 Lógica de Crafteo Inteligente:**
    - **Crafteo en Cascada:** Al crear grandes lotes, la cantidad se distribuye automáticamente entre todas las tarjetas activas del mismo ítem.
    - **Cálculo "Auto" Dinámico:** La lista de recursos automáticos ahora calcula solo lo que **te falta** en tiempo real, ignorando lo que ya tienes en inventario.
- **🔄 Auto-Actualización Blindada:** Sistema OTA robusto que actualiza la aplicación sin bloqueos de archivos ni errores de permisos.
- **☁️ Sincronización Cloud:** Tu progreso en el PC se refleja instantáneamente en tu móvil y viceversa.
- **⚡ Controles Rápidos:** Botones de `[+]` y `[-]` en las tarjetas para ajustes rápidos de cantidad.
- **📝 Monitoreo de Logs:** Detecta eventos del juego en tiempo real (ítems obtenidos/consumidos, recetas craftadas) evitando conteos dobles.
- **🌍 Soporte Multiidioma:** Interfaz completa en Español, Inglés, Francés y Portugués.
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
*   **Gestión de Estado:** React Hooks + Context API
*   **Persistencia:** AsyncStorage (móvil/web) + Electron Store (desktop)
*   **Estilos:** StyleSheet nativo + Linear Gradient

### 📖 Guía de Uso Rápido
1.  **Instalación:** Ejecuta `Setup.exe`. Elige "Solo para mí".
2.  **Configuración:** Verifica la ruta de `wakfu.log` en Ajustes.
3.  **Login:** Conecta tu cuenta de Discord para habilitar la nube.
4.  **Uso:** Busca ítems y añádelos con `(+)`. El tracker se actualizará solo al jugar.

### 🗑️ Desinstalación
Ejecuta el archivo `uninstall.bat` ubicado en la carpeta de instalación.

### 🗺️ Roadmap / Planes

*   **Corto Plazo:** Optimización del sistema de WebSocket y refinamiento de la UI móvil.
*   **Medio Plazo:**
    *   Integración de **Firebase (FCM)** para notificaciones Push en el móvil.
    *   **Background Sync:** Sincronización en segundo plano en móvil.
    *   Backups encriptados end-to-end.
*   **Largo Plazo (Wakfu Hub):**
    *   Convertir la aplicación en un **Hub de Herramientas** integral.
    *   **Combat Meter:** Medidor de daño y estadísticas en tiempo real.
    *   **Daily Tasks:** Gestor de tareas diarias (Mazmorras, Moduladas, Almanax, etc.).
    *   **Chat Tracker:** Monitoreo del chat con filtros Regex.

### 🙏 Agradecimentos

Este proyecto no sería posible sin las siguientes fuentes de datos y recursos:

- **[Wakfu Wiki](https://wakfu.wiki.gg/)**: Documentación completa del juego y datos de ítems
- **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**: Repositorio de assets gráficos (iconos de mobs, ítems)
- **[CraftKBU](https://craftkbu.com/)**: Base de datos de recetas y crafteo
- **[MethodWakfu](https://methodwakfu.com/)**: Datos de drops, niveles y estadísticas de mobs
- **[Ankama](https://www.ankama.com/)**: Desarrolladores de Wakfu y propietarios de los datos del juego

### 📄 Licencia

**MIT License**

Copyright (c) 2025 Antikux (Olivo28)

Se concede permiso, de forma gratuita, a cualquier persona que obtenga una copia de este software y archivos de documentación asociados (el "Software"), para utilizar el Software sin restricciones, incluyendo sin limitación los derechos de usar, copiar, modificar, fusionar, publicar, distribuir, sublicenciar y/o vender copias del Software, y permitir a las personas a las que se les proporcione el Software hacer lo mismo, sujeto a las siguientes condiciones:

El aviso de copyright anterior y este aviso de permiso se incluirán en todas las copias o porciones sustanciales del Software.

EL SOFTWARE SE PROPORCIONA "TAL CUAL", SIN GARANTÍA DE NINGÚN TIPO, EXPRESA O IMPLÍCITA, INCLUYENDO PERO NO LIMITADO A LAS GARANTÍAS DE COMERCIABILIDAD, IDONEIDAD PARA UN PROPÓSITO PARTICULAR Y NO INFRACCIÓN. EN NINGÚN CASO LOS AUTORES O TITULARES DEL COPYRIGHT SERÁN RESPONSABLES DE NINGUNA RECLAMACIÓN, DAÑOS U OTRA RESPONSABILIDAD, YA SEA EN UNA ACCIÓN DE CONTRATO, AGRAVIO O DE OTRO TIPO, QUE SURJA DE, FUERA DE O EN CONEXIÓN CON EL SOFTWARE O EL USO U OTROS TRATOS EN EL SOFTWARE.

### ☕ Apoya el Proyecto

*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`

---

<a name="en"></a>
## 🇬🇧 English (EN)

### 💡 What is it?
**Wakfu Tracker** is a cross-platform companion tool designed to optimize your Wakfu gameplay. It is a connected ecosystem between your PC and Mobile that tracks resources, recipes, and professions in real-time.

**New in v1.1.0w:** This version introduces **advanced inventory intelligence**. The system now detects rarity conflicts (duplicate names), allows choosing between multiple recipes for a single item, and uses "cascading craft" logic to keep your counts perfect.

### 🏗️ Project Architecture
The system consists of three connected pillars:
1.  **Desktop Client (Electron):** The main application with log monitoring.
2.  **Mobile Client (Expo):** A compact version to check progress anywhere.
3.  **API Server (Node.js):** The brain managing real-time sync and update alerts.

### ✨ Key Features

- **🛡️ Rarity Conflict Resolution:** (NEW) Smart system that detects when the game drops an item with an ambiguous name (e.g., *Rare vs Mythical Equipment*) and lets you visually select the correct version.
- **📜 Multi-Recipe Selector:** (NEW) For items that can be crafted in multiple ways (e.g., *Eternal Leather*), you can now swap the active recipe with a single click.
- **🧮 Smart Crafting Logic:**
    - **Cascading Craft:** When creating large batches, the quantity is automatically distributed among all active cards for the same item.
    - **Dynamic "Auto" Calculation:** The automatic resources list now calculates only what is **missing** in real-time, ignoring what you already have in inventory.
- **🔄 Bulletproof Auto-Update:** Robust OTA system that updates the app without file locks or permission errors.
- **☁️ Cloud Sync:** Instant progress reflection between PC and mobile via real-time sockets.
- **⚡ Quick Controls:** `[+]` and `[-]` buttons on cards for fast quantity adjustments.
- **📝 Log Monitoring:** Detects game events in real-time preventing double counting.
- **🌍 Multi-language Support:** Full interface in Spanish, English, French, and Portuguese.
- **📦 Complete Item Details:** View icons, effects, descriptions, levels, and sources.

### 🔒 Privacy & Security
*   **Local Data:** Inventory data is stored locally on your device.
*   **Secure Sync:** Cloud communication via **HTTPS/TLS** and **Discord OAuth2** authentication.
*   **No Sensitive Data:** We do not read files outside the Wakfu log folder.

### 🛠️ Tech Stack
*   **Frontend:** React Native 0.81.5 + React 19.1.0
*   **Framework:** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop:** Electron 39.2.6 + Electron Builder
*   **Language:** TypeScript 5.9.2
*   **State Management:** React Hooks + Context API
*   **Persistence:** AsyncStorage (mobile/web) + Electron Store (desktop)
*   **Styling:** Native StyleSheet + Linear Gradient

### 📖 Quick Start Guide
1.  **Installation:** Run `Setup.exe`. Choose "Only for me".
2.  **Setup:** Verify `wakfu.log` path.
3.  **Login:** Connect Discord account for cloud sync.
4.  **Play:** Add items and play; the tracker updates automatically.

### 🗑️ Uninstallation
Run the `uninstall.bat` file located in the installation folder.

### 🗺️ Roadmap

*   **Short Term:** WebSocket optimization and mobile UI refinement.
*   **Medium Term:**
    *   **Firebase (FCM)** integration for mobile Push Notifications.
    *   **Background Sync:** Background synchronization on mobile.
    *   End-to-end encrypted backups.
*   **Long Term (Wakfu Hub):**
    *   Transform the app into an all-in-one **Tool Hub**.
    *   **Combat Meter:** Real-time damage stats.
    *   **Daily Tasks:** Manager for Dungeons, Modulox, etc.
    *   **Chat Tracker:** Chat monitoring with Regex.

### 🙏 Acknowledgments

This project wouldn't be possible without these resources:

- **[Wakfu Wiki](https://wakfu.wiki.gg/)**: Complete game documentation and item data.
- **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**: Graphic assets repository.
- **[CraftKBU](https://craftkbu.com/)**: Recipe and crafting database.
- **[MethodWakfu](https://methodwakfu.com/)**: Drop data and mob statistics.
- **[Ankama](https://www.ankama.com/)**: Wakfu developers and game data owners.

### 📄 License

**MIT License**

Copyright (c) 2025 Antikux (Olivo28)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### ☕ Support the Project

*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`

---

<a name="fr"></a>
## 🇫🇷 Français (FR)

### 💡 Qu'est-ce que c'est ?
**Wakfu Tracker** est un outil compagnon multiplateforme conçu pour optimiser votre expérience de jeu sur Wakfu. C'est un écosystème connecté entre votre PC et votre mobile qui suit les ressources et les recettes en temps réel.

**Nouveauté v1.1.0w :** Cette version introduit une **intelligence d'inventaire avancée**. Le système détecte désormais les conflits de rareté (noms en double), permet de choisir entre plusieurs recettes pour un même objet et utilise une logique "d'artisanat en cascade" pour garder vos comptes parfaits.

### 🏗️ Architecture du Projet
Le système repose sur trois piliers :
1.  **Client Desktop (Electron) :** L'application principale avec surveillance des logs.
2.  **Client Mobile (Expo) :** Une version compacte pour suivre votre progression partout.
3.  **Serveur API (Node.js) :** Le cerveau qui gère la synchronisation et les alertes.

### ✨ Fonctionnalités Principales

- **🛡️ Résolution de Conflits de Rareté :** (NOUVEAU) Système intelligent qui détecte lorsque le jeu donne un objet au nom ambigu (ex. *Équipement Rare vs Mythique*) et vous permet de choisir visuellement la bonne version.
- **📜 Sélecteur Multi-Recettes :** (NOUVEAU) Pour les objets pouvant être fabriqués de plusieurs manières (ex. *Cuir Éternel*), vous pouvez désormais changer la recette active en un clic.
- **🧮 Logique d'Artisanat Intelligente :**
    - **Artisanat en Cascade :** Lors de la création de grands lots, la quantité est automatiquement répartie entre toutes les cartes actives du même objet.
    - **Calcul "Auto" Dynamique :** La liste des ressources automatiques ne calcule désormais que ce qui **manque** en temps réel, ignorant ce que vous avez déjà en inventaire.
- **🔄 Mise à Jour Automatique Blindée :** Système OTA robuste qui met à jour l'application sans blocage de fichiers ni erreur de permission.
- **☁️ Cloud Sync :** Votre progression voyage instantanément entre PC et mobile.
- **⚡ Contrôles Rapides :** Boutons `[+]` et `[-]` sur les cartes pour des ajustements rapides de quantité.
- **📝 Surveillance des Logs :** Détecte les événements du jeu en temps réel, évitant le double comptage.
- **🌍 Support Multilingue :** Interface complète en Espagnol, Anglais, Français et Portugais.
- **📦 Détails Complets des Objets :** Visualisez icônes, effets, descriptions, niveaux et sources.

### 🔒 Confidentialité et Sécurité
*   **Données Locales :** Les données d'inventaire sont stockées localement.
*   **Sync Sécurisée :** Communication cloud via **HTTPS/TLS** et **Discord OAuth2**.
*   **Pas de Données Sensibles :** Nous ne lisons pas de fichiers hors du dossier de logs Wakfu.

### 🛠️ Stack Technique
*   **Frontend :** React Native 0.81.5 + React 19.1.0
*   **Framework :** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop :** Electron 39.2.6 + Electron Builder
*   **Langage :** TypeScript 5.9.2
*   **Gestion d'État :** React Hooks + Context API
*   **Persistance :** AsyncStorage (mobile/web) + Electron Store (desktop)
*   **Styles :** StyleSheet natif + Linear Gradient

### 📖 Guide Rapide
1.  **Installation :** Exécutez `Setup.exe`.
2.  **Config :** Vérifiez le chemin des logs.
3.  **Connexion :** Connectez Discord pour la sync cloud.
4.  **Jouer :** Ajoutez des objets ; le tracker se met à jour tout seul.

### 🗑️ Désinstallation
Exécutez le fichier `uninstall.bat` dans le dossier d'installation.

### 🗺️ Roadmap / Avenir

*   **Court Terme :** Optimisation des WebSockets et raffinement UI mobile.
*   **Moyen Terme :**
    *   Intégration **Firebase** pour notifications push.
    *   **Background Sync :** Synchronisation en arrière-plan.
*   **Long Terme (Wakfu Hub) :**
    *   Conversion en un **Hub d'Outils** complet.
    *   **Combat Meter :** Suivi des dégâts.
    *   **Tâches Quotidiennes :** Gestion des donjons, etc.
    *   **Chat Tracker :** Surveillance du chat avec filtres Regex.

### 🙏 Remerciements

Ce projet ne serait pas possible sans :

- **[Wakfu Wiki](https://wakfu.wiki.gg/)** : Documentation et données.
- **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)** : Assets graphiques.
- **[CraftKBU](https://craftkbu.com/)** : Base de données de recettes.
- **[MethodWakfu](https://methodwakfu.com/)** : Données de drops et mobs.
- **[Ankama](https://www.ankama.com/)** : Développeurs de Wakfu et propriétaires des données.

### 📄 Licence

**MIT License**

Copyright (c) 2025 Antikux (Olivo28)

L'autorisation est accordée, gratuitement, à toute personne obtenant une copie de ce logiciel et des fichiers de documentation associés (le "Logiciel"), de traiter le Logiciel sans restriction... (voir texte complet ci-dessus en anglais).

### ☕ Soutenir le projet

*   **Ko-Fi :** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID :** `196153443`

---

<a name="pt"></a>
## 🇵🇹 Português (PT)

### 💡 O que é?
**Wakfu Tracker** é uma ferramenta "companion" multiplataforma projetada para otimizar sua jogabilidade no Wakfu. É um ecossistema conectado entre seu PC e Celular que rastreia recursos e receitas em tempo real.

**Novidade v1.1.0w:** Esta versão introduz **inteligência de inventário avançada**. O sistema agora detecta conflitos de raridade (nomes duplicados), permite escolher entre várias receitas para um mesmo item e usa lógica de "crafting em cascata" para manter suas contas perfeitas.

### 🏗️ Arquitetura do Projeto
O sistema é composto por três pilares conectados:
1.  **Cliente Desktop (Electron):** A aplicação principal com monitoramento de logs.
2.  **Cliente Mobile (Expo):** Uma versão compacta para verificar seu progresso em qualquer lugar.
3.  **Servidor API (Node.js):** O cérebro que gerencia a sincronização e alertas de atualização.

### ✨ Funcionalidades Principais

- **🛡️ Resolução de Conflitos de Raridade:** (NOVO) Sistema inteligente que detecta quando o jogo dropa um item com nome ambíguo (ex. *Equipamento Raro vs Mítico*) e permite escolher visualmente a versão correta.
- **📜 Seletor Multi-Receita:** (NOVO) Para itens que podem ser fabricados de várias formas (ex. *Couro Eterno*), agora você pode trocar a receita ativa com um clique.
- **🧮 Lógica de Crafting Inteligente:**
    - **Crafting em Cascata:** Ao criar grandes lotes, a quantidade é distribuída automaticamente entre todos os cartões ativos do mesmo item.
    - **Cálculo "Auto" Dinâmico:** A lista de recursos automáticos agora calcula apenas o que **falta** em tempo real, ignorando o que você já tem no inventário.
- **🔄 Atualização Automática Blindada:** Sistema OTA robusto que atualiza o aplicativo sem bloqueios de arquivos ou erros de permissão.
- **☁️ Sincronização Cloud:** Seu progresso viaja instantaneamente entre PC e celular.
- **⚡ Controles Rápidos:** Botões `[+]` e `[-]` nos cartões para ajustes rápidos de quantidade.
- **📝 Monitoramento de Logs:** Detecta eventos do jogo em tempo real, evitando contagem dupla.
- **🌍 Suporte Multilíngue**: Interface completa em Espanhol, Inglês, Francês e Português.
- **📦 Detalhes Completos de Itens**: Visualize ícones, efeitos, descrições, níveis e fontes.

### 🔒 Privacidade e Segurança
*   **Dados Locais:** Informações salvas localmente.
*   **Sincronização Segura:** Comunicação na nuvem via **HTTPS/TLS** e **Discord OAuth2**.
*   **Sem Dados Sensíveis:** Não lemos arquivos fora da pasta de logs.

### 🛠️ Stack Tecnológico
*   **Frontend:** React Native 0.81.5 + React 19.1.0
*   **Framework:** Expo ~54.0 (Router, File System, Image, etc.)
*   **Desktop:** Electron 39.2.6 + Electron Builder
*   **Linguagem:** TypeScript 5.9.2
*   **Gestão de Estado:** React Hooks + Context API
*   **Persistência:** AsyncStorage (mobile/web) + Electron Store (desktop)
*   **Estilos:** StyleSheet nativo + Linear Gradient

### 📖 Guia Rápido
1.  **Instalação:** Execute `Setup.exe`.
2.  **Configuração:** Verifique o caminho dos logs.
3.  **Login:** Conecte o Discord para habilitar a nuvem.
4.  **Jogar:** Adicione itens; o tracker atualiza sozinho.

### 🗑️ Desinstalação
Execute o arquivo `uninstall.bat` na pasta de instalação.

### 🗺️ Roadmap / Futuro

*   **Curto Prazo:** Otimização de WebSocket e refinamento de UI mobile.
*   **Médio Prazo:**
    *   Integração **Firebase** para notificações push.
    *   **Background Sync:** Sincronização em segundo plano no celular.
*   **Longo Prazo (Wakfu Hub):**
    *   Transformar o app em um **Hub de Ferramentas**.
    *   **Combat Meter:** Medidor de dano.
    *   **Tarefas Diárias:** Gerenciador de Calabouços, etc.
    *   **Chat Tracker:** Monitoramento de chat com filtros Regex.

### 🙏 Agradecimentos

Obrigado a:

- **[Wakfu Wiki](https://wakfu.wiki.gg/)**: Documentação e dados.
- **[Vertylo/wakassets](https://github.com/Vertylo/wakassets)**: Repositório de assets gráficos.
- **[CraftKBU](https://craftkbu.com/)**: Banco de dados de receitas.
- **[MethodWakfu](https://methodwakfu.com/)**: Dados de drops e mobs.
- **[Ankama](https://www.ankama.com/)**: Desenvolvedores do Wakfu e proprietários dos dados.

### 📄 Licença

**MIT License**

Copyright (c) 2025 Antikux (Olivo28)

É concedida permissão, gratuitamente, a qualquer pessoa que obtenha uma cópia deste software e arquivos de documentação associados (o "Software"), para lidar com o Software sem restrições... (ver texto completo acima em inglês).

### ☕ Apoie o projeto

*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`

---

**Legal Notice:** This tool processes information obtained from the game client and public sources. The author is not liable for any misuse. Use at your own risk.
