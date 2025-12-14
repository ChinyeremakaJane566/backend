# University Library Catalogue System

A complete digital library management system for universities with book catalogue, borrowing system, and admin panel.

## Features

### 1. Authentication & Book Submission (15 Marks)
-  Student registration and login
-  Admin users can add, update, and delete books
-  Secure password hashing with bcrypt

### 2. Book Catalogue (15 Marks)
-  Display all books with title, author, ISBN, and availability status
-  Search functionality (by title, author, or ISBN)
-  Filter by category
-  Professional card-based layout

### 3. Borrow & Return Management (15 Marks)
-  Students can borrow available books
-  Track borrowed books with borrow dates
-  Return books functionality
-  Automatic availability updates

### 4. Deployment (15 Marks)
-  Backend: Node.js + Express + PostgreSQL on Render
-  Frontend: HTML, CSS, JavaScript (ready for GitHub Pages)
-  RESTful API with proper error handling

## Technology Stack

### Frontend
- HTML5
- CSS3 (Modern design with gradients and animations)
- Vanilla JavaScript (Fetch API for all requests)
- Responsive design

### Backend
- Node.js
- Express.js
- PostgreSQL
- bcryptjs (password hashing)

## Setup Instructions

### Backend Setup

1. **Install Dependencies**
   bash
   cd backend
   npm install express cors pg bcryptjs
   

2. **Database Setup**
   - Create tables in pgAdmin using `database/schema.sql`
   - Update connection string in `backend/index.js`

3. **Run Backend**
   bash
   node index.js
   Server runs on `http://localhost:4000`

### Frontend Setup

1. **Add Images**
   - Place your school logo in `frontend/Images/logo.png`
   - Optional: Add background image `frontend/Images/library.jpg`

2. **Update API URL**
   - For local: Already configured
   - For production: Update `frontend/js/api.js` with your Render URL

3. **Open in Browser**
   - Simply open `frontend/index.html` in a browser
   - Or use a local server for better experience

## API Endpoints

### Authentication
- `POST /api/register` - Register new user
- `POST /api/login` - User login

### Books
- `GET /api/books` - Get all books
- `POST /api/books` - Add new book (Admin)
- `PUT /api/books/:id` - Update book (Admin)
- `DELETE /api/books/:id` - Delete book (Admin)

### Borrowing
- `POST /api/borrow` - Borrow a book
- `POST /api/return` - Return a book
- `GET /api/users/:userId/borrowed` - Get user's borrowed books

## Database Schema

### Users Table
- `id` (SERIAL PRIMARY KEY)
- `full_name` (VARCHAR)
- `email` (VARCHAR UNIQUE)
- `password` (VARCHAR - hashed)
- `role` (VARCHAR - default: 'student')

### Books Table
- `id` (SERIAL PRIMARY KEY)
- `title` (VARCHAR)
- `author` (VARCHAR)
- `category` (VARCHAR)
- `isbn` (VARCHAR - optional)
- `description` (TEXT - optional)
- `copies` (INTEGER)

### Borrowed Books Table
- `id` (SERIAL PRIMARY KEY)
- `user_id` (INTEGER - references users)
- `book_id` (INTEGER - references books)
- `borrow_date` (TIMESTAMP)

## Deployment

### Backend (Render)
1. Push code to GitHub
2. Create new Web Service on Render
3. Connect GitHub repository
4. Set build command: `npm install`
5. Set start command: `node index.js`
6. Add PostgreSQL database
7. Update connection string

### Frontend (GitHub Pages)
1. Push frontend code to GitHub
2. Go to Settings > Pages
3. Select source branch
4. Update API URL in js/api.js to point to Render backend
5. Site will be live at username.github.io/repo-name`

## Admin Access

## To make a user an admin, run in pgAdmin:
sql
UPDATE users SET role = 'admin' WHERE email = 'your-email@example.com';

## authentication details
Demo admin: Read@books.com / build567
Demo student: student / student421
Note that you have to register before you can login for students

## Project Structure

LIBRARY_CATALOGUE/
 backend/
   index.js                   # Express server & API route                          
   package-lock.json          # Dependencies
   package.json     
       database/
        schema.sql    # Database schema
   frontend/
      index.html        # Login page
       register.html     # Registration page
       dashboard.html
                        # Main catalogue
         css/
            styles.css    # All styles
          js/
            api.js        # API configuration
            auth.js       # Authentication
            dashboard.js  # Main functionality
        Images/           # Emoji(books) and images
        README.md


## Features Highlights

 **Modern UI/UX**: Professional design with smooth animations
 **Responsive**: Works on desktop, tablet, and mobil
 **Secure**: Password hashing and input validation
 **Fast**: Optimized API calls and efficient rendering
**User-Friendly**: Intuitive navigation and clear feedback

## Testing

1. Register a new user
2. Login with credentials
3. Browse books in catalogue
4. Search and filter books
5. Borrow a book
6. View borrowed books
7. Return a book
8. (Admin) Add/Edit/Delete/update books
## How to run frontend locally
Open the folder in VS Code.
Install the Live Server extension.
Right-click index.html.
Click Open with Live Server.
it will open on site
intall dependencies:
npm install
npm start
npm run dev
Then open thunder client and type this:
http://localhost:4000.

## how to run on backend:
cd backend
npm install
node server.js
open thunder client and type:
http://localhost:4000
you can register,select a table of columns which you want to see;
and the table will be displayed.

## changelles
Jane as the developer had so many challanges which was solved,
most of her changelles were from the backend connection.
1. Jane had so many errors with the backend connection
2. Jane also had errors whiles installing the `Node.index.js`
## solution
1. Jane fixed the backend errors by checking the errors line by line despite having
 laptop issues which kept making matter worse.
2. The `Node index.js` was installed using the right commands.

## References
https://www.youtube.com/watch?v=oYRda7UtuhA
https://www.youtube.com/watch?v=6XmDdIRmg84&t=1647s
The Backend was the lectures leacturing videos.

## Deployment links 
1. Frontend link:https://chinyeremakajane566.github.io/frontend/
2. backend link: https://backend-malb.onrender.com

## it's christmas season
Chinyeremaka Jane wishes you a very wonderful Christmas and a prosperous new year!!!

## Developer
Chinyeremaka Jane - 10012300046
Computer Science





