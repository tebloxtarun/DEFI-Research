In the database schema, several tables are interconnected through relationships defined by foreign keys (`Ref` references). These relationships facilitate data retrieval and maintain data integrity across different tables. Here's the communication or relationships between these tables based on the foreign key references:

### 1. Achievements and Achievement Tokens

- **Achievements (`achievements` table)**:
  - Identified by `id`.
  - Connected to `achievement_tokens` through `achievement_id`.

- **Achievement Tokens (`achievement_tokens` table)**:
  - Identified by `id`.
  - Contains `achievement_id` which references `achievements.id`.
  - This relationship allows associating multiple tokens with an achievement.

### 2. Active Storage Attachments and Blobs

- **Active Storage Blobs (`active_storage_blobs` table)**:
  - Identified by `id`.
  - Stores actual file contents (`key`, `filename`, `content_type`, etc.).

- **Active Storage Attachments (`active_storage_attachments` table)**:
  - Identified by `id`.
  - Uses `blob_id` to reference `active_storage_blobs.id`.
  - Links a specific file attachment (`name`, `record_type`, `record_id`) to its blob.

### 3. Comments

- **Comments (`comments` table)**:
  - Identified by `id`.
  - Contains `user_id`, `market_id`, and optional `parent_id` for nested comments.
  - Foreign keys:
    - `user_id` references `users.id`.
    - `market_id` references `markets.id`.
    - `parent_id` self-references `comments.id` for nested comments.

### 4. Likes

- **Likes (`likes` table)**:
  - Identified by `id`.
  - Links `likeable_type` and `likeable_id` to associate likes with various entities.
  - Foreign key:
    - `user_id` references `users.id` indicating which user liked the item.

### 5. Market Outcomes

- **Market Outcomes (`market_outcomes` table)**:
  - Identified by `id`.
  - Belongs to a specific `market_id` from the `markets` table.
  - Foreign key:
    - `market_id` references `markets.id`.

### 6. Reports

- **Reports (`reports` table)**:
  - Identified by `id`.
  - Associates `user_id` with the user who made the report (`users.id`).

### 7. Tournaments and Tournament Groups

- **Tournaments (`tournaments` table)**:
  - Identified by `id`.
  - Belongs to a `tournament_group_id` referencing `tournament_groups.id`.
  - Foreign key:
    - `tournament_group_id` references `tournament_groups.id`.

### 8. Activities

- **Activities (`activities` table)**:
  - Identified by `id`.
  - Tracks actions (`action`), amounts (`amount`), and other details related to a specific `market_id` from `markets`.

### 9. Eth Events and Queries

- **Eth Events (`eth_events` table)**:
  - Identified by `id`.
  - Stores Ethereum blockchain events (`event`, `address`, etc.).
  - Used in `eth_events_queries` to track related queries (`eth_event_id`).

- **Eth Queries (`eth_queries` table)**:
  - Identified by `id`.
  - Contains details about Ethereum blockchain queries (`contract_name`, `event`, `last_block_number`).
  - Used in `eth_events_queries` to associate with `eth_events`.
