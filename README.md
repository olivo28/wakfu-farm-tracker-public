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

### Desinstalación
Actualmente, la aplicación no cuenta con un desinstalador nativo de Windows (unins000.exe).
Para desinstalarla, **ejecuta el archivo `uninstall.bat`** que se encuentra dentro de la carpeta de instalación (o haz clic derecho en el acceso directo -> "Abrir ubicación del archivo"). Este script eliminará la aplicación, los accesos directos y limpiará el registro automáticamente.

### Planes / Roadmap (detalle)

Corto plazo (próxima versión):
- **Actualizaciones (CRÍTICO): Implementación completa del `UpdateManager.ts`** para realizar la comprobación de versión y gestionar la descarga automática de nuevas versiones.
- **Desinstalador Nativo:** Crear un ejecutable de desinstalación real para reemplazar el script `.bat`.
- macOS / Linux: preparar empaquetados (DMG, PKG, AppImage).
- Datos: optimizar el cache local, soportar actualizaciones incrementales desde el CDN y modo offline total.

Medio plazo:
- Sincronización opcional: diseñar un sistema de sync cifrado (end-to-end) y backups en la nube; importar/exportar listas en JSON/CSV.
- Integraciones: permitir importar listas y plantillas desde fuentes comunitarias.
- Rendimiento: optimizaciones de memoria y CPU al construir snapshots grandes.

### Licencia

**MIT License**

Copyright (c) 2025 Antikux

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: the above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Aviso legal corto
Esta herramienta procesa y muestra información obtenida del cliente/juego y de fuentes públicas. El autor no se hace responsable de su uso ni de daños derivados del software. Usa el ejecutable bajo tu responsabilidad.

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

### Uninstallation
Currently, the application does not have a native Windows uninstaller (unins000.exe).
To uninstall, **run the `uninstall.bat` file** located in the installation folder (or right-click the shortcut -> "Open file location"). This script will automatically remove the application, shortcuts, and clean the registry.

### Plans / TODO (detailed)

Short term (next release):
- **Updates (CRITICAL): Full implementation of `UpdateManager.ts`** for version checking and auto-updating.
- **Native Uninstaller:** Create a real uninstaller executable to replace the `.bat` script.
- macOS / Linux: Prepare native packages (DMG, PKG, AppImage).
- Data: Harden local caching, support incremental CDN updates, and offline mode.

Medium term:
- Optional sync: End-to-end encrypted cloud backup; JSON/CSV import/export.
- Integrations: Import community lists/templates.
- Performance: Reduce memory/CPU usage.

### License

**MIT License**

Copyright (c) 2024 Antikux

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: the above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Short legal notice
This tool processes and displays information obtained from the game client and public sources. The author is not liable for any misuse or damages. Use the executable at your own risk.

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

### Désinstallation
Actuellement, l'application ne dispose pas d'un désinstallateur Windows natif.
Pour désinstaller, **exécutez le fichier `uninstall.bat`** situé dans le dossier d'installation (ou faites un clic droit sur le raccourci -> "Ouvrir l'emplacement du fichier"). Ce script supprimera automatiquement l'application, les raccourcis et nettoiera le registre.

### Plans / TODO (détaillé)

Court terme (prochaine version) :
- **Mises à jour (CRITIQUE) : Implémentation de `UpdateManager.ts`** pour les mises à jour automatiques.
- **Désinstallateur Natif :** Créer un véritable exécutable de désinstallation.
- macOS / Linux : Préparer des paquets natifs.
- Données : Renforcer le cache local et le mode hors-ligne.

Moyen terme :
- Synchronisation : Sauvegarde cloud chiffrée ; import/export JSON/CSV.
- Intégrations : Listes communautaires.

### Licence

**MIT License**

Copyright (c) 2024 Antikux

Ce logiciel est fourni « tel quel », sans garantie d'aucune sorte, expresse ou implicite, y compris, mais sans s'y limiter, les garanties de qualité marchande, d'adéquation à un usage particulier et d'absence de contrefaçon. En aucun cas, les auteurs ou titulaires du droit d'auteur ne seront responsables de toute réclamation, dommage ou autre responsabilité, que ce soit dans une action contractuelle, délictuelle ou autre, découlant de, hors de ou en connexion avec le logiciel ou l'utilisation ou d'autres transactions dans le logiciel.

**Avis Légal Court :**
Cet outil traite et affiche des informations obtenues à partir du client du jeu et de sources publiques. L'auteur n'est pas responsable de toute mauvaise utilisation ou de tout dommage. Utilisez l'exécutable à vos risques et périls.


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

### Desinstalação
Atualmente, a aplicação não possui um desinstalador nativo do Windows.
Para desinstalar, **execute o arquivo `uninstall.bat`** localizado na pasta de instalação (ou clique com o botão direito no atalho -> "Abrir local do arquivo"). Este script removerá automaticamente a aplicação, os atalhos e limpará o registro.

### Planos / Roadmap (detalhado)

Curto prazo (próxima versão):
- **Atualizações (CRÍTICO): Implementação do `UpdateManager.ts`** para atualizações automáticas.
- **Desinstalador Nativo:** Criar um executável de desinstalação real.
- macOS / Linux : Pacotes nativos.
- Dados: Cache local e modo offline.

Médio prazo:
- Sincronização: Backup em nuvem criptografado; import/export JSON/CSV.
- Integrações: Listas comunitárias.

### Licença

**MIT License**

Copyright (c) 2024 Antikux

Este software é fornecido "no estado em que se encontra", sem garantia de qualquer tipo, expressa ou implícita, incluindo, mas não se limitando às garantias de comercialização, adequação a uma finalidade específica e não violação. Em hipótese alguma os autores ou detentores de direitos autorais serão responsáveis por qualquer reclamação, danos ou outra responsabilidade, seja em uma ação de contrato, ato ilícito ou de outra forma, decorrente de, fora de ou em conexão com o software ou o uso ou outras negociações no software.

**Aviso Legal Curto:**
Esta ferramenta processa e exibe informações obtidas no cliente do jogo e em fontes públicas. O autor não se responsabiliza por qualquer uso indevido ou danos. Utilize o executável por sua conta e risco.
   
