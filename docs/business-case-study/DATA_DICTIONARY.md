# Supabase audit data dictionary

This companion catalogs all inspected databases and schemas, table/view/materialized-view structure, exact base-table snapshot counts, available timestamp ranges, application constraints/indexes/functions and triggers. Non-application function signatures are summarized by schema because extensions contain hundreds of standard functions; their names do not establish application business use. No function body, credential record, customer value, recorded conversation, or row-level authorization expression containing identifiers is published. Row counts are raw relation counts, never a sum of unique business events. Catalog metadata and payload snapshots were taken separately. Empty/no-business databases remain inventoried.

## vk-realty / _supabase

Schemas: `_analytics`, `_supavisor`, `public`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| _supavisor.cluster_tenants | table | 0 | False |
| _supavisor.clusters | table | 0 | False |
| _supavisor.schema_migrations | table | 22 | False |
| _supavisor.tenants | table | 1 | False |
| _supavisor.users | table | 1 | False |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |

## vk-realty / postgres

Schemas: `_realtime`, `auth`, `extensions`, `graphql`, `graphql_public`, `net`, `public`, `realtime`, `storage`, `supabase_functions`, `vault`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| _realtime.extensions | table | 1 | False |
| _realtime.feature_flags | table | 1 | False |
| _realtime.schema_migrations | table | 33 | False |
| _realtime.tenants | table | 1 | False |
| auth.audit_log_entries | table | 0 | True |
| auth.custom_oauth_providers | table | 0 | False |
| auth.flow_state | table | 0 | True |
| auth.identities | table | 0 | True |
| auth.instances | table | 0 | True |
| auth.mfa_amr_claims | table | 0 | True |
| auth.mfa_challenges | table | 0 | True |
| auth.mfa_factors | table | 0 | True |
| auth.oauth_authorizations | table | 0 | False |
| auth.oauth_client_states | table | 0 | False |
| auth.oauth_clients | table | 0 | False |
| auth.oauth_consents | table | 0 | False |
| auth.one_time_tokens | table | 0 | True |
| auth.refresh_tokens | table | 0 | True |
| auth.saml_providers | table | 0 | True |
| auth.saml_relay_states | table | 0 | True |
| auth.schema_migrations | table | 77 | True |
| auth.sessions | table | 0 | True |
| auth.sso_domains | table | 0 | True |
| auth.sso_providers | table | 0 | True |
| auth.users | table | 0 | True |
| auth.webauthn_challenges | table | 0 | False |
| auth.webauthn_credentials | table | 0 | False |
| extensions.pg_stat_statements | view (not counted) | N/A | False |
| extensions.pg_stat_statements_info | view (not counted) | N/A | False |
| net._http_response | table | 0 | False |
| net.http_request_queue | table | 0 | False |
| public.active_calls | table | 65 | True |
| public.agent_knowledge_assignments | table | 0 | True |
| public.agent_knowledge_files | table | 0 | True |
| public.agents | table | 1 | True |
| public.api_tokens | table | 0 | True |
| public.app_kv_store | table | 0 | True |
| public.app_settings | table | 3 | True |
| public.audit_log | table | 182 | True |
| public.calendar_bookings | table | 0 | True |
| public.call_configurations | table | 1 | True |
| public.call_listing_mentions | table | 0 | True |
| public.call_logs | table | 79 | True |
| public.call_transcripts | table | 793 | True |
| public.campaign_listings | table | 0 | True |
| public.campaign_numbers | table | 0 | True |
| public.conversational_flows | table | 1 | True |
| public.crm_sync_log | table | 0 | True |
| public.invitations | table | 0 | True |
| public.knowledge_documents | table | 0 | True |
| public.lead_actions | table | 0 | True |
| public.lead_objections | table | 0 | True |
| public.lead_property_signals | table | 0 | True |
| public.leads | table | 0 | True |
| public.listings | table | 3 | True |
| public.memberships | table | 1 | True |
| public.mfa_factors | table | 0 | True |
| public.mfa_recovery_codes | table | 0 | True |
| public.organizations | table | 1 | True |
| public.outbound_campaigns | table | 0 | True |
| public.password_resets | table | 0 | True |
| public.pin_to_pim_mappings | table | 3 | True |
| public.post_call_actions | table | 1 | True |
| public.post_call_deliveries | table | 0 | True |
| public.sessions | table | 182 | True |
| public.users | table | 1 | True |
| public.v_pin_pim_resolved | view (not counted) | N/A | False |
| public.whatsapp_conversations | table | 0 | True |
| public.whatsapp_messages | table | 0 | True |
| public.whatsapp_sessions | table | 0 | True |
| realtime.messages | partitioned table | 0 | True |
| realtime.messages_2026_10_27 | table | 0 | False |
| realtime.messages_2026_10_28 | table | 0 | False |
| realtime.messages_2026_10_29 | table | 0 | False |
| realtime.messages_2026_10_30 | table | 0 | False |
| realtime.messages_2026_10_31 | table | 0 | False |
| realtime.schema_migrations | table | 82 | False |
| realtime.subscription | table | 0 | False |
| storage.buckets | table | 2 | True |
| storage.buckets_analytics | table | 0 | True |
| storage.buckets_vectors | table | 0 | True |
| storage.iceberg_namespaces | table | 0 | True |
| storage.iceberg_tables | table | 0 | True |
| storage.migrations | table | 70 | True |
| storage.objects | table | 65 | True |
| storage.s3_multipart_uploads | table | 0 | True |
| storage.s3_multipart_uploads_parts | table | 0 | True |
| storage.vector_indexes | table | 0 | True |
| supabase_functions.hooks | table | 0 | False |
| supabase_functions.migrations | table | 2 | False |
| vault.decrypted_secrets | view (not counted) | N/A | False |
| vault.secrets | table | 0 | False |

### public.active_calls

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| room_id | text | NO |
| phone | text | YES |
| caller_name | text | YES |
| status | text | NO |
| agent_id | uuid | YES |
| campaign_id | uuid | YES |
| from_number | text | YES |
| to_number | text | YES |
| started_at | timestamp with time zone | NO |
| last_updated | timestamp with time zone | NO |
| metadata | jsonb | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| started_at | 2026-09-17T05:22:14.111274+00:00 | 2026-11-04T13:26:25.260707+00:00 | 65 |
| last_updated | 2026-09-17T05:22:57.544258+00:00 | 2026-11-04T13:27:58.03184+00:00 | 65 |

### public.agent_knowledge_assignments

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| document_id | text | NO |
| knowledge_data_path | text | YES |
| config_preset | text | YES |
| loaded_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| loaded_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.agent_knowledge_files

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| file_name | text | NO |
| file_path | text | YES |
| storage_path | text | YES |
| file_size | bigint | YES |
| mime_type | text | YES |
| config_preset | text | YES |
| search_enabled | boolean | NO |
| status | text | NO |
| metadata | jsonb | NO |
| added_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| added_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.agents

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| description | text | YES |
| purpose | text | YES |
| system_prompt | text | NO |
| languages | jsonb | NO |
| llm_provider | text | NO |
| llm_model | text | NO |
| temperature | numeric | NO |
| stt_provider | text | NO |
| stt_model | text | YES |
| tts_provider | text | NO |
| tts_voice_id | text | NO |
| welcome_message | text | YES |
| max_call_duration_seconds | integer | NO |
| is_active | boolean | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| metadata | jsonb | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.264554+00:00 | 2026-09-16T19:53:34.264554+00:00 | 1 |
| updated_at | 2026-09-16T20:31:18.819488+00:00 | 2026-09-16T20:31:18.819488+00:00 | 1 |

### public.api_tokens

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| token_hash | text | NO |
| scopes | ARRAY | NO |
| org_id | uuid | NO |
| created_by | uuid | YES |
| expires_at | timestamp with time zone | YES |
| last_used_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| last_used_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.app_kv_store

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| key | text | NO |
| value | jsonb | NO |
| expires_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.app_settings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| key | text | NO |
| value | jsonb | NO |
| description | text | YES |
| updated_at | timestamp with time zone | NO |
| updated_by | text | YES |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| updated_at | 2026-09-16T19:53:34.277936+00:00 | 2026-09-17T05:10:32.637647+00:00 | 3 |

### public.audit_log

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| actor_user_id | uuid | YES |
| org_id | uuid | YES |
| action | text | NO |
| resource_type | text | YES |
| resource_id | text | YES |
| before | jsonb | YES |
| after | jsonb | YES |
| ip | text | YES |
| user_agent | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-17T05:11:40.215157+00:00 | 2026-11-04T11:45:49.734055+00:00 | 182 |

### public.calendar_bookings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | bigint | YES |
| lead_id | uuid | YES |
| phone | text | NO |
| listing_id | text | YES |
| scheduled_at | timestamp with time zone | NO |
| provider | text | NO |
| external_id | text | YES |
| status | text | NO |
| notes | text | YES |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| scheduled_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.call_configurations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| silence_handling | jsonb | NO |
| end_call_rules | jsonb | NO |
| transfer_routing | jsonb | NO |
| response_behavior | jsonb | NO |
| ambient_sound | jsonb | NO |
| advanced_settings | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.268294+00:00 | 2026-09-16T19:53:34.268294+00:00 | 1 |
| updated_at | 2026-09-16T19:53:34.268294+00:00 | 2026-09-16T19:53:34.268294+00:00 | 1 |

### public.call_listing_mentions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | bigint | NO |
| listing_id | text | NO |
| mention_type | text | NO |
| pin_used | text | YES |
| context | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.call_logs

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | bigint | NO |
| created_at | timestamp with time zone | NO |
| phone_number | text | YES |
| caller_phone | text | YES |
| caller_name | text | YES |
| caller_email | text | YES |
| duration_seconds | integer | YES |
| transcript | text | YES |
| summary | text | YES |
| recording_url | text | YES |
| sentiment | text | YES |
| estimated_cost_usd | numeric | YES |
| call_date | date | YES |
| call_hour | integer | YES |
| call_day_of_week | text | YES |
| was_booked | boolean | NO |
| interrupt_count | integer | NO |
| audio_codec | text | YES |
| call_purpose | text | YES |
| call_summary | text | YES |
| appointment_time | timestamp with time zone | YES |
| tts_voice | text | YES |
| agent_id | uuid | YES |
| call_status | text | NO |
| call_direction | text | NO |
| channel_type | text | NO |
| call_transferred | boolean | NO |
| ended_by | text | YES |
| room_id | text | YES |
| from_number | text | YES |
| to_number | text | YES |
| bulk_call_id | uuid | YES |
| extracted_info | jsonb | NO |
| ai_summary | jsonb | YES |
| migrated_to_re_memory | boolean | YES |
| metadata | jsonb | NO |
| org_id | uuid | YES |
| turn_metrics | jsonb | YES |
| config_hash | text | YES |
| felt_latency_p50_ms | integer | YES |
| felt_latency_p95_ms | integer | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-17T05:11:40.242331+00:00 | 2026-11-04T13:27:54.098292+00:00 | 79 |
| call_date | 2026-09-17 | 2026-11-04 | 55 |
| appointment_time | N/A | N/A | 0 |

### public.call_transcripts

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_room_id | text | NO |
| call_id | bigint | YES |
| phone | text | YES |
| role | text | YES |
| content | text | YES |
| sequence_num | integer | YES |
| created_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-17T05:18:48.091332+00:00 | 2026-11-04T13:27:50.315797+00:00 | 793 |

### public.campaign_listings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| campaign_id | uuid | NO |
| listing_id | text | NO |
| sort_order | integer | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.campaign_numbers

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| campaign_id | uuid | NO |
| phone | text | NO |
| status | text | NO |
| dispatch_id | text | YES |
| error_message | text | YES |
| call_log_id | bigint | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.conversational_flows

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| sections | jsonb | NO |
| version | integer | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.266654+00:00 | 2026-09-16T19:53:34.266654+00:00 | 1 |
| updated_at | 2026-09-16T19:53:34.266654+00:00 | 2026-09-16T19:53:34.266654+00:00 | 1 |

### public.crm_sync_log

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | YES |
| phone | text | YES |
| call_id | bigint | YES |
| crm_type | text | NO |
| action | text | NO |
| status | text | NO |
| request_payload | jsonb | NO |
| response_payload | jsonb | YES |
| error_message | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.invitations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| token_hash | text | NO |
| email | USER-DEFINED | NO |
| org_id | uuid | NO |
| role | text | NO |
| invited_by | uuid | YES |
| expires_at | timestamp with time zone | NO |
| accepted_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| accepted_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.knowledge_documents

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| document_id | text | NO |
| doc_type | text | NO |
| title | text | NO |
| content | text | NO |
| department | text | YES |
| language | text | NO |
| tags | jsonb | NO |
| metadata | jsonb | NO |
| embedding_id | text | YES |
| is_active | boolean | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.lead_actions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | text | NO |
| call_log_id | bigint | YES |
| lead_id | uuid | YES |
| action | text | NO |
| performed_at | timestamp with time zone | NO |
| performed_by | text | YES |
| notes | text | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| performed_at | N/A | N/A | 0 |

### public.lead_objections

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | NO |
| phone | text | NO |
| objection_type | text | NO |
| listing_id | text | YES |
| raw_phrase | text | NO |
| script_used | text | NO |
| outcome | text | NO |
| call_id | bigint | YES |
| call_count_at_time | integer | NO |
| call_date | timestamp with time zone | NO |
| created_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| call_date | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.lead_property_signals

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | NO |
| phone | text | NO |
| listing_id | text | NO |
| signal | text | NO |
| price_reaction | text | NO |
| features_liked | jsonb | NO |
| objections_raised | jsonb | NO |
| price_at_signal | integer | YES |
| call_id | bigint | YES |
| call_date | timestamp with time zone | NO |
| created_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| call_date | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.leads

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | NO |
| phone | text | NO |
| stable_name | text | NO |
| role | text | NO |
| budget_min | integer | YES |
| budget_max | integer | YES |
| preferred_areas | jsonb | NO |
| excluded_areas | jsonb | NO |
| must_haves | jsonb | NO |
| deal_breakers | jsonb | NO |
| timeline_weeks | integer | YES |
| loan_status | text | NO |
| decision_factors | jsonb | NO |
| intent_score | numeric | NO |
| deal_stage | text | NO |
| assigned_agent | text | YES |
| assigned_agent_id | uuid | YES |
| call_count | integer | NO |
| last_contact_at | timestamp with time zone | YES |
| language_pref | text | NO |
| notes | text | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| last_contact_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.listings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| listing_id | text | NO |
| pim_sku | text | YES |
| title | text | NO |
| area | text | YES |
| city | text | YES |
| property_type | text | YES |
| bedrooms | integer | YES |
| bathrooms | integer | YES |
| sqft_min | integer | YES |
| sqft_max | integer | YES |
| price_min | bigint | YES |
| price_max | bigint | YES |
| currency | text | NO |
| status | text | NO |
| facts | jsonb | NO |
| amenities | jsonb | NO |
| tags | ARRAY | NO |
| source | text | YES |
| external_url | text | YES |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.27421+00:00 | 2026-09-16T19:53:34.27421+00:00 | 3 |
| updated_at | 2026-09-16T19:53:35.252819+00:00 | 2026-09-16T19:53:35.252819+00:00 | 3 |

### public.memberships

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| org_id | uuid | NO |
| role | text | NO |
| status | text | NO |
| invited_by | uuid | YES |
| joined_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| joined_at | N/A | N/A | 0 |
| created_at | 2026-09-17T04:22:18.798374+00:00 | 2026-09-17T04:22:18.798374+00:00 | 1 |
| updated_at | 2026-09-17T04:22:18.798374+00:00 | 2026-09-17T04:22:18.798374+00:00 | 1 |

### public.mfa_factors

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| type | text | NO |
| secret_encrypted | text | NO |
| confirmed_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| confirmed_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.mfa_recovery_codes

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| code_hash | text | NO |
| used_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| used_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.organizations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| slug | text | NO |
| status | text | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.666616+00:00 | 2026-09-16T19:53:34.666616+00:00 | 1 |
| updated_at | 2026-09-16T19:53:34.666616+00:00 | 2026-09-16T19:53:34.666616+00:00 | 1 |

### public.outbound_campaigns

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| agent_id | uuid | YES |
| status | text | NO |
| delay_seconds | integer | NO |
| max_concurrent | integer | NO |
| window_start | text | NO |
| window_end | text | NO |
| timezone | text | NO |
| respect_window | boolean | NO |
| total_numbers | integer | NO |
| dispatched | integer | NO |
| succeeded | integer | NO |
| failed | integer | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| started_at | timestamp with time zone | YES |
| completed_at | timestamp with time zone | YES |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |
| started_at | N/A | N/A | 0 |
| completed_at | N/A | N/A | 0 |

### public.password_resets

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| token_hash | text | NO |
| expires_at | timestamp with time zone | NO |
| used_at | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| used_at | N/A | N/A | 0 |

### public.pin_to_pim_mappings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| pin | text | NO |
| pim_listing_id | text | NO |
| source | text | NO |
| label | text | YES |
| description | text | YES |
| is_active | boolean | NO |
| priority | integer | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.276168+00:00 | 2026-09-16T19:53:34.276168+00:00 | 3 |
| updated_at | 2026-09-16T19:53:34.276168+00:00 | 2026-09-16T19:53:34.276168+00:00 | 3 |

### public.post_call_actions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| delivery_method | text | NO |
| trigger_statuses | jsonb | NO |
| include_summary | boolean | NO |
| include_full_transcript | boolean | NO |
| include_sentiment | boolean | NO |
| include_extracted_info | boolean | NO |
| extracted_variables | jsonb | NO |
| webhook_url | text | YES |
| webhook_headers | jsonb | NO |
| email_recipients | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-16T19:53:34.271987+00:00 | 2026-09-16T19:53:34.271987+00:00 | 1 |
| updated_at | 2026-09-16T19:53:34.271987+00:00 | 2026-09-16T19:53:34.271987+00:00 | 1 |

### public.post_call_deliveries

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | bigint | NO |
| agent_id | uuid | YES |
| delivery_method | text | NO |
| destination | text | YES |
| status | text | NO |
| http_status | integer | YES |
| response_body | text | YES |
| payload | jsonb | NO |
| error_message | text | YES |
| created_at | timestamp with time zone | NO |
| delivered_at | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| delivered_at | N/A | N/A | 0 |

### public.sessions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| org_id | uuid | YES |
| refresh_token_hash | text | NO |
| user_agent | text | YES |
| ip | text | YES |
| created_at | timestamp with time zone | NO |
| last_seen_at | timestamp with time zone | NO |
| revoked_at | timestamp with time zone | YES |
| expires_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-17T05:11:40.210546+00:00 | 2026-11-04T11:45:49.729761+00:00 | 182 |
| last_seen_at | 2026-09-17T05:11:40.209532+00:00 | 2026-11-04T11:45:49.728713+00:00 | 182 |
| revoked_at | 2026-09-18T13:27:01.42359+00:00 | 2026-11-02T15:06:30.105094+00:00 | 113 |
| expires_at | 2026-10-17T05:11:40.209532+00:00 | 2026-12-04T11:45:49.728713+00:00 | 182 |

### public.users

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| email | USER-DEFINED | NO |
| password_hash | text | NO |
| display_name | text | YES |
| avatar_url | text | YES |
| status | text | NO |
| email_verified_at | timestamp with time zone | YES |
| last_login_at | timestamp with time zone | YES |
| failed_login_count | integer | NO |
| locked_until | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| email_verified_at | N/A | N/A | 0 |
| last_login_at | N/A | N/A | 0 |
| locked_until | N/A | N/A | 0 |
| created_at | 2026-09-17T04:22:18.791214+00:00 | 2026-09-17T04:22:18.791214+00:00 | 1 |
| updated_at | 2026-09-17T04:22:18.791214+00:00 | 2026-09-17T04:22:18.791214+00:00 | 1 |

### public.v_pin_pim_resolved

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| pin | text | YES |
| source | text | YES |
| label | text | YES |
| is_active | boolean | YES |
| listing_id | text | YES |
| pim_sku | text | YES |
| title | text | YES |
| area | text | YES |
| property_type | text | YES |
| bedrooms | integer | YES |
| price_min | bigint | YES |
| price_max | bigint | YES |
| facts | jsonb | YES |
| status | text | YES |

### public.whatsapp_conversations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| org_id | uuid | NO |
| whatsapp_number_id | uuid | NO |
| contact_number | text | NO |
| contact_name | text | YES |
| last_message_preview | text | YES |
| last_message_at | timestamp with time zone | YES |
| unread_count | integer | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| last_message_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.whatsapp_messages

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| conversation_id | uuid | NO |
| direction | text | NO |
| message_type | text | NO |
| content | text | YES |
| media_url | text | YES |
| sent_by | text | NO |
| status | text | NO |
| wa_message_id | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.whatsapp_sessions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| org_id | uuid | NO |
| phone_number | text | YES |
| creds_json | jsonb | NO |
| keys_json | jsonb | NO |
| status | text | NO |
| connected_at | timestamp with time zone | YES |
| expires_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| connected_at | N/A | N/A | 0 |
| expires_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |
| public.active_calls | active_calls_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.active_calls | active_calls_campaign_id_fkey | f | FOREIGN KEY (campaign_id) REFERENCES outbound_campaigns(id) ON DELETE SET NULL |
| public.active_calls | active_calls_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.active_calls | active_calls_pkey | p | PRIMARY KEY (room_id) |
| public.active_calls | active_calls_status_check | c | CHECK ((status = ANY (ARRAY['ringing'::text, 'active'::text, 'completed'::text, 'failed'::text]))) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_agent_id_document_id_key | u | UNIQUE (agent_id, document_id) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.agent_knowledge_assignments | agent_knowledge_assignments_document_id_fkey | f | FOREIGN KEY (document_id) REFERENCES knowledge_documents(document_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.agent_knowledge_assignments | agent_knowledge_assignments_pkey | p | PRIMARY KEY (id) |
| public.agent_knowledge_files | agent_knowledge_files_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.agent_knowledge_files | agent_knowledge_files_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.agent_knowledge_files | agent_knowledge_files_pkey | p | PRIMARY KEY (id) |
| public.agent_knowledge_files | agent_knowledge_files_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'processing'::text, 'indexed'::text, 'failed'::text]))) |
| public.agents | agents_max_call_duration_seconds_check | c | CHECK ((max_call_duration_seconds > 0)) |
| public.agents | agents_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.agents | agents_pkey | p | PRIMARY KEY (id) |
| public.agents | agents_temperature_check | c | CHECK (((temperature >= (0)::numeric) AND (temperature <= (2)::numeric))) |
| public.api_tokens | api_tokens_created_by_fkey | f | FOREIGN KEY (created_by) REFERENCES users(id) ON DELETE SET NULL |
| public.api_tokens | api_tokens_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.api_tokens | api_tokens_pkey | p | PRIMARY KEY (id) |
| public.api_tokens | api_tokens_token_hash_key | u | UNIQUE (token_hash) |
| public.app_kv_store | app_kv_store_pkey | p | PRIMARY KEY (key) |
| public.app_settings | app_settings_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.app_settings | app_settings_pkey | p | PRIMARY KEY (key) |
| public.audit_log | audit_log_actor_user_id_fkey | f | FOREIGN KEY (actor_user_id) REFERENCES users(id) ON DELETE SET NULL |
| public.audit_log | audit_log_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.audit_log | audit_log_pkey | p | PRIMARY KEY (id) |
| public.calendar_bookings | calendar_bookings_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_pkey | p | PRIMARY KEY (id) |
| public.calendar_bookings | calendar_bookings_provider_check | c | CHECK ((provider = ANY (ARRAY['cal.com'::text, 'google_calendar'::text, 'manual'::text]))) |
| public.calendar_bookings | calendar_bookings_status_check | c | CHECK ((status = ANY (ARRAY['scheduled'::text, 'confirmed'::text, 'cancelled'::text, 'completed'::text, 'no_show'::text]))) |
| public.call_configurations | call_configurations_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.call_configurations | call_configurations_agent_id_key | u | UNIQUE (agent_id) |
| public.call_configurations | call_configurations_pkey | p | PRIMARY KEY (id) |
| public.call_listing_mentions | call_listing_mentions_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE CASCADE |
| public.call_listing_mentions | call_listing_mentions_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.call_listing_mentions | call_listing_mentions_mention_type_check | c | CHECK ((mention_type = ANY (ARRAY['discussed'::text, 'sent'::text, 'viewed'::text, 'offered'::text, 'rejected'::text, 'booked'::text]))) |
| public.call_listing_mentions | call_listing_mentions_pkey | p | PRIMARY KEY (id) |
| public.call_logs | call_logs_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.call_logs | call_logs_bulk_call_id_fkey | f | FOREIGN KEY (bulk_call_id) REFERENCES outbound_campaigns(id) ON DELETE SET NULL |
| public.call_logs | call_logs_call_direction_check | c | CHECK ((call_direction = ANY (ARRAY['inbound'::text, 'outbound'::text]))) |
| public.call_logs | call_logs_call_hour_check | c | CHECK (((call_hour IS NULL) OR ((call_hour >= 0) AND (call_hour <= 23)))) |
| public.call_logs | call_logs_call_status_check | c | CHECK ((call_status = ANY (ARRAY['ringing'::text, 'active'::text, 'completed'::text, 'failed'::text, 'no_answer'::text, 'voicemail'::text, 'transferred'::text, 'booked'::text, 'archived'::text, 'cancelled'::text]))) |
| public.call_logs | call_logs_channel_type_check | c | CHECK ((channel_type = ANY (ARRAY['phone'::text, 'web'::text, 'sip'::text, 'whatsapp'::text]))) |
| public.call_logs | call_logs_ended_by_check | c | CHECK (((ended_by IS NULL) OR (ended_by = ANY (ARRAY['caller'::text, 'assistant'::text, 'system'::text, 'timeout'::text])))) |
| public.call_logs | call_logs_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.call_logs | call_logs_pkey | p | PRIMARY KEY (id) |
| public.call_logs | fk_call_logs_agent | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.call_logs | fk_call_logs_campaign | f | FOREIGN KEY (bulk_call_id) REFERENCES outbound_campaigns(id) ON DELETE SET NULL |
| public.call_transcripts | call_transcripts_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.call_transcripts | call_transcripts_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.call_transcripts | call_transcripts_pkey | p | PRIMARY KEY (id) |
| public.call_transcripts | call_transcripts_role_check | c | CHECK ((role = ANY (ARRAY['user'::text, 'assistant'::text]))) |
| public.campaign_listings | campaign_listings_campaign_id_fkey | f | FOREIGN KEY (campaign_id) REFERENCES outbound_campaigns(id) ON DELETE CASCADE |
| public.campaign_listings | campaign_listings_campaign_id_listing_id_key | u | UNIQUE (campaign_id, listing_id) |
| public.campaign_listings | campaign_listings_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.campaign_listings | campaign_listings_pkey | p | PRIMARY KEY (id) |
| public.campaign_numbers | campaign_numbers_campaign_id_fkey | f | FOREIGN KEY (campaign_id) REFERENCES outbound_campaigns(id) ON DELETE CASCADE |
| public.campaign_numbers | campaign_numbers_campaign_id_phone_key | u | UNIQUE (campaign_id, phone) |
| public.campaign_numbers | campaign_numbers_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.campaign_numbers | campaign_numbers_pkey | p | PRIMARY KEY (id) |
| public.campaign_numbers | campaign_numbers_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'dispatched'::text, 'completed'::text, 'failed'::text, 'skipped'::text]))) |
| public.conversational_flows | conversational_flows_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.conversational_flows | conversational_flows_agent_id_key | u | UNIQUE (agent_id) |
| public.conversational_flows | conversational_flows_pkey | p | PRIMARY KEY (id) |
| public.conversational_flows | conversational_flows_version_check | c | CHECK ((version >= 1)) |
| public.crm_sync_log | crm_sync_log_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.crm_sync_log | crm_sync_log_crm_type_check | c | CHECK ((crm_type = ANY (ARRAY['hubspot'::text, 'salesforce'::text, 'webhook'::text, 'none'::text]))) |
| public.crm_sync_log | crm_sync_log_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE SET NULL |
| public.crm_sync_log | crm_sync_log_pkey | p | PRIMARY KEY (id) |
| public.crm_sync_log | crm_sync_log_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'success'::text, 'failed'::text]))) |
| public.invitations | invitations_email_org_id_accepted_at_key | u | UNIQUE (email, org_id, accepted_at) |
| public.invitations | invitations_invited_by_fkey | f | FOREIGN KEY (invited_by) REFERENCES users(id) ON DELETE SET NULL |
| public.invitations | invitations_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.invitations | invitations_pkey | p | PRIMARY KEY (id) |
| public.invitations | invitations_role_check | c | CHECK ((role = ANY (ARRAY['admin'::text, 'member'::text, 'viewer'::text]))) |
| public.invitations | invitations_token_hash_key | u | UNIQUE (token_hash) |
| public.knowledge_documents | knowledge_documents_doc_type_check | c | CHECK ((doc_type = ANY (ARRAY['company_info'::text, 'office_info'::text, 'property_listing'::text, 'faq'::text, 'process'::text, 'policy'::text, 'script'::text, 'other'::text]))) |
| public.knowledge_documents | knowledge_documents_document_id_key | u | UNIQUE (document_id) |
| public.knowledge_documents | knowledge_documents_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.knowledge_documents | knowledge_documents_pkey | p | PRIMARY KEY (id) |
| public.lead_actions | lead_actions_action_check | c | CHECK ((action = ANY (ARRAY['send_whatsapp'::text, 'schedule_site_visit'::text, 'mark_booked'::text, 'escalate_human'::text, 'archive'::text]))) |
| public.lead_actions | lead_actions_call_log_id_fkey | f | FOREIGN KEY (call_log_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.lead_actions | lead_actions_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE SET NULL |
| public.lead_actions | lead_actions_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.lead_actions | lead_actions_pkey | p | PRIMARY KEY (id) |
| public.lead_objections | lead_objections_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.lead_objections | lead_objections_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE CASCADE |
| public.lead_objections | lead_objections_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE SET NULL |
| public.lead_objections | lead_objections_objection_type_check | c | CHECK ((objection_type = ANY (ARRAY['price'::text, 'location'::text, 'size'::text, 'amenity'::text, 'timing'::text, 'agent_trust'::text, 'process'::text, 'other'::text]))) |
| public.lead_objections | lead_objections_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.lead_objections | lead_objections_outcome_check | c | CHECK ((outcome = ANY (ARRAY['resolved'::text, 'unresolved'::text, 'escalated'::text, 'deferred'::text]))) |
| public.lead_objections | lead_objections_pkey | p | PRIMARY KEY (id) |
| public.lead_property_signals | lead_property_signals_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.lead_property_signals | lead_property_signals_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE CASCADE |
| public.lead_property_signals | lead_property_signals_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.lead_property_signals | lead_property_signals_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.lead_property_signals | lead_property_signals_pkey | p | PRIMARY KEY (id) |
| public.lead_property_signals | lead_property_signals_price_reaction_check | c | CHECK ((price_reaction = ANY (ARRAY['positive'::text, 'negative'::text, 'neutral'::text, 'no_reaction'::text]))) |
| public.lead_property_signals | lead_property_signals_signal_check | c | CHECK ((signal = ANY (ARRAY['liked'::text, 'rejected'::text, 'viewed'::text, 'offered'::text, 'sent'::text, 'enquired'::text]))) |
| public.leads | leads_assigned_agent_id_fkey | f | FOREIGN KEY (assigned_agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.leads | leads_deal_stage_check | c | CHECK ((deal_stage = ANY (ARRAY['cold'::text, 'aware'::text, 'interested'::text, 'viewing'::text, 'hot'::text, 'offer'::text, 'closed'::text, 'lost'::text]))) |
| public.leads | leads_language_pref_check | c | CHECK ((language_pref = ANY (ARRAY['en'::text, 'hi'::text, 'hinglish'::text, 'tamil'::text, 'telugu'::text]))) |
| public.leads | leads_lead_id_key | u | UNIQUE (lead_id) |
| public.leads | leads_loan_status_check | c | CHECK ((loan_status = ANY (ARRAY['pre_approved'::text, 'exploring'::text, 'cash'::text, 'unknown'::text]))) |
| public.leads | leads_phone_key | u | UNIQUE (phone) |
| public.leads | leads_pkey | p | PRIMARY KEY (id) |
| public.leads | leads_role_check | c | CHECK ((role = ANY (ARRAY['buyer'::text, 'seller'::text, 'renter'::text, 'investor'::text]))) |
| public.listings | listings_listing_id_key | u | UNIQUE (listing_id) |
| public.listings | listings_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.listings | listings_pim_sku_key | u | UNIQUE (pim_sku) |
| public.listings | listings_pkey | p | PRIMARY KEY (id) |
| public.listings | listings_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'reserved'::text, 'sold'::text, 'inactive'::text, 'draft'::text]))) |
| public.memberships | memberships_invited_by_fkey | f | FOREIGN KEY (invited_by) REFERENCES users(id) ON DELETE SET NULL |
| public.memberships | memberships_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.memberships | memberships_pkey | p | PRIMARY KEY (id) |
| public.memberships | memberships_role_check | c | CHECK ((role = ANY (ARRAY['owner'::text, 'admin'::text, 'member'::text, 'viewer'::text]))) |
| public.memberships | memberships_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'suspended'::text]))) |
| public.memberships | memberships_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.memberships | memberships_user_id_org_id_key | u | UNIQUE (user_id, org_id) |
| public.mfa_factors | mfa_factors_pkey | p | PRIMARY KEY (id) |
| public.mfa_factors | mfa_factors_type_check | c | CHECK ((type = 'totp'::text)) |
| public.mfa_factors | mfa_factors_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.mfa_factors | mfa_factors_user_id_type_key | u | UNIQUE (user_id, type) |
| public.mfa_recovery_codes | mfa_recovery_codes_pkey | p | PRIMARY KEY (id) |
| public.mfa_recovery_codes | mfa_recovery_codes_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.organizations | organizations_pkey | p | PRIMARY KEY (id) |
| public.organizations | organizations_slug_key | u | UNIQUE (slug) |
| public.organizations | organizations_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'suspended'::text, 'archived'::text]))) |
| public.outbound_campaigns | outbound_campaigns_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.outbound_campaigns | outbound_campaigns_delay_seconds_check | c | CHECK (((delay_seconds >= 0) AND (delay_seconds <= 120))) |
| public.outbound_campaigns | outbound_campaigns_max_concurrent_check | c | CHECK ((max_concurrent >= 1)) |
| public.outbound_campaigns | outbound_campaigns_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.outbound_campaigns | outbound_campaigns_pkey | p | PRIMARY KEY (id) |
| public.outbound_campaigns | outbound_campaigns_status_check | c | CHECK ((status = ANY (ARRAY['draft'::text, 'running'::text, 'paused'::text, 'completed'::text, 'cancelled'::text]))) |
| public.password_resets | password_resets_pkey | p | PRIMARY KEY (id) |
| public.password_resets | password_resets_token_hash_key | u | UNIQUE (token_hash) |
| public.password_resets | password_resets_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pim_listing_id_fkey | f | FOREIGN KEY (pim_listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pin_source_key | u | UNIQUE (pin, source) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pkey | p | PRIMARY KEY (id) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_source_check | c | CHECK ((source = ANY (ARRAY['manual'::text, 'ivr'::text, 'builder_portal'::text, 'crm'::text, 'csv_import'::text, 'api'::text]))) |
| public.post_call_actions | post_call_actions_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.post_call_actions | post_call_actions_agent_id_key | u | UNIQUE (agent_id) |
| public.post_call_actions | post_call_actions_delivery_method_check | c | CHECK ((delivery_method = ANY (ARRAY['webhook'::text, 'email'::text, 'both'::text, 'none'::text]))) |
| public.post_call_actions | post_call_actions_pkey | p | PRIMARY KEY (id) |
| public.post_call_deliveries | post_call_deliveries_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.post_call_deliveries | post_call_deliveries_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE CASCADE |
| public.post_call_deliveries | post_call_deliveries_pkey | p | PRIMARY KEY (id) |
| public.post_call_deliveries | post_call_deliveries_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'sent'::text, 'failed'::text, 'skipped'::text]))) |
| public.sessions | sessions_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.sessions | sessions_pkey | p | PRIMARY KEY (id) |
| public.sessions | sessions_refresh_token_hash_key | u | UNIQUE (refresh_token_hash) |
| public.sessions | sessions_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.users | users_email_key | u | UNIQUE (email) |
| public.users | users_pkey | p | PRIMARY KEY (id) |
| public.users | users_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'invited'::text, 'suspended'::text, 'deleted'::text]))) |
| public.whatsapp_conversations | whatsapp_conversations_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.whatsapp_conversations | whatsapp_conversations_pkey | p | PRIMARY KEY (id) |
| public.whatsapp_conversations | whatsapp_conversations_unread_count_check | c | CHECK ((unread_count >= 0)) |
| public.whatsapp_conversations | whatsapp_conversations_whatsapp_number_id_contact_number_key | u | UNIQUE (whatsapp_number_id, contact_number) |
| public.whatsapp_conversations | whatsapp_conversations_whatsapp_number_id_fkey | f | FOREIGN KEY (whatsapp_number_id) REFERENCES whatsapp_sessions(id) ON DELETE CASCADE |
| public.whatsapp_messages | whatsapp_messages_conversation_id_fkey | f | FOREIGN KEY (conversation_id) REFERENCES whatsapp_conversations(id) ON DELETE CASCADE |
| public.whatsapp_messages | whatsapp_messages_direction_check | c | CHECK ((direction = ANY (ARRAY['inbound'::text, 'outbound'::text]))) |
| public.whatsapp_messages | whatsapp_messages_message_type_check | c | CHECK ((message_type = ANY (ARRAY['text'::text, 'image'::text, 'audio'::text, 'document'::text]))) |
| public.whatsapp_messages | whatsapp_messages_pkey | p | PRIMARY KEY (id) |
| public.whatsapp_messages | whatsapp_messages_sent_by_check | c | CHECK ((sent_by = ANY (ARRAY['contact'::text, 'assistant'::text, 'human_agent'::text]))) |
| public.whatsapp_messages | whatsapp_messages_status_check | c | CHECK ((status = ANY (ARRAY['sent'::text, 'delivered'::text, 'read'::text, 'failed'::text]))) |
| public.whatsapp_sessions | whatsapp_sessions_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.whatsapp_sessions | whatsapp_sessions_pkey | p | PRIMARY KEY (id) |
| public.whatsapp_sessions | whatsapp_sessions_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'connected'::text, 'disconnected'::text, 'expired'::text]))) |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |
| public.active_calls | active_calls_pkey | CREATE UNIQUE INDEX active_calls_pkey ON public.active_calls USING btree (room_id) |
| public.active_calls | idx_active_calls_org | CREATE INDEX idx_active_calls_org ON public.active_calls USING btree (org_id) |
| public.active_calls | idx_active_calls_status | CREATE INDEX idx_active_calls_status ON public.active_calls USING btree (status) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_agent_id_document_id_key | CREATE UNIQUE INDEX agent_knowledge_assignments_agent_id_document_id_key ON public.agent_knowledge_assignments USING btree (agent_id, document_id) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_pkey | CREATE UNIQUE INDEX agent_knowledge_assignments_pkey ON public.agent_knowledge_assignments USING btree (id) |
| public.agent_knowledge_files | agent_knowledge_files_pkey | CREATE UNIQUE INDEX agent_knowledge_files_pkey ON public.agent_knowledge_files USING btree (id) |
| public.agent_knowledge_files | idx_agent_kb_files_org | CREATE INDEX idx_agent_kb_files_org ON public.agent_knowledge_files USING btree (org_id) |
| public.agent_knowledge_files | idx_agent_knowledge_files_agent | CREATE INDEX idx_agent_knowledge_files_agent ON public.agent_knowledge_files USING btree (agent_id) |
| public.agents | agents_pkey | CREATE UNIQUE INDEX agents_pkey ON public.agents USING btree (id) |
| public.agents | idx_agents_created_at | CREATE INDEX idx_agents_created_at ON public.agents USING btree (created_at DESC) |
| public.agents | idx_agents_is_active | CREATE INDEX idx_agents_is_active ON public.agents USING btree (is_active) WHERE (is_active = true) |
| public.agents | idx_agents_org | CREATE INDEX idx_agents_org ON public.agents USING btree (org_id) |
| public.agents | idx_agents_purpose | CREATE INDEX idx_agents_purpose ON public.agents USING btree (purpose) |
| public.api_tokens | api_tokens_pkey | CREATE UNIQUE INDEX api_tokens_pkey ON public.api_tokens USING btree (id) |
| public.api_tokens | api_tokens_token_hash_key | CREATE UNIQUE INDEX api_tokens_token_hash_key ON public.api_tokens USING btree (token_hash) |
| public.app_kv_store | app_kv_store_pkey | CREATE UNIQUE INDEX app_kv_store_pkey ON public.app_kv_store USING btree (key) |
| public.app_kv_store | idx_app_kv_store_expires | CREATE INDEX idx_app_kv_store_expires ON public.app_kv_store USING btree (expires_at) WHERE (expires_at IS NOT NULL) |
| public.app_settings | app_settings_pkey | CREATE UNIQUE INDEX app_settings_pkey ON public.app_settings USING btree (key) |
| public.app_settings | idx_app_settings_org | CREATE INDEX idx_app_settings_org ON public.app_settings USING btree (org_id) |
| public.audit_log | audit_log_pkey | CREATE UNIQUE INDEX audit_log_pkey ON public.audit_log USING btree (id) |
| public.audit_log | idx_audit_log_actor | CREATE INDEX idx_audit_log_actor ON public.audit_log USING btree (actor_user_id, created_at DESC) |
| public.audit_log | idx_audit_log_org | CREATE INDEX idx_audit_log_org ON public.audit_log USING btree (org_id, created_at DESC) |
| public.calendar_bookings | calendar_bookings_pkey | CREATE UNIQUE INDEX calendar_bookings_pkey ON public.calendar_bookings USING btree (id) |
| public.calendar_bookings | idx_calendar_bookings_org | CREATE INDEX idx_calendar_bookings_org ON public.calendar_bookings USING btree (org_id) |
| public.calendar_bookings | idx_calendar_bookings_phone | CREATE INDEX idx_calendar_bookings_phone ON public.calendar_bookings USING btree (phone) |
| public.calendar_bookings | idx_calendar_bookings_time | CREATE INDEX idx_calendar_bookings_time ON public.calendar_bookings USING btree (scheduled_at) |
| public.call_configurations | call_configurations_agent_id_key | CREATE UNIQUE INDEX call_configurations_agent_id_key ON public.call_configurations USING btree (agent_id) |
| public.call_configurations | call_configurations_pkey | CREATE UNIQUE INDEX call_configurations_pkey ON public.call_configurations USING btree (id) |
| public.call_configurations | idx_call_configurations_agent_id | CREATE INDEX idx_call_configurations_agent_id ON public.call_configurations USING btree (agent_id) |
| public.call_listing_mentions | call_listing_mentions_pkey | CREATE UNIQUE INDEX call_listing_mentions_pkey ON public.call_listing_mentions USING btree (id) |
| public.call_listing_mentions | idx_call_listing_mentions_call | CREATE INDEX idx_call_listing_mentions_call ON public.call_listing_mentions USING btree (call_id) |
| public.call_logs | call_logs_pkey | CREATE UNIQUE INDEX call_logs_pkey ON public.call_logs USING btree (id) |
| public.call_logs | call_logs_room_id_unique | CREATE UNIQUE INDEX call_logs_room_id_unique ON public.call_logs USING btree (room_id) |
| public.call_logs | idx_call_logs_agent_id | CREATE INDEX idx_call_logs_agent_id ON public.call_logs USING btree (agent_id) |
| public.call_logs | idx_call_logs_bulk_call_id | CREATE INDEX idx_call_logs_bulk_call_id ON public.call_logs USING btree (bulk_call_id) WHERE (bulk_call_id IS NOT NULL) |
| public.call_logs | idx_call_logs_call_direction | CREATE INDEX idx_call_logs_call_direction ON public.call_logs USING btree (call_direction) |
| public.call_logs | idx_call_logs_call_status | CREATE INDEX idx_call_logs_call_status ON public.call_logs USING btree (call_status) |
| public.call_logs | idx_call_logs_caller_phone | CREATE INDEX idx_call_logs_caller_phone ON public.call_logs USING btree (caller_phone) |
| public.call_logs | idx_call_logs_config_hash | CREATE INDEX idx_call_logs_config_hash ON public.call_logs USING btree (config_hash) WHERE (config_hash IS NOT NULL) |
| public.call_logs | idx_call_logs_created_at | CREATE INDEX idx_call_logs_created_at ON public.call_logs USING btree (created_at DESC) |
| public.call_logs | idx_call_logs_from_number | CREATE INDEX idx_call_logs_from_number ON public.call_logs USING btree (from_number) |
| public.call_logs | idx_call_logs_migrated | CREATE INDEX idx_call_logs_migrated ON public.call_logs USING btree (migrated_to_re_memory) WHERE (migrated_to_re_memory IS NULL) |
| public.call_logs | idx_call_logs_org | CREATE INDEX idx_call_logs_org ON public.call_logs USING btree (org_id) |
| public.call_logs | idx_call_logs_phone | CREATE INDEX idx_call_logs_phone ON public.call_logs USING btree (phone_number) |
| public.call_logs | idx_call_logs_room_id | CREATE INDEX idx_call_logs_room_id ON public.call_logs USING btree (room_id) |
| public.call_logs | idx_call_logs_to_number | CREATE INDEX idx_call_logs_to_number ON public.call_logs USING btree (to_number) |
| public.call_logs | idx_call_logs_was_booked | CREATE INDEX idx_call_logs_was_booked ON public.call_logs USING btree (was_booked) WHERE (was_booked = true) |
| public.call_transcripts | call_transcripts_pkey | CREATE UNIQUE INDEX call_transcripts_pkey ON public.call_transcripts USING btree (id) |
| public.call_transcripts | idx_call_transcripts_call_id | CREATE INDEX idx_call_transcripts_call_id ON public.call_transcripts USING btree (call_id) |
| public.call_transcripts | idx_call_transcripts_org | CREATE INDEX idx_call_transcripts_org ON public.call_transcripts USING btree (org_id) |
| public.call_transcripts | idx_call_transcripts_phone | CREATE INDEX idx_call_transcripts_phone ON public.call_transcripts USING btree (phone) |
| public.call_transcripts | idx_call_transcripts_room | CREATE INDEX idx_call_transcripts_room ON public.call_transcripts USING btree (call_room_id) |
| public.campaign_listings | campaign_listings_campaign_id_listing_id_key | CREATE UNIQUE INDEX campaign_listings_campaign_id_listing_id_key ON public.campaign_listings USING btree (campaign_id, listing_id) |
| public.campaign_listings | campaign_listings_pkey | CREATE UNIQUE INDEX campaign_listings_pkey ON public.campaign_listings USING btree (id) |
| public.campaign_listings | idx_campaign_listings_campaign_id | CREATE INDEX idx_campaign_listings_campaign_id ON public.campaign_listings USING btree (campaign_id) |
| public.campaign_numbers | campaign_numbers_campaign_id_phone_key | CREATE UNIQUE INDEX campaign_numbers_campaign_id_phone_key ON public.campaign_numbers USING btree (campaign_id, phone) |
| public.campaign_numbers | campaign_numbers_pkey | CREATE UNIQUE INDEX campaign_numbers_pkey ON public.campaign_numbers USING btree (id) |
| public.campaign_numbers | idx_campaign_numbers_campaign_id | CREATE INDEX idx_campaign_numbers_campaign_id ON public.campaign_numbers USING btree (campaign_id) |
| public.campaign_numbers | idx_campaign_numbers_org | CREATE INDEX idx_campaign_numbers_org ON public.campaign_numbers USING btree (org_id) |
| public.campaign_numbers | idx_campaign_numbers_phone | CREATE INDEX idx_campaign_numbers_phone ON public.campaign_numbers USING btree (phone) |
| public.conversational_flows | conversational_flows_agent_id_key | CREATE UNIQUE INDEX conversational_flows_agent_id_key ON public.conversational_flows USING btree (agent_id) |
| public.conversational_flows | conversational_flows_pkey | CREATE UNIQUE INDEX conversational_flows_pkey ON public.conversational_flows USING btree (id) |
| public.conversational_flows | idx_conversational_flows_agent_id | CREATE INDEX idx_conversational_flows_agent_id ON public.conversational_flows USING btree (agent_id) |
| public.crm_sync_log | crm_sync_log_pkey | CREATE UNIQUE INDEX crm_sync_log_pkey ON public.crm_sync_log USING btree (id) |
| public.crm_sync_log | idx_crm_sync_log_phone | CREATE INDEX idx_crm_sync_log_phone ON public.crm_sync_log USING btree (phone) |
| public.invitations | invitations_email_org_id_accepted_at_key | CREATE UNIQUE INDEX invitations_email_org_id_accepted_at_key ON public.invitations USING btree (email, org_id, accepted_at) |
| public.invitations | invitations_pkey | CREATE UNIQUE INDEX invitations_pkey ON public.invitations USING btree (id) |
| public.invitations | invitations_token_hash_key | CREATE UNIQUE INDEX invitations_token_hash_key ON public.invitations USING btree (token_hash) |
| public.knowledge_documents | idx_knowledge_documents_org | CREATE INDEX idx_knowledge_documents_org ON public.knowledge_documents USING btree (org_id) |
| public.knowledge_documents | idx_knowledge_documents_type | CREATE INDEX idx_knowledge_documents_type ON public.knowledge_documents USING btree (doc_type) |
| public.knowledge_documents | knowledge_documents_document_id_key | CREATE UNIQUE INDEX knowledge_documents_document_id_key ON public.knowledge_documents USING btree (document_id) |
| public.knowledge_documents | knowledge_documents_pkey | CREATE UNIQUE INDEX knowledge_documents_pkey ON public.knowledge_documents USING btree (id) |
| public.lead_actions | idx_lead_actions_call_id | CREATE INDEX idx_lead_actions_call_id ON public.lead_actions USING btree (call_id) |
| public.lead_actions | idx_lead_actions_org | CREATE INDEX idx_lead_actions_org ON public.lead_actions USING btree (org_id) |
| public.lead_actions | idx_lead_actions_performed_at | CREATE INDEX idx_lead_actions_performed_at ON public.lead_actions USING btree (performed_at DESC) |
| public.lead_actions | lead_actions_pkey | CREATE UNIQUE INDEX lead_actions_pkey ON public.lead_actions USING btree (id) |
| public.lead_objections | idx_lead_objections_lead | CREATE INDEX idx_lead_objections_lead ON public.lead_objections USING btree (lead_id) |
| public.lead_objections | idx_lead_objections_org | CREATE INDEX idx_lead_objections_org ON public.lead_objections USING btree (org_id) |
| public.lead_objections | lead_objections_pkey | CREATE UNIQUE INDEX lead_objections_pkey ON public.lead_objections USING btree (id) |
| public.lead_property_signals | idx_lead_property_signals_lead | CREATE INDEX idx_lead_property_signals_lead ON public.lead_property_signals USING btree (lead_id) |
| public.lead_property_signals | idx_lead_signals_org | CREATE INDEX idx_lead_signals_org ON public.lead_property_signals USING btree (org_id) |
| public.lead_property_signals | lead_property_signals_pkey | CREATE UNIQUE INDEX lead_property_signals_pkey ON public.lead_property_signals USING btree (id) |
| public.leads | idx_leads_deal_stage | CREATE INDEX idx_leads_deal_stage ON public.leads USING btree (deal_stage) |
| public.leads | idx_leads_intent_score | CREATE INDEX idx_leads_intent_score ON public.leads USING btree (intent_score DESC) |
| public.leads | idx_leads_phone | CREATE INDEX idx_leads_phone ON public.leads USING btree (phone) |
| public.leads | leads_lead_id_key | CREATE UNIQUE INDEX leads_lead_id_key ON public.leads USING btree (lead_id) |
| public.leads | leads_phone_key | CREATE UNIQUE INDEX leads_phone_key ON public.leads USING btree (phone) |
| public.leads | leads_pkey | CREATE UNIQUE INDEX leads_pkey ON public.leads USING btree (id) |
| public.listings | idx_listings_area | CREATE INDEX idx_listings_area ON public.listings USING btree (area) |
| public.listings | idx_listings_listing_id | CREATE INDEX idx_listings_listing_id ON public.listings USING btree (listing_id) |
| public.listings | idx_listings_org | CREATE INDEX idx_listings_org ON public.listings USING btree (org_id) |
| public.listings | idx_listings_status | CREATE INDEX idx_listings_status ON public.listings USING btree (status) WHERE (status = 'active'::text) |
| public.listings | listings_listing_id_key | CREATE UNIQUE INDEX listings_listing_id_key ON public.listings USING btree (listing_id) |
| public.listings | listings_pim_sku_key | CREATE UNIQUE INDEX listings_pim_sku_key ON public.listings USING btree (pim_sku) |
| public.listings | listings_pkey | CREATE UNIQUE INDEX listings_pkey ON public.listings USING btree (id) |
| public.memberships | memberships_pkey | CREATE UNIQUE INDEX memberships_pkey ON public.memberships USING btree (id) |
| public.memberships | memberships_user_id_org_id_key | CREATE UNIQUE INDEX memberships_user_id_org_id_key ON public.memberships USING btree (user_id, org_id) |
| public.mfa_factors | mfa_factors_pkey | CREATE UNIQUE INDEX mfa_factors_pkey ON public.mfa_factors USING btree (id) |
| public.mfa_factors | mfa_factors_user_id_type_key | CREATE UNIQUE INDEX mfa_factors_user_id_type_key ON public.mfa_factors USING btree (user_id, type) |
| public.mfa_recovery_codes | idx_mfa_recovery_user | CREATE INDEX idx_mfa_recovery_user ON public.mfa_recovery_codes USING btree (user_id) |
| public.mfa_recovery_codes | mfa_recovery_codes_pkey | CREATE UNIQUE INDEX mfa_recovery_codes_pkey ON public.mfa_recovery_codes USING btree (id) |
| public.organizations | organizations_pkey | CREATE UNIQUE INDEX organizations_pkey ON public.organizations USING btree (id) |
| public.organizations | organizations_slug_key | CREATE UNIQUE INDEX organizations_slug_key ON public.organizations USING btree (slug) |
| public.outbound_campaigns | idx_outbound_campaigns_agent_id | CREATE INDEX idx_outbound_campaigns_agent_id ON public.outbound_campaigns USING btree (agent_id) |
| public.outbound_campaigns | idx_outbound_campaigns_created_at | CREATE INDEX idx_outbound_campaigns_created_at ON public.outbound_campaigns USING btree (created_at DESC) |
| public.outbound_campaigns | idx_outbound_campaigns_org | CREATE INDEX idx_outbound_campaigns_org ON public.outbound_campaigns USING btree (org_id) |
| public.outbound_campaigns | idx_outbound_campaigns_status | CREATE INDEX idx_outbound_campaigns_status ON public.outbound_campaigns USING btree (status) |
| public.outbound_campaigns | outbound_campaigns_pkey | CREATE UNIQUE INDEX outbound_campaigns_pkey ON public.outbound_campaigns USING btree (id) |
| public.password_resets | password_resets_pkey | CREATE UNIQUE INDEX password_resets_pkey ON public.password_resets USING btree (id) |
| public.password_resets | password_resets_token_hash_key | CREATE UNIQUE INDEX password_resets_token_hash_key ON public.password_resets USING btree (token_hash) |
| public.pin_to_pim_mappings | idx_pin_to_pim_pim | CREATE INDEX idx_pin_to_pim_pim ON public.pin_to_pim_mappings USING btree (pim_listing_id) |
| public.pin_to_pim_mappings | idx_pin_to_pim_pin | CREATE INDEX idx_pin_to_pim_pin ON public.pin_to_pim_mappings USING btree (pin) WHERE (is_active = true) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pin_source_key | CREATE UNIQUE INDEX pin_to_pim_mappings_pin_source_key ON public.pin_to_pim_mappings USING btree (pin, source) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pkey | CREATE UNIQUE INDEX pin_to_pim_mappings_pkey ON public.pin_to_pim_mappings USING btree (id) |
| public.post_call_actions | idx_post_call_actions_agent_id | CREATE INDEX idx_post_call_actions_agent_id ON public.post_call_actions USING btree (agent_id) |
| public.post_call_actions | post_call_actions_agent_id_key | CREATE UNIQUE INDEX post_call_actions_agent_id_key ON public.post_call_actions USING btree (agent_id) |
| public.post_call_actions | post_call_actions_pkey | CREATE UNIQUE INDEX post_call_actions_pkey ON public.post_call_actions USING btree (id) |
| public.post_call_deliveries | idx_post_call_deliveries_call | CREATE INDEX idx_post_call_deliveries_call ON public.post_call_deliveries USING btree (call_id) |
| public.post_call_deliveries | post_call_deliveries_pkey | CREATE UNIQUE INDEX post_call_deliveries_pkey ON public.post_call_deliveries USING btree (id) |
| public.sessions | idx_sessions_refresh_hash | CREATE INDEX idx_sessions_refresh_hash ON public.sessions USING btree (refresh_token_hash) |
| public.sessions | idx_sessions_user_id | CREATE INDEX idx_sessions_user_id ON public.sessions USING btree (user_id) |
| public.sessions | sessions_pkey | CREATE UNIQUE INDEX sessions_pkey ON public.sessions USING btree (id) |
| public.sessions | sessions_refresh_token_hash_key | CREATE UNIQUE INDEX sessions_refresh_token_hash_key ON public.sessions USING btree (refresh_token_hash) |
| public.users | users_email_key | CREATE UNIQUE INDEX users_email_key ON public.users USING btree (email) |
| public.users | users_pkey | CREATE UNIQUE INDEX users_pkey ON public.users USING btree (id) |
| public.whatsapp_conversations | idx_whatsapp_conversations_number_last | CREATE INDEX idx_whatsapp_conversations_number_last ON public.whatsapp_conversations USING btree (whatsapp_number_id, last_message_at DESC NULLS LAST) |
| public.whatsapp_conversations | idx_whatsapp_conversations_org | CREATE INDEX idx_whatsapp_conversations_org ON public.whatsapp_conversations USING btree (org_id) |
| public.whatsapp_conversations | whatsapp_conversations_pkey | CREATE UNIQUE INDEX whatsapp_conversations_pkey ON public.whatsapp_conversations USING btree (id) |
| public.whatsapp_conversations | whatsapp_conversations_whatsapp_number_id_contact_number_key | CREATE UNIQUE INDEX whatsapp_conversations_whatsapp_number_id_contact_number_key ON public.whatsapp_conversations USING btree (whatsapp_number_id, contact_number) |
| public.whatsapp_messages | idx_whatsapp_messages_conv_created | CREATE INDEX idx_whatsapp_messages_conv_created ON public.whatsapp_messages USING btree (conversation_id, created_at DESC) |
| public.whatsapp_messages | idx_whatsapp_messages_wa_id | CREATE UNIQUE INDEX idx_whatsapp_messages_wa_id ON public.whatsapp_messages USING btree (wa_message_id) WHERE (wa_message_id IS NOT NULL) |
| public.whatsapp_messages | whatsapp_messages_pkey | CREATE UNIQUE INDEX whatsapp_messages_pkey ON public.whatsapp_messages USING btree (id) |
| public.whatsapp_sessions | idx_whatsapp_sessions_org | CREATE UNIQUE INDEX idx_whatsapp_sessions_org ON public.whatsapp_sessions USING btree (org_id) |
| public.whatsapp_sessions | whatsapp_sessions_pkey | CREATE UNIQUE INDEX whatsapp_sessions_pkey ON public.whatsapp_sessions USING btree (id) |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |
| public.citext | boolean | citext | False |
| public.citext | character | citext | False |
| public.citext | inet | citext | False |
| public.citext_cmp | citext, citext | integer | False |
| public.citext_eq | citext, citext | boolean | False |
| public.citext_ge | citext, citext | boolean | False |
| public.citext_gt | citext, citext | boolean | False |
| public.citext_hash | citext | integer | False |
| public.citext_hash_extended | citext, bigint | bigint | False |
| public.citext_larger | citext, citext | citext | False |
| public.citext_le | citext, citext | boolean | False |
| public.citext_lt | citext, citext | boolean | False |
| public.citext_ne | citext, citext | boolean | False |
| public.citext_pattern_cmp | citext, citext | integer | False |
| public.citext_pattern_ge | citext, citext | boolean | False |
| public.citext_pattern_gt | citext, citext | boolean | False |
| public.citext_pattern_le | citext, citext | boolean | False |
| public.citext_pattern_lt | citext, citext | boolean | False |
| public.citext_smaller | citext, citext | citext | False |
| public.citextin | cstring | citext | False |
| public.citextout | citext | cstring | False |
| public.citextrecv | internal | citext | False |
| public.citextsend | citext | bytea | False |
| public.enforce_single_active_agent |  | trigger | False |
| public.max | citext | citext | False |
| public.min | citext | citext | False |
| public.regexp_match | citext, citext, text | text[] | False |
| public.regexp_match | citext, citext | text[] | False |
| public.regexp_matches | citext, citext, text | SETOF text[] | False |
| public.regexp_matches | citext, citext | SETOF text[] | False |
| public.regexp_replace | citext, citext, text | text | False |
| public.regexp_replace | citext, citext, text, text | text | False |
| public.regexp_split_to_array | citext, citext | text[] | False |
| public.regexp_split_to_array | citext, citext, text | text[] | False |
| public.regexp_split_to_table | citext, citext, text | SETOF text | False |
| public.regexp_split_to_table | citext, citext | SETOF text | False |
| public.replace | citext, citext, citext | text | False |
| public.set_updated_at |  | trigger | False |
| public.split_part | citext, citext, integer | text | False |
| public.strpos | citext, citext | integer | False |
| public.texticlike | citext, text | boolean | False |
| public.texticlike | citext, citext | boolean | False |
| public.texticnlike | citext, text | boolean | False |
| public.texticnlike | citext, citext | boolean | False |
| public.texticregexeq | citext, citext | boolean | False |
| public.texticregexeq | citext, text | boolean | False |
| public.texticregexne | citext, text | boolean | False |
| public.texticregexne | citext, citext | boolean | False |
| public.translate | citext, citext, text | text | False |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |
| auth | 4 |
| extensions | 55 |
| graphql_public | 1 |
| net | 12 |
| pgbouncer | 1 |
| public | 49 |
| realtime | 15 |
| storage | 19 |
| supabase_functions | 1 |
| vault | 5 |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |
| auth.email |  | text |
| auth.jwt |  | jsonb |
| auth.role |  | text |
| auth.uid |  | uuid |
| extensions.armor | bytea, text[], text[] | text |
| extensions.armor | bytea | text |
| extensions.crypt | text, text | text |
| extensions.dearmor | text | bytea |
| extensions.decrypt | bytea, bytea, text | bytea |
| extensions.decrypt_iv | bytea, bytea, bytea, text | bytea |
| extensions.digest | text, text | bytea |
| extensions.digest | bytea, text | bytea |
| extensions.encrypt | bytea, bytea, text | bytea |
| extensions.encrypt_iv | bytea, bytea, bytea, text | bytea |
| extensions.gen_random_bytes | integer | bytea |
| extensions.gen_random_uuid |  | uuid |
| extensions.gen_salt | text, integer | text |
| extensions.gen_salt | text | text |
| extensions.grant_pg_cron_access |  | event_trigger |
| extensions.grant_pg_graphql_access |  | event_trigger |
| extensions.grant_pg_net_access |  | event_trigger |
| extensions.hmac | text, text, text | bytea |
| extensions.hmac | bytea, bytea, text | bytea |
| extensions.pg_stat_statements | showtext boolean, OUT userid oid, OUT dbid oid, OUT toplevel boolean, OUT queryid bigint, OUT query text, OUT plans bigint, OUT total_plan_time double precision, OUT min_plan_time double precision, OUT max_plan_time double precision, OUT mean_plan_time double precision, OUT stddev_plan_time double precision, OUT calls bigint, OUT total_exec_time double precision, OUT min_exec_time double precision, OUT max_exec_time double precision, OUT mean_exec_time double precision, OUT stddev_exec_time double precision, OUT rows bigint, OUT shared_blks_hit bigint, OUT shared_blks_read bigint, OUT shared_blks_dirtied bigint, OUT shared_blks_written bigint, OUT local_blks_hit bigint, OUT local_blks_read bigint, OUT local_blks_dirtied bigint, OUT local_blks_written bigint, OUT temp_blks_read bigint, OUT temp_blks_written bigint, OUT shared_blk_read_time double precision, OUT shared_blk_write_time double precision, OUT local_blk_read_time double precision, OUT local_blk_write_time double precision, OUT temp_blk_read_time double precision, OUT temp_blk_write_time double precision, OUT wal_records bigint, OUT wal_fpi bigint, OUT wal_bytes numeric, OUT jit_functions bigint, OUT jit_generation_time double precision, OUT jit_inlining_count bigint, OUT jit_inlining_time double precision, OUT jit_optimization_count bigint, OUT jit_optimization_time double precision, OUT jit_emission_count bigint, OUT jit_emission_time double precision, OUT jit_deform_count bigint, OUT jit_deform_time double precision, OUT stats_since timestamp with time zone, OUT minmax_stats_since timestamp with time zone | SETOF record |
| extensions.pg_stat_statements_info | OUT dealloc bigint, OUT stats_reset timestamp with time zone | record |
| extensions.pg_stat_statements_reset | userid oid, dbid oid, queryid bigint, minmax_only boolean | timestamp with time zone |
| extensions.pgp_armor_headers | text, OUT key text, OUT value text | SETOF record |
| extensions.pgp_key_id | bytea | text |
| extensions.pgp_pub_decrypt | bytea, bytea, text, text | text |
| extensions.pgp_pub_decrypt | bytea, bytea, text | text |
| extensions.pgp_pub_decrypt | bytea, bytea | text |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea, text | bytea |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea | bytea |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea, text, text | bytea |
| extensions.pgp_pub_encrypt | text, bytea | bytea |
| extensions.pgp_pub_encrypt | text, bytea, text | bytea |
| extensions.pgp_pub_encrypt_bytea | bytea, bytea, text | bytea |
| extensions.pgp_pub_encrypt_bytea | bytea, bytea | bytea |
| extensions.pgp_sym_decrypt | bytea, text, text | text |
| extensions.pgp_sym_decrypt | bytea, text | text |
| extensions.pgp_sym_decrypt_bytea | bytea, text | bytea |
| extensions.pgp_sym_decrypt_bytea | bytea, text, text | bytea |
| extensions.pgp_sym_encrypt | text, text, text | bytea |
| extensions.pgp_sym_encrypt | text, text | bytea |
| extensions.pgp_sym_encrypt_bytea | bytea, text | bytea |
| extensions.pgp_sym_encrypt_bytea | bytea, text, text | bytea |
| extensions.pgrst_ddl_watch |  | event_trigger |
| extensions.pgrst_drop_watch |  | event_trigger |
| extensions.set_graphql_placeholder |  | event_trigger |
| extensions.uuid_generate_v1 |  | uuid |
| extensions.uuid_generate_v1mc |  | uuid |
| extensions.uuid_generate_v3 | namespace uuid, name text | uuid |
| extensions.uuid_generate_v4 |  | uuid |
| extensions.uuid_generate_v5 | namespace uuid, name text | uuid |
| extensions.uuid_nil |  | uuid |
| extensions.uuid_ns_dns |  | uuid |
| extensions.uuid_ns_oid |  | uuid |
| extensions.uuid_ns_url |  | uuid |
| extensions.uuid_ns_x500 |  | uuid |
| graphql_public.graphql | "operationName" text, query text, variables jsonb, extensions jsonb | jsonb |
| net._await_response | request_id bigint | boolean |
| net._encode_url_with_params_array | url text, params_array text[] | text |
| net._http_collect_response | request_id bigint, async boolean | net.http_response_result |
| net._urlencode_string | string character varying | text |
| net.check_worker_is_up |  | void |
| net.http_collect_response | request_id bigint, async boolean | net.http_response_result |
| net.http_delete | url text, params jsonb, headers jsonb, timeout_milliseconds integer, body jsonb | bigint |
| net.http_get | url text, params jsonb, headers jsonb, timeout_milliseconds integer | bigint |
| net.http_post | url text, body jsonb, params jsonb, headers jsonb, timeout_milliseconds integer | bigint |
| net.wait_until_running |  | void |
| net.wake |  | void |
| net.worker_restart |  | boolean |
| pgbouncer.get_auth | p_usename text | TABLE(username text, password text) |
| public.citext | boolean | citext |
| public.citext | character | citext |
| public.citext | inet | citext |
| public.citext_cmp | citext, citext | integer |
| public.citext_eq | citext, citext | boolean |
| public.citext_ge | citext, citext | boolean |
| public.citext_gt | citext, citext | boolean |
| public.citext_hash | citext | integer |
| public.citext_hash_extended | citext, bigint | bigint |
| public.citext_larger | citext, citext | citext |
| public.citext_le | citext, citext | boolean |
| public.citext_lt | citext, citext | boolean |
| public.citext_ne | citext, citext | boolean |
| public.citext_pattern_cmp | citext, citext | integer |
| public.citext_pattern_ge | citext, citext | boolean |
| public.citext_pattern_gt | citext, citext | boolean |
| public.citext_pattern_le | citext, citext | boolean |
| public.citext_pattern_lt | citext, citext | boolean |
| public.citext_smaller | citext, citext | citext |
| public.citextin | cstring | citext |
| public.citextout | citext | cstring |
| public.citextrecv | internal | citext |
| public.citextsend | citext | bytea |
| public.enforce_single_active_agent |  | trigger |
| public.max | citext | citext |
| public.min | citext | citext |
| public.regexp_match | citext, citext, text | text[] |
| public.regexp_match | citext, citext | text[] |
| public.regexp_matches | citext, citext, text | SETOF text[] |
| public.regexp_matches | citext, citext | SETOF text[] |
| public.regexp_replace | citext, citext, text | text |
| public.regexp_replace | citext, citext, text, text | text |
| public.regexp_split_to_array | citext, citext | text[] |
| public.regexp_split_to_array | citext, citext, text | text[] |
| public.regexp_split_to_table | citext, citext, text | SETOF text |
| public.regexp_split_to_table | citext, citext | SETOF text |
| public.replace | citext, citext, citext | text |
| public.set_updated_at |  | trigger |
| public.split_part | citext, citext, integer | text |
| public.strpos | citext, citext | integer |
| public.texticlike | citext, text | boolean |
| public.texticlike | citext, citext | boolean |
| public.texticnlike | citext, text | boolean |
| public.texticnlike | citext, citext | boolean |
| public.texticregexeq | citext, citext | boolean |
| public.texticregexeq | citext, text | boolean |
| public.texticregexne | citext, text | boolean |
| public.texticregexne | citext, citext | boolean |
| public.translate | citext, citext, text | text |
| realtime.apply_rls | wal jsonb, max_record_bytes integer | SETOF realtime.wal_rls |
| realtime.broadcast_changes | topic_name text, event_name text, operation text, table_name text, table_schema text, new record, old record, level text | void |
| realtime.build_prepared_statement_sql | prepared_statement_name text, entity regclass, columns realtime.wal_column[] | text |
| realtime.cast | val text, type_ regtype | jsonb |
| realtime.check_equality_op | op realtime.equality_op, type_ regtype, val_1 text, val_2 text | boolean |
| realtime.check_equality_op | op realtime.equality_op, type_ regtype, val_1 text, val_2 text, negate boolean | boolean |
| realtime.is_visible_through_filters | columns realtime.wal_column[], filters realtime.user_defined_filter[] | boolean |
| realtime.list_changes | publication name, slot_name name, max_changes integer, max_record_bytes integer | TABLE(wal jsonb, is_rls_enabled boolean, subscription_ids uuid[], errors text[], slot_changes_count bigint) |
| realtime.quote_wal2json | entity regclass | text |
| realtime.send | payload jsonb, event text, topic text, private boolean | void |
| realtime.send_binary | payload bytea, event text, topic text, private boolean | void |
| realtime.subscription_check_filters |  | trigger |
| realtime.to_regrole | role_name text | regrole |
| realtime.topic |  | text |
| realtime.wal2json_escape_identifier | name text | text |
| storage.allow_any_operation | expected_operations text[] | boolean |
| storage.allow_only_operation | expected_operation text | boolean |
| storage.can_insert_object | bucketid text, name text, owner uuid, metadata jsonb | void |
| storage.enforce_bucket_lifecycle_service_role |  | trigger |
| storage.enforce_bucket_name_length |  | trigger |
| storage.extension | name text | text |
| storage.filename | name text | text |
| storage.foldername | name text | text[] |
| storage.get_common_prefix | p_key text, p_prefix text, p_delimiter text | text |
| storage.get_size_by_bucket |  | TABLE(size bigint, bucket_id text) |
| storage.list_multipart_uploads_with_delimiter | bucket_id text, prefix_param text, delimiter_param text, max_keys integer, next_key_token text, next_upload_token text | TABLE(key text, id text, created_at timestamp with time zone) |
| storage.list_objects_with_delimiter | _bucket_id text, prefix_param text, delimiter_param text, max_keys integer, start_after text, next_token text, sort_order text | TABLE(name text, id uuid, metadata jsonb, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone) |
| storage.operation |  | text |
| storage.protect_bucket_control_columns |  | trigger |
| storage.protect_delete |  | trigger |
| storage.search | prefix text, bucketname text, limits integer, levels integer, offsets integer, search text, sortcolumn text, sortorder text | TABLE(name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.search_by_timestamp | p_prefix text, p_bucket_id text, p_limit integer, p_level integer, p_start_after text, p_sort_order text, p_sort_column text, p_sort_column_after text | TABLE(key text, name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.search_v2 | prefix text, bucket_name text, limits integer, levels integer, start_after text, sort_order text, sort_column text, sort_column_after text | TABLE(key text, name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.update_updated_at_column |  | trigger |
| supabase_functions.http_request |  | trigger |
| vault._crypto_aead_det_decrypt | message bytea, additional bytea, key_id bigint, context bytea, nonce bytea | bytea |
| vault._crypto_aead_det_encrypt | message bytea, additional bytea, key_id bigint, context bytea, nonce bytea | bytea |
| vault._crypto_aead_det_noncegen |  | bytea |
| vault.create_secret | new_secret text, new_name text, new_description text, new_key_id uuid | uuid |
| vault.update_secret | secret_id uuid, new_secret text, new_name text, new_description text, new_key_id uuid | void |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |
| public.agent_knowledge_files | trg_agent_knowledge_files_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.agents | trg_agents_single_active | AFTER | INSERT | EXECUTE FUNCTION enforce_single_active_agent() |
| public.agents | trg_agents_single_active | AFTER | UPDATE | EXECUTE FUNCTION enforce_single_active_agent() |
| public.agents | trg_agents_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.calendar_bookings | trg_calendar_bookings_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.call_configurations | trg_call_configurations_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.campaign_numbers | trg_campaign_numbers_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.conversational_flows | trg_conversational_flows_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.knowledge_documents | trg_knowledge_documents_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.leads | trg_leads_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.listings | trg_listings_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.outbound_campaigns | trg_outbound_campaigns_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.pin_to_pim_mappings | trg_pin_to_pim_mappings_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.post_call_actions | trg_post_call_actions_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| realtime.subscription | tr_check_filters | BEFORE | INSERT | EXECUTE FUNCTION realtime.subscription_check_filters() |
| realtime.subscription | tr_check_filters | BEFORE | UPDATE | EXECUTE FUNCTION realtime.subscription_check_filters() |
| storage.buckets | enforce_bucket_name_length_trigger | BEFORE | INSERT | EXECUTE FUNCTION storage.enforce_bucket_name_length() |
| storage.buckets | enforce_bucket_name_length_trigger | BEFORE | UPDATE | EXECUTE FUNCTION storage.enforce_bucket_name_length() |
| storage.buckets | protect_bucket_control_insert | BEFORE | INSERT | EXECUTE FUNCTION storage.protect_bucket_control_columns('service_role') |
| storage.buckets | protect_bucket_control_update | BEFORE | UPDATE | EXECUTE FUNCTION storage.protect_bucket_control_columns() |
| storage.buckets | protect_bucket_control_update_role | AFTER | UPDATE | EXECUTE FUNCTION storage.enforce_bucket_lifecycle_service_role('service_role') |
| storage.buckets | protect_buckets_delete | BEFORE | DELETE | EXECUTE FUNCTION storage.protect_delete() |
| storage.objects | protect_objects_delete | BEFORE | DELETE | EXECUTE FUNCTION storage.protect_delete() |
| storage.objects | update_objects_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION storage.update_updated_at_column() |

## education / _supabase

Schemas: `_analytics`, `_supavisor`, `public`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |

## education / postgres

Schemas: `_realtime`, `auth`, `extensions`, `graphql`, `graphql_public`, `net`, `public`, `realtime`, `speaksy`, `storage`, `supabase_functions`, `vault`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| _realtime.extensions | table | 1 | False |
| _realtime.feature_flags | table | 1 | False |
| _realtime.schema_migrations | table | 33 | False |
| _realtime.tenants | table | 1 | False |
| auth.audit_log_entries | table | 0 | True |
| auth.custom_oauth_providers | table | 0 | False |
| auth.flow_state | table | 0 | True |
| auth.identities | table | 0 | True |
| auth.instances | table | 0 | True |
| auth.mfa_amr_claims | table | 0 | True |
| auth.mfa_challenges | table | 0 | True |
| auth.mfa_factors | table | 0 | True |
| auth.oauth_authorizations | table | 0 | False |
| auth.oauth_client_states | table | 0 | False |
| auth.oauth_clients | table | 0 | False |
| auth.oauth_consents | table | 0 | False |
| auth.one_time_tokens | table | 0 | True |
| auth.refresh_tokens | table | 0 | True |
| auth.saml_providers | table | 0 | True |
| auth.saml_relay_states | table | 0 | True |
| auth.schema_migrations | table | 77 | True |
| auth.sessions | table | 0 | True |
| auth.sso_domains | table | 0 | True |
| auth.sso_providers | table | 0 | True |
| auth.users | table | 0 | True |
| auth.webauthn_challenges | table | 0 | False |
| auth.webauthn_credentials | table | 0 | False |
| extensions.pg_stat_statements | view (not counted) | N/A | False |
| extensions.pg_stat_statements_info | view (not counted) | N/A | False |
| net._http_response | table | 0 | False |
| net.http_request_queue | table | 0 | False |
| public.speaksy_migrations | table | 10 | False |
| realtime.messages | partitioned table | 0 | True |
| realtime.messages_2026_09_23 | table | 0 | False |
| realtime.messages_2026_09_24 | table | 0 | False |
| realtime.messages_2026_09_25 | table | 0 | False |
| realtime.messages_2026_09_26 | table | 0 | False |
| realtime.messages_2026_09_27 | table | 0 | False |
| realtime.schema_migrations | table | 82 | False |
| realtime.subscription | table | 0 | False |
| speaksy.audit_log | table | 157 | True |
| speaksy.call_events | table | 9882 | True |
| speaksy.call_transcripts | table | 1633 | True |
| speaksy.call_turns | table | 500 | True |
| speaksy.calls | table | 549 | True |
| speaksy.campaigns | table | 63 | True |
| speaksy.followups | table | 0 | True |
| speaksy.heartbeats | table | 267 | True |
| speaksy.leads | table | 269 | True |
| speaksy.reminder_settings | table | 1 | True |
| speaksy.student_enquiries | table | 0 | True |
| speaksy.suppressions | table | 2 | True |
| speaksy.tenants | table | 1 | True |
| storage.buckets | table | 1 | True |
| storage.buckets_analytics | table | 0 | True |
| storage.buckets_vectors | table | 0 | True |
| storage.iceberg_namespaces | table | 0 | True |
| storage.iceberg_tables | table | 0 | True |
| storage.migrations | table | 70 | True |
| storage.objects | table | 349 | True |
| storage.s3_multipart_uploads | table | 0 | True |
| storage.s3_multipart_uploads_parts | table | 0 | True |
| storage.vector_indexes | table | 0 | True |
| supabase_functions.hooks | table | 0 | False |
| supabase_functions.migrations | table | 2 | False |
| vault.decrypted_secrets | view (not counted) | N/A | False |
| vault.secrets | table | 0 | False |

### public.speaksy_migrations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| name | text | NO |
| sha256 | text | NO |
| applied_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| applied_at | 2026-09-24T13:16:07.580278+00:00 | 2026-09-25T10:40:58.921367+00:00 | 10 |

### speaksy.audit_log

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| actor | text | NO |
| action | text | NO |
| entity_id | uuid | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:22:51.133815+00:00 | 2026-09-29T05:24:28.704023+00:00 | 157 |

### speaksy.call_events

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| call_id | uuid | NO |
| event_key | text | NO |
| kind | text | NO |
| payload | jsonb | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:22:52.720616+00:00 | 2026-09-29T05:24:50.182605+00:00 | 9882 |

### speaksy.call_transcripts

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| call_id | uuid | NO |
| item_id | text | NO |
| role | text | NO |
| text | text | NO |
| interrupted | boolean | NO |
| spoken_at | timestamp with time zone | NO |
| offset_seconds | double precision | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| spoken_at | 2026-09-24T17:28:54.467655+00:00 | 2026-09-27T03:55:52.374585+00:00 | 1633 |

### speaksy.call_turns

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| call_id | uuid | NO |
| turn | integer | NO |
| intent | text | YES |
| language | text | YES |
| topics | jsonb | NO |
| classification_ms | double precision | YES |
| response_ms | double precision | YES |
| stt_delay_ms | double precision | YES |
| tts_ttfb_ms | double precision | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T17:29:07.991085+00:00 | 2026-09-27T03:55:52.371161+00:00 | 500 |

### speaksy.calls

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| campaign_id | uuid | NO |
| lead_id | uuid | NO |
| status | text | NO |
| idempotency_key | text | NO |
| room_name | text | NO |
| dispatch_id | text | YES |
| worker_token | uuid | YES |
| snapshot | jsonb | NO |
| config_hash | text | NO |
| outcome | text | YES |
| error_code | text | YES |
| queued_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| started_at | timestamp with time zone | YES |
| ended_at | timestamp with time zone | YES |
| reminder_profile | text | YES |
| reminder_event | jsonb | YES |
| scheduled_for | timestamp with time zone | YES |
| reminder_deadline | timestamp with time zone | YES |
| direct_call | boolean | NO |
| from_number | text | YES |
| ended_by | text | YES |
| end_reason | text | YES |
| duration_seconds | double precision | YES |
| recording_path | text | YES |
| recording_status | text | YES |
| egress_id | text | YES |
| manual_reauthorized | boolean | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| queued_at | 2026-09-24T13:22:51.156488+00:00 | 2026-09-29T05:24:28.704023+00:00 | 549 |
| updated_at | 2026-09-24T13:22:52.710254+00:00 | 2026-09-29T05:26:30.110349+00:00 | 549 |
| started_at | 2026-09-24T13:32:57.897341+00:00 | 2026-09-27T03:55:12.185335+00:00 | 228 |
| ended_at | 2026-09-24T13:22:52.710254+00:00 | 2026-09-29T05:26:30.110349+00:00 | 549 |
| scheduled_for | 2026-09-24T14:45:01.022828+00:00 | 2026-09-29T05:24:28.706705+00:00 | 544 |
| reminder_deadline | 2026-09-24T15:00:01.022828+00:00 | 2026-10-04T03:12:22.466447+00:00 | 544 |

### speaksy.campaigns

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| name | text | NO |
| status | text | NO |
| snapshot | jsonb | NO |
| config_hash | text | NO |
| created_at | timestamp with time zone | NO |
| reminder_profile | text | YES |
| reminder_event | jsonb | YES |
| reminder_lead_ids | ARRAY | YES |
| scheduled_for | timestamp with time zone | YES |
| reminder_deadline | timestamp with time zone | YES |
| outbound_list | boolean | NO |
| call_timezone | text | NO |
| window_start | time without time zone | NO |
| window_end | time without time zone | NO |
| delay_seconds | integer | NO |
| request_id | uuid | YES |
| request_payload | jsonb | YES |
| respect_window | boolean | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:22:51.146737+00:00 | 2026-09-29T05:24:28.704023+00:00 | 63 |
| scheduled_for | 2026-09-24T14:45:01.022828+00:00 | 2026-09-29T05:24:28.706705+00:00 | 58 |
| reminder_deadline | 2026-09-24T15:00:01.022828+00:00 | 2026-10-04T03:12:22.466447+00:00 | 58 |

### speaksy.followups

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| call_id | uuid | NO |
| kind | text | NO |
| note | text | NO |
| status | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### speaksy.heartbeats

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| component | text | NO |
| instance_id | text | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| updated_at | 2026-09-24T13:23:35.062575+00:00 | 2026-10-06T12:18:30.441853+00:00 | 267 |

### speaksy.leads

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| name | text | NO |
| phone | text | NO |
| consent_source | text | NO |
| consent_at | timestamp with time zone | NO |
| consent_expires_at | timestamp with time zone | NO |
| preferred_language | text | NO |
| opted_out | boolean | NO |
| created_at | timestamp with time zone | NO |
| registered_event_url | text | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| consent_at | 2026-09-24T13:21:51.113122+00:00 | 2026-09-26T16:31:14.696768+00:00 | 269 |
| consent_expires_at | 2026-09-24T13:34:34.040796+00:00 | 2026-09-26T16:31:15.696768+00:00 | 269 |
| created_at | 2026-09-24T13:22:51.133815+00:00 | 2026-09-26T16:31:16.696768+00:00 | 269 |

### speaksy.reminder_settings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| active_profile | text | NO |
| event_overrides | jsonb | NO |
| updated_at | timestamp with time zone | NO |
| call_usage_started_at | timestamp with time zone | YES |
| call_usage_baseline_seconds | double precision | NO |
| cartesia_rotated_at | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| updated_at | 2026-09-28T14:20:53.642277+00:00 | 2026-09-28T14:20:53.642277+00:00 | 1 |
| call_usage_started_at | 2026-09-25T10:33:15.978324+00:00 | 2026-09-25T10:33:15.978324+00:00 | 1 |
| cartesia_rotated_at | 2026-09-27T03:34:25.737754+00:00 | 2026-09-27T03:34:25.737754+00:00 | 1 |

### speaksy.student_enquiries

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| lead_id | uuid | NO |
| country | text | YES |
| course | text | YES |
| intake | text | YES |
| budget | numeric | YES |
| application_stage | text | YES |
| source | text | YES |
| approved_by | text | YES |
| verified_at | timestamp with time zone | YES |
| expires_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| verified_at | N/A | N/A | 0 |
| expires_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### speaksy.suppressions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| phone | text | NO |
| reason | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-25T09:33:32.127424+00:00 | 2026-09-26T15:41:02.372182+00:00 | 2 |

### speaksy.tenants

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:16:07.580278+00:00 | 2026-09-24T13:16:07.580278+00:00 | 1 |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |
| public.speaksy_migrations | speaksy_migrations_pkey | p | PRIMARY KEY (name) |
| speaksy.audit_log | audit_log_pkey | p | PRIMARY KEY (id) |
| speaksy.audit_log | audit_log_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.call_events | call_events_pkey | p | PRIMARY KEY (id) |
| speaksy.call_events | call_events_tenant_id_call_id_event_key_key | u | UNIQUE (tenant_id, call_id, event_key) |
| speaksy.call_events | call_events_tenant_id_call_id_fkey | f | FOREIGN KEY (tenant_id, call_id) REFERENCES speaksy.calls(tenant_id, id) |
| speaksy.call_transcripts | call_transcripts_pkey | p | PRIMARY KEY (tenant_id, call_id, item_id) |
| speaksy.call_transcripts | call_transcripts_role_check | c | CHECK ((role = ANY (ARRAY['user'::text, 'assistant'::text]))) |
| speaksy.call_transcripts | call_transcripts_tenant_id_call_id_fkey | f | FOREIGN KEY (tenant_id, call_id) REFERENCES speaksy.calls(tenant_id, id) |
| speaksy.call_turns | call_turns_pkey | p | PRIMARY KEY (tenant_id, call_id, turn) |
| speaksy.call_turns | call_turns_tenant_id_call_id_fkey | f | FOREIGN KEY (tenant_id, call_id) REFERENCES speaksy.calls(tenant_id, id) |
| speaksy.calls | calls_pkey | p | PRIMARY KEY (id) |
| speaksy.calls | calls_room_name_key | u | UNIQUE (room_name) |
| speaksy.calls | calls_status_check | c | CHECK ((status = ANY (ARRAY['queued'::text, 'dispatching'::text, 'dispatched'::text, 'initializing'::text, 'dialing'::text, 'active'::text, 'terminating'::text, 'completed'::text, 'failed'::text, 'cancelled'::text, 'needs_review'::text]))) |
| speaksy.calls | calls_tenant_id_campaign_id_fkey | f | FOREIGN KEY (tenant_id, campaign_id) REFERENCES speaksy.campaigns(tenant_id, id) |
| speaksy.calls | calls_tenant_id_campaign_id_lead_id_key | u | UNIQUE (tenant_id, campaign_id, lead_id) |
| speaksy.calls | calls_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.calls | calls_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.calls | calls_tenant_id_idempotency_key_key | u | UNIQUE (tenant_id, idempotency_key) |
| speaksy.calls | calls_tenant_id_lead_id_fkey | f | FOREIGN KEY (tenant_id, lead_id) REFERENCES speaksy.leads(tenant_id, id) |
| speaksy.calls | manual_reauthorization_requires_direct_call | c | CHECK (((NOT manual_reauthorized) OR direct_call)) |
| speaksy.campaigns | campaigns_config_hash_check | c | CHECK ((length(config_hash) = 64)) |
| speaksy.campaigns | campaigns_delay_seconds_check | c | CHECK (((delay_seconds >= 20) AND (delay_seconds <= 600))) |
| speaksy.campaigns | campaigns_name_check | c | CHECK (((length(name) >= 1) AND (length(name) <= 100))) |
| speaksy.campaigns | campaigns_pkey | p | PRIMARY KEY (id) |
| speaksy.campaigns | campaigns_reminder_profile_check | c | CHECK ((reminder_profile = ANY (ARRAY['day_before_event_reminder'::text, 'pre_event_reminder'::text]))) |
| speaksy.campaigns | campaigns_status_check | c | CHECK ((status = ANY (ARRAY['draft'::text, 'running'::text, 'paused'::text, 'stopped'::text, 'completed'::text]))) |
| speaksy.campaigns | campaigns_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.campaigns | campaigns_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.followups | followups_note_check | c | CHECK ((length(note) <= 1000)) |
| speaksy.followups | followups_pkey | p | PRIMARY KEY (id) |
| speaksy.followups | followups_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'done'::text]))) |
| speaksy.followups | followups_tenant_id_call_id_fkey | f | FOREIGN KEY (tenant_id, call_id) REFERENCES speaksy.calls(tenant_id, id) |
| speaksy.followups | followups_tenant_id_call_id_kind_key | u | UNIQUE (tenant_id, call_id, kind) |
| speaksy.heartbeats | heartbeats_pkey | p | PRIMARY KEY (tenant_id, component, instance_id) |
| speaksy.heartbeats | heartbeats_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.leads | leads_check | c | CHECK ((consent_expires_at > consent_at)) |
| speaksy.leads | leads_consent_source_check | c | CHECK (((length(consent_source) >= 5) AND (length(consent_source) <= 500))) |
| speaksy.leads | leads_name_check | c | CHECK (((length(name) >= 1) AND (length(name) <= 100))) |
| speaksy.leads | leads_phone_check | c | CHECK ((phone ~ '^\+[1-9][0-9]{7,14}$'::text)) |
| speaksy.leads | leads_pkey | p | PRIMARY KEY (id) |
| speaksy.leads | leads_preferred_language_check | c | CHECK ((preferred_language = ANY (ARRAY['tinglish'::text, 'hinglish'::text, 'en'::text, 'mr'::text]))) |
| speaksy.leads | leads_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.leads | leads_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.leads | leads_tenant_id_phone_key | u | UNIQUE (tenant_id, phone) |
| speaksy.reminder_settings | reminder_settings_active_profile_check | c | CHECK ((active_profile = ANY (ARRAY['day_before_event_reminder'::text, 'pre_event_reminder'::text]))) |
| speaksy.reminder_settings | reminder_settings_call_usage_baseline_seconds_check | c | CHECK ((call_usage_baseline_seconds >= (0)::double precision)) |
| speaksy.reminder_settings | reminder_settings_pkey | p | PRIMARY KEY (tenant_id) |
| speaksy.reminder_settings | reminder_settings_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.student_enquiries | student_enquiries_application_stage_check | c | CHECK ((application_stage = ANY (ARRAY['exploring'::text, 'shortlisting'::text, 'applying'::text, 'submitted'::text, 'closed'::text]))) |
| speaksy.student_enquiries | student_enquiries_budget_check | c | CHECK ((budget >= (0)::numeric)) |
| speaksy.student_enquiries | student_enquiries_check | c | CHECK ((((verified_at IS NULL) AND (expires_at IS NULL) AND (approved_by IS NULL)) OR ((source IS NOT NULL) AND (approved_by IS NOT NULL) AND (verified_at IS NOT NULL) AND (expires_at > verified_at)))) |
| speaksy.student_enquiries | student_enquiries_pkey | p | PRIMARY KEY (id) |
| speaksy.student_enquiries | student_enquiries_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.student_enquiries | student_enquiries_tenant_id_lead_id_fkey | f | FOREIGN KEY (tenant_id, lead_id) REFERENCES speaksy.leads(tenant_id, id) |
| speaksy.suppressions | suppressions_pkey | p | PRIMARY KEY (tenant_id, phone) |
| speaksy.suppressions | suppressions_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.tenants | tenants_pkey | p | PRIMARY KEY (id) |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |
| public.speaksy_migrations | speaksy_migrations_pkey | CREATE UNIQUE INDEX speaksy_migrations_pkey ON public.speaksy_migrations USING btree (name) |
| speaksy.audit_log | audit_log_pkey | CREATE UNIQUE INDEX audit_log_pkey ON speaksy.audit_log USING btree (id) |
| speaksy.call_events | call_events_pkey | CREATE UNIQUE INDEX call_events_pkey ON speaksy.call_events USING btree (id) |
| speaksy.call_events | call_events_recent | CREATE INDEX call_events_recent ON speaksy.call_events USING btree (tenant_id, call_id, created_at) |
| speaksy.call_events | call_events_tenant_id_call_id_event_key_key | CREATE UNIQUE INDEX call_events_tenant_id_call_id_event_key_key ON speaksy.call_events USING btree (tenant_id, call_id, event_key) |
| speaksy.call_transcripts | call_transcripts_pkey | CREATE UNIQUE INDEX call_transcripts_pkey ON speaksy.call_transcripts USING btree (tenant_id, call_id, item_id) |
| speaksy.call_turns | call_turns_pkey | CREATE UNIQUE INDEX call_turns_pkey ON speaksy.call_turns USING btree (tenant_id, call_id, turn) |
| speaksy.calls | call_cooldown | CREATE INDEX call_cooldown ON speaksy.calls USING btree (tenant_id, ended_at DESC) WHERE (ended_at IS NOT NULL) |
| speaksy.calls | calls_campaign | CREATE INDEX calls_campaign ON speaksy.calls USING btree (tenant_id, campaign_id) |
| speaksy.calls | calls_pkey | CREATE UNIQUE INDEX calls_pkey ON speaksy.calls USING btree (id) |
| speaksy.calls | calls_queue | CREATE INDEX calls_queue ON speaksy.calls USING btree (tenant_id, status, queued_at) |
| speaksy.calls | calls_room_name_key | CREATE UNIQUE INDEX calls_room_name_key ON speaksy.calls USING btree (room_name) |
| speaksy.calls | calls_tenant_id_campaign_id_lead_id_key | CREATE UNIQUE INDEX calls_tenant_id_campaign_id_lead_id_key ON speaksy.calls USING btree (tenant_id, campaign_id, lead_id) |
| speaksy.calls | calls_tenant_id_id_key | CREATE UNIQUE INDEX calls_tenant_id_id_key ON speaksy.calls USING btree (tenant_id, id) |
| speaksy.calls | calls_tenant_id_idempotency_key_key | CREATE UNIQUE INDEX calls_tenant_id_idempotency_key_key ON speaksy.calls USING btree (tenant_id, idempotency_key) |
| speaksy.calls | reminder_due | CREATE INDEX reminder_due ON speaksy.calls USING btree (tenant_id, scheduled_for) WHERE (status = 'queued'::text) |
| speaksy.campaigns | campaigns_pkey | CREATE UNIQUE INDEX campaigns_pkey ON speaksy.campaigns USING btree (id) |
| speaksy.campaigns | campaigns_tenant_id_id_key | CREATE UNIQUE INDEX campaigns_tenant_id_id_key ON speaksy.campaigns USING btree (tenant_id, id) |
| speaksy.campaigns | outbound_campaign_request | CREATE UNIQUE INDEX outbound_campaign_request ON speaksy.campaigns USING btree (tenant_id, request_id) WHERE (request_id IS NOT NULL) |
| speaksy.followups | followups_pkey | CREATE UNIQUE INDEX followups_pkey ON speaksy.followups USING btree (id) |
| speaksy.followups | followups_tenant_id_call_id_kind_key | CREATE UNIQUE INDEX followups_tenant_id_call_id_kind_key ON speaksy.followups USING btree (tenant_id, call_id, kind) |
| speaksy.heartbeats | heartbeats_pkey | CREATE UNIQUE INDEX heartbeats_pkey ON speaksy.heartbeats USING btree (tenant_id, component, instance_id) |
| speaksy.leads | leads_pkey | CREATE UNIQUE INDEX leads_pkey ON speaksy.leads USING btree (id) |
| speaksy.leads | leads_tenant_id_id_key | CREATE UNIQUE INDEX leads_tenant_id_id_key ON speaksy.leads USING btree (tenant_id, id) |
| speaksy.leads | leads_tenant_id_phone_key | CREATE UNIQUE INDEX leads_tenant_id_phone_key ON speaksy.leads USING btree (tenant_id, phone) |
| speaksy.reminder_settings | reminder_settings_pkey | CREATE UNIQUE INDEX reminder_settings_pkey ON speaksy.reminder_settings USING btree (tenant_id) |
| speaksy.student_enquiries | student_enquiries_lead | CREATE INDEX student_enquiries_lead ON speaksy.student_enquiries USING btree (tenant_id, lead_id) |
| speaksy.student_enquiries | student_enquiries_pkey | CREATE UNIQUE INDEX student_enquiries_pkey ON speaksy.student_enquiries USING btree (id) |
| speaksy.student_enquiries | student_enquiries_tenant_id_id_key | CREATE UNIQUE INDEX student_enquiries_tenant_id_id_key ON speaksy.student_enquiries USING btree (tenant_id, id) |
| speaksy.suppressions | suppressions_pkey | CREATE UNIQUE INDEX suppressions_pkey ON speaksy.suppressions USING btree (tenant_id, phone) |
| speaksy.tenants | tenants_pkey | CREATE UNIQUE INDEX tenants_pkey ON speaksy.tenants USING btree (id) |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |
| auth | 4 |
| extensions | 55 |
| graphql_public | 1 |
| net | 12 |
| pgbouncer | 1 |
| realtime | 15 |
| storage | 19 |
| supabase_functions | 1 |
| vault | 5 |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |
| auth.email |  | text |
| auth.jwt |  | jsonb |
| auth.role |  | text |
| auth.uid |  | uuid |
| extensions.armor | bytea, text[], text[] | text |
| extensions.armor | bytea | text |
| extensions.crypt | text, text | text |
| extensions.dearmor | text | bytea |
| extensions.decrypt | bytea, bytea, text | bytea |
| extensions.decrypt_iv | bytea, bytea, bytea, text | bytea |
| extensions.digest | bytea, text | bytea |
| extensions.digest | text, text | bytea |
| extensions.encrypt | bytea, bytea, text | bytea |
| extensions.encrypt_iv | bytea, bytea, bytea, text | bytea |
| extensions.gen_random_bytes | integer | bytea |
| extensions.gen_random_uuid |  | uuid |
| extensions.gen_salt | text | text |
| extensions.gen_salt | text, integer | text |
| extensions.grant_pg_cron_access |  | event_trigger |
| extensions.grant_pg_graphql_access |  | event_trigger |
| extensions.grant_pg_net_access |  | event_trigger |
| extensions.hmac | bytea, bytea, text | bytea |
| extensions.hmac | text, text, text | bytea |
| extensions.pg_stat_statements | showtext boolean, OUT userid oid, OUT dbid oid, OUT toplevel boolean, OUT queryid bigint, OUT query text, OUT plans bigint, OUT total_plan_time double precision, OUT min_plan_time double precision, OUT max_plan_time double precision, OUT mean_plan_time double precision, OUT stddev_plan_time double precision, OUT calls bigint, OUT total_exec_time double precision, OUT min_exec_time double precision, OUT max_exec_time double precision, OUT mean_exec_time double precision, OUT stddev_exec_time double precision, OUT rows bigint, OUT shared_blks_hit bigint, OUT shared_blks_read bigint, OUT shared_blks_dirtied bigint, OUT shared_blks_written bigint, OUT local_blks_hit bigint, OUT local_blks_read bigint, OUT local_blks_dirtied bigint, OUT local_blks_written bigint, OUT temp_blks_read bigint, OUT temp_blks_written bigint, OUT shared_blk_read_time double precision, OUT shared_blk_write_time double precision, OUT local_blk_read_time double precision, OUT local_blk_write_time double precision, OUT temp_blk_read_time double precision, OUT temp_blk_write_time double precision, OUT wal_records bigint, OUT wal_fpi bigint, OUT wal_bytes numeric, OUT jit_functions bigint, OUT jit_generation_time double precision, OUT jit_inlining_count bigint, OUT jit_inlining_time double precision, OUT jit_optimization_count bigint, OUT jit_optimization_time double precision, OUT jit_emission_count bigint, OUT jit_emission_time double precision, OUT jit_deform_count bigint, OUT jit_deform_time double precision, OUT stats_since timestamp with time zone, OUT minmax_stats_since timestamp with time zone | SETOF record |
| extensions.pg_stat_statements_info | OUT dealloc bigint, OUT stats_reset timestamp with time zone | record |
| extensions.pg_stat_statements_reset | userid oid, dbid oid, queryid bigint, minmax_only boolean | timestamp with time zone |
| extensions.pgp_armor_headers | text, OUT key text, OUT value text | SETOF record |
| extensions.pgp_key_id | bytea | text |
| extensions.pgp_pub_decrypt | bytea, bytea, text | text |
| extensions.pgp_pub_decrypt | bytea, bytea, text, text | text |
| extensions.pgp_pub_decrypt | bytea, bytea | text |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea, text | bytea |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea, text, text | bytea |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea | bytea |
| extensions.pgp_pub_encrypt | text, bytea, text | bytea |
| extensions.pgp_pub_encrypt | text, bytea | bytea |
| extensions.pgp_pub_encrypt_bytea | bytea, bytea | bytea |
| extensions.pgp_pub_encrypt_bytea | bytea, bytea, text | bytea |
| extensions.pgp_sym_decrypt | bytea, text, text | text |
| extensions.pgp_sym_decrypt | bytea, text | text |
| extensions.pgp_sym_decrypt_bytea | bytea, text, text | bytea |
| extensions.pgp_sym_decrypt_bytea | bytea, text | bytea |
| extensions.pgp_sym_encrypt | text, text, text | bytea |
| extensions.pgp_sym_encrypt | text, text | bytea |
| extensions.pgp_sym_encrypt_bytea | bytea, text | bytea |
| extensions.pgp_sym_encrypt_bytea | bytea, text, text | bytea |
| extensions.pgrst_ddl_watch |  | event_trigger |
| extensions.pgrst_drop_watch |  | event_trigger |
| extensions.set_graphql_placeholder |  | event_trigger |
| extensions.uuid_generate_v1 |  | uuid |
| extensions.uuid_generate_v1mc |  | uuid |
| extensions.uuid_generate_v3 | namespace uuid, name text | uuid |
| extensions.uuid_generate_v4 |  | uuid |
| extensions.uuid_generate_v5 | namespace uuid, name text | uuid |
| extensions.uuid_nil |  | uuid |
| extensions.uuid_ns_dns |  | uuid |
| extensions.uuid_ns_oid |  | uuid |
| extensions.uuid_ns_url |  | uuid |
| extensions.uuid_ns_x500 |  | uuid |
| graphql_public.graphql | "operationName" text, query text, variables jsonb, extensions jsonb | jsonb |
| net._await_response | request_id bigint | boolean |
| net._encode_url_with_params_array | url text, params_array text[] | text |
| net._http_collect_response | request_id bigint, async boolean | net.http_response_result |
| net._urlencode_string | string character varying | text |
| net.check_worker_is_up |  | void |
| net.http_collect_response | request_id bigint, async boolean | net.http_response_result |
| net.http_delete | url text, params jsonb, headers jsonb, timeout_milliseconds integer, body jsonb | bigint |
| net.http_get | url text, params jsonb, headers jsonb, timeout_milliseconds integer | bigint |
| net.http_post | url text, body jsonb, params jsonb, headers jsonb, timeout_milliseconds integer | bigint |
| net.wait_until_running |  | void |
| net.wake |  | void |
| net.worker_restart |  | boolean |
| pgbouncer.get_auth | p_usename text | TABLE(username text, password text) |
| realtime.apply_rls | wal jsonb, max_record_bytes integer | SETOF realtime.wal_rls |
| realtime.broadcast_changes | topic_name text, event_name text, operation text, table_name text, table_schema text, new record, old record, level text | void |
| realtime.build_prepared_statement_sql | prepared_statement_name text, entity regclass, columns realtime.wal_column[] | text |
| realtime.cast | val text, type_ regtype | jsonb |
| realtime.check_equality_op | op realtime.equality_op, type_ regtype, val_1 text, val_2 text, negate boolean | boolean |
| realtime.check_equality_op | op realtime.equality_op, type_ regtype, val_1 text, val_2 text | boolean |
| realtime.is_visible_through_filters | columns realtime.wal_column[], filters realtime.user_defined_filter[] | boolean |
| realtime.list_changes | publication name, slot_name name, max_changes integer, max_record_bytes integer | TABLE(wal jsonb, is_rls_enabled boolean, subscription_ids uuid[], errors text[], slot_changes_count bigint) |
| realtime.quote_wal2json | entity regclass | text |
| realtime.send | payload jsonb, event text, topic text, private boolean | void |
| realtime.send_binary | payload bytea, event text, topic text, private boolean | void |
| realtime.subscription_check_filters |  | trigger |
| realtime.to_regrole | role_name text | regrole |
| realtime.topic |  | text |
| realtime.wal2json_escape_identifier | name text | text |
| storage.allow_any_operation | expected_operations text[] | boolean |
| storage.allow_only_operation | expected_operation text | boolean |
| storage.can_insert_object | bucketid text, name text, owner uuid, metadata jsonb | void |
| storage.enforce_bucket_lifecycle_service_role |  | trigger |
| storage.enforce_bucket_name_length |  | trigger |
| storage.extension | name text | text |
| storage.filename | name text | text |
| storage.foldername | name text | text[] |
| storage.get_common_prefix | p_key text, p_prefix text, p_delimiter text | text |
| storage.get_size_by_bucket |  | TABLE(size bigint, bucket_id text) |
| storage.list_multipart_uploads_with_delimiter | bucket_id text, prefix_param text, delimiter_param text, max_keys integer, next_key_token text, next_upload_token text | TABLE(key text, id text, created_at timestamp with time zone) |
| storage.list_objects_with_delimiter | _bucket_id text, prefix_param text, delimiter_param text, max_keys integer, start_after text, next_token text, sort_order text | TABLE(name text, id uuid, metadata jsonb, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone) |
| storage.operation |  | text |
| storage.protect_bucket_control_columns |  | trigger |
| storage.protect_delete |  | trigger |
| storage.search | prefix text, bucketname text, limits integer, levels integer, offsets integer, search text, sortcolumn text, sortorder text | TABLE(name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.search_by_timestamp | p_prefix text, p_bucket_id text, p_limit integer, p_level integer, p_start_after text, p_sort_order text, p_sort_column text, p_sort_column_after text | TABLE(key text, name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.search_v2 | prefix text, bucket_name text, limits integer, levels integer, start_after text, sort_order text, sort_column text, sort_column_after text | TABLE(key text, name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.update_updated_at_column |  | trigger |
| supabase_functions.http_request |  | trigger |
| vault._crypto_aead_det_decrypt | message bytea, additional bytea, key_id bigint, context bytea, nonce bytea | bytea |
| vault._crypto_aead_det_encrypt | message bytea, additional bytea, key_id bigint, context bytea, nonce bytea | bytea |
| vault._crypto_aead_det_noncegen |  | bytea |
| vault.create_secret | new_secret text, new_name text, new_description text, new_key_id uuid | uuid |
| vault.update_secret | secret_id uuid, new_secret text, new_name text, new_description text, new_key_id uuid | void |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |
| realtime.subscription | tr_check_filters | BEFORE | UPDATE | EXECUTE FUNCTION realtime.subscription_check_filters() |
| realtime.subscription | tr_check_filters | BEFORE | INSERT | EXECUTE FUNCTION realtime.subscription_check_filters() |
| storage.buckets | enforce_bucket_name_length_trigger | BEFORE | INSERT | EXECUTE FUNCTION storage.enforce_bucket_name_length() |
| storage.buckets | enforce_bucket_name_length_trigger | BEFORE | UPDATE | EXECUTE FUNCTION storage.enforce_bucket_name_length() |
| storage.buckets | protect_bucket_control_insert | BEFORE | INSERT | EXECUTE FUNCTION storage.protect_bucket_control_columns('service_role') |
| storage.buckets | protect_bucket_control_update | BEFORE | UPDATE | EXECUTE FUNCTION storage.protect_bucket_control_columns() |
| storage.buckets | protect_bucket_control_update_role | AFTER | UPDATE | EXECUTE FUNCTION storage.enforce_bucket_lifecycle_service_role('service_role') |
| storage.buckets | protect_buckets_delete | BEFORE | DELETE | EXECUTE FUNCTION storage.protect_delete() |
| storage.objects | protect_objects_delete | BEFORE | DELETE | EXECUTE FUNCTION storage.protect_delete() |
| storage.objects | update_objects_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION storage.update_updated_at_column() |

## education-legacy / postgres

Schemas: `public`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |

## education-legacy / speaksy_education

Schemas: `public`, `speaksy`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| public.speaksy_migrations | table | 5 | False |
| speaksy.audit_log | table | 23 | True |
| speaksy.call_events | table | 500 | True |
| speaksy.calls | table | 8 | True |
| speaksy.campaigns | table | 8 | True |
| speaksy.followups | table | 0 | True |
| speaksy.heartbeats | table | 13 | True |
| speaksy.leads | table | 2 | True |
| speaksy.reminder_settings | table | 1 | True |
| speaksy.student_enquiries | table | 0 | True |
| speaksy.suppressions | table | 0 | True |
| speaksy.tenants | table | 1 | True |

### public.speaksy_migrations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| name | text | NO |
| sha256 | text | NO |
| applied_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| applied_at | 2026-09-24T13:16:07.580278+00:00 | 2026-09-24T14:42:29.038166+00:00 | 5 |

### speaksy.audit_log

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| actor | text | NO |
| action | text | NO |
| entity_id | uuid | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:22:51.133815+00:00 | 2026-09-24T15:13:46.182273+00:00 | 23 |

### speaksy.call_events

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| call_id | uuid | NO |
| event_key | text | NO |
| kind | text | NO |
| payload | jsonb | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:22:52.720616+00:00 | 2026-09-24T15:15:04.281846+00:00 | 500 |

### speaksy.calls

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| campaign_id | uuid | NO |
| lead_id | uuid | NO |
| status | text | NO |
| idempotency_key | text | NO |
| room_name | text | NO |
| dispatch_id | text | YES |
| worker_token | uuid | YES |
| snapshot | jsonb | NO |
| config_hash | text | NO |
| outcome | text | YES |
| error_code | text | YES |
| queued_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| started_at | timestamp with time zone | YES |
| ended_at | timestamp with time zone | YES |
| reminder_profile | text | YES |
| reminder_event | jsonb | YES |
| scheduled_for | timestamp with time zone | YES |
| reminder_deadline | timestamp with time zone | YES |
| direct_call | boolean | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| queued_at | 2026-09-24T13:22:51.156488+00:00 | 2026-09-24T15:13:46.182273+00:00 | 8 |
| updated_at | 2026-09-24T13:22:52.710254+00:00 | 2026-09-24T15:15:04.274026+00:00 | 8 |
| started_at | 2026-09-24T13:32:57.897341+00:00 | 2026-09-24T15:14:12.754179+00:00 | 4 |
| ended_at | 2026-09-24T13:22:52.710254+00:00 | 2026-09-24T15:15:04.274026+00:00 | 8 |
| scheduled_for | 2026-09-24T14:45:01.022828+00:00 | 2026-09-24T15:13:46.187293+00:00 | 3 |
| reminder_deadline | 2026-09-24T15:00:01.022828+00:00 | 2026-09-24T15:28:46.187293+00:00 | 3 |

### speaksy.campaigns

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| name | text | NO |
| status | text | NO |
| snapshot | jsonb | NO |
| config_hash | text | NO |
| created_at | timestamp with time zone | NO |
| reminder_profile | text | YES |
| reminder_event | jsonb | YES |
| reminder_lead_ids | ARRAY | YES |
| scheduled_for | timestamp with time zone | YES |
| reminder_deadline | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:22:51.146737+00:00 | 2026-09-24T15:13:46.182273+00:00 | 8 |
| scheduled_for | 2026-09-24T14:45:01.022828+00:00 | 2026-09-24T15:13:46.187293+00:00 | 3 |
| reminder_deadline | 2026-09-24T15:00:01.022828+00:00 | 2026-09-24T15:28:46.187293+00:00 | 3 |

### speaksy.followups

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| call_id | uuid | NO |
| kind | text | NO |
| note | text | NO |
| status | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### speaksy.heartbeats

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| component | text | NO |
| instance_id | text | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| updated_at | 2026-09-24T13:23:35.062575+00:00 | 2026-09-24T15:47:32.12709+00:00 | 13 |

### speaksy.leads

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| name | text | NO |
| phone | text | NO |
| consent_source | text | NO |
| consent_at | timestamp with time zone | NO |
| consent_expires_at | timestamp with time zone | NO |
| preferred_language | text | NO |
| opted_out | boolean | NO |
| created_at | timestamp with time zone | NO |
| registered_event_url | text | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| consent_at | 2026-09-24T13:21:51.113122+00:00 | 2026-09-24T14:46:19.597071+00:00 | 2 |
| consent_expires_at | 2026-09-24T13:34:34.040796+00:00 | 2026-09-24T14:46:20.597071+00:00 | 2 |
| created_at | 2026-09-24T13:22:51.133815+00:00 | 2026-09-24T14:46:21.597071+00:00 | 2 |

### speaksy.reminder_settings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| active_profile | text | NO |
| event_overrides | jsonb | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| updated_at | 2026-09-24T15:09:44.432736+00:00 | 2026-09-24T15:09:44.432736+00:00 | 1 |

### speaksy.student_enquiries

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| tenant_id | uuid | NO |
| lead_id | uuid | NO |
| country | text | YES |
| course | text | YES |
| intake | text | YES |
| budget | numeric | YES |
| application_stage | text | YES |
| source | text | YES |
| approved_by | text | YES |
| verified_at | timestamp with time zone | YES |
| expires_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| verified_at | N/A | N/A | 0 |
| expires_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### speaksy.suppressions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| tenant_id | uuid | NO |
| phone | text | NO |
| reason | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### speaksy.tenants

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-09-24T13:16:07.580278+00:00 | 2026-09-24T13:16:07.580278+00:00 | 1 |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |
| public.speaksy_migrations | speaksy_migrations_pkey | p | PRIMARY KEY (name) |
| speaksy.audit_log | audit_log_pkey | p | PRIMARY KEY (id) |
| speaksy.audit_log | audit_log_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.call_events | call_events_pkey | p | PRIMARY KEY (id) |
| speaksy.call_events | call_events_tenant_id_call_id_event_key_key | u | UNIQUE (tenant_id, call_id, event_key) |
| speaksy.call_events | call_events_tenant_id_call_id_fkey | f | FOREIGN KEY (tenant_id, call_id) REFERENCES speaksy.calls(tenant_id, id) |
| speaksy.calls | calls_pkey | p | PRIMARY KEY (id) |
| speaksy.calls | calls_room_name_key | u | UNIQUE (room_name) |
| speaksy.calls | calls_status_check | c | CHECK ((status = ANY (ARRAY['queued'::text, 'dispatching'::text, 'dispatched'::text, 'initializing'::text, 'dialing'::text, 'active'::text, 'terminating'::text, 'completed'::text, 'failed'::text, 'cancelled'::text, 'needs_review'::text]))) |
| speaksy.calls | calls_tenant_id_campaign_id_fkey | f | FOREIGN KEY (tenant_id, campaign_id) REFERENCES speaksy.campaigns(tenant_id, id) |
| speaksy.calls | calls_tenant_id_campaign_id_lead_id_key | u | UNIQUE (tenant_id, campaign_id, lead_id) |
| speaksy.calls | calls_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.calls | calls_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.calls | calls_tenant_id_idempotency_key_key | u | UNIQUE (tenant_id, idempotency_key) |
| speaksy.calls | calls_tenant_id_lead_id_fkey | f | FOREIGN KEY (tenant_id, lead_id) REFERENCES speaksy.leads(tenant_id, id) |
| speaksy.campaigns | campaigns_config_hash_check | c | CHECK ((length(config_hash) = 64)) |
| speaksy.campaigns | campaigns_name_check | c | CHECK (((length(name) >= 1) AND (length(name) <= 100))) |
| speaksy.campaigns | campaigns_pkey | p | PRIMARY KEY (id) |
| speaksy.campaigns | campaigns_reminder_profile_check | c | CHECK ((reminder_profile = ANY (ARRAY['day_before_event_reminder'::text, 'pre_event_reminder'::text]))) |
| speaksy.campaigns | campaigns_status_check | c | CHECK ((status = ANY (ARRAY['draft'::text, 'running'::text, 'paused'::text, 'stopped'::text, 'completed'::text]))) |
| speaksy.campaigns | campaigns_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.campaigns | campaigns_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.followups | followups_note_check | c | CHECK ((length(note) <= 1000)) |
| speaksy.followups | followups_pkey | p | PRIMARY KEY (id) |
| speaksy.followups | followups_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'done'::text]))) |
| speaksy.followups | followups_tenant_id_call_id_fkey | f | FOREIGN KEY (tenant_id, call_id) REFERENCES speaksy.calls(tenant_id, id) |
| speaksy.followups | followups_tenant_id_call_id_kind_key | u | UNIQUE (tenant_id, call_id, kind) |
| speaksy.heartbeats | heartbeats_pkey | p | PRIMARY KEY (tenant_id, component, instance_id) |
| speaksy.heartbeats | heartbeats_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.leads | leads_check | c | CHECK ((consent_expires_at > consent_at)) |
| speaksy.leads | leads_consent_source_check | c | CHECK (((length(consent_source) >= 5) AND (length(consent_source) <= 500))) |
| speaksy.leads | leads_name_check | c | CHECK (((length(name) >= 1) AND (length(name) <= 100))) |
| speaksy.leads | leads_phone_check | c | CHECK ((phone ~ '^\+[1-9][0-9]{7,14}$'::text)) |
| speaksy.leads | leads_pkey | p | PRIMARY KEY (id) |
| speaksy.leads | leads_preferred_language_check | c | CHECK ((preferred_language = ANY (ARRAY['tinglish'::text, 'hinglish'::text, 'en'::text, 'mr'::text]))) |
| speaksy.leads | leads_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.leads | leads_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.leads | leads_tenant_id_phone_key | u | UNIQUE (tenant_id, phone) |
| speaksy.reminder_settings | reminder_settings_active_profile_check | c | CHECK ((active_profile = ANY (ARRAY['day_before_event_reminder'::text, 'pre_event_reminder'::text]))) |
| speaksy.reminder_settings | reminder_settings_pkey | p | PRIMARY KEY (tenant_id) |
| speaksy.reminder_settings | reminder_settings_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.student_enquiries | student_enquiries_application_stage_check | c | CHECK ((application_stage = ANY (ARRAY['exploring'::text, 'shortlisting'::text, 'applying'::text, 'submitted'::text, 'closed'::text]))) |
| speaksy.student_enquiries | student_enquiries_budget_check | c | CHECK ((budget >= (0)::numeric)) |
| speaksy.student_enquiries | student_enquiries_check | c | CHECK ((((verified_at IS NULL) AND (expires_at IS NULL) AND (approved_by IS NULL)) OR ((source IS NOT NULL) AND (approved_by IS NOT NULL) AND (verified_at IS NOT NULL) AND (expires_at > verified_at)))) |
| speaksy.student_enquiries | student_enquiries_pkey | p | PRIMARY KEY (id) |
| speaksy.student_enquiries | student_enquiries_tenant_id_id_key | u | UNIQUE (tenant_id, id) |
| speaksy.student_enquiries | student_enquiries_tenant_id_lead_id_fkey | f | FOREIGN KEY (tenant_id, lead_id) REFERENCES speaksy.leads(tenant_id, id) |
| speaksy.suppressions | suppressions_pkey | p | PRIMARY KEY (tenant_id, phone) |
| speaksy.suppressions | suppressions_tenant_id_fkey | f | FOREIGN KEY (tenant_id) REFERENCES speaksy.tenants(id) |
| speaksy.tenants | tenants_pkey | p | PRIMARY KEY (id) |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |
| public.speaksy_migrations | speaksy_migrations_pkey | CREATE UNIQUE INDEX speaksy_migrations_pkey ON public.speaksy_migrations USING btree (name) |
| speaksy.audit_log | audit_log_pkey | CREATE UNIQUE INDEX audit_log_pkey ON speaksy.audit_log USING btree (id) |
| speaksy.call_events | call_events_pkey | CREATE UNIQUE INDEX call_events_pkey ON speaksy.call_events USING btree (id) |
| speaksy.call_events | call_events_recent | CREATE INDEX call_events_recent ON speaksy.call_events USING btree (tenant_id, call_id, created_at) |
| speaksy.call_events | call_events_tenant_id_call_id_event_key_key | CREATE UNIQUE INDEX call_events_tenant_id_call_id_event_key_key ON speaksy.call_events USING btree (tenant_id, call_id, event_key) |
| speaksy.calls | calls_campaign | CREATE INDEX calls_campaign ON speaksy.calls USING btree (tenant_id, campaign_id) |
| speaksy.calls | calls_pkey | CREATE UNIQUE INDEX calls_pkey ON speaksy.calls USING btree (id) |
| speaksy.calls | calls_queue | CREATE INDEX calls_queue ON speaksy.calls USING btree (tenant_id, status, queued_at) |
| speaksy.calls | calls_room_name_key | CREATE UNIQUE INDEX calls_room_name_key ON speaksy.calls USING btree (room_name) |
| speaksy.calls | calls_tenant_id_campaign_id_lead_id_key | CREATE UNIQUE INDEX calls_tenant_id_campaign_id_lead_id_key ON speaksy.calls USING btree (tenant_id, campaign_id, lead_id) |
| speaksy.calls | calls_tenant_id_id_key | CREATE UNIQUE INDEX calls_tenant_id_id_key ON speaksy.calls USING btree (tenant_id, id) |
| speaksy.calls | calls_tenant_id_idempotency_key_key | CREATE UNIQUE INDEX calls_tenant_id_idempotency_key_key ON speaksy.calls USING btree (tenant_id, idempotency_key) |
| speaksy.calls | reminder_due | CREATE INDEX reminder_due ON speaksy.calls USING btree (tenant_id, scheduled_for) WHERE (status = 'queued'::text) |
| speaksy.campaigns | campaigns_pkey | CREATE UNIQUE INDEX campaigns_pkey ON speaksy.campaigns USING btree (id) |
| speaksy.campaigns | campaigns_tenant_id_id_key | CREATE UNIQUE INDEX campaigns_tenant_id_id_key ON speaksy.campaigns USING btree (tenant_id, id) |
| speaksy.followups | followups_pkey | CREATE UNIQUE INDEX followups_pkey ON speaksy.followups USING btree (id) |
| speaksy.followups | followups_tenant_id_call_id_kind_key | CREATE UNIQUE INDEX followups_tenant_id_call_id_kind_key ON speaksy.followups USING btree (tenant_id, call_id, kind) |
| speaksy.heartbeats | heartbeats_pkey | CREATE UNIQUE INDEX heartbeats_pkey ON speaksy.heartbeats USING btree (tenant_id, component, instance_id) |
| speaksy.leads | leads_pkey | CREATE UNIQUE INDEX leads_pkey ON speaksy.leads USING btree (id) |
| speaksy.leads | leads_tenant_id_id_key | CREATE UNIQUE INDEX leads_tenant_id_id_key ON speaksy.leads USING btree (tenant_id, id) |
| speaksy.leads | leads_tenant_id_phone_key | CREATE UNIQUE INDEX leads_tenant_id_phone_key ON speaksy.leads USING btree (tenant_id, phone) |
| speaksy.reminder_settings | reminder_settings_pkey | CREATE UNIQUE INDEX reminder_settings_pkey ON speaksy.reminder_settings USING btree (tenant_id) |
| speaksy.student_enquiries | student_enquiries_lead | CREATE INDEX student_enquiries_lead ON speaksy.student_enquiries USING btree (tenant_id, lead_id) |
| speaksy.student_enquiries | student_enquiries_pkey | CREATE UNIQUE INDEX student_enquiries_pkey ON speaksy.student_enquiries USING btree (id) |
| speaksy.student_enquiries | student_enquiries_tenant_id_id_key | CREATE UNIQUE INDEX student_enquiries_tenant_id_id_key ON speaksy.student_enquiries USING btree (tenant_id, id) |
| speaksy.suppressions | suppressions_pkey | CREATE UNIQUE INDEX suppressions_pkey ON speaksy.suppressions USING btree (tenant_id, phone) |
| speaksy.tenants | tenants_pkey | CREATE UNIQUE INDEX tenants_pkey ON speaksy.tenants USING btree (id) |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |

## ecommerce / _supabase

Schemas: `_analytics`, `_supavisor`, `public`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| _supavisor.cluster_tenants | table | 0 | False |
| _supavisor.clusters | table | 0 | False |
| _supavisor.schema_migrations | table | 22 | False |
| _supavisor.tenants | table | 1 | False |
| _supavisor.users | table | 1 | False |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |

## ecommerce / postgres

Schemas: `_realtime`, `auth`, `extensions`, `graphql`, `graphql_public`, `net`, `public`, `realtime`, `storage`, `supabase_functions`, `vault`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| _realtime.extensions | table | 1 | False |
| _realtime.feature_flags | table | 1 | False |
| _realtime.schema_migrations | table | 33 | False |
| _realtime.tenants | table | 1 | False |
| auth.audit_log_entries | table | 0 | True |
| auth.custom_oauth_providers | table | 0 | False |
| auth.flow_state | table | 0 | True |
| auth.identities | table | 0 | True |
| auth.instances | table | 0 | True |
| auth.mfa_amr_claims | table | 0 | True |
| auth.mfa_challenges | table | 0 | True |
| auth.mfa_factors | table | 0 | True |
| auth.oauth_authorizations | table | 0 | False |
| auth.oauth_client_states | table | 0 | False |
| auth.oauth_clients | table | 0 | False |
| auth.oauth_consents | table | 0 | False |
| auth.one_time_tokens | table | 0 | True |
| auth.refresh_tokens | table | 0 | True |
| auth.saml_providers | table | 0 | True |
| auth.saml_relay_states | table | 0 | True |
| auth.schema_migrations | table | 77 | True |
| auth.sessions | table | 0 | True |
| auth.sso_domains | table | 0 | True |
| auth.sso_providers | table | 0 | True |
| auth.users | table | 0 | True |
| auth.webauthn_challenges | table | 0 | False |
| auth.webauthn_credentials | table | 0 | False |
| extensions.pg_stat_statements | view (not counted) | N/A | False |
| extensions.pg_stat_statements_info | view (not counted) | N/A | False |
| net._http_response | table | 0 | False |
| net.http_request_queue | table | 0 | False |
| public.abandoned_carts | table | 3 | True |
| public.active_calls | table | 0 | True |
| public.agent_knowledge_assignments | table | 0 | True |
| public.agent_knowledge_files | table | 0 | True |
| public.agents | table | 1 | True |
| public.api_tokens | table | 0 | True |
| public.app_kv_store | table | 0 | True |
| public.app_settings | table | 1 | True |
| public.audit_log | table | 99 | True |
| public.calendar_bookings | table | 0 | True |
| public.call_configurations | table | 0 | True |
| public.call_listing_mentions | table | 0 | True |
| public.call_logs | table | 22 | True |
| public.call_transcripts | table | 0 | True |
| public.campaign_listings | table | 0 | True |
| public.campaign_numbers | table | 0 | True |
| public.conversational_flows | table | 0 | True |
| public.crm_sync_log | table | 0 | True |
| public.invitations | table | 0 | True |
| public.knowledge_documents | table | 0 | True |
| public.lead_actions | table | 0 | True |
| public.lead_objections | table | 0 | True |
| public.lead_property_signals | table | 0 | True |
| public.leads | table | 0 | True |
| public.listings | table | 0 | True |
| public.memberships | table | 1 | True |
| public.mfa_factors | table | 0 | True |
| public.mfa_recovery_codes | table | 0 | True |
| public.organizations | table | 1 | True |
| public.outbound_campaigns | table | 0 | True |
| public.password_resets | table | 0 | True |
| public.pin_to_pim_mappings | table | 0 | True |
| public.post_call_actions | table | 0 | True |
| public.post_call_deliveries | table | 0 | True |
| public.sessions | table | 99 | True |
| public.users | table | 1 | True |
| public.v_pin_pim_resolved | view (not counted) | N/A | False |
| public.whatsapp_conversations | table | 0 | True |
| public.whatsapp_messages | table | 0 | True |
| public.whatsapp_sessions | table | 0 | True |
| realtime.messages | partitioned table | 0 | True |
| realtime.messages_2026_10_07 | table | 0 | False |
| realtime.messages_2026_10_08 | table | 0 | False |
| realtime.messages_2026_10_09 | table | 0 | False |
| realtime.messages_2026_10_10 | table | 0 | False |
| realtime.messages_2026_10_11 | table | 0 | False |
| realtime.schema_migrations | table | 82 | False |
| realtime.subscription | table | 0 | False |
| storage.buckets | table | 1 | True |
| storage.buckets_analytics | table | 0 | True |
| storage.buckets_vectors | table | 0 | True |
| storage.iceberg_namespaces | table | 0 | True |
| storage.iceberg_tables | table | 0 | True |
| storage.migrations | table | 70 | True |
| storage.objects | table | 21 | True |
| storage.s3_multipart_uploads | table | 0 | True |
| storage.s3_multipart_uploads_parts | table | 0 | True |
| storage.vector_indexes | table | 0 | True |
| supabase_functions.hooks | table | 0 | False |
| supabase_functions.migrations | table | 2 | False |
| vault.decrypted_secrets | view (not counted) | N/A | False |
| vault.secrets | table | 0 | False |

### public.abandoned_carts

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| org_id | uuid | NO |
| customer_name | text | NO |
| phone | text | NO |
| email | text | NO |
| products | text | NO |
| cart_value | numeric | NO |
| currency | text | NO |
| status | text | NO |
| abandonment_reason | text | NO |
| checkout_url | text | NO |
| notes | text | NO |
| contact_consent | boolean | NO |
| last_call_id | bigint | YES |
| recovered_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| source | text | NO |
| source_cart_id | uuid | YES |
| source_version | integer | NO |
| source_status | text | YES |
| line_items | jsonb | NO |
| customer_details | jsonb | NO |
| first_added_at | timestamp with time zone | YES |
| last_activity_at | timestamp with time zone | YES |
| abandoned_at | timestamp with time zone | YES |
| synced_at | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| recovered_at | N/A | N/A | 0 |
| created_at | 2026-10-08T18:19:04.164616+00:00 | 2026-10-10T05:36:36.45507+00:00 | 3 |
| updated_at | 2026-10-08T18:29:07.909088+00:00 | 2026-10-25T13:05:57.400331+00:00 | 3 |
| first_added_at | 2026-10-08T18:18:30.255672+00:00 | 2026-10-10T05:36:15.306016+00:00 | 3 |
| last_activity_at | 2026-10-08T18:28:53.900249+00:00 | 2026-10-25T13:05:45.885777+00:00 | 3 |
| abandoned_at | 2026-10-08T18:28:53.94828+00:00 | 2026-10-25T13:05:55.659499+00:00 | 3 |
| synced_at | 2026-10-08T18:28:54.358713+00:00 | 2026-10-25T13:05:57.400331+00:00 | 3 |

### public.active_calls

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| room_id | text | NO |
| phone | text | YES |
| caller_name | text | YES |
| status | text | NO |
| agent_id | uuid | YES |
| campaign_id | uuid | YES |
| from_number | text | YES |
| to_number | text | YES |
| started_at | timestamp with time zone | NO |
| last_updated | timestamp with time zone | NO |
| metadata | jsonb | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| started_at | N/A | N/A | 0 |
| last_updated | N/A | N/A | 0 |

### public.agent_knowledge_assignments

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| document_id | text | NO |
| knowledge_data_path | text | YES |
| config_preset | text | YES |
| loaded_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| loaded_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.agent_knowledge_files

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| file_name | text | NO |
| file_path | text | YES |
| storage_path | text | YES |
| file_size | bigint | YES |
| mime_type | text | YES |
| config_preset | text | YES |
| search_enabled | boolean | NO |
| status | text | NO |
| metadata | jsonb | NO |
| added_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| added_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.agents

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| description | text | YES |
| purpose | text | YES |
| system_prompt | text | NO |
| languages | jsonb | NO |
| llm_provider | text | NO |
| llm_model | text | NO |
| temperature | numeric | NO |
| stt_provider | text | NO |
| stt_model | text | YES |
| tts_provider | text | NO |
| tts_voice_id | text | NO |
| welcome_message | text | YES |
| max_call_duration_seconds | integer | NO |
| is_active | boolean | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| metadata | jsonb | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T17:25:21.099358+00:00 | 2026-10-08T17:25:21.099358+00:00 | 1 |
| updated_at | 2026-10-10T05:09:27.548574+00:00 | 2026-10-10T05:09:27.548574+00:00 | 1 |

### public.api_tokens

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| token_hash | text | NO |
| scopes | ARRAY | NO |
| org_id | uuid | NO |
| created_by | uuid | YES |
| expires_at | timestamp with time zone | YES |
| last_used_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| last_used_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.app_kv_store

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| key | text | NO |
| value | jsonb | NO |
| expires_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.app_settings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| key | text | NO |
| value | jsonb | NO |
| description | text | YES |
| updated_at | timestamp with time zone | NO |
| updated_by | text | YES |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| updated_at | 2026-10-08T17:25:21.106576+00:00 | 2026-10-08T17:25:21.106576+00:00 | 1 |

### public.audit_log

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| actor_user_id | uuid | YES |
| org_id | uuid | YES |
| action | text | NO |
| resource_type | text | YES |
| resource_id | text | YES |
| before | jsonb | YES |
| after | jsonb | YES |
| ip | text | YES |
| user_agent | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T17:24:29.894432+00:00 | 2026-10-28T09:13:51.633858+00:00 | 99 |

### public.calendar_bookings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | bigint | YES |
| lead_id | uuid | YES |
| phone | text | NO |
| listing_id | text | YES |
| scheduled_at | timestamp with time zone | NO |
| provider | text | NO |
| external_id | text | YES |
| status | text | NO |
| notes | text | YES |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| scheduled_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.call_configurations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| silence_handling | jsonb | NO |
| end_call_rules | jsonb | NO |
| transfer_routing | jsonb | NO |
| response_behavior | jsonb | NO |
| ambient_sound | jsonb | NO |
| advanced_settings | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.call_listing_mentions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | bigint | NO |
| listing_id | text | NO |
| mention_type | text | NO |
| pin_used | text | YES |
| context | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.call_logs

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | bigint | NO |
| created_at | timestamp with time zone | NO |
| phone_number | text | YES |
| caller_phone | text | YES |
| caller_name | text | YES |
| caller_email | text | YES |
| duration_seconds | integer | YES |
| transcript | text | YES |
| summary | text | YES |
| recording_url | text | YES |
| sentiment | text | YES |
| estimated_cost_usd | numeric | YES |
| call_date | date | YES |
| call_hour | integer | YES |
| call_day_of_week | text | YES |
| was_booked | boolean | NO |
| interrupt_count | integer | NO |
| audio_codec | text | YES |
| call_purpose | text | YES |
| call_summary | text | YES |
| appointment_time | timestamp with time zone | YES |
| tts_voice | text | YES |
| agent_id | uuid | YES |
| call_status | text | NO |
| call_direction | text | NO |
| channel_type | text | NO |
| call_transferred | boolean | NO |
| ended_by | text | YES |
| room_id | text | YES |
| from_number | text | YES |
| to_number | text | YES |
| bulk_call_id | uuid | YES |
| extracted_info | jsonb | NO |
| ai_summary | jsonb | YES |
| migrated_to_re_memory | boolean | YES |
| metadata | jsonb | NO |
| org_id | uuid | YES |
| turn_metrics | jsonb | YES |
| config_hash | text | YES |
| felt_latency_p50_ms | integer | YES |
| felt_latency_p95_ms | integer | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T18:28:55.047893+00:00 | 2026-10-28T09:18:32.148637+00:00 | 22 |
| call_date | N/A | N/A | 0 |
| appointment_time | N/A | N/A | 0 |

### public.call_transcripts

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_room_id | text | NO |
| call_id | bigint | YES |
| phone | text | YES |
| role | text | YES |
| content | text | YES |
| sequence_num | integer | YES |
| created_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.campaign_listings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| campaign_id | uuid | NO |
| listing_id | text | NO |
| sort_order | integer | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.campaign_numbers

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| campaign_id | uuid | NO |
| phone | text | NO |
| status | text | NO |
| dispatch_id | text | YES |
| error_message | text | YES |
| call_log_id | bigint | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.conversational_flows

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| sections | jsonb | NO |
| version | integer | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.crm_sync_log

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | YES |
| phone | text | YES |
| call_id | bigint | YES |
| crm_type | text | NO |
| action | text | NO |
| status | text | NO |
| request_payload | jsonb | NO |
| response_payload | jsonb | YES |
| error_message | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.invitations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| token_hash | text | NO |
| email | USER-DEFINED | NO |
| org_id | uuid | NO |
| role | text | NO |
| invited_by | uuid | YES |
| expires_at | timestamp with time zone | NO |
| accepted_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| accepted_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.knowledge_documents

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| document_id | text | NO |
| doc_type | text | NO |
| title | text | NO |
| content | text | NO |
| department | text | YES |
| language | text | NO |
| tags | jsonb | NO |
| metadata | jsonb | NO |
| embedding_id | text | YES |
| is_active | boolean | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.lead_actions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | text | NO |
| call_log_id | bigint | YES |
| lead_id | uuid | YES |
| action | text | NO |
| performed_at | timestamp with time zone | NO |
| performed_by | text | YES |
| notes | text | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| performed_at | N/A | N/A | 0 |

### public.lead_objections

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | NO |
| phone | text | NO |
| objection_type | text | NO |
| listing_id | text | YES |
| raw_phrase | text | NO |
| script_used | text | NO |
| outcome | text | NO |
| call_id | bigint | YES |
| call_count_at_time | integer | NO |
| call_date | timestamp with time zone | NO |
| created_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| call_date | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.lead_property_signals

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | NO |
| phone | text | NO |
| listing_id | text | NO |
| signal | text | NO |
| price_reaction | text | NO |
| features_liked | jsonb | NO |
| objections_raised | jsonb | NO |
| price_at_signal | integer | YES |
| call_id | bigint | YES |
| call_date | timestamp with time zone | NO |
| created_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| call_date | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.leads

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| lead_id | uuid | NO |
| phone | text | NO |
| stable_name | text | NO |
| role | text | NO |
| budget_min | integer | YES |
| budget_max | integer | YES |
| preferred_areas | jsonb | NO |
| excluded_areas | jsonb | NO |
| must_haves | jsonb | NO |
| deal_breakers | jsonb | NO |
| timeline_weeks | integer | YES |
| loan_status | text | NO |
| decision_factors | jsonb | NO |
| intent_score | numeric | NO |
| deal_stage | text | NO |
| assigned_agent | text | YES |
| assigned_agent_id | uuid | YES |
| call_count | integer | NO |
| last_contact_at | timestamp with time zone | YES |
| language_pref | text | NO |
| notes | text | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| last_contact_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.listings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| listing_id | text | NO |
| pim_sku | text | YES |
| title | text | NO |
| area | text | YES |
| city | text | YES |
| property_type | text | YES |
| bedrooms | integer | YES |
| bathrooms | integer | YES |
| sqft_min | integer | YES |
| sqft_max | integer | YES |
| price_min | bigint | YES |
| price_max | bigint | YES |
| currency | text | NO |
| status | text | NO |
| facts | jsonb | NO |
| amenities | jsonb | NO |
| tags | ARRAY | NO |
| source | text | YES |
| external_url | text | YES |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.memberships

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| org_id | uuid | NO |
| role | text | NO |
| status | text | NO |
| invited_by | uuid | YES |
| joined_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| joined_at | N/A | N/A | 0 |
| created_at | 2026-10-08T17:23:00.038259+00:00 | 2026-10-08T17:23:00.038259+00:00 | 1 |
| updated_at | 2026-10-08T17:23:00.038259+00:00 | 2026-10-08T17:23:00.038259+00:00 | 1 |

### public.mfa_factors

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| type | text | NO |
| secret_encrypted | text | NO |
| confirmed_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| confirmed_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.mfa_recovery_codes

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| code_hash | text | NO |
| used_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| used_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |

### public.organizations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| slug | text | NO |
| status | text | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T17:22:59.759266+00:00 | 2026-10-08T17:22:59.759266+00:00 | 1 |
| updated_at | 2026-10-08T17:22:59.759266+00:00 | 2026-10-08T17:22:59.759266+00:00 | 1 |

### public.outbound_campaigns

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| name | text | NO |
| agent_id | uuid | YES |
| status | text | NO |
| delay_seconds | integer | NO |
| max_concurrent | integer | NO |
| window_start | text | NO |
| window_end | text | NO |
| timezone | text | NO |
| respect_window | boolean | NO |
| total_numbers | integer | NO |
| dispatched | integer | NO |
| succeeded | integer | NO |
| failed | integer | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |
| started_at | timestamp with time zone | YES |
| completed_at | timestamp with time zone | YES |
| org_id | uuid | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |
| started_at | N/A | N/A | 0 |
| completed_at | N/A | N/A | 0 |

### public.password_resets

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| token_hash | text | NO |
| expires_at | timestamp with time zone | NO |
| used_at | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| expires_at | N/A | N/A | 0 |
| used_at | N/A | N/A | 0 |

### public.pin_to_pim_mappings

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| pin | text | NO |
| pim_listing_id | text | NO |
| source | text | NO |
| label | text | YES |
| description | text | YES |
| is_active | boolean | NO |
| priority | integer | NO |
| metadata | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.post_call_actions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| agent_id | uuid | NO |
| delivery_method | text | NO |
| trigger_statuses | jsonb | NO |
| include_summary | boolean | NO |
| include_full_transcript | boolean | NO |
| include_sentiment | boolean | NO |
| include_extracted_info | boolean | NO |
| extracted_variables | jsonb | NO |
| webhook_url | text | YES |
| webhook_headers | jsonb | NO |
| email_recipients | jsonb | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.post_call_deliveries

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| call_id | bigint | NO |
| agent_id | uuid | YES |
| delivery_method | text | NO |
| destination | text | YES |
| status | text | NO |
| http_status | integer | YES |
| response_body | text | YES |
| payload | jsonb | NO |
| error_message | text | YES |
| created_at | timestamp with time zone | NO |
| delivered_at | timestamp with time zone | YES |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |
| delivered_at | N/A | N/A | 0 |

### public.sessions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| user_id | uuid | NO |
| org_id | uuid | YES |
| refresh_token_hash | text | NO |
| user_agent | text | YES |
| ip | text | YES |
| created_at | timestamp with time zone | NO |
| last_seen_at | timestamp with time zone | NO |
| revoked_at | timestamp with time zone | YES |
| expires_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T17:24:29.890376+00:00 | 2026-10-28T09:13:51.629789+00:00 | 99 |
| last_seen_at | 2026-10-08T17:24:29.889483+00:00 | 2026-10-28T09:13:51.628821+00:00 | 99 |
| revoked_at | 2026-10-10T02:54:44.78563+00:00 | 2026-10-27T04:08:50.739613+00:00 | 55 |
| expires_at | 2026-11-07T17:24:29.889483+00:00 | 2026-11-27T09:13:51.628821+00:00 | 99 |

### public.users

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| email | USER-DEFINED | NO |
| password_hash | text | NO |
| display_name | text | YES |
| avatar_url | text | YES |
| status | text | NO |
| email_verified_at | timestamp with time zone | YES |
| last_login_at | timestamp with time zone | YES |
| failed_login_count | integer | NO |
| locked_until | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| email_verified_at | N/A | N/A | 0 |
| last_login_at | N/A | N/A | 0 |
| locked_until | N/A | N/A | 0 |
| created_at | 2026-10-08T17:23:00.027054+00:00 | 2026-10-08T17:23:00.027054+00:00 | 1 |
| updated_at | 2026-10-08T17:41:13.116781+00:00 | 2026-10-08T17:41:13.116781+00:00 | 1 |

### public.v_pin_pim_resolved

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| pin | text | YES |
| source | text | YES |
| label | text | YES |
| is_active | boolean | YES |
| listing_id | text | YES |
| pim_sku | text | YES |
| title | text | YES |
| area | text | YES |
| property_type | text | YES |
| bedrooms | integer | YES |
| price_min | bigint | YES |
| price_max | bigint | YES |
| facts | jsonb | YES |
| status | text | YES |

### public.whatsapp_conversations

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| org_id | uuid | NO |
| whatsapp_number_id | uuid | NO |
| contact_number | text | NO |
| contact_name | text | YES |
| last_message_preview | text | YES |
| last_message_at | timestamp with time zone | YES |
| unread_count | integer | NO |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| last_message_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### public.whatsapp_messages

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| conversation_id | uuid | NO |
| direction | text | NO |
| message_type | text | NO |
| content | text | YES |
| media_url | text | YES |
| sent_by | text | NO |
| status | text | NO |
| wa_message_id | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.whatsapp_sessions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| org_id | uuid | NO |
| phone_number | text | YES |
| creds_json | jsonb | NO |
| keys_json | jsonb | NO |
| status | text | NO |
| connected_at | timestamp with time zone | YES |
| expires_at | timestamp with time zone | YES |
| created_at | timestamp with time zone | NO |
| updated_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| connected_at | N/A | N/A | 0 |
| expires_at | N/A | N/A | 0 |
| created_at | N/A | N/A | 0 |
| updated_at | N/A | N/A | 0 |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |
| public.abandoned_carts | abandoned_carts_cart_value_check | c | CHECK ((cart_value >= (0)::numeric)) |
| public.abandoned_carts | abandoned_carts_currency_check | c | CHECK ((currency = 'INR'::text)) |
| public.abandoned_carts | abandoned_carts_last_call_id_fkey | f | FOREIGN KEY (last_call_id) REFERENCES call_logs(id) |
| public.abandoned_carts | abandoned_carts_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) |
| public.abandoned_carts | abandoned_carts_pkey | p | PRIMARY KEY (id) |
| public.abandoned_carts | abandoned_carts_status_check | c | CHECK ((status = ANY (ARRAY['abandoned'::text, 'contacted'::text, 'recovered'::text, 'closed'::text, 'resumed'::text]))) |
| public.active_calls | active_calls_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.active_calls | active_calls_campaign_id_fkey | f | FOREIGN KEY (campaign_id) REFERENCES outbound_campaigns(id) ON DELETE SET NULL |
| public.active_calls | active_calls_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.active_calls | active_calls_pkey | p | PRIMARY KEY (room_id) |
| public.active_calls | active_calls_status_check | c | CHECK ((status = ANY (ARRAY['ringing'::text, 'active'::text, 'completed'::text, 'failed'::text]))) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_agent_id_document_id_key | u | UNIQUE (agent_id, document_id) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.agent_knowledge_assignments | agent_knowledge_assignments_document_id_fkey | f | FOREIGN KEY (document_id) REFERENCES knowledge_documents(document_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.agent_knowledge_assignments | agent_knowledge_assignments_pkey | p | PRIMARY KEY (id) |
| public.agent_knowledge_files | agent_knowledge_files_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.agent_knowledge_files | agent_knowledge_files_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.agent_knowledge_files | agent_knowledge_files_pkey | p | PRIMARY KEY (id) |
| public.agent_knowledge_files | agent_knowledge_files_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'processing'::text, 'indexed'::text, 'failed'::text]))) |
| public.agents | agents_max_call_duration_seconds_check | c | CHECK ((max_call_duration_seconds > 0)) |
| public.agents | agents_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.agents | agents_pkey | p | PRIMARY KEY (id) |
| public.agents | agents_temperature_check | c | CHECK (((temperature >= (0)::numeric) AND (temperature <= (2)::numeric))) |
| public.api_tokens | api_tokens_created_by_fkey | f | FOREIGN KEY (created_by) REFERENCES users(id) ON DELETE SET NULL |
| public.api_tokens | api_tokens_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.api_tokens | api_tokens_pkey | p | PRIMARY KEY (id) |
| public.api_tokens | api_tokens_token_hash_key | u | UNIQUE (token_hash) |
| public.app_kv_store | app_kv_store_pkey | p | PRIMARY KEY (key) |
| public.app_settings | app_settings_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.app_settings | app_settings_pkey | p | PRIMARY KEY (key) |
| public.audit_log | audit_log_actor_user_id_fkey | f | FOREIGN KEY (actor_user_id) REFERENCES users(id) ON DELETE SET NULL |
| public.audit_log | audit_log_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.audit_log | audit_log_pkey | p | PRIMARY KEY (id) |
| public.calendar_bookings | calendar_bookings_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.calendar_bookings | calendar_bookings_pkey | p | PRIMARY KEY (id) |
| public.calendar_bookings | calendar_bookings_provider_check | c | CHECK ((provider = ANY (ARRAY['cal.com'::text, 'google_calendar'::text, 'manual'::text]))) |
| public.calendar_bookings | calendar_bookings_status_check | c | CHECK ((status = ANY (ARRAY['scheduled'::text, 'confirmed'::text, 'cancelled'::text, 'completed'::text, 'no_show'::text]))) |
| public.call_configurations | call_configurations_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.call_configurations | call_configurations_agent_id_key | u | UNIQUE (agent_id) |
| public.call_configurations | call_configurations_pkey | p | PRIMARY KEY (id) |
| public.call_listing_mentions | call_listing_mentions_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE CASCADE |
| public.call_listing_mentions | call_listing_mentions_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.call_listing_mentions | call_listing_mentions_mention_type_check | c | CHECK ((mention_type = ANY (ARRAY['discussed'::text, 'sent'::text, 'viewed'::text, 'offered'::text, 'rejected'::text, 'booked'::text]))) |
| public.call_listing_mentions | call_listing_mentions_pkey | p | PRIMARY KEY (id) |
| public.call_logs | call_logs_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.call_logs | call_logs_bulk_call_id_fkey | f | FOREIGN KEY (bulk_call_id) REFERENCES outbound_campaigns(id) ON DELETE SET NULL |
| public.call_logs | call_logs_call_direction_check | c | CHECK ((call_direction = ANY (ARRAY['inbound'::text, 'outbound'::text]))) |
| public.call_logs | call_logs_call_hour_check | c | CHECK (((call_hour IS NULL) OR ((call_hour >= 0) AND (call_hour <= 23)))) |
| public.call_logs | call_logs_call_status_check | c | CHECK ((call_status = ANY (ARRAY['ringing'::text, 'active'::text, 'completed'::text, 'failed'::text, 'no_answer'::text, 'voicemail'::text, 'transferred'::text, 'booked'::text, 'archived'::text, 'cancelled'::text]))) |
| public.call_logs | call_logs_channel_type_check | c | CHECK ((channel_type = ANY (ARRAY['phone'::text, 'web'::text, 'sip'::text, 'whatsapp'::text]))) |
| public.call_logs | call_logs_ended_by_check | c | CHECK (((ended_by IS NULL) OR (ended_by = ANY (ARRAY['caller'::text, 'assistant'::text, 'system'::text, 'timeout'::text])))) |
| public.call_logs | call_logs_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.call_logs | call_logs_pkey | p | PRIMARY KEY (id) |
| public.call_logs | fk_call_logs_agent | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.call_logs | fk_call_logs_campaign | f | FOREIGN KEY (bulk_call_id) REFERENCES outbound_campaigns(id) ON DELETE SET NULL |
| public.call_transcripts | call_transcripts_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.call_transcripts | call_transcripts_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.call_transcripts | call_transcripts_pkey | p | PRIMARY KEY (id) |
| public.call_transcripts | call_transcripts_role_check | c | CHECK ((role = ANY (ARRAY['user'::text, 'assistant'::text]))) |
| public.campaign_listings | campaign_listings_campaign_id_fkey | f | FOREIGN KEY (campaign_id) REFERENCES outbound_campaigns(id) ON DELETE CASCADE |
| public.campaign_listings | campaign_listings_campaign_id_listing_id_key | u | UNIQUE (campaign_id, listing_id) |
| public.campaign_listings | campaign_listings_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.campaign_listings | campaign_listings_pkey | p | PRIMARY KEY (id) |
| public.campaign_numbers | campaign_numbers_campaign_id_fkey | f | FOREIGN KEY (campaign_id) REFERENCES outbound_campaigns(id) ON DELETE CASCADE |
| public.campaign_numbers | campaign_numbers_campaign_id_phone_key | u | UNIQUE (campaign_id, phone) |
| public.campaign_numbers | campaign_numbers_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.campaign_numbers | campaign_numbers_pkey | p | PRIMARY KEY (id) |
| public.campaign_numbers | campaign_numbers_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'dispatched'::text, 'completed'::text, 'failed'::text, 'skipped'::text]))) |
| public.conversational_flows | conversational_flows_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.conversational_flows | conversational_flows_agent_id_key | u | UNIQUE (agent_id) |
| public.conversational_flows | conversational_flows_pkey | p | PRIMARY KEY (id) |
| public.conversational_flows | conversational_flows_version_check | c | CHECK ((version >= 1)) |
| public.crm_sync_log | crm_sync_log_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.crm_sync_log | crm_sync_log_crm_type_check | c | CHECK ((crm_type = ANY (ARRAY['hubspot'::text, 'salesforce'::text, 'webhook'::text, 'none'::text]))) |
| public.crm_sync_log | crm_sync_log_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE SET NULL |
| public.crm_sync_log | crm_sync_log_pkey | p | PRIMARY KEY (id) |
| public.crm_sync_log | crm_sync_log_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'success'::text, 'failed'::text]))) |
| public.invitations | invitations_email_org_id_accepted_at_key | u | UNIQUE (email, org_id, accepted_at) |
| public.invitations | invitations_invited_by_fkey | f | FOREIGN KEY (invited_by) REFERENCES users(id) ON DELETE SET NULL |
| public.invitations | invitations_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.invitations | invitations_pkey | p | PRIMARY KEY (id) |
| public.invitations | invitations_role_check | c | CHECK ((role = ANY (ARRAY['admin'::text, 'member'::text, 'viewer'::text]))) |
| public.invitations | invitations_token_hash_key | u | UNIQUE (token_hash) |
| public.knowledge_documents | knowledge_documents_doc_type_check | c | CHECK ((doc_type = ANY (ARRAY['company_info'::text, 'office_info'::text, 'property_listing'::text, 'faq'::text, 'process'::text, 'policy'::text, 'script'::text, 'other'::text]))) |
| public.knowledge_documents | knowledge_documents_document_id_key | u | UNIQUE (document_id) |
| public.knowledge_documents | knowledge_documents_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.knowledge_documents | knowledge_documents_pkey | p | PRIMARY KEY (id) |
| public.lead_actions | lead_actions_action_check | c | CHECK ((action = ANY (ARRAY['send_whatsapp'::text, 'schedule_site_visit'::text, 'mark_booked'::text, 'escalate_human'::text, 'archive'::text]))) |
| public.lead_actions | lead_actions_call_log_id_fkey | f | FOREIGN KEY (call_log_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.lead_actions | lead_actions_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE SET NULL |
| public.lead_actions | lead_actions_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.lead_actions | lead_actions_pkey | p | PRIMARY KEY (id) |
| public.lead_objections | lead_objections_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.lead_objections | lead_objections_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE CASCADE |
| public.lead_objections | lead_objections_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE SET NULL |
| public.lead_objections | lead_objections_objection_type_check | c | CHECK ((objection_type = ANY (ARRAY['price'::text, 'location'::text, 'size'::text, 'amenity'::text, 'timing'::text, 'agent_trust'::text, 'process'::text, 'other'::text]))) |
| public.lead_objections | lead_objections_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.lead_objections | lead_objections_outcome_check | c | CHECK ((outcome = ANY (ARRAY['resolved'::text, 'unresolved'::text, 'escalated'::text, 'deferred'::text]))) |
| public.lead_objections | lead_objections_pkey | p | PRIMARY KEY (id) |
| public.lead_property_signals | lead_property_signals_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE SET NULL |
| public.lead_property_signals | lead_property_signals_lead_id_fkey | f | FOREIGN KEY (lead_id) REFERENCES leads(id) ON DELETE CASCADE |
| public.lead_property_signals | lead_property_signals_listing_id_fkey | f | FOREIGN KEY (listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.lead_property_signals | lead_property_signals_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.lead_property_signals | lead_property_signals_pkey | p | PRIMARY KEY (id) |
| public.lead_property_signals | lead_property_signals_price_reaction_check | c | CHECK ((price_reaction = ANY (ARRAY['positive'::text, 'negative'::text, 'neutral'::text, 'no_reaction'::text]))) |
| public.lead_property_signals | lead_property_signals_signal_check | c | CHECK ((signal = ANY (ARRAY['liked'::text, 'rejected'::text, 'viewed'::text, 'offered'::text, 'sent'::text, 'enquired'::text]))) |
| public.leads | leads_assigned_agent_id_fkey | f | FOREIGN KEY (assigned_agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.leads | leads_deal_stage_check | c | CHECK ((deal_stage = ANY (ARRAY['cold'::text, 'aware'::text, 'interested'::text, 'viewing'::text, 'hot'::text, 'offer'::text, 'closed'::text, 'lost'::text]))) |
| public.leads | leads_language_pref_check | c | CHECK ((language_pref = ANY (ARRAY['en'::text, 'hi'::text, 'hinglish'::text, 'tamil'::text, 'telugu'::text]))) |
| public.leads | leads_lead_id_key | u | UNIQUE (lead_id) |
| public.leads | leads_loan_status_check | c | CHECK ((loan_status = ANY (ARRAY['pre_approved'::text, 'exploring'::text, 'cash'::text, 'unknown'::text]))) |
| public.leads | leads_phone_key | u | UNIQUE (phone) |
| public.leads | leads_pkey | p | PRIMARY KEY (id) |
| public.leads | leads_role_check | c | CHECK ((role = ANY (ARRAY['buyer'::text, 'seller'::text, 'renter'::text, 'investor'::text]))) |
| public.listings | listings_listing_id_key | u | UNIQUE (listing_id) |
| public.listings | listings_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE SET NULL |
| public.listings | listings_pim_sku_key | u | UNIQUE (pim_sku) |
| public.listings | listings_pkey | p | PRIMARY KEY (id) |
| public.listings | listings_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'reserved'::text, 'sold'::text, 'inactive'::text, 'draft'::text]))) |
| public.memberships | memberships_invited_by_fkey | f | FOREIGN KEY (invited_by) REFERENCES users(id) ON DELETE SET NULL |
| public.memberships | memberships_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.memberships | memberships_pkey | p | PRIMARY KEY (id) |
| public.memberships | memberships_role_check | c | CHECK ((role = ANY (ARRAY['owner'::text, 'admin'::text, 'member'::text, 'viewer'::text]))) |
| public.memberships | memberships_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'suspended'::text]))) |
| public.memberships | memberships_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.memberships | memberships_user_id_org_id_key | u | UNIQUE (user_id, org_id) |
| public.mfa_factors | mfa_factors_pkey | p | PRIMARY KEY (id) |
| public.mfa_factors | mfa_factors_type_check | c | CHECK ((type = 'totp'::text)) |
| public.mfa_factors | mfa_factors_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.mfa_factors | mfa_factors_user_id_type_key | u | UNIQUE (user_id, type) |
| public.mfa_recovery_codes | mfa_recovery_codes_pkey | p | PRIMARY KEY (id) |
| public.mfa_recovery_codes | mfa_recovery_codes_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.organizations | organizations_pkey | p | PRIMARY KEY (id) |
| public.organizations | organizations_slug_key | u | UNIQUE (slug) |
| public.organizations | organizations_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'suspended'::text, 'archived'::text]))) |
| public.outbound_campaigns | outbound_campaigns_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.outbound_campaigns | outbound_campaigns_delay_seconds_check | c | CHECK (((delay_seconds >= 0) AND (delay_seconds <= 120))) |
| public.outbound_campaigns | outbound_campaigns_max_concurrent_check | c | CHECK ((max_concurrent >= 1)) |
| public.outbound_campaigns | outbound_campaigns_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.outbound_campaigns | outbound_campaigns_pkey | p | PRIMARY KEY (id) |
| public.outbound_campaigns | outbound_campaigns_status_check | c | CHECK ((status = ANY (ARRAY['draft'::text, 'running'::text, 'paused'::text, 'completed'::text, 'cancelled'::text]))) |
| public.password_resets | password_resets_pkey | p | PRIMARY KEY (id) |
| public.password_resets | password_resets_token_hash_key | u | UNIQUE (token_hash) |
| public.password_resets | password_resets_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pim_listing_id_fkey | f | FOREIGN KEY (pim_listing_id) REFERENCES listings(listing_id) ON UPDATE CASCADE ON DELETE CASCADE |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pin_source_key | u | UNIQUE (pin, source) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pkey | p | PRIMARY KEY (id) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_source_check | c | CHECK ((source = ANY (ARRAY['manual'::text, 'ivr'::text, 'builder_portal'::text, 'crm'::text, 'csv_import'::text, 'api'::text]))) |
| public.post_call_actions | post_call_actions_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE CASCADE |
| public.post_call_actions | post_call_actions_agent_id_key | u | UNIQUE (agent_id) |
| public.post_call_actions | post_call_actions_delivery_method_check | c | CHECK ((delivery_method = ANY (ARRAY['webhook'::text, 'email'::text, 'both'::text, 'none'::text]))) |
| public.post_call_actions | post_call_actions_pkey | p | PRIMARY KEY (id) |
| public.post_call_deliveries | post_call_deliveries_agent_id_fkey | f | FOREIGN KEY (agent_id) REFERENCES agents(id) ON DELETE SET NULL |
| public.post_call_deliveries | post_call_deliveries_call_id_fkey | f | FOREIGN KEY (call_id) REFERENCES call_logs(id) ON DELETE CASCADE |
| public.post_call_deliveries | post_call_deliveries_pkey | p | PRIMARY KEY (id) |
| public.post_call_deliveries | post_call_deliveries_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'sent'::text, 'failed'::text, 'skipped'::text]))) |
| public.sessions | sessions_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.sessions | sessions_pkey | p | PRIMARY KEY (id) |
| public.sessions | sessions_refresh_token_hash_key | u | UNIQUE (refresh_token_hash) |
| public.sessions | sessions_user_id_fkey | f | FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE |
| public.users | users_email_key | u | UNIQUE (email) |
| public.users | users_pkey | p | PRIMARY KEY (id) |
| public.users | users_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'invited'::text, 'suspended'::text, 'deleted'::text]))) |
| public.whatsapp_conversations | whatsapp_conversations_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.whatsapp_conversations | whatsapp_conversations_pkey | p | PRIMARY KEY (id) |
| public.whatsapp_conversations | whatsapp_conversations_unread_count_check | c | CHECK ((unread_count >= 0)) |
| public.whatsapp_conversations | whatsapp_conversations_whatsapp_number_id_contact_number_key | u | UNIQUE (whatsapp_number_id, contact_number) |
| public.whatsapp_conversations | whatsapp_conversations_whatsapp_number_id_fkey | f | FOREIGN KEY (whatsapp_number_id) REFERENCES whatsapp_sessions(id) ON DELETE CASCADE |
| public.whatsapp_messages | whatsapp_messages_conversation_id_fkey | f | FOREIGN KEY (conversation_id) REFERENCES whatsapp_conversations(id) ON DELETE CASCADE |
| public.whatsapp_messages | whatsapp_messages_direction_check | c | CHECK ((direction = ANY (ARRAY['inbound'::text, 'outbound'::text]))) |
| public.whatsapp_messages | whatsapp_messages_message_type_check | c | CHECK ((message_type = ANY (ARRAY['text'::text, 'image'::text, 'audio'::text, 'document'::text]))) |
| public.whatsapp_messages | whatsapp_messages_pkey | p | PRIMARY KEY (id) |
| public.whatsapp_messages | whatsapp_messages_sent_by_check | c | CHECK ((sent_by = ANY (ARRAY['contact'::text, 'assistant'::text, 'human_agent'::text]))) |
| public.whatsapp_messages | whatsapp_messages_status_check | c | CHECK ((status = ANY (ARRAY['sent'::text, 'delivered'::text, 'read'::text, 'failed'::text]))) |
| public.whatsapp_sessions | whatsapp_sessions_org_id_fkey | f | FOREIGN KEY (org_id) REFERENCES organizations(id) ON DELETE CASCADE |
| public.whatsapp_sessions | whatsapp_sessions_pkey | p | PRIMARY KEY (id) |
| public.whatsapp_sessions | whatsapp_sessions_status_check | c | CHECK ((status = ANY (ARRAY['pending'::text, 'connected'::text, 'disconnected'::text, 'expired'::text]))) |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |
| public.abandoned_carts | abandoned_carts_org_status | CREATE INDEX abandoned_carts_org_status ON public.abandoned_carts USING btree (org_id, status, created_at DESC) |
| public.abandoned_carts | abandoned_carts_pkey | CREATE UNIQUE INDEX abandoned_carts_pkey ON public.abandoned_carts USING btree (id) |
| public.abandoned_carts | abandoned_carts_source_identity | CREATE UNIQUE INDEX abandoned_carts_source_identity ON public.abandoned_carts USING btree (source, source_cart_id) |
| public.active_calls | active_calls_pkey | CREATE UNIQUE INDEX active_calls_pkey ON public.active_calls USING btree (room_id) |
| public.active_calls | idx_active_calls_org | CREATE INDEX idx_active_calls_org ON public.active_calls USING btree (org_id) |
| public.active_calls | idx_active_calls_status | CREATE INDEX idx_active_calls_status ON public.active_calls USING btree (status) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_agent_id_document_id_key | CREATE UNIQUE INDEX agent_knowledge_assignments_agent_id_document_id_key ON public.agent_knowledge_assignments USING btree (agent_id, document_id) |
| public.agent_knowledge_assignments | agent_knowledge_assignments_pkey | CREATE UNIQUE INDEX agent_knowledge_assignments_pkey ON public.agent_knowledge_assignments USING btree (id) |
| public.agent_knowledge_files | agent_knowledge_files_pkey | CREATE UNIQUE INDEX agent_knowledge_files_pkey ON public.agent_knowledge_files USING btree (id) |
| public.agent_knowledge_files | idx_agent_kb_files_org | CREATE INDEX idx_agent_kb_files_org ON public.agent_knowledge_files USING btree (org_id) |
| public.agent_knowledge_files | idx_agent_knowledge_files_agent | CREATE INDEX idx_agent_knowledge_files_agent ON public.agent_knowledge_files USING btree (agent_id) |
| public.agents | agents_pkey | CREATE UNIQUE INDEX agents_pkey ON public.agents USING btree (id) |
| public.agents | idx_agents_created_at | CREATE INDEX idx_agents_created_at ON public.agents USING btree (created_at DESC) |
| public.agents | idx_agents_is_active | CREATE INDEX idx_agents_is_active ON public.agents USING btree (is_active) WHERE (is_active = true) |
| public.agents | idx_agents_org | CREATE INDEX idx_agents_org ON public.agents USING btree (org_id) |
| public.agents | idx_agents_purpose | CREATE INDEX idx_agents_purpose ON public.agents USING btree (purpose) |
| public.api_tokens | api_tokens_pkey | CREATE UNIQUE INDEX api_tokens_pkey ON public.api_tokens USING btree (id) |
| public.api_tokens | api_tokens_token_hash_key | CREATE UNIQUE INDEX api_tokens_token_hash_key ON public.api_tokens USING btree (token_hash) |
| public.app_kv_store | app_kv_store_pkey | CREATE UNIQUE INDEX app_kv_store_pkey ON public.app_kv_store USING btree (key) |
| public.app_kv_store | idx_app_kv_store_expires | CREATE INDEX idx_app_kv_store_expires ON public.app_kv_store USING btree (expires_at) WHERE (expires_at IS NOT NULL) |
| public.app_settings | app_settings_pkey | CREATE UNIQUE INDEX app_settings_pkey ON public.app_settings USING btree (key) |
| public.app_settings | idx_app_settings_org | CREATE INDEX idx_app_settings_org ON public.app_settings USING btree (org_id) |
| public.audit_log | audit_log_pkey | CREATE UNIQUE INDEX audit_log_pkey ON public.audit_log USING btree (id) |
| public.audit_log | idx_audit_log_actor | CREATE INDEX idx_audit_log_actor ON public.audit_log USING btree (actor_user_id, created_at DESC) |
| public.audit_log | idx_audit_log_org | CREATE INDEX idx_audit_log_org ON public.audit_log USING btree (org_id, created_at DESC) |
| public.calendar_bookings | calendar_bookings_pkey | CREATE UNIQUE INDEX calendar_bookings_pkey ON public.calendar_bookings USING btree (id) |
| public.calendar_bookings | idx_calendar_bookings_org | CREATE INDEX idx_calendar_bookings_org ON public.calendar_bookings USING btree (org_id) |
| public.calendar_bookings | idx_calendar_bookings_phone | CREATE INDEX idx_calendar_bookings_phone ON public.calendar_bookings USING btree (phone) |
| public.calendar_bookings | idx_calendar_bookings_time | CREATE INDEX idx_calendar_bookings_time ON public.calendar_bookings USING btree (scheduled_at) |
| public.call_configurations | call_configurations_agent_id_key | CREATE UNIQUE INDEX call_configurations_agent_id_key ON public.call_configurations USING btree (agent_id) |
| public.call_configurations | call_configurations_pkey | CREATE UNIQUE INDEX call_configurations_pkey ON public.call_configurations USING btree (id) |
| public.call_configurations | idx_call_configurations_agent_id | CREATE INDEX idx_call_configurations_agent_id ON public.call_configurations USING btree (agent_id) |
| public.call_listing_mentions | call_listing_mentions_pkey | CREATE UNIQUE INDEX call_listing_mentions_pkey ON public.call_listing_mentions USING btree (id) |
| public.call_listing_mentions | idx_call_listing_mentions_call | CREATE INDEX idx_call_listing_mentions_call ON public.call_listing_mentions USING btree (call_id) |
| public.call_logs | call_logs_pkey | CREATE UNIQUE INDEX call_logs_pkey ON public.call_logs USING btree (id) |
| public.call_logs | call_logs_room_id_unique | CREATE UNIQUE INDEX call_logs_room_id_unique ON public.call_logs USING btree (room_id) |
| public.call_logs | idx_call_logs_agent_id | CREATE INDEX idx_call_logs_agent_id ON public.call_logs USING btree (agent_id) |
| public.call_logs | idx_call_logs_bulk_call_id | CREATE INDEX idx_call_logs_bulk_call_id ON public.call_logs USING btree (bulk_call_id) WHERE (bulk_call_id IS NOT NULL) |
| public.call_logs | idx_call_logs_call_direction | CREATE INDEX idx_call_logs_call_direction ON public.call_logs USING btree (call_direction) |
| public.call_logs | idx_call_logs_call_status | CREATE INDEX idx_call_logs_call_status ON public.call_logs USING btree (call_status) |
| public.call_logs | idx_call_logs_caller_phone | CREATE INDEX idx_call_logs_caller_phone ON public.call_logs USING btree (caller_phone) |
| public.call_logs | idx_call_logs_config_hash | CREATE INDEX idx_call_logs_config_hash ON public.call_logs USING btree (config_hash) WHERE (config_hash IS NOT NULL) |
| public.call_logs | idx_call_logs_created_at | CREATE INDEX idx_call_logs_created_at ON public.call_logs USING btree (created_at DESC) |
| public.call_logs | idx_call_logs_from_number | CREATE INDEX idx_call_logs_from_number ON public.call_logs USING btree (from_number) |
| public.call_logs | idx_call_logs_migrated | CREATE INDEX idx_call_logs_migrated ON public.call_logs USING btree (migrated_to_re_memory) WHERE (migrated_to_re_memory IS NULL) |
| public.call_logs | idx_call_logs_org | CREATE INDEX idx_call_logs_org ON public.call_logs USING btree (org_id) |
| public.call_logs | idx_call_logs_phone | CREATE INDEX idx_call_logs_phone ON public.call_logs USING btree (phone_number) |
| public.call_logs | idx_call_logs_room_id | CREATE INDEX idx_call_logs_room_id ON public.call_logs USING btree (room_id) |
| public.call_logs | idx_call_logs_to_number | CREATE INDEX idx_call_logs_to_number ON public.call_logs USING btree (to_number) |
| public.call_logs | idx_call_logs_was_booked | CREATE INDEX idx_call_logs_was_booked ON public.call_logs USING btree (was_booked) WHERE (was_booked = true) |
| public.call_transcripts | call_transcripts_pkey | CREATE UNIQUE INDEX call_transcripts_pkey ON public.call_transcripts USING btree (id) |
| public.call_transcripts | idx_call_transcripts_call_id | CREATE INDEX idx_call_transcripts_call_id ON public.call_transcripts USING btree (call_id) |
| public.call_transcripts | idx_call_transcripts_org | CREATE INDEX idx_call_transcripts_org ON public.call_transcripts USING btree (org_id) |
| public.call_transcripts | idx_call_transcripts_phone | CREATE INDEX idx_call_transcripts_phone ON public.call_transcripts USING btree (phone) |
| public.call_transcripts | idx_call_transcripts_room | CREATE INDEX idx_call_transcripts_room ON public.call_transcripts USING btree (call_room_id) |
| public.campaign_listings | campaign_listings_campaign_id_listing_id_key | CREATE UNIQUE INDEX campaign_listings_campaign_id_listing_id_key ON public.campaign_listings USING btree (campaign_id, listing_id) |
| public.campaign_listings | campaign_listings_pkey | CREATE UNIQUE INDEX campaign_listings_pkey ON public.campaign_listings USING btree (id) |
| public.campaign_listings | idx_campaign_listings_campaign_id | CREATE INDEX idx_campaign_listings_campaign_id ON public.campaign_listings USING btree (campaign_id) |
| public.campaign_numbers | campaign_numbers_campaign_id_phone_key | CREATE UNIQUE INDEX campaign_numbers_campaign_id_phone_key ON public.campaign_numbers USING btree (campaign_id, phone) |
| public.campaign_numbers | campaign_numbers_pkey | CREATE UNIQUE INDEX campaign_numbers_pkey ON public.campaign_numbers USING btree (id) |
| public.campaign_numbers | idx_campaign_numbers_campaign_id | CREATE INDEX idx_campaign_numbers_campaign_id ON public.campaign_numbers USING btree (campaign_id) |
| public.campaign_numbers | idx_campaign_numbers_org | CREATE INDEX idx_campaign_numbers_org ON public.campaign_numbers USING btree (org_id) |
| public.campaign_numbers | idx_campaign_numbers_phone | CREATE INDEX idx_campaign_numbers_phone ON public.campaign_numbers USING btree (phone) |
| public.conversational_flows | conversational_flows_agent_id_key | CREATE UNIQUE INDEX conversational_flows_agent_id_key ON public.conversational_flows USING btree (agent_id) |
| public.conversational_flows | conversational_flows_pkey | CREATE UNIQUE INDEX conversational_flows_pkey ON public.conversational_flows USING btree (id) |
| public.conversational_flows | idx_conversational_flows_agent_id | CREATE INDEX idx_conversational_flows_agent_id ON public.conversational_flows USING btree (agent_id) |
| public.crm_sync_log | crm_sync_log_pkey | CREATE UNIQUE INDEX crm_sync_log_pkey ON public.crm_sync_log USING btree (id) |
| public.crm_sync_log | idx_crm_sync_log_phone | CREATE INDEX idx_crm_sync_log_phone ON public.crm_sync_log USING btree (phone) |
| public.invitations | invitations_email_org_id_accepted_at_key | CREATE UNIQUE INDEX invitations_email_org_id_accepted_at_key ON public.invitations USING btree (email, org_id, accepted_at) |
| public.invitations | invitations_pkey | CREATE UNIQUE INDEX invitations_pkey ON public.invitations USING btree (id) |
| public.invitations | invitations_token_hash_key | CREATE UNIQUE INDEX invitations_token_hash_key ON public.invitations USING btree (token_hash) |
| public.knowledge_documents | idx_knowledge_documents_org | CREATE INDEX idx_knowledge_documents_org ON public.knowledge_documents USING btree (org_id) |
| public.knowledge_documents | idx_knowledge_documents_type | CREATE INDEX idx_knowledge_documents_type ON public.knowledge_documents USING btree (doc_type) |
| public.knowledge_documents | knowledge_documents_document_id_key | CREATE UNIQUE INDEX knowledge_documents_document_id_key ON public.knowledge_documents USING btree (document_id) |
| public.knowledge_documents | knowledge_documents_pkey | CREATE UNIQUE INDEX knowledge_documents_pkey ON public.knowledge_documents USING btree (id) |
| public.lead_actions | idx_lead_actions_call_id | CREATE INDEX idx_lead_actions_call_id ON public.lead_actions USING btree (call_id) |
| public.lead_actions | idx_lead_actions_org | CREATE INDEX idx_lead_actions_org ON public.lead_actions USING btree (org_id) |
| public.lead_actions | idx_lead_actions_performed_at | CREATE INDEX idx_lead_actions_performed_at ON public.lead_actions USING btree (performed_at DESC) |
| public.lead_actions | lead_actions_pkey | CREATE UNIQUE INDEX lead_actions_pkey ON public.lead_actions USING btree (id) |
| public.lead_objections | idx_lead_objections_lead | CREATE INDEX idx_lead_objections_lead ON public.lead_objections USING btree (lead_id) |
| public.lead_objections | idx_lead_objections_org | CREATE INDEX idx_lead_objections_org ON public.lead_objections USING btree (org_id) |
| public.lead_objections | lead_objections_pkey | CREATE UNIQUE INDEX lead_objections_pkey ON public.lead_objections USING btree (id) |
| public.lead_property_signals | idx_lead_property_signals_lead | CREATE INDEX idx_lead_property_signals_lead ON public.lead_property_signals USING btree (lead_id) |
| public.lead_property_signals | idx_lead_signals_org | CREATE INDEX idx_lead_signals_org ON public.lead_property_signals USING btree (org_id) |
| public.lead_property_signals | lead_property_signals_pkey | CREATE UNIQUE INDEX lead_property_signals_pkey ON public.lead_property_signals USING btree (id) |
| public.leads | idx_leads_deal_stage | CREATE INDEX idx_leads_deal_stage ON public.leads USING btree (deal_stage) |
| public.leads | idx_leads_intent_score | CREATE INDEX idx_leads_intent_score ON public.leads USING btree (intent_score DESC) |
| public.leads | idx_leads_phone | CREATE INDEX idx_leads_phone ON public.leads USING btree (phone) |
| public.leads | leads_lead_id_key | CREATE UNIQUE INDEX leads_lead_id_key ON public.leads USING btree (lead_id) |
| public.leads | leads_phone_key | CREATE UNIQUE INDEX leads_phone_key ON public.leads USING btree (phone) |
| public.leads | leads_pkey | CREATE UNIQUE INDEX leads_pkey ON public.leads USING btree (id) |
| public.listings | idx_listings_area | CREATE INDEX idx_listings_area ON public.listings USING btree (area) |
| public.listings | idx_listings_listing_id | CREATE INDEX idx_listings_listing_id ON public.listings USING btree (listing_id) |
| public.listings | idx_listings_org | CREATE INDEX idx_listings_org ON public.listings USING btree (org_id) |
| public.listings | idx_listings_status | CREATE INDEX idx_listings_status ON public.listings USING btree (status) WHERE (status = 'active'::text) |
| public.listings | listings_listing_id_key | CREATE UNIQUE INDEX listings_listing_id_key ON public.listings USING btree (listing_id) |
| public.listings | listings_pim_sku_key | CREATE UNIQUE INDEX listings_pim_sku_key ON public.listings USING btree (pim_sku) |
| public.listings | listings_pkey | CREATE UNIQUE INDEX listings_pkey ON public.listings USING btree (id) |
| public.memberships | memberships_pkey | CREATE UNIQUE INDEX memberships_pkey ON public.memberships USING btree (id) |
| public.memberships | memberships_user_id_org_id_key | CREATE UNIQUE INDEX memberships_user_id_org_id_key ON public.memberships USING btree (user_id, org_id) |
| public.mfa_factors | mfa_factors_pkey | CREATE UNIQUE INDEX mfa_factors_pkey ON public.mfa_factors USING btree (id) |
| public.mfa_factors | mfa_factors_user_id_type_key | CREATE UNIQUE INDEX mfa_factors_user_id_type_key ON public.mfa_factors USING btree (user_id, type) |
| public.mfa_recovery_codes | idx_mfa_recovery_user | CREATE INDEX idx_mfa_recovery_user ON public.mfa_recovery_codes USING btree (user_id) |
| public.mfa_recovery_codes | mfa_recovery_codes_pkey | CREATE UNIQUE INDEX mfa_recovery_codes_pkey ON public.mfa_recovery_codes USING btree (id) |
| public.organizations | organizations_pkey | CREATE UNIQUE INDEX organizations_pkey ON public.organizations USING btree (id) |
| public.organizations | organizations_slug_key | CREATE UNIQUE INDEX organizations_slug_key ON public.organizations USING btree (slug) |
| public.outbound_campaigns | idx_outbound_campaigns_agent_id | CREATE INDEX idx_outbound_campaigns_agent_id ON public.outbound_campaigns USING btree (agent_id) |
| public.outbound_campaigns | idx_outbound_campaigns_created_at | CREATE INDEX idx_outbound_campaigns_created_at ON public.outbound_campaigns USING btree (created_at DESC) |
| public.outbound_campaigns | idx_outbound_campaigns_org | CREATE INDEX idx_outbound_campaigns_org ON public.outbound_campaigns USING btree (org_id) |
| public.outbound_campaigns | idx_outbound_campaigns_status | CREATE INDEX idx_outbound_campaigns_status ON public.outbound_campaigns USING btree (status) |
| public.outbound_campaigns | outbound_campaigns_pkey | CREATE UNIQUE INDEX outbound_campaigns_pkey ON public.outbound_campaigns USING btree (id) |
| public.password_resets | password_resets_pkey | CREATE UNIQUE INDEX password_resets_pkey ON public.password_resets USING btree (id) |
| public.password_resets | password_resets_token_hash_key | CREATE UNIQUE INDEX password_resets_token_hash_key ON public.password_resets USING btree (token_hash) |
| public.pin_to_pim_mappings | idx_pin_to_pim_pim | CREATE INDEX idx_pin_to_pim_pim ON public.pin_to_pim_mappings USING btree (pim_listing_id) |
| public.pin_to_pim_mappings | idx_pin_to_pim_pin | CREATE INDEX idx_pin_to_pim_pin ON public.pin_to_pim_mappings USING btree (pin) WHERE (is_active = true) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pin_source_key | CREATE UNIQUE INDEX pin_to_pim_mappings_pin_source_key ON public.pin_to_pim_mappings USING btree (pin, source) |
| public.pin_to_pim_mappings | pin_to_pim_mappings_pkey | CREATE UNIQUE INDEX pin_to_pim_mappings_pkey ON public.pin_to_pim_mappings USING btree (id) |
| public.post_call_actions | idx_post_call_actions_agent_id | CREATE INDEX idx_post_call_actions_agent_id ON public.post_call_actions USING btree (agent_id) |
| public.post_call_actions | post_call_actions_agent_id_key | CREATE UNIQUE INDEX post_call_actions_agent_id_key ON public.post_call_actions USING btree (agent_id) |
| public.post_call_actions | post_call_actions_pkey | CREATE UNIQUE INDEX post_call_actions_pkey ON public.post_call_actions USING btree (id) |
| public.post_call_deliveries | idx_post_call_deliveries_call | CREATE INDEX idx_post_call_deliveries_call ON public.post_call_deliveries USING btree (call_id) |
| public.post_call_deliveries | post_call_deliveries_pkey | CREATE UNIQUE INDEX post_call_deliveries_pkey ON public.post_call_deliveries USING btree (id) |
| public.sessions | idx_sessions_refresh_hash | CREATE INDEX idx_sessions_refresh_hash ON public.sessions USING btree (refresh_token_hash) |
| public.sessions | idx_sessions_user_id | CREATE INDEX idx_sessions_user_id ON public.sessions USING btree (user_id) |
| public.sessions | sessions_pkey | CREATE UNIQUE INDEX sessions_pkey ON public.sessions USING btree (id) |
| public.sessions | sessions_refresh_token_hash_key | CREATE UNIQUE INDEX sessions_refresh_token_hash_key ON public.sessions USING btree (refresh_token_hash) |
| public.users | users_email_key | CREATE UNIQUE INDEX users_email_key ON public.users USING btree (email) |
| public.users | users_pkey | CREATE UNIQUE INDEX users_pkey ON public.users USING btree (id) |
| public.whatsapp_conversations | idx_whatsapp_conversations_number_last | CREATE INDEX idx_whatsapp_conversations_number_last ON public.whatsapp_conversations USING btree (whatsapp_number_id, last_message_at DESC NULLS LAST) |
| public.whatsapp_conversations | idx_whatsapp_conversations_org | CREATE INDEX idx_whatsapp_conversations_org ON public.whatsapp_conversations USING btree (org_id) |
| public.whatsapp_conversations | whatsapp_conversations_pkey | CREATE UNIQUE INDEX whatsapp_conversations_pkey ON public.whatsapp_conversations USING btree (id) |
| public.whatsapp_conversations | whatsapp_conversations_whatsapp_number_id_contact_number_key | CREATE UNIQUE INDEX whatsapp_conversations_whatsapp_number_id_contact_number_key ON public.whatsapp_conversations USING btree (whatsapp_number_id, contact_number) |
| public.whatsapp_messages | idx_whatsapp_messages_conv_created | CREATE INDEX idx_whatsapp_messages_conv_created ON public.whatsapp_messages USING btree (conversation_id, created_at DESC) |
| public.whatsapp_messages | idx_whatsapp_messages_wa_id | CREATE UNIQUE INDEX idx_whatsapp_messages_wa_id ON public.whatsapp_messages USING btree (wa_message_id) WHERE (wa_message_id IS NOT NULL) |
| public.whatsapp_messages | whatsapp_messages_pkey | CREATE UNIQUE INDEX whatsapp_messages_pkey ON public.whatsapp_messages USING btree (id) |
| public.whatsapp_sessions | idx_whatsapp_sessions_org | CREATE UNIQUE INDEX idx_whatsapp_sessions_org ON public.whatsapp_sessions USING btree (org_id) |
| public.whatsapp_sessions | whatsapp_sessions_pkey | CREATE UNIQUE INDEX whatsapp_sessions_pkey ON public.whatsapp_sessions USING btree (id) |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |
| public.citext | character | citext | False |
| public.citext | boolean | citext | False |
| public.citext | inet | citext | False |
| public.citext_cmp | citext, citext | integer | False |
| public.citext_eq | citext, citext | boolean | False |
| public.citext_ge | citext, citext | boolean | False |
| public.citext_gt | citext, citext | boolean | False |
| public.citext_hash | citext | integer | False |
| public.citext_hash_extended | citext, bigint | bigint | False |
| public.citext_larger | citext, citext | citext | False |
| public.citext_le | citext, citext | boolean | False |
| public.citext_lt | citext, citext | boolean | False |
| public.citext_ne | citext, citext | boolean | False |
| public.citext_pattern_cmp | citext, citext | integer | False |
| public.citext_pattern_ge | citext, citext | boolean | False |
| public.citext_pattern_gt | citext, citext | boolean | False |
| public.citext_pattern_le | citext, citext | boolean | False |
| public.citext_pattern_lt | citext, citext | boolean | False |
| public.citext_smaller | citext, citext | citext | False |
| public.citextin | cstring | citext | False |
| public.citextout | citext | cstring | False |
| public.citextrecv | internal | citext | False |
| public.citextsend | citext | bytea | False |
| public.enforce_single_active_agent |  | trigger | False |
| public.max | citext | citext | False |
| public.min | citext | citext | False |
| public.regexp_match | citext, citext, text | text[] | False |
| public.regexp_match | citext, citext | text[] | False |
| public.regexp_matches | citext, citext | SETOF text[] | False |
| public.regexp_matches | citext, citext, text | SETOF text[] | False |
| public.regexp_replace | citext, citext, text, text | text | False |
| public.regexp_replace | citext, citext, text | text | False |
| public.regexp_split_to_array | citext, citext | text[] | False |
| public.regexp_split_to_array | citext, citext, text | text[] | False |
| public.regexp_split_to_table | citext, citext, text | SETOF text | False |
| public.regexp_split_to_table | citext, citext | SETOF text | False |
| public.replace | citext, citext, citext | text | False |
| public.set_updated_at |  | trigger | False |
| public.split_part | citext, citext, integer | text | False |
| public.strpos | citext, citext | integer | False |
| public.sync_storefront_cart | p_payload jsonb, p_org uuid | uuid | True |
| public.texticlike | citext, text | boolean | False |
| public.texticlike | citext, citext | boolean | False |
| public.texticnlike | citext, citext | boolean | False |
| public.texticnlike | citext, text | boolean | False |
| public.texticregexeq | citext, text | boolean | False |
| public.texticregexeq | citext, citext | boolean | False |
| public.texticregexne | citext, citext | boolean | False |
| public.texticregexne | citext, text | boolean | False |
| public.translate | citext, citext, text | text | False |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |
| auth | 4 |
| extensions | 55 |
| graphql_public | 1 |
| net | 12 |
| pgbouncer | 1 |
| public | 50 |
| realtime | 15 |
| storage | 19 |
| supabase_functions | 1 |
| vault | 5 |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |
| auth.email |  | text |
| auth.jwt |  | jsonb |
| auth.role |  | text |
| auth.uid |  | uuid |
| extensions.armor | bytea | text |
| extensions.armor | bytea, text[], text[] | text |
| extensions.crypt | text, text | text |
| extensions.dearmor | text | bytea |
| extensions.decrypt | bytea, bytea, text | bytea |
| extensions.decrypt_iv | bytea, bytea, bytea, text | bytea |
| extensions.digest | bytea, text | bytea |
| extensions.digest | text, text | bytea |
| extensions.encrypt | bytea, bytea, text | bytea |
| extensions.encrypt_iv | bytea, bytea, bytea, text | bytea |
| extensions.gen_random_bytes | integer | bytea |
| extensions.gen_random_uuid |  | uuid |
| extensions.gen_salt | text | text |
| extensions.gen_salt | text, integer | text |
| extensions.grant_pg_cron_access |  | event_trigger |
| extensions.grant_pg_graphql_access |  | event_trigger |
| extensions.grant_pg_net_access |  | event_trigger |
| extensions.hmac | bytea, bytea, text | bytea |
| extensions.hmac | text, text, text | bytea |
| extensions.pg_stat_statements | showtext boolean, OUT userid oid, OUT dbid oid, OUT toplevel boolean, OUT queryid bigint, OUT query text, OUT plans bigint, OUT total_plan_time double precision, OUT min_plan_time double precision, OUT max_plan_time double precision, OUT mean_plan_time double precision, OUT stddev_plan_time double precision, OUT calls bigint, OUT total_exec_time double precision, OUT min_exec_time double precision, OUT max_exec_time double precision, OUT mean_exec_time double precision, OUT stddev_exec_time double precision, OUT rows bigint, OUT shared_blks_hit bigint, OUT shared_blks_read bigint, OUT shared_blks_dirtied bigint, OUT shared_blks_written bigint, OUT local_blks_hit bigint, OUT local_blks_read bigint, OUT local_blks_dirtied bigint, OUT local_blks_written bigint, OUT temp_blks_read bigint, OUT temp_blks_written bigint, OUT shared_blk_read_time double precision, OUT shared_blk_write_time double precision, OUT local_blk_read_time double precision, OUT local_blk_write_time double precision, OUT temp_blk_read_time double precision, OUT temp_blk_write_time double precision, OUT wal_records bigint, OUT wal_fpi bigint, OUT wal_bytes numeric, OUT jit_functions bigint, OUT jit_generation_time double precision, OUT jit_inlining_count bigint, OUT jit_inlining_time double precision, OUT jit_optimization_count bigint, OUT jit_optimization_time double precision, OUT jit_emission_count bigint, OUT jit_emission_time double precision, OUT jit_deform_count bigint, OUT jit_deform_time double precision, OUT stats_since timestamp with time zone, OUT minmax_stats_since timestamp with time zone | SETOF record |
| extensions.pg_stat_statements_info | OUT dealloc bigint, OUT stats_reset timestamp with time zone | record |
| extensions.pg_stat_statements_reset | userid oid, dbid oid, queryid bigint, minmax_only boolean | timestamp with time zone |
| extensions.pgp_armor_headers | text, OUT key text, OUT value text | SETOF record |
| extensions.pgp_key_id | bytea | text |
| extensions.pgp_pub_decrypt | bytea, bytea, text | text |
| extensions.pgp_pub_decrypt | bytea, bytea, text, text | text |
| extensions.pgp_pub_decrypt | bytea, bytea | text |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea, text | bytea |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea | bytea |
| extensions.pgp_pub_decrypt_bytea | bytea, bytea, text, text | bytea |
| extensions.pgp_pub_encrypt | text, bytea, text | bytea |
| extensions.pgp_pub_encrypt | text, bytea | bytea |
| extensions.pgp_pub_encrypt_bytea | bytea, bytea | bytea |
| extensions.pgp_pub_encrypt_bytea | bytea, bytea, text | bytea |
| extensions.pgp_sym_decrypt | bytea, text | text |
| extensions.pgp_sym_decrypt | bytea, text, text | text |
| extensions.pgp_sym_decrypt_bytea | bytea, text | bytea |
| extensions.pgp_sym_decrypt_bytea | bytea, text, text | bytea |
| extensions.pgp_sym_encrypt | text, text | bytea |
| extensions.pgp_sym_encrypt | text, text, text | bytea |
| extensions.pgp_sym_encrypt_bytea | bytea, text | bytea |
| extensions.pgp_sym_encrypt_bytea | bytea, text, text | bytea |
| extensions.pgrst_ddl_watch |  | event_trigger |
| extensions.pgrst_drop_watch |  | event_trigger |
| extensions.set_graphql_placeholder |  | event_trigger |
| extensions.uuid_generate_v1 |  | uuid |
| extensions.uuid_generate_v1mc |  | uuid |
| extensions.uuid_generate_v3 | namespace uuid, name text | uuid |
| extensions.uuid_generate_v4 |  | uuid |
| extensions.uuid_generate_v5 | namespace uuid, name text | uuid |
| extensions.uuid_nil |  | uuid |
| extensions.uuid_ns_dns |  | uuid |
| extensions.uuid_ns_oid |  | uuid |
| extensions.uuid_ns_url |  | uuid |
| extensions.uuid_ns_x500 |  | uuid |
| graphql_public.graphql | "operationName" text, query text, variables jsonb, extensions jsonb | jsonb |
| net._await_response | request_id bigint | boolean |
| net._encode_url_with_params_array | url text, params_array text[] | text |
| net._http_collect_response | request_id bigint, async boolean | net.http_response_result |
| net._urlencode_string | string character varying | text |
| net.check_worker_is_up |  | void |
| net.http_collect_response | request_id bigint, async boolean | net.http_response_result |
| net.http_delete | url text, params jsonb, headers jsonb, timeout_milliseconds integer, body jsonb | bigint |
| net.http_get | url text, params jsonb, headers jsonb, timeout_milliseconds integer | bigint |
| net.http_post | url text, body jsonb, params jsonb, headers jsonb, timeout_milliseconds integer | bigint |
| net.wait_until_running |  | void |
| net.wake |  | void |
| net.worker_restart |  | boolean |
| pgbouncer.get_auth | p_usename text | TABLE(username text, password text) |
| public.citext | character | citext |
| public.citext | boolean | citext |
| public.citext | inet | citext |
| public.citext_cmp | citext, citext | integer |
| public.citext_eq | citext, citext | boolean |
| public.citext_ge | citext, citext | boolean |
| public.citext_gt | citext, citext | boolean |
| public.citext_hash | citext | integer |
| public.citext_hash_extended | citext, bigint | bigint |
| public.citext_larger | citext, citext | citext |
| public.citext_le | citext, citext | boolean |
| public.citext_lt | citext, citext | boolean |
| public.citext_ne | citext, citext | boolean |
| public.citext_pattern_cmp | citext, citext | integer |
| public.citext_pattern_ge | citext, citext | boolean |
| public.citext_pattern_gt | citext, citext | boolean |
| public.citext_pattern_le | citext, citext | boolean |
| public.citext_pattern_lt | citext, citext | boolean |
| public.citext_smaller | citext, citext | citext |
| public.citextin | cstring | citext |
| public.citextout | citext | cstring |
| public.citextrecv | internal | citext |
| public.citextsend | citext | bytea |
| public.enforce_single_active_agent |  | trigger |
| public.max | citext | citext |
| public.min | citext | citext |
| public.regexp_match | citext, citext, text | text[] |
| public.regexp_match | citext, citext | text[] |
| public.regexp_matches | citext, citext | SETOF text[] |
| public.regexp_matches | citext, citext, text | SETOF text[] |
| public.regexp_replace | citext, citext, text, text | text |
| public.regexp_replace | citext, citext, text | text |
| public.regexp_split_to_array | citext, citext | text[] |
| public.regexp_split_to_array | citext, citext, text | text[] |
| public.regexp_split_to_table | citext, citext, text | SETOF text |
| public.regexp_split_to_table | citext, citext | SETOF text |
| public.replace | citext, citext, citext | text |
| public.set_updated_at |  | trigger |
| public.split_part | citext, citext, integer | text |
| public.strpos | citext, citext | integer |
| public.sync_storefront_cart | p_payload jsonb, p_org uuid | uuid |
| public.texticlike | citext, text | boolean |
| public.texticlike | citext, citext | boolean |
| public.texticnlike | citext, citext | boolean |
| public.texticnlike | citext, text | boolean |
| public.texticregexeq | citext, text | boolean |
| public.texticregexeq | citext, citext | boolean |
| public.texticregexne | citext, citext | boolean |
| public.texticregexne | citext, text | boolean |
| public.translate | citext, citext, text | text |
| realtime.apply_rls | wal jsonb, max_record_bytes integer | SETOF realtime.wal_rls |
| realtime.broadcast_changes | topic_name text, event_name text, operation text, table_name text, table_schema text, new record, old record, level text | void |
| realtime.build_prepared_statement_sql | prepared_statement_name text, entity regclass, columns realtime.wal_column[] | text |
| realtime.cast | val text, type_ regtype | jsonb |
| realtime.check_equality_op | op realtime.equality_op, type_ regtype, val_1 text, val_2 text | boolean |
| realtime.check_equality_op | op realtime.equality_op, type_ regtype, val_1 text, val_2 text, negate boolean | boolean |
| realtime.is_visible_through_filters | columns realtime.wal_column[], filters realtime.user_defined_filter[] | boolean |
| realtime.list_changes | publication name, slot_name name, max_changes integer, max_record_bytes integer | TABLE(wal jsonb, is_rls_enabled boolean, subscription_ids uuid[], errors text[], slot_changes_count bigint) |
| realtime.quote_wal2json | entity regclass | text |
| realtime.send | payload jsonb, event text, topic text, private boolean | void |
| realtime.send_binary | payload bytea, event text, topic text, private boolean | void |
| realtime.subscription_check_filters |  | trigger |
| realtime.to_regrole | role_name text | regrole |
| realtime.topic |  | text |
| realtime.wal2json_escape_identifier | name text | text |
| storage.allow_any_operation | expected_operations text[] | boolean |
| storage.allow_only_operation | expected_operation text | boolean |
| storage.can_insert_object | bucketid text, name text, owner uuid, metadata jsonb | void |
| storage.enforce_bucket_lifecycle_service_role |  | trigger |
| storage.enforce_bucket_name_length |  | trigger |
| storage.extension | name text | text |
| storage.filename | name text | text |
| storage.foldername | name text | text[] |
| storage.get_common_prefix | p_key text, p_prefix text, p_delimiter text | text |
| storage.get_size_by_bucket |  | TABLE(size bigint, bucket_id text) |
| storage.list_multipart_uploads_with_delimiter | bucket_id text, prefix_param text, delimiter_param text, max_keys integer, next_key_token text, next_upload_token text | TABLE(key text, id text, created_at timestamp with time zone) |
| storage.list_objects_with_delimiter | _bucket_id text, prefix_param text, delimiter_param text, max_keys integer, start_after text, next_token text, sort_order text | TABLE(name text, id uuid, metadata jsonb, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone) |
| storage.operation |  | text |
| storage.protect_bucket_control_columns |  | trigger |
| storage.protect_delete |  | trigger |
| storage.search | prefix text, bucketname text, limits integer, levels integer, offsets integer, search text, sortcolumn text, sortorder text | TABLE(name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.search_by_timestamp | p_prefix text, p_bucket_id text, p_limit integer, p_level integer, p_start_after text, p_sort_order text, p_sort_column text, p_sort_column_after text | TABLE(key text, name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.search_v2 | prefix text, bucket_name text, limits integer, levels integer, start_after text, sort_order text, sort_column text, sort_column_after text | TABLE(key text, name text, id uuid, updated_at timestamp with time zone, created_at timestamp with time zone, last_accessed_at timestamp with time zone, metadata jsonb) |
| storage.update_updated_at_column |  | trigger |
| supabase_functions.http_request |  | trigger |
| vault._crypto_aead_det_decrypt | message bytea, additional bytea, key_id bigint, context bytea, nonce bytea | bytea |
| vault._crypto_aead_det_encrypt | message bytea, additional bytea, key_id bigint, context bytea, nonce bytea | bytea |
| vault._crypto_aead_det_noncegen |  | bytea |
| vault.create_secret | new_secret text, new_name text, new_description text, new_key_id uuid | uuid |
| vault.update_secret | secret_id uuid, new_secret text, new_name text, new_description text, new_key_id uuid | void |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |
| public.agent_knowledge_files | trg_agent_knowledge_files_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.agents | trg_agents_single_active | AFTER | UPDATE | EXECUTE FUNCTION enforce_single_active_agent() |
| public.agents | trg_agents_single_active | AFTER | INSERT | EXECUTE FUNCTION enforce_single_active_agent() |
| public.agents | trg_agents_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.calendar_bookings | trg_calendar_bookings_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.call_configurations | trg_call_configurations_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.campaign_numbers | trg_campaign_numbers_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.conversational_flows | trg_conversational_flows_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.knowledge_documents | trg_knowledge_documents_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.leads | trg_leads_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.listings | trg_listings_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.outbound_campaigns | trg_outbound_campaigns_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.pin_to_pim_mappings | trg_pin_to_pim_mappings_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| public.post_call_actions | trg_post_call_actions_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION set_updated_at() |
| realtime.subscription | tr_check_filters | BEFORE | UPDATE | EXECUTE FUNCTION realtime.subscription_check_filters() |
| realtime.subscription | tr_check_filters | BEFORE | INSERT | EXECUTE FUNCTION realtime.subscription_check_filters() |
| storage.buckets | enforce_bucket_name_length_trigger | BEFORE | UPDATE | EXECUTE FUNCTION storage.enforce_bucket_name_length() |
| storage.buckets | enforce_bucket_name_length_trigger | BEFORE | INSERT | EXECUTE FUNCTION storage.enforce_bucket_name_length() |
| storage.buckets | protect_bucket_control_insert | BEFORE | INSERT | EXECUTE FUNCTION storage.protect_bucket_control_columns('service_role') |
| storage.buckets | protect_bucket_control_update | BEFORE | UPDATE | EXECUTE FUNCTION storage.protect_bucket_control_columns() |
| storage.buckets | protect_bucket_control_update_role | AFTER | UPDATE | EXECUTE FUNCTION storage.enforce_bucket_lifecycle_service_role('service_role') |
| storage.buckets | protect_buckets_delete | BEFORE | DELETE | EXECUTE FUNCTION storage.protect_delete() |
| storage.objects | protect_objects_delete | BEFORE | DELETE | EXECUTE FUNCTION storage.protect_delete() |
| storage.objects | update_objects_updated_at | BEFORE | UPDATE | EXECUTE FUNCTION storage.update_updated_at_column() |

## storefront / kalamandir_shop

Schemas: `public`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |
| public.cart_items | table | 3 | False |
| public.carts | table | 3 | False |
| public.orders | table | 0 | False |
| public.products | table | 10 | False |
| public.shop_sessions | table | 14 | False |
| public.sync_outbox | table | 14 | False |

### public.cart_items

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| cart_id | uuid | NO |
| product_id | text | NO |
| name | text | NO |
| sku | text | NO |
| unit_price_minor | integer | NO |
| quantity | integer | NO |
| image | text | NO |
| details | jsonb | NO |
| added_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| added_at | 2026-10-08T18:18:30.255672+00:00 | 2026-10-10T05:36:15.306016+00:00 | 3 |

### public.carts

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| session_hash | text | NO |
| customer | jsonb | NO |
| status | text | NO |
| version | integer | NO |
| ever_abandoned | boolean | NO |
| created_at | timestamp with time zone | NO |
| last_activity_at | timestamp with time zone | NO |
| abandoned_at | timestamp with time zone | YES |
| converted_at | timestamp with time zone | YES |
| abandonment_reason | text | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T18:18:30.255672+00:00 | 2026-10-10T05:36:15.306016+00:00 | 3 |
| last_activity_at | 2026-10-08T18:28:53.900249+00:00 | 2026-10-25T13:05:45.885777+00:00 | 3 |
| abandoned_at | 2026-10-08T18:28:53.94828+00:00 | 2026-10-25T13:05:55.659499+00:00 | 3 |
| converted_at | N/A | N/A | 0 |

### public.orders

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | uuid | NO |
| cart_id | uuid | NO |
| order_number | text | NO |
| total_minor | integer | NO |
| customer | jsonb | NO |
| shipping | jsonb | NO |
| items | jsonb | NO |
| payment_mode | text | NO |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | N/A | N/A | 0 |

### public.products

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | text | NO |
| name | text | NO |
| category | text | NO |
| price_minor | integer | NO |
| compare_at_minor | integer | YES |
| sku | text | NO |
| images | jsonb | NO |
| details | jsonb | NO |
| stock | integer | NO |
| active | boolean | NO |

### public.shop_sessions

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| token_hash | text | NO |
| contact | jsonb | NO |
| current_cart_id | uuid | YES |
| created_at | timestamp with time zone | NO |
| last_seen_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| created_at | 2026-10-08T18:07:12.157922+00:00 | 2026-10-12T18:16:49.324754+00:00 | 14 |
| last_seen_at | 2026-10-08T18:07:12.157922+00:00 | 2026-10-12T18:16:49.324754+00:00 | 14 |

### public.sync_outbox

| Column | PostgreSQL type | Nullable |
| --- | --- | --- |
| id | bigint | NO |
| cart_id | uuid | NO |
| version | integer | NO |
| payload | jsonb | NO |
| attempts | integer | NO |
| next_attempt_at | timestamp with time zone | NO |
| sent_at | timestamp with time zone | YES |
| last_error | text | YES |
| created_at | timestamp with time zone | NO |

Available date ranges (UTC for zoned fields):

| Column | Minimum | Maximum | Non-null |
| --- | --- | --- | --- |
| next_attempt_at | 2026-10-08T18:18:59.935876+00:00 | 2026-10-25T13:05:55.659499+00:00 | 14 |
| sent_at | 2026-10-08T18:19:04.136833+00:00 | 2026-10-25T13:05:57.390335+00:00 | 14 |
| created_at | 2026-10-08T18:18:59.935876+00:00 | 2026-10-25T13:05:55.659499+00:00 | 14 |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |
| public.cart_items | cart_items_cart_id_fkey | f | FOREIGN KEY (cart_id) REFERENCES carts(id) ON DELETE CASCADE |
| public.cart_items | cart_items_pkey | p | PRIMARY KEY (cart_id, product_id) |
| public.cart_items | cart_items_product_id_fkey | f | FOREIGN KEY (product_id) REFERENCES products(id) |
| public.cart_items | cart_items_quantity_check | c | CHECK (((quantity >= 1) AND (quantity <= 10))) |
| public.cart_items | cart_items_unit_price_minor_check | c | CHECK ((unit_price_minor > 0)) |
| public.carts | carts_pkey | p | PRIMARY KEY (id) |
| public.carts | carts_session_hash_fkey | f | FOREIGN KEY (session_hash) REFERENCES shop_sessions(token_hash) |
| public.carts | carts_status_check | c | CHECK ((status = ANY (ARRAY['active'::text, 'abandoned'::text, 'converted'::text, 'empty'::text]))) |
| public.orders | orders_cart_id_fkey | f | FOREIGN KEY (cart_id) REFERENCES carts(id) |
| public.orders | orders_cart_id_key | u | UNIQUE (cart_id) |
| public.orders | orders_order_number_key | u | UNIQUE (order_number) |
| public.orders | orders_pkey | p | PRIMARY KEY (id) |
| public.orders | orders_total_minor_check | c | CHECK ((total_minor > 0)) |
| public.products | products_pkey | p | PRIMARY KEY (id) |
| public.products | products_price_minor_check | c | CHECK ((price_minor > 0)) |
| public.products | products_stock_check | c | CHECK ((stock >= 0)) |
| public.shop_sessions | shop_sessions_pkey | p | PRIMARY KEY (token_hash) |
| public.sync_outbox | sync_outbox_cart_id_fkey | f | FOREIGN KEY (cart_id) REFERENCES carts(id) |
| public.sync_outbox | sync_outbox_cart_id_version_key | u | UNIQUE (cart_id, version) |
| public.sync_outbox | sync_outbox_pkey | p | PRIMARY KEY (id) |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |
| public.cart_items | cart_items_pkey | CREATE UNIQUE INDEX cart_items_pkey ON public.cart_items USING btree (cart_id, product_id) |
| public.carts | carts_inactivity | CREATE INDEX carts_inactivity ON public.carts USING btree (last_activity_at) WHERE (status = 'active'::text) |
| public.carts | carts_pkey | CREATE UNIQUE INDEX carts_pkey ON public.carts USING btree (id) |
| public.orders | orders_cart_id_key | CREATE UNIQUE INDEX orders_cart_id_key ON public.orders USING btree (cart_id) |
| public.orders | orders_order_number_key | CREATE UNIQUE INDEX orders_order_number_key ON public.orders USING btree (order_number) |
| public.orders | orders_pkey | CREATE UNIQUE INDEX orders_pkey ON public.orders USING btree (id) |
| public.products | products_pkey | CREATE UNIQUE INDEX products_pkey ON public.products USING btree (id) |
| public.shop_sessions | shop_sessions_pkey | CREATE UNIQUE INDEX shop_sessions_pkey ON public.shop_sessions USING btree (token_hash) |
| public.sync_outbox | sync_outbox_cart_id_version_key | CREATE UNIQUE INDEX sync_outbox_cart_id_version_key ON public.sync_outbox USING btree (cart_id, version) |
| public.sync_outbox | sync_outbox_pkey | CREATE UNIQUE INDEX sync_outbox_pkey ON public.sync_outbox USING btree (id) |
| public.sync_outbox | sync_pending | CREATE INDEX sync_pending ON public.sync_outbox USING btree (next_attempt_at, id) WHERE (sent_at IS NULL) |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |

## storefront / postgres

Schemas: `public`.

### All relations

| Schema.relation | Kind | Exact rows | RLS enabled |
| --- | --- | --- | --- |

### Application constraints and relationships

| Schema.table | Constraint | Type | Definition |
| --- | --- | --- | --- |

### Application indexes

| Schema.table | Index | Definition |
| --- | --- | --- |

### Application function signatures

| Schema.function | Arguments | Result | Security definer |
| --- | --- | --- | --- |

All discovered function counts by schema:

| Schema | Functions |
| --- | --- |

<details>
<summary>Complete function signature catalog, including extensions</summary>

| Schema.function | Arguments | Result |
| --- | --- | --- |

</details>

### Database triggers

| Schema.table | Trigger | Timing | Event | Procedure |
| --- | --- | --- | --- | --- |
