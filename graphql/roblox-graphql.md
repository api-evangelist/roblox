# Roblox GraphQL Schema

Conceptual GraphQL schema for the Roblox platform, covering the Open Cloud API, Engine API, and the broader Roblox web surfaces (users, groups, games, economy, avatar, inventory, social, messaging, analytics, and data persistence).

## Source APIs

| Surface | Base URL | Auth |
|---------|----------|------|
| Open Cloud REST API | https://apis.roblox.com | API Key / OAuth 2.0 |
| Creator Hub Docs | https://create.roblox.com/docs/cloud/open-cloud | — |
| Engine API (Luau) | https://create.roblox.com/docs/reference/engine | In-engine only |
| Legacy Web APIs | https://*.roblox.com | Cookie / OAuth |

## Schema File

`roblox-schema.graphql`

## Type Coverage

The schema defines **70+ named types** across the following domains.

### User Domain
- `User` — core identity, presence, friend/group/inventory/badge edges
- `UserProfile` — extended bio and social links
- `UserPresence` — real-time status (online, in-game, in-studio, offline)
- `UserStatus` (enum) — presence state values
- `SocialLink` — external profile links

### Friend / Social Domain
- `Friend` — friend edge with presence
- `FriendRequest` — pending / accepted / declined requests
- `FollowingStatus` — bidirectional follow + friendship check
- `FriendConnection`, `FriendRequestConnection`

### Group Domain
- `Group` — community group with shout, roles, members, payout
- `GroupRole` — ranked role with full permission matrix
- `GroupRolePermissions`, `GroupPostsPermissions`, `GroupMembershipPermissions`, `GroupManagementPermissions`, `GroupEconomyPermissions`
- `GroupMember` — user + role association
- `GroupMembershipRequest` — join request awaiting approval
- `GroupPayoutRecipient` — Robux distribution percentages
- `GroupShout` — pinned group announcement

### Game / Universe / Place Domain
- `Game` — universe with metadata, playing count, visit stats, creator
- `GameMedia` — images and video attached to a game page
- `GameSettings` — private server pricing, region opt-in/out
- `GamePermission` — third-party teleport/asset/purchase flags
- `GameBadge` — badges awarded within a universe
- `Server` — running game server instance
- `PlaceUpdate` — published place version record

### DataStore Domain
- `DataStore` — named key-value store for an experience
- `DataStoreEntry` — versioned value with user-id tagging and attributes
- `OrderedDataStore` — sorted leaderboard-style store
- `OrderedDataStoreEntry` — key + integer value pair

### Messaging Domain
- `Message` — user inbox message
- `MessagingServiceMessage` — cross-server pub/sub payload

### Asset Domain
- `Asset` — uploadable creator content item (image, audio, model, etc.)
- `AssetVersion` — historical version of an asset
- `AssetOwner` — user or group that owns an asset
- `AssetType` (enum) — 60+ Roblox asset type identifiers
- `ModerationState` (enum) — content moderation status

### Badge Domain
- `Badge` — achievement definition
- `BadgeStatistics` — award rates and counts
- `BadgeAwarded` — badge grant record per user

### Bundle & GamePass Domain
- `Bundle` — avatar bundle grouping multiple items
- `BundleItem` — individual item within a bundle
- `GamePass` — per-game access pass
- `CatalogProduct` — sale metadata including premium pricing
- `PremiumPricing` — discounted price for Premium subscribers

### Economy / Currency / Premium Domain
- `Premium` — Premium Membership status per user
- `PremiumSubscription` — active subscription with renewal info
- `PremiumProduct` — Premium tier definition with Robux stipend
- `Currency` — Robux balance wrapper
- `Robux` — amount + owner reference
- `Subscription` — recurring subscription record
- `Transaction` — economy ledger entry
- `TransactionAgent` — buyer or seller side of a transaction
- `TransactionDetails` — item detail side of a transaction
- `DeveloperExchange` — Robux-to-cash exchange request
- `TransactionType` (enum) — purchase, sale, trade, DEX, subscription, etc.

### Creator Domain
- `Creator` — user or group acting as content creator
- `CreatorProfile` — extended creator bio and social presence

### Inventory Domain
- `InventoryItem` — item owned by a user (asset + collectible metadata)

### Trade Domain
- `Trade` — two-party item exchange proposal
- `TradeOffer` — one side of a trade (items + Robux)
- `TradeItem` — specific asset within a trade offer
- `TradeStatus` — current state of a trade record
- `TradeStatus` (enum) — open, pending, completed, declined, etc.

### Avatar Domain
- `Avatar` — full avatar state including body type, colors, scales, assets
- `AvatarScale` — six body proportion dimensions
- `AvatarColorsMap` — named BrickColor with RGB values
- `AvatarBodyColors` — six-zone color assignment
- `AvatarAsset` — equipped asset reference on an avatar
- `AvatarEmote` — emote animation slot assignment
- `UserAvatar` — user-to-avatar binding
- `UserOutfit` — saved avatar configuration
- `AvatarType` (enum) — R6 or R15 rig

### Thumbnail Domain
- `Thumbnail` — rendered image URL with state tracking
- `ThumbnailState` (enum) — completed, pending, error, blocked
- `Animation` — animation asset record

### Analytics / Stats Domain
- `UniverseStats` — visits, favorites, playing, likes, revenue
- `AnalyticsEvent` — event stream record for a universe

### Instance Domain
- `Instance` — Open Cloud Instances API object in the scene graph
- `InstanceDetails` — class name and property bag

### Shared / Pagination
- `PageInfo` — cursor-based pagination metadata
- `Creator` / `SocialLink` — shared cross-domain references

## Operations

### Queries (30+)
User lookup (by ID or username), presence, friend graph, groups, games, servers, assets, badges, bundles, game passes, avatar, outfits, inventory, trades, Robux balance, transactions, Premium status, data store entries, messages, universe stats, thumbnails, instances.

### Mutations (30+)
Friend requests (send/accept/decline/unfriend), follow/unfollow, group join/leave/approve/decline/role-change/shout, avatar updates, outfit CRUD, data store set/delete, ordered data store update/delete, messaging publish and send, place publish, trade send/accept/decline/counter.

### Subscriptions (4)
- `userPresenceUpdated` — real-time presence changes
- `messageReceived` — inbox push
- `analyticsEvent` — live event stream per universe
- `tradeStatusUpdated` — trade state transitions

## Authentication

| Operation type | Mechanism |
|---------------|-----------|
| Server-to-server (Open Cloud) | API Key (`x-api-key` header), scoped per resource |
| Third-party apps (OAuth 2.0) | Authorization Code + PKCE; access token as `Bearer` |
| In-engine scripts | Roblox runtime — no external auth |

## References

- Open Cloud API Reference: https://create.roblox.com/docs/cloud/reference
- Open Cloud Getting Started: https://create.roblox.com/docs/cloud/open-cloud
- Engine API Reference: https://create.roblox.com/docs/reference/engine
- Roblox GitHub Organization: https://github.com/Roblox
- Luau Language: https://luau.org
