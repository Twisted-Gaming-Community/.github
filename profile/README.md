# InfiniTea WIKI

Welcome to the **InfiniTea Discord Bot** documentation! This page provides an overview of the bot’s features, commands, and configurations.  

---

## 📌 Commands

### 🎁 Giveaway
- **`/giveaway <channel|role|guild>`**  
  - Randomly selects a person from the specified **channel**, **role**, or the **entire Discord**.

### 🔗 Navigation
- **`/navigate <title>`**  
  - Generates an **embed** containing the provided URL(s) to help users navigate your Discord server.

### 🛑 Role Management
- **`/purge <role>`**  
  - Removes a specific role from **all members** in the community.

### 📝 Registration System
- **`/register <game>`**  
  - Generates an embed for **Application Tracking** of members within your community.
  - Supported Titles:
    - ✅ **Path of Exile 2** (Supported)
    - 🏗️ **Valheim** (Under Development)
    - 🏗️ **Minecraft** (Under Development)

### ⭐ Reputation System
- **`/give_rep <user>`**  
  - Gives `+1` reputation to a user.
  - If given by:
    - **Administrator** → Increases `staff_rep`
    - **User** → Increases `community_rep`
- **`/remove_rep <user> <amount>`**  
  - **Staff only.** Removes `<x>` reputation from a user.
  - **Affects both** `community_rep` and `staff_rep`, but does not drop below `0`.

### 🔍 Server Status
- **`/status`**  
  - Retrieves a list of **server statuses** from **AMP by CubeCoders**.
  - *Only use this if you own AMP and self-host gaming servers.*

### ⏳ Temporary Messages
- **`/temp_message <duration> <message>`**  
  - Creates a **self-destructing message** that disappears after `<duration>`.
  - Displays a **countdown** (updates every second, but may change in the future).

---

## ⚙️ Configuration

By default, **all features/commands are disabled**.  
To enable a feature, use:  
**`/configure <feature>, <feature>, <feature>`**

### 🛠 Additional Configurations

#### 📜 PoE2 Registration
- **Command:** `/configure poe2_registration`
- Requires:
  - A **"Registration Channel" URL** (must be visible to players).
  - Admins with `manage_messages` permission can interact with:
    - **Approve**, **Delay**, **Info**, and **Report** actions.

#### 🗺 Navigation System
- **Command:** `/configure navigate <action>`
- Features:
  - CRUD actions for navigation embeds.
  - Uses **Groups** (e.g., `Info`, `Game X`, `Sub Community Y`).
  - **FIFO** (First In, First Out) order.
  - Ordering is still under development.

---

## 🔥 Non-Command Features

### 🎤 Auto Voice Channel Creation
- If a **voice channel is named** `"Create VC"` (exactly):
  - The bot **creates a new voice channel** and moves the user there.
  - The bot will **delete** the channel when it becomes empty.
- Planned features:
  - Resizing channels.
  - Making channels private.

### 🌟 Starboard
- Tracks **reactions** and **copies messages** to a **starboard**.
- Requirements:
  - A **channel named** `⭐│starboard` (exactly).
  - A message needs **10 ⭐ reactions** to be added.
  - If reactions drop **below 10**, the starboard message is removed.
  - Includes a **"Jump" button** to the original message.
- Future update:
  - `/configure` command to set **starboard channel & reaction count**.

### 📊 Member Activity Tracking
- Tracks **text & voice activity**:
  - **1 XP per message** (every 10 sec).
  - **1 XP per minute** in voice chat.
- Future plans:
  - A **/top leaderboard**.
  - More features to encourage Discord engagement.

---

## 🎯 Final Notes
- **All features are opt-in.** Enable only what you need.
- More updates coming soon—stay tuned!
