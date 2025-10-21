# 🎵 Playlist Curator Agent 🎵

> An intelligent multi-agent AI system that creates exceptional themed playlists by analyzing musical requirements and curating tracks from Spotify. Powered by [cagent](https://github.com/docker/cagent).

---

## 🎭 About

Playlist Curator Agent is your personal music curation team powered by AI. This multi-agent system analyzes your playlist themes with musical expertise, searches Spotify's vast catalog, and creates perfectly crafted playlists that capture the exact mood and vibe you're looking for. Whether you want "cozy acoustic songs for a rainy Sunday" or "high-energy workout bangers," our specialized agents work together to deliver the perfect musical experience.

---

## 🛠️ Tech Stack

- **cagent** (multi-agent runtime)
- **YAML** (agent configuration)
- **Spotify API** (music search and playlist creation)
- **Docker** (MCP Spotify server)
- **Anthropic Claude** (AI model provider)

---

## 📋 Prerequisites

- Prebuilt binaries for Windows, macOS and Linux can be found on the releases page of the [project's GitHub repository](https://github.com/docker/cagent/releases)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) for running the Spotify MCP server
- Spotify API credentials (Client ID, Client Secret)
- Anthropic API key

---

## 🚀 Quick Start

### 1. Download & Install

Download the prebuilt binary for your platform from the [cagent releases page](https://github.com/docker/cagent/releases).

On macOS/Linux, make it executable:

```bash
chmod +x /path/to/cagent-binary
```

### 2. Set Your API Keys

Copy the environment template and add your keys:

```bash
cp .env.example .env
```

Then edit `.env` with your actual API keys:

```bash
# Anthropic API Configuration
ANTHROPIC_API_KEY=your_anthropic_api_key_here

# OpenAI API Configuration (optional, for research features)
OPENAI_API_KEY=your_openai_api_key_here

# Spotify API Configuration
SPOTIFY_CLIENT_ID=your_spotify_client_id_here
SPOTIFY_CLIENT_SECRET=your_spotify_client_secret_here
SPOTIFY_REDIRECT_URI=http://127.0.0.1:8080/callback
```

**Important:** Never commit your `.env` file to version control. It contains sensitive API keys.

### 3. Run Your Playlist Curator

```bash
cagent run playlist-curator-agent.yml --debug
```

### 4. Create Your First Playlist

Simply provide a theme when prompted:
- "Upbeat indie songs for a road trip"
- "Melancholic jazz for late night studying"
- "Energetic electronic music for working out"
- "Chill lo-fi beats for coding"

---

## 🎯 Key Features

- 🧠 **Intelligent Theme Analysis** – Deep musical understanding of genres, moods, and characteristics
- 🎵 **Spotify Integration** – Direct access to millions of tracks via Spotify API
- 🤖 **Multi-agent Coordination** – Specialized agents for analysis and curation
- 🎨 **Creative Playlist Naming** – Evocative titles that capture the essence
- 📝 **YAML Configuration** – Clean, readable agent definitions
- 🎼 **Perfect Flow** – Optimized track ordering for seamless listening
- 🔗 **Instant Access** – Direct Spotify playlist links for immediate listening

---

## 🏃 Example Usage

Run the playlist curator:

```bash
cagent run playlist-curator-agent.yml --debug
```

Example interaction:
```
User: "Create a playlist for cozy acoustic songs for a rainy Sunday"

🎵 PLAYLIST CREATED: Rainy Sunday Reverie
🔗 SPOTIFY LINK: https://open.spotify.com/playlist/...

TRACKS:
1. Bon Iver - Holocene
   Why: Perfect melancholic acoustic opener with beautiful vocals

2. The Paper Kites - Bloom
   Why: Dreamy acoustic layers that capture rainy day introspection

3. Fleet Foxes - White Winter Hymnal
   Why: Harmonious folk that builds emotional depth

4. Sufjan Stevens - Mystery of Love
   Why: Tender closing track with perfect rainy day resolution
```

---

## 🎪 Agent Architecture

The system uses three specialized agents:

### 🎯 Lead Music Curator (Root)
- Coordinates the entire curation process
- Ensures quality and cohesive flow
- Presents final playlists with beautiful formatting

### 🔍 Theme Analyzer
- Musical expertise and mood interpretation
- Extracts genres, energy levels, and search strategies
- Provides structured analysis for optimal curation

### 🎵 Playlist Builder
- Direct Spotify API integration
- Track searching and selection
- Playlist creation and optimization

---

## 📚 More Resources

- [cagent Documentation](https://github.com/docker/cagent)
- [Spotify Web API Reference](https://developer.spotify.com/documentation/web-api)
- [MCP Toolkit & Catalog](https://docs.docker.com/ai/mcp-catalog-and-toolkit/toolkit/)
- [Agent Examples](https://github.com/docker/cagent/tree/main/examples)

---

## 💡 Getting Help

For command help:

```bash
./cagent --help
./cagent [command] --help
```

For feedback or issues:

```bash
./cagent feedback
```

---

Made with 🎵, AI, and a passion for perfect playlists!