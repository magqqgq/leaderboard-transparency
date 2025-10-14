# Multipli × Kaito Transparency Data

This repository hosts public transparency data for the **Kaito × Multipli Leaderboard**.
Each dataset reflects the raw API response received from Kaito, showing Crystal distributions and ranking details for the top Yappers during a given period.

All data is published exactly as received, with no manual modification, to ensure full transparency and auditability.

---

## Repository Structure

```
.
├── snapshot/
│   └── kaito_leaderboard_2025-10-14.json
├── signature/
│   └── kaito_leaderboard_2025-10-14_hash.txt
└── README.md
```

* `snapshot/` contains the raw JSON data from Kaito’s API.
* `signature/` contains the SHA256 hash of the JSON file for integrity verification.
* Each file is named by date using the format `kaito_leaderboard_YYYY-MM-DD.json`.
* Each upload represents a single leaderboard snapshot.

---

## File Descriptions

### `snapshot/kaito_leaderboard_2025-10-14.json`

Official leaderboard data as returned by the Kaito API for the week of **October 7–14, 2025**.
Includes Community and Creator leaderboards and all relevant engagement metrics.

**Example structure (illustrative):**

```json
{
  "timestamp": "2025-10-14T18:00:00Z",
  "source": "kaito_api_v1",
  "leaderboards": {
    "community": [
      {
        "rank": 1,
        "username": "@alpha",
        "impressions": 12450,
        "likes": 890,
        "engagement_rate": 7.15,
        "crystals_awarded": 350
      }
    ],
    "creator": [
      {
        "rank": 1,
        "username": "@beta",
        "impressions": 15600,
        "likes": 1040,
        "engagement_rate": 6.67,
        "crystals_awarded": 370
      }
    ]
  }
}
```

### `signature/kaito_leaderboard_2025-10-14_hash.txt`

SHA256 checksum of the JSON file for verification.

---

## Verification and Authenticity

* The JSON file was generated directly from the Kaito API response.
* No post-processing, filtering, or manual edits were made.
* File integrity can be verified using the SHA256 checksum below.

**SHA256 Checksum**

```
sha256(kaito_leaderboard_2025-10-14.json)= <insert-checksum-here>
```

**Verify locally**

```bash
shasum -a 256 snapshot/kaito_leaderboard_2025-10-14.json
```

---

## Update Policy

* **Update Frequency:** Weekly (every Tuesday)
* **Next Update:** 2025-10-21
* **Last Updated:** 2025-10-14

All previous snapshots will remain permanently accessible for audit and comparison.

---

## Transparency Note

This repository is part of Multipli’s ongoing effort to maintain open and verifiable data practices.
By publishing the unaltered Kaito leaderboard data, we aim to provide the community with clear insight into leaderboard activity, Crystal emissions, and engagement distribution.
