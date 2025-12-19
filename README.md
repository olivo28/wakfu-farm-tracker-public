# 📘 Wakfu Tracker — User Manual / Manual de Uso

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0.7-blue.svg)](https://github.com/olivo28/wakfu-farm-tracker)

**Version:** `1.0.7` | **Platforms:** Windows / Linux / Mobile

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

**Novedad v1.0.7:** Ahora incluye un instalador profesional, sincronización real en la nube y una aplicación móvil totalmente funcional.

### 🚀 Funcionalidades Principales

*   **☁️ Sincronización Cloud (Sync Alert + Pull):** Tu progreso en el PC se refleja instantáneamente en tu móvil y viceversa. Olvida las transferencias manuales; todo viaja por sockets en tiempo real.
*   **📱 App Móvil Dedicada:** Una interfaz compacta y táctil diseñada para llevar tu lista de farmeo al supermercado o al sofá.
*   **🔔 Notificaciones Estilo Steam:** Alertas visuales elegantes y no intrusivas en tu escritorio (con animaciones Slide In/Out) cuando completas una receta o alcanzas la meta de recursos.
*   **📝 Monitoreo de Logs Inteligente:**
    *   Detecta automáticamente ítems obtenidos y consumidos.
    *   Diferencia entre perder materiales (por craft) y fabricar ítems, evitando conteos dobles.
*   **📊 Rastreo de Recursos (Auto):** Calcula dinámicamente los materiales base (hierro, madera, etc.) necesarios para *todas* tus recetas activas combinadas.
*   **🛡️ Protección de Datos:** Lógica "Anti-Zombie" y "Anti-Rebote" para evitar errores de conteo o conflictos de fecha al sincronizar.

### 📖 Guía de Uso Rápido

1.  **Instalación:**
    *   Ejecuta `Setup.exe`.
    *   Elige "Solo para mí" (recomendado). La aplicación se copiará a tu carpeta de usuario y creará accesos directos automáticamente.
2.  **Primeros Pasos (PC):**
    *   Abre la aplicación.
    *   Ve a **Configuración (⚙️)**: Verifica la ruta de `wakfu.log` y selecciona tu idioma.
    *   **Login:** Conecta tu cuenta de Discord para habilitar la sincronización en la nube.
3.  **Vincular Móvil:**
    *   Instala la APK en tu Android.
    *   Inicia sesión con la misma cuenta de Discord. ¡Listo! Tus datos se fusionarán automáticamente.
4.  **Añadir Trackers:**
    *   Usa el buscador inferior para encontrar ítems (ej: "Gema tosca").
    *   Pulsa el botón `(+)` o el `ojo` para rastrear.
5.  **Jugar:**
    *   El programa leerá los logs. Si recolectas hierro, la barra subirá sola. Si crafteas, los recursos se descontarán y la receta aumentará.

### 🗑️ Desinstalación
Al ser una instalación ligera (copia de archivos), simplemente ejecuta el archivo `uninstall.bat` ubicado en la carpeta de instalación (Click derecho en el icono del escritorio -> Abrir ubicación del archivo) para borrar los archivos y los accesos directos.

### 🗺️ Roadmap / Planes

*   **Corto Plazo:** Implementación completa de `UpdateManager.ts` para actualizaciones automáticas "over-the-air".
*   **Medio Plazo:**
    *   Integración de **Firebase (FCM)** para notificaciones Push en el móvil (recibir alertas de crafteo completado en tu teléfono).
    *   **Background Sync:** Sincronización en segundo plano en móvil, permitiendo que la app se actualice incluso estando "cerrada".
    *   Backups encriptados end-to-end.
*   **Largo Plazo (Wakfu Hub):**
    *   Convertir la aplicación en un **Hub de Herramientas** integral.
    *   **Combat Meter:** Medidor de daño y estadísticas en tiempo real.
    *   **Daily Tasks:** Gestor de tareas diarias (Mazmorras, Moduladas, Almanax, etc.).
    *   **Alertas de Misiones:** Notificaciones automáticas de misiones ambientales/competitivas.
    *   **Chat Tracker:** Monitoreo del chat con filtros Regex o palabras clave específicas.
    *   **Buscador de Grupos (LFG):** Sistema avanzado para organizar partidas.
        *   Crear salas para mazmorras específicas.
        *   Listado público para buscar grupos.
        *   Notificación automática al líder cuando el grupo esté lleno.
        *   **Gestión de Invitaciones:** Los usuarios configurarán su perfil (Nombre de personaje/Servidor) para que el líder sepa exactamente a quién invitar al juego.

### ☕ Apoya el Proyecto

Si la herramienta te ayuda a farmear más rápido, considera invitarme un café:

*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`

---

<a name="en"></a>
## 🇬🇧 English (EN)

### 💡 What is it?
**Wakfu Tracker** is a cross-platform companion tool designed to optimize your Wakfu gameplay. It's not just a to-do list; it's a connected ecosystem between your PC and Mobile that tracks resources, recipes, and professions in real-time.

**New in v1.0.7:** Now includes a professional installer, real cloud synchronization, and a fully functional mobile app.

### 🚀 Key Features

*   **☁️ Cloud Sync (Sync Alert + Pull):** Your PC progress is instantly reflected on your mobile and vice versa. Forget manual transfers; everything travels via real-time sockets.
*   **📱 Dedicated Mobile App:** A compact, touch-optimized interface designed to take your farming list to the grocery store or the couch.
*   **🔔 Steam-style Notifications:** Elegant, non-intrusive visual alerts on your desktop (with Slide In/Out animations) when you complete a recipe or reach a resource goal.
*   **📝 Smart Log Monitoring:**
    *   Automatically detects items gained and consumed.
    *   Smartly differentiates between losing materials (via crafting) and crafting items, preventing double counting.
*   **📊 Resource Tracking (Auto):** Dynamically calculates the base materials (iron, wood, etc.) needed for *all* your active recipes combined.
*   **🛡️ Data Protection:** "Anti-Zombie" and "Anti-Rebounce" logic to prevent counting errors or date conflicts during sync.

### 📖 Quick Start Guide

1.  **Installation:**
    *   Run `Setup.exe`.
    *   Choose "Only for me" (recommended). The app will be copied to your user folder and shortcuts created automatically.
2.  **First Steps (PC):**
    *   Open the app.
    *   Go to **Settings (⚙️)**: Verify your `wakfu.log` path and select your language.
    *   **Login:** Connect your Discord account to enable cloud synchronization.
3.  **Link Mobile:**
    *   Install the APK on your Android.
    *   Log in with the same Discord account. Done! Your data will merge automatically.
4.  **Add Trackers:**
    *   Use the bottom search bar to find items (e.g., "Rough Gem").
    *   Click the `(+)` button or the `eye` icon to track.
5.  **Play:**
    *   The program reads the logs. If you harvest iron, the bar goes up. If you craft, resources are deducted, and the recipe count increases.

### 🗑️ Uninstallation
Since this is a lightweight installation (file copy), simply run the `uninstall.bat` file located in the installation folder (Right-click desktop icon -> Open file location) to remove the files and shortcuts.

### 🗺️ Roadmap

*   **Short Term:** Full implementation of `UpdateManager.ts` for automatic over-the-air updates.
*   **Medium Term:**
    *   **Firebase (FCM)** integration for mobile Push Notifications.
    *   **Background Sync:** Background synchronization on mobile, allowing the app to update even when "closed".
    *   End-to-end encrypted backups.
*   **Long Term (Wakfu Hub):**
    *   Transform the app into an all-in-one **Tool Hub**.
    *   **Combat Meter:** Real-time damage and stats tracker.
    *   **Daily Tasks:** Manager for Dungeons, Modulox, Almanax, etc.
    *   **Quest Alerts:** Automatic notifications for environmental/competitive quests.
    *   **Chat Tracker:** Chat monitoring with specific keywords or Regex filters.
    *   **Group Finder (LFG):** Advanced party organizing system.
        *   Create lobbies for specific dungeons.
        *   Public list for finding groups.
        *   Automatic "Group Full" notifications for the leader.
        *   **Invite Management:** Users will configure their profile (Character Name/Server) so the leader knows exactly who to invite in-game.

### ☕ Support the Project

If this tool helps you farm faster, consider buying me a coffee:

*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`
*   **USDT (BEP20):** `0x041bedc9c0aab1955552a6a0c4a1bfa44276cabe`

---

<a name="fr"></a>
## 🇫🇷 Français (FR)

### 💡 Qu'est-ce que c'est ?
**Wakfu Tracker** est un outil compagnon multiplateforme conçu pour optimiser votre expérience de jeu sur Wakfu. Ce n'est pas seulement une liste de tâches ; c'est un écosystème connecté entre votre PC et votre mobile qui suit les ressources, les recettes et les métiers en temps réel.

**Nouveauté v1.0.7 :** Inclut désormais un installateur professionnel, une véritable synchronisation cloud et une application mobile entièrement fonctionnelle.

### 🚀 Fonctionnalités Clés

*   **☁️ Cloud Sync (Sync Alert + Pull) :** Votre progression sur PC est instantanément reflétée sur votre mobile et vice versa.
*   **📱 App Mobile Dédiée :** Une interface compacte et tactile conçue pour emporter votre liste de farm partout.
*   **🔔 Notifications style Steam :** Des alertes visuelles élégantes et non intrusives sur votre bureau (avec animations) lorsque vous terminez une recette.
*   **📝 Surveillance Intelligente des Logs :**
    *   Détecte automatiquement les objets obtenus et consommés.
    *   Différencie la perte de matériaux (par craft) de la fabrication d'objets, évitant le double comptage.
*   **📊 Suivi des Ressources (Auto) :** Calcule dynamiquement les matériaux de base nécessaires pour *toutes* vos recettes actives combinées.

### 📖 Guide Rapide

1.  **Installation :** Exécutez `Setup.exe`. Choisissez "Seulement pour moi". L'application est copiée localement.
2.  **PC :** Ouvrez l'app, configurez le chemin des logs dans **Paramètres (⚙️)** et connectez-vous avec Discord.
3.  **Mobile :** Installez l'APK, connectez-vous avec Discord. La synchronisation est automatique.
4.  **Utilisation :** Cherchez des objets en bas et ajoutez-les. Le programme mettra à jour les quantités automatiquement en lisant les logs du jeu.

### 🗑️ Désinstallation
Exécutez simplement le fichier `uninstall.bat` situé dans le dossier d'installation pour supprimer les fichiers et les raccourcis.

### 🗺️ Roadmap / Avenir

*   **Court Terme :** Mises à jour automatiques.
*   **Moyen Terme :**
    *   Intégration **Firebase** pour les notifications push sur mobile.
    *   **Background Sync :** Synchronisation en arrière-plan sur mobile.
*   **Long Terme (Wakfu Hub) :**
    *   Conversion en un **Hub d'Outils** complet.
    *   **Combat Meter :** Suivi des dégâts en temps réel.
    *   **Tâches Quotidiennes :** Gestion des donjons, modulés, etc.
    *   **Chat Tracker :** Surveillance du chat avec mots-clés ou Regex.
    *   **Recherche de Groupe (LFG) :** Système avancé pour organiser des groupes.
        *   Créer des salons pour des donjons spécifiques.
        *   Liste publique pour trouver des groupes.
        *   Notification "Groupe Complet" pour le chef.
        *   **Gestion des invitations :** Les utilisateurs configureront leur profil (Nom du perso/Serveur) pour faciliter les invitations en jeu.

### ☕ Soutenir le projet

*   **Ko-Fi :** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID :** `196153443`

---

<a name="pt"></a>
## 🇵🇹 Português (PT)

### 💡 O que é?
**Wakfu Tracker** é uma ferramenta "companion" multiplataforma projetada para otimizar sua jogabilidade no Wakfu. É um ecossistema conectado entre seu PC e Celular que rastreia recursos, receitas e profissões em tempo real.

**Novidade v1.0.7:** Agora inclui um instalador profissional, sincronização real na nuvem e um aplicativo móvel totalmente funcional.

### 🚀 Funcionalidades Principais

*   **☁️ Sincronização Cloud (Sync Alert + Pull):** Seu progresso no PC é refletido instantaneamente no celular e vice-versa.
*   **📱 App Mobile Dedicado:** Interface compacta e tátil para levar sua lista de farm para qualquer lugar.
*   **🔔 Notificações Estilo Steam:** Alertas visuais elegantes na área de trabalho quando você completa uma receita.
*   **📝 Monitoramento Inteligente de Logs:** Detecta itens obtidos/consumidos e evita contagem dupla ao craftar.
*   **📊 Rastreamento de Recursos (Auto):** Calcula dinamicamente os materiais base necessários para *todas* as suas receitas ativas.

### 📖 Guia Rápido

1.  **Instalação:** Execute o `Setup.exe`. Escolha "Apenas para mim". A aplicação será copiada e configurada automaticamente.
2.  **PC:** Abra o app, configure o caminho dos logs em **Configurações (⚙️)** e faça login com o Discord.
3.  **Mobile:** Instale o APK, faça login com o Discord. A sincronização é automática.
4.  **Uso:** Busque itens na barra inferior e adicione-os. O programa atualizará as quantidades automaticamente lendo os logs do jogo.

### 🗑️ Desinstalação
Basta executar o arquivo `uninstall.bat` localizado na pasta de instalação para remover os arquivos e atalhos.

### 🗺️ Roadmap / Futuro

*   **Curto Prazo:** Atualizações automáticas.
*   **Médio Prazo:**
    *   Integração **Firebase** para notificações push no celular.
    *   **Background Sync:** Sincronização em segundo plano no celular.
*   **Longo Prazo (Wakfu Hub):**
    *   Transformar o app em um **Hub de Ferramentas**.
    *   **Combat Meter:** Medidor de dano em tempo real.
    *   **Tarefas Diárias:** Gerenciador de Calabouços, Moduladas, etc.
    *   **Chat Tracker:** Monitoramento de chat com palavras-chave ou Regex.
    *   **Localizador de Grupos (LFG):** Sistema avançado de organização de grupos.
        *   Criar salas para calabouços específicos.
        *   Lista pública para encontrar grupos.
        *   Notificação automática de "Grupo Cheio" para o líder.
        *   **Gestão de Convites:** Os usuários configurarão seu perfil (Nome do personagem/Servidor) para facilitar o convite dentro do jogo.

### ☕ Apoie o projeto

*   **Ko-Fi:** [ko-fi.com/olivo28](https://ko-fi.com/olivo28)
*   **Binance Pay ID:** `196153443`

---

**Legal Notice:** This tool processes information obtained from the game client and public sources. The author is not liable for any misuse. Use at your own risk.
