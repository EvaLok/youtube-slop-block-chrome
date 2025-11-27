# youtube-slop-block-chrome
blocks the slop on youtube, for the Chrome web browser

# Privacy Policy for YouTube Slop Block

**Last Updated: November 27, 2025**

## Overview

YouTube Slop Block is an open-source Chrome extension for transparent content filtering and recommendations on YouTube. This privacy policy explains how the extension collects, uses, and shares user data.

## Data We Collect

### 1. User Identifier
- **What:** A randomly generated UUID (anonymous identifier)
- **How:** Generated locally on first install and stored in Chrome sync storage
- **Purpose:** To associate your content ratings with your account across devices
- **Note:** This ID is not linked to any personal information like name or email

### 2. Authentication Data (Optional)
- **What:** Email address and authentication tokens when you sign in
- **How:** Collected when you voluntarily log in via email/password or Google OAuth
- **Purpose:** To authenticate API requests and sync your ratings
- **Storage:** Auth tokens are stored locally in Chrome storage

### 3. Video Rating Data
- **What:** YouTube video IDs, channel IDs, and your rating (slop/clean)
- **How:** Collected when you rate a video using the extension
- **Purpose:** To record your content preferences and contribute to community ratings
- **Storage:** Cached locally in IndexedDB; synced to our server when authenticated

### 4. Aggregate Channel Statistics
- **What:** Per-channel counts of videos you've rated as slop or clean
- **How:** Calculated from your individual ratings
- **Purpose:** To help identify channels with content you may want to filter
- **Storage:** Stored locally in IndexedDB

## How We Use Your Data

- **Content Filtering:** Display slop ratings on YouTube thumbnails based on community votes
- **Personalization:** Track your individual rating preferences locally
- **Community Ratings:** Aggregate anonymous ratings to help other users identify low-quality content
- **Authentication:** Verify your identity when submitting ratings to the server

## Third Parties We Share Data With

| Party | Data Shared | Purpose |
|-------|-------------|---------|
| **Supabase** (supabase.co) | Auth tokens, video ratings (video ID, channel ID, slop/clean status) | Backend database and authentication services |
| **Google** (via Chrome Identity API) | Email (only during OAuth login) | Optional Google Sign-In authentication |

**We do not sell, rent, or share your data with any other third parties.**

## Data Storage Locations

- **Local (Your Device):**
  - Anonymous user ID (Chrome sync storage)
  - Auth tokens (Chrome local storage)
  - Video ratings cache (IndexedDB)
  - Channel statistics (IndexedDB)

- **Remote (Our Servers via Supabase):**
  - Your email (if you created an account)
  - Video ratings you submit
  - Aggregated community statistics

## Data Retention

- **Local Data:** Persists until you uninstall the extension or clear browser data
- **Server Data:** Retained indefinitely to maintain community ratings; you may request deletion by contacting us

## Your Rights

- **Access:** View your local data via browser developer tools
- **Delete Local Data:** Uninstall the extension or clear extension data in Chrome settings
- **Delete Server Data:** Contact us to request deletion of your account and associated ratings
- **Opt Out:** Use the extension without signing in (ratings will only be stored locally)

## Security

- All API communications use HTTPS encryption
- Authentication uses industry-standard OAuth 2.0 (via Supabase)
- No sensitive data (passwords) is stored by the extension

## Permissions Explained

| Permission | Why We Need It |
|------------|----------------|
| `storage` | Store your ratings and preferences locally |
| `identity` | Enable Google Sign-In authentication |
| `alarms` | Periodically sync pending ratings to the server |
| `Host: youtube.com` | Display ratings on YouTube pages |
| `Host: supabase.co` | Communicate with our backend API |

## Changes to This Policy

We may update this privacy policy from time to time. Significant changes will be noted in extension update release notes.

## Contact

For privacy concerns or data deletion requests, please open an issue on our GitHub repository: https://github.com/EvaLok/youtube-slop-block-chrome


## Open Source

This extension is currently under early active development. It will be released once it's available to the general public (currently closed testing only)
