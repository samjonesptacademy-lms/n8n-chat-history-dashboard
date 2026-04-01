# n8n Chat History Dashboard

A real-time dashboard for viewing n8n AI Agent chat histories integrated with Supabase.

## Features

- **Real-time Data**: Fetches chat histories and learner information directly from Supabase
- **Session Grouping**: Groups messages by session_id to show complete conversations
- **Learner Information**: Automatically matches learner emails with the learners table to display names
- **Clean UI**: Modern, responsive interface for easy conversation review
- **Email Extraction**: Automatically extracts learner emails from chat messages

## Live Dashboard

👉 [Open Dashboard](https://samjonesptacademy-lms.github.io/n8n-chat-history-dashboard/)

## How It Works

1. The dashboard connects to your Supabase project
2. Loads all learners and creates an email-to-name lookup
3. Fetches all chat histories from the `n8n_chat_histories` table
4. Groups messages by `session_id` to reconstruct conversations
5. Extracts learner emails from message content and matches with learner names
6. Displays conversations in an interactive sidebar with full chat view

## Data Sources

- **Chat Histories Table**: `n8n_chat_histories` (id, session_id, message)
- **Learners Table**: `learners` (id, email, first_name, last_name, ...)

## Configuration

The Supabase credentials are embedded in the dashboard. For security, consider:
- Using a row-level security (RLS) policy to restrict access
- Using an anon key with limited permissions
- Deploying behind authentication if needed
