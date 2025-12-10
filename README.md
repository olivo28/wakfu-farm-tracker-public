# Wakfu Farm Tracker — Manual de uso (ES / EN / FR / PT)

## Índice

- [Español (ES)](#es)
- [English (EN)](#en)
- [Français (FR)](#fr)
- [Português (PT)](#pt)

---

<a name="es"></a>
## Español (ES)

### ¿Qué es?
Wakfu Farm Tracker es una aplicación de escritorio para ayudar a jugadores de Wakfu a rastrear recursos, recetas y progresos de farm/oficios. 
**Ahora incluye un instalador profesional** que configura la aplicación, crea accesos directos y permite una fácil desinstalación.

### Qué hace (Actualizado)
- Escanea archivos de log del juego y detecta eventos (objetos obtenidos/consumidos, recetas realizadas).
- **Rastreo Inteligente de Recursos:** Mantiene una lista de **Recursos Necesarios (Auto)**, calculando dinámicamente el total de materiales base que te faltan de todas las recetas activas y sincronizando el progreso de tu inventario.
- **Sincronización Bidireccional:** El progreso anotado en la lista de recursos se refleja automáticamente en la receta que lo requiere, y viceversa.
- Mantiene una lista de trackers (tarjetas) con recetas y recursos, calculando cantidades necesarias y seguimiento de ítems.
- Muestra detalles de ítems (icono, rareza, efectos y descripción) usando los datos del motor de datos.
- Permite búsqueda rápida de ítems y añadir trackers desde resultados.
- Soporta múltiples idiomas (ES, EN, FR, PT) y selección rápida desde la interfaz.
- **Chequeo de Versión:** Guarda localmente la versión de la aplicación para buscar actualizaciones periódicas.

### Uso (rápido)
1. **Instalación:** Ejecuta el archivo `Setup.exe`.
   - Selecciona tu idioma.
   - Elige el tipo de instalación: "Solo para mí" (recomendado) o "Todos los usuarios".
   - El instalador copiará los archivos y creará accesos directos en el **Escritorio** y el **Menú Inicio**.
2. Abre la aplicación desde el nuevo icono en tu escritorio.
3. En la barra superior selecciona el idioma si es necesario.
4. **Configuración (⚙️):** Configura la ruta de tus logs (`logs/wakfu.log`), el inicio automático y activa el modo **Recursos Necesarios (Auto)**.
5. Usa el buscador inferior para localizar un ítem y pulsa `Buscar` para agregar un tracker.
6. El programa leerá los logs del juego automáticamente.

### Cómo funciona (técnico - breve)
- **Instalador:** Basado en Electron y NSIS, gestiona la copia de archivos, registro en Windows (para aparecer en "Agregar o quitar programas") y creación de accesos directos `.lnk`.
- DataEngine: descarga o lee JSON con datos de ítems/recipes y genera "snapshots".
- TrackerManager: guarda/gestiona trackers, persiste en disco y aplica cambios que vienen del LogWatcher. Es responsable del **recálculo recursivo del inventario (`saved_ings`)** para que los checks verdes de 'Listo' funcionen dinámicamente.
- LogWatcher: vigila el archivo de log del juego (lectura incremental).

### Planes / Roadmap (detalle)

Corto plazo (próxima versión):
- **Actualizaciones (CRÍTICO): Implementación completa del `UpdateManager.ts`** para realizar la comprobación de versión y gestionar la descarga automática de nuevas versiones.
- macOS / Linux: preparar empaquetados (DMG, PKG, AppImage) y scripts de instalación similares a Windows.
- Datos: optimizar el cache local, soportar actualizaciones incrementales desde el CDN y modo offline total.

Medio plazo:
- Sincronización opcional: diseñar un sistema de sync cifrado (end-to-end) y backups en la nube; importar/exportar listas en JSON/CSV.
- Integraciones: permitir importar listas y plantillas desde fuentes comunitarias.
- Rendimiento: optimizaciones de memoria y CPU al construir snapshots grandes.

### Licencia

**MIT License**

Copyright (c) 2024 Antikux

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Aviso legal corto
Esta herramienta procesa y muestra información obtendida del cliente/juego y de fuentes públicas. El autor no se hace responsable de su uso ni de daños derivados del software. Usa el software bajo tu responsabilidad.

---

<a name="en"></a>
## English (EN)

### What is it?
Wakfu Farm Tracker is a desktop application to help Wakfu players track resources, recipes, and farming progress. 
**Now features a professional installer** that handles setup, shortcuts, and uninstallation.

### What it does (Updated)
- Watches the game's log files and detects events (items gained/used, recipes crafted).
- **Smart Resource Tracking:** Maintains a list of **Required Resources (Auto)**, dynamically calculating the total base materials needed from all active recipes and syncing your inventory progress.
- **Bidirectional Sync:** Progress noted in the resource list is automatically reflected in the requiring recipe, and vice-versa.
- Keeps a list of trackers (cards) for recipes and resources.
- Shows item details (icon, rarity, effects, and description).
- Supports multiple languages (ES, EN, FR, PT).
- **Version Check:** Locally stores the application version to check for periodic updates.

### Quick usage
1. **Installation:** Run the `Setup.exe` file.
   - Select your language.
   - Choose installation type: "Only for me" (recommended) or "All users".
   - The installer will copy files and create shortcuts on the **Desktop** and **Start Menu**.
2. Launch the app from the new shortcut.
3. **Settings (⚙️):** Configure your log path, auto-start, and activate the **Required Resources (Auto)** mode.
4. Use the bottom search to find an item and click `Search` to add a tracker.

### How it works (technical - brief)
- **Installer:** Electron/NSIS based. Handles file copying, Windows Registry keys (for "Add/Remove Programs"), and `.lnk` shortcut creation.
- DataEngine: Downloads/reads JSON datasets.
- TrackerManager: Manages trackers and persists data. Responsible for **recursive inventory recalculation**.
- LogWatcher: Monitors the game's log file incrementally.

### Plans / TODO (detailed)

Short term (next release):
- **Updates (CRITICAL): Full implementation of `UpdateManager.ts`** for version checking and auto-updating.
- macOS / Linux: Prepare native packages (DMG, PKG, AppImage).
- Data: Harden local caching, support incremental CDN updates, and offline mode.

Medium term:
- Optional sync: End-to-end encrypted cloud backup; JSON/CSV import/export.
- Integrations: Import community lists/templates.
- Performance: Reduce memory/CPU usage.

### License

**MIT License**

Copyright (c) 2024 Antikux

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Short legal notice
This tool processes and displays information obtained from the game client and public sources. The author is not liable for any misuse or damages. Use at your own risk.

---

<a name="fr"></a>
## Français (FR)

### Qu'est-ce que c'est ?
Wakfu Farm Tracker est une application de bureau aidant les joueurs de Wakfu à suivre ressources, recettes et progressions.
**Dispose désormais d'un installateur professionnel** qui gère la configuration, les raccourcis et la désinstallation.

### Ce que fait l'application (Mis à jour)
- Surveille les fichiers de log du jeu et détecte les événements.
- **Suivi Intelligent des Ressources :** Maintient une liste de **Ressources Nécessaires (Auto)**, calculant dynamiquement le total des matériaux de base manquants.
- **Synchronisation Bidirectionnelle :** La progression notée dans la liste de ressources est automatiquement reflétée dans la recette.
- Garde une liste de trackers (cartes) pour recettes et ressources.
- Affiche les détails des objets (icône, rareté, effets).
- Supporte plusieurs langues (ES, EN, FR, PT).
- **Vérification de Version :** Vérifie les mises à jour périodiques.

### Utilisation rapide
1. **Installation :** Lancez le fichier `Setup.exe`.
   - Sélectionnez votre langue.
   - Choisissez le type d'installation : "Seulement pour moi" (recommandé) ou "Tous les utilisateurs".
   - L'installateur créera des raccourcis sur le **Bureau** et dans le **Menu Démarrer**.
2. Lancez l'application depuis le nouveau raccourci.
3. **Configuration (⚙️) :** Configurez le chemin des logs et activez le mode **Ressources Nécessaires (Auto)**.
4. Utilisez la recherche pour ajouter un tracker.

### Comment ça marche (technique - bref)
- **Installateur :** Basé sur Electron/NSIS. Gère la copie des fichiers, le Registre Windows et la création de raccourcis.
- DataEngine : Gère les données JSON.
- TrackerManager : Gère les trackers et le **recalcul récursif de l'inventaire**.

### Plans / TODO (détaillé)

Court terme (prochaine version) :
- **Mises à jour (CRITIQUE) : Implémentation de `UpdateManager.ts`** pour les mises à jour automatiques.
- macOS / Linux : Préparer des paquets natifs.
- Données : Renforcer le cache local et le mode hors-ligne.

Moyen terme :
- Synchronisation : Sauvegarde cloud chiffrée ; import/export JSON/CSV.
- Intégrations : Listes communautaires.

### Licence

**MIT License**

Copyright (c) 2024 Antikux

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Avis légal court
Cet outil traite des informations issues du client de jeu et de sources publiques. L'auteur décline toute responsabilité. Utilisez à vos risques et périls.

---

<a name="pt"></a>
## Português (PT)

### O que é?
Wakfu Farm Tracker é uma aplicação de desktop para ajudar jogadores de Wakfu a rastrear recursos e receitas.
**Agora inclui um instalador profissional** que gerencia configuração, atalhos e desinstalação.

### O que faz (Atualizado)
- Monitora arquivos de log do jogo e detecta eventos.
- **Rastreamento Inteligente de Recursos:** Mantém uma lista de **Recursos Necessários (Auto)**, calculando dinamicamente o total de materiais base necessários.
- **Sincronização Bidirecional:** O progresso anotado na lista de recursos é automaticamente refletido na receita.
- Mantém lista de trackers (cartões).
- Mostra detalhes de itens.
- Suporta múltiplos idiomas (ES, EN, FR, PT).
- **Verificação de Versão:** Verifica atualizações periodicamente.

### Uso rápido
1. **Instalação:** Execute o arquivo `Setup.exe`.
   - Selecione o idioma.
   - Escolha o tipo de instalação: "Apenas para mim" (recomendado) ou "Todos os usuários".
   - O instalador criará atalhos na **Área de Trabalho** e no **Menu Iniciar**.
2. Abra a aplicação pelo novo atalho.
3. **Configuração (⚙️):** Configure o caminho dos logs e ative o modo **Recursos Necessários (Auto)**.
4. Use a busca para adicionar um tracker.

### Como funciona (técnico - breve)
- **Instalador:** Baseado em Electron/NSIS. Gerencia cópia de arquivos, Registro do Windows e atalhos.
- DataEngine: Gerencia dados JSON.
- TrackerManager: Gerencia trackers e o **recálculo recursivo do inventário**.

### Planos / Roadmap (detalhado)

Curto prazo (próxima versão):
- **Atualizações (CRÍTICO): Implementação do `UpdateManager.ts`** para atualizações automáticas.
- macOS / Linux : Pacotes nativos.
- Dados: Cache local e modo offline.

Médio prazo:
- Sincronização: Backup em nuvem criptografado; import/export JSON/CSV.
- Integrações: Listas comunitárias.

### Licença

**MIT License**

Copyright (c) 2024 Antikux

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Aviso legal curto
Esta ferramenta processa informações obtidas do cliente do jogo. O autor não se responsabiliza por uso indevido. Use por sua conta e risco.
```
