# NICKET - Modern Event Registration System

A modern web-based event registration system built with Laravel 12, Filament Admin Panel, and Tailwind CSS featuring a minimalist black and white design.

## System Description

NICKET is an event registration platform that allows users to view event listings, see event details, and register for events they're interested in. The platform comes with a powerful admin panel to manage events and participant registrations.

## Key Features

### Frontend (User)
- **Home Page**: Displays a list of available events
- **Event Detail Page**: Provides comprehensive information about events
- **Registration Form**: Allows participants to register for specific events
- **Responsive Design**: Accessible from both desktop and mobile devices

### Backend (Admin)
- **Admin Panel**: Filament-powered admin panel for system management
- **Event Management**: Create, edit, and delete events
- **Separate Image Management**: Special feature for managing event images
- **Registration Management**: View and manage registration data

## Technologies Used

- **Laravel 12**: PHP framework for web application development
- **Filament 3**: Admin panel for Laravel
- **Tailwind CSS**: CSS framework for styling
- **MySQL**: Relational database
- **HTML/CSS/JavaScript**: Frontend

## System Requirements

- PHP >= 8.2
- Composer
- MySQL
- Node.js and NPM

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/nickelsync/NICKET.git
   cd NICKET
   ```

2. **Install PHP dependencies**
   ```bash
   composer install
   ```

3. **Set up .env file**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Configure database in .env file**
   ```
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=nicket
   DB_USERNAME=root
   DB_PASSWORD=
   ```

5. **Run migrations and seeders**
   ```bash
   php artisan migrate --seed
   ```

6. **Set up storage link**
   ```bash
   php artisan storage:link
   ```

7. **Install JavaScript dependencies**
   ```bash
   npm install
   npm run dev
   ```

8. **Run the server**
   ```bash
   php artisan serve
   ```

9. **Access the application**
   - Frontend: http://localhost:8000
   - Admin panel: http://localhost:8000/admin
   - Default admin credentials:
     - Email: admin@example.com
     - Password: 12345678

## Database Structure

### Events Table
- id (primary key)
- name (event name)
- event_date (event date)
- information (event description)
- image_path (event image path)
- created_at
- updated_at

### Registrations Table
- id (primary key)
- event_id (foreign key to events table)
- name (participant name)
- email (participant email)
- birth_date (participant birth date)
- address (participant address)
- created_at
- updated_at

## Special Feature: Separate Image Editing

This system has a special feature for managing event images separately from the event data edit form. This allows admins to:

1. Focus solely on image management
2. Upload new images with a drag-and-drop interface
3. Preview images before uploading
4. Easily delete event images

## Usage

### Frontend

1. **View Event List**
   - Visit the home page to see all available events

2. **View Event Details**
   - Click on an event to see complete information
   - View date, time, and other event details

3. **Register for an Event**
   - Click the "Register Now" button on the event detail page
   - Fill out the registration form with required data
   - Submit the registration

### Backend (Admin)

1. **Log in to Admin Panel**
   - Access http://localhost:8000/admin
   - Log in with admin credentials

2. **Manage Events**
   - View, add, edit, and delete events
   - Manage event details and images

3. **Edit Event Images**
   - Click "Edit Image" on the event table or event detail page
   - Upload new images or delete existing ones

4. **Manage Registrations**
   - View the list of participants registered for each event
