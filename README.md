# Laravel Blog

A full-featured blog platform built with Laravel. Supports posts, categories, comments, user authentication, and newsletter subscriptions via Mailchimp integration.

## Features

- **Posts** — create, edit, delete posts with category tagging and rich text
- **Comments** — authenticated users can comment on posts
- **Categories** — organize posts by category with filtering
- **Admin Panel** — admin-only post management via `AdminPostController`
- **Authentication** — register, login, logout via session-based auth
- **Newsletter** — subscribe via email, integrated with Mailchimp API
- **Search** — full-text post search

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Laravel |
| Frontend | Blade templates |
| Auth | Session-based (custom) |
| Newsletter | Mailchimp API |
| Database | MySQL |

## Models

| Model | Description |
|---|---|
| `User` | Blog author and commenter |
| `Post` | Article with title, body, category, slug |
| `Category` | Post taxonomy |
| `Comment` | User comment on a post |

## Controllers

| Controller | Responsibility |
|---|---|
| `PostController` | Public post listing and single-post view |
| `AdminPostController` | Admin CRUD for posts |
| `CommentController` | Store and manage comments |
| `PostCommentsController` | List comments per post |
| `NewsletterController` | Handle newsletter subscription |
| `RegisterController` | User registration |
| `SessionsController` | Login / logout |

## Installation

```bash
git clone https://github.com/Ma7moud1599/Laravel_Blog.git
cd Laravel_Blog

composer install
cp .env.example .env
php artisan key:generate

# Add Mailchimp API key and list ID to .env:
# MAILCHIMP_KEY=your-key
# MAILCHIMP_LIST_ID=your-list-id

php artisan migrate --seed
php artisan serve
```

## License

MIT
