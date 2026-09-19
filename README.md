# Free Fire Player Info & Wishlist API — Complete Developer Guide

Ei project-ti ekti advanced **Flask-based API utility** ja Free Fire player personal info ebong wishlist data khub druto ebong nirapohode fetch korar jonno toiri kora hoyeche [cite: 3]. Eta AES encryption, Protobuf decoding ebong automatic JWT token cache management support kore [cite: 3].

---

## 📌 Source & Developer Information

* **Source Creator:** [XEROX_MODS](https://t.me/SEXTYMODS) [cite: 3]
* **Telegram Channel:** [SEXTYMODS](https://t.me/SEXTYMODS) [cite: 3]

> **Important:** Source share ba modify korar somoy obossoi original creator credit (`XEROX_MODS` & `SEXTYMODS`) thik rakhben [cite: 3].

---

## 🚀 Core Features

* **Flask REST API:** Halka ebong druto response deoyar jonno Flask framework bebohar kora hoyeche [cite: 3].
* **Dynamic Region Support:** IND, BD, PK, VN, ME, ID, TH, BR, US, SAC soho bibhinno region-er server handle korte pare [cite: 3].
* **JWT Token Sync & Caching:** Automatic JWT token fetch ebong in-memory cache system, ja API request ke fast rakhe [cite: 3].
* **AES CBC Encryption:** Game server request er data secure rakhar jonno AES encryption use kora hoyeche [cite: 3].
* **Protobuf to JSON:** Binary protobuf response ke easily readable JSON format-e convert kore [cite: 3].
* **Real-time Metadata:** Response-er sathe Devloper name, Telegram link, Time Span ebong Asia/Kolkata timezone er date/time auto-inject hoy [cite: 3].
* **Embedded Web UI:** Root URL (`/`) visit korlei ekti modern UI dekhabe jar maddhome API status ebong endpoints dekha jay [cite: 3].

---

## ⚙️ Requirements & Installation Guide

Nicher Python packages gulo apnar system-e install thaka lagbe [cite: 3]:

```bash
pip install flask requests pycryptodome protobuf urllib3
```

---

## 🌐 Supported Regions & Server Mapping

API ti bibhinno region er jonno nicher server gulo use kore [cite: 3]:

| Region Code | Server Type / URL Endpoint |
| :--- | :--- |
| **IND** | India Server (`client.ind.freefiremobile.com`) [cite: 3] |
| **BR / US / SAC** | Americas / US Server (`client.us.freefiremobile.com`) [cite: 3] |
| **BD / PK / VN / ME / ID / TH** | Global BP Server (`clientbp.ggpolarbear.com`) [cite: 3] |

---

## 🔌 API Endpoints & Usage Details

### 1. Home Page UI
* **Route:** `GET /`
* **Description:** API running status ebong quick endpoint access deoyar jonno UI render kore [cite: 3].

### 2. Player Info API
* **Route:** `GET /info`
* **Query Parameters:**
  * `uid` (Required): Player er Free Fire UID [cite: 3].
  * `region` (Optional): Server region code (default: `ind`) [cite: 3].
  * `key` (Optional): Custom AES encryption key [cite: 3].
  * `iv` (Optional): Custom AES initialization vector [cite: 3].
* **Example URL:** 
  ```text
  http://localhost:1080/info?uid=5038779552&region=ind
  ```

### 3. Wishlist Info API
* **Route:** `GET /wishlist`
* **Query Parameters:**
  * `uid` (Required): Player er Free Fire UID [cite: 3].
  * `region` (Optional): Server region code [cite: 3].
* **Example URL:** 
  ```text
  http://localhost:1080/wishlist?uid=5038779552&region=ind
  ```

---

## 📄 Complete Example JSON Response (`/info`)

```json
{
  "basic_info": {
    "account_id": 5038779552,
    "account_type": 1,
    "nickname": "₦₲ㅤㅤᏒAHULㅤ모ㅤ",
    "region": "IND",
    "level": 74,
    "exp": 4089629,
    "banner_id": 901042013,
    "head_pic": 902000123,
    "rank": 325,
    "ranking_points": 5700,
    "has_elite_pass": false,
    "badge_cnt": 90,
    "badge_id": 1001000100,
    "season_id": 53,
    "liked": 30212,
    "show_rank": true,
    "last_login_at": 1789790764,
    "cs_rank": 322,
    "cs_ranking_points": 114,
    "weapon_skin_shows": [907103017, 912040001],
    "max_rank": 325,
    "cs_max_rank": 322,
    "peak_rank_pos": 0,
    "account_prefers": {
      "br_pregame_show": 0,
      "hide_clan_info": false,
      "hide_weapon_skins": false,
      "show_elite_pass": false,
      "show_title": false,
      "raw_field_3": 0
    },
    "create_at": 1642525530,
    "title": 904590059,
    "external_icon_info": {
      "status": "ICON_INACTIVE",
      "show_type": "ICON_VISIBLE",
      "raw_field_3": 1
    },
    "release_version": "OB55",
    "show_br_rank": false,
    "show_cs_rank": false,
    "social_highlights": {
      "entries": []
    },
    "item_tag_info": "0a0a080110ceb3bfd50618010a0a0806109bc2b9d50618010a0a0802108afdc2d50618010a0a080410b0c7b9d50618040a0a080510a7b8bfd5061801",
    "hippo_rank": 19,
    "hippo_ranking_points": 19,
    "cs_rank_entries": [],
    "raw_field_60": 0,
    "prime_info": {
      "prime_level": 3
    }
  },
  "profile_info": {
    "avatar_id": 102000007,
    "cosmetic_items": [50],
    "equipped_skills": [211000598, 211000433, 203000096, 205000059, 204000181, 214000000],
    "pve_primary_weapon": 1,
    "skill_slots": [
      {
        "slot_index": 0,
        "skill_id": 606
      },
      {
        "slot_index": 1,
        "skill_id": 5301
      },
      {
        "slot_index": 2,
        "skill_id": 1803
      },
      {
        "slot_index": 3,
        "skill_id": 7406
      }
    ],
    "skin_unlock_time": 1,
    "raw_field_12": 1
  },
  "ranking_leaderboard_pos": 0,
  "news": [],
  "history_ep_info": [],
  "clan_basic_info": {
    "clan_id": 0,
    "clan_name": "",
    "captain_id": 0,
    "clan_level": 0,
    "max_members": 0,
    "current_members": 0
  },
  "captain_basic_info": {
    "account_id": 0,
    "account_type": 0,
    "nickname": "",
    "region": "",
    "level": 0,
    "exp": 0,
    "banner_id": 0,
    "head_pic": 0,
    "rank": 0,
    "ranking_points": 0,
    "has_elite_pass": false,
    "badge_cnt": 0,
    "badge_id": 0,
    "season_id": 0,
    "liked": 0,
    "show_rank": false,
    "last_login_at": 0,
    "cs_rank": 0,
    "cs_ranking_points": 0,
    "weapon_skin_shows": [],
    "max_rank": 0,
    "cs_max_rank": 0,
    "peak_rank_pos": 0,
    "account_prefers": {
      "br_pregame_show": 0,
      "hide_clan_info": false,
      "hide_weapon_skins": false,
      "show_elite_pass": false,
      "show_title": false,
      "raw_field_3": 0
    },
    "create_at": 0,
    "title": 0,
    "external_icon_info": {
      "status": "ICON_INACTIVE",
      "show_type": "ICON_HIDDEN",
      "raw_field_3": 0
    },
    "release_version": "",
    "show_br_rank": false,
    "show_cs_rank": false,
    "social_highlights": {
      "entries": []
    },
    "item_tag_info": "",
    "hippo_rank": 0,
    "hippo_ranking_points": 0,
    "cs_rank_entries": [],
    "raw_field_60": 0,
    "prime_info": {
      "prime_level": 0
    }
  },
  "pet_info": {
    "pet_id": 1300000091,
    "pet_name": "GOOD_BOY",
    "level": 7,
    "exp": 6019,
    "is_selected": true,
    "skin_id": 1310000093,
    "selected_skill_id": 1315000011
  },
  "social_info": {
    "account_id": 5038779552,
    "gender": "GENDER_UNKNOWN",
    "language": 17,
    "social_highlight": "Battle in Style!",
    "privacy": "PRIVACY_FRIENDS_ONLY",
    "region_stats": [
      {
        "region_code": "",
        "total_matches": 0,
        "wins": 0,
        "highest_rank": 0,
        "last_season_played": 0,
        "last_match_time": 0
      }
    ]
  },
  "diamond_cost_res": {
    "diamond_cost": 390,
    "currency_type": 0,
    "discount_percent": 0
  },
  "credit_score_info": {
    "score": 100,
    "status": 1,
    "start": 1789662607,
    "end": 1789921807,
    "reason": 2
  },
  "pre_veteran_action": {
    "action_type": 0,
    "action_expire_time": 0
  },
  "equipped_achievements": [],
  "mmr_ratings": [],
  "Devloper": "XEROX_MODS",
  "Telegram": "SEXTYMODS",
  "Time_Spne": "3.81s",
  "Time": "10:09 AM, Saturday, September 19, 2026"
}
```

---

## 🚀 How to Run the Project Locally

1. Sohojoge sobi ekti folder-e rakhoon (`main.py`, protobuf files, etc.) [cite: 3].
2. Terminal ba Command Prompt open kore project directory te jan [cite: 3].
3. Nicher command diye server start korun [cite: 3]:
   ```bash
   python main.py
   ```
4. Server ti default vabe `http://0.0.0.0:1080` port e cholbe [cite: 3]. Apni apnar browser ba API client (Postman/Insomnia) diye test korte paren [cite: 3].


---

## 🛡️ Original Credit & Attribution

```text
===============================================================
                    SOURCE CREDIT
===============================================================

This Source Was Created and Developed By: XEROX_MODS

Official Telegram Channel: SEXTYMODS

Please Do Not Remove, Edit, Hide, or Replace
The Original Creator Credit.

Creator Name  : XEROX_MODS
Telegram      : SEXTYMODS
Source Credit : XEROX_MODS

===============================================================
```

---

## ⚖️ Disclaimer & License

* **Disclaimer:** The creator does not guarantee uninterrupted operation because the project relies on external APIs and services. Users are responsible for their own use of the software, account credentials, and compliance with applicable terms.
* **License:** No separate open-source license is specified. Unless the creator explicitly grants permission, do not commercially redistribute or relicense this source.

---

