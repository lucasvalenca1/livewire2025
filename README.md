# Laravel Vite Starter 2025

<p align="center">
  <a href="https://laravel.com" target="_blank">
    <img src="https://laravel.com/img/logomark.min.svg" width="100" alt="Laravel Logo">
  </a>
  <a href="https://vitejs.dev" target="_blank">
    <img src="https://vitejs.dev/logo.svg" width="100" alt="Vite Logo">
  </a>
</p>

<p align="center">
  <a href="https://github.com/lucasvalenca1/livewire2025/actions"><img src="https://img.shields.io/github/actions/workflow/status/lucasvalenca1/livewire2025/laravel.yml?style=flat-square" alt="Build Status"></a>
  <a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

---

## About This Project

A modern Laravel starter template with Vite integration, demonstrating hot module replacement (HMR) and efficient frontend asset compilation. Created by **[Lucas Valença](https://github.com/lucasvalenca1)**.

**Key Features**:
- ⚡️ Vite-powered asset compilation
- 🔥 Hot Module Replacement (HMR)
- 🐳 Optional Docker development with Laravel Sail
- 🛠 Blade template engine integration
- 🌐 Built-in development server

---

## Development Setup

### Requirements
- PHP 8.2+
- Node.js 18+
- Composer 2.2+

### Installation

1. **Clone repository**
git clone https://github.com/lucasvalenca1/livewire2025.git
cd livewire2025

text

2. **Install dependencies**
composer install
npm install

text

3. **Configure environment**
cp .env.example .env
php artisan key:generate

text

4. **Start development servers**

In separate terminals:
Terminal 1: Laravel backend
php artisan serve

Terminal 2: Vite frontend
npm run dev

text

Or using Sail:
./vendor/bin/sail up

text

---

## Project Structure

livewire2025/
├── resources/
│ ├── js/ # JavaScript entry points
│ ├── css/ # Global styles
│ └── views/ # Blade templates
├── vite.config.js # Vite configuration
└── package.json # Frontend dependencies

text

---

## Development Commands

| Command | Description |
|---------|-------------|
| `npm run dev` | Start Vite development server |
| `npm run build` | Build production assets |
| `php artisan serve` | Start Laravel dev server (port 8000) |
| `sail up` | Start Docker development environment |

---

## Configuration

**Vite Development Server**  
Configured in `vite.config.js`:
export default defineConfig({
plugins: [
laravel({
input: ['resources/css/app.css', 'resources/js/app.js'],
refresh: true,
}),
],
});

text

**Environment**  
Set `APP_URL` in `.env`:
APP_URL=http://localhost:8000

text

---

## Documentation
- [Laravel Documentation](https://laravel.com/docs)
- [Vite Documentation](https://vitejs.dev/guide/)
- [Laravel Vite Documentation](https://laravel.com/docs/vite)

---

## License
This project is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).

---

**Created by [Lucas Valença](https://github.com/lucasvalenca1)**  
*Demonstration project for modern Laravel development*
