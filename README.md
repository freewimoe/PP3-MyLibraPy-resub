# 📚 MyLibraPy

> 🚀 Try it now on Heroku:  
[**Launch Terminal App**](https://mylibrapy-pp3-3db58ea9dc6b.herokuapp.com)

> 🧠 About this project:  
[About This App](https://mylibrapy-pp3-3db58ea9dc6b.herokuapp.com/about)

```text
  __  __       _      _ _               _____       
 |  \/  |     | |    (_) |             |  __ \      
 | \  / |_   _| |     _| |__  _ __ __ _| |__) |   _ 
 | |\/| | | | | |    | | '_ \| '__/ _` |  ___/ | | |
 | |  | | |_| | |____| | |_) | | | (_| | |   | |_| |
 |_|  |_|\__, |______|_|_.__/|_|  \__,_|_|    \__, |
          __/ |                                __/ |
         |___/                                |___/ 

```
A simple CLI library manager – built for learning, testing, and practical use in school settings

---

## 🔒 Inspiration From the Classroom

As a teacher at the **European School Karlsruhe**, I constantly explore ways to blend code with everyday school experiences. One of the most practical and relatable topics? **Books.**

This small app grew out of that: a terminal-based tool to help track personal book collections. Students were curious about file handling, persistent data, and terminal UIs – so we started building something together. Not flashy. Not fancy. But it works, and it grows with us.

In parallel, we're also working on a bigger platform: a full-featured **BookExchange** app (database, GUI, server, the works). But **MyLibraPy** is where we try things out. A sandbox. A real-use example. A place where students, colleagues, and I can experiment with real code, for real use.

> “Sir, can we make it print in color?”  
> “Yes. And now we’re importing Colorama.”

This project became part lesson, part library.

---

## ✨ Features

### ✅ Implemented

- 📚 **Add Book**  
  Enter title, author, genre, and status (read/unread/wishlist) – saved to books.json.

- 👀 **View Books**  
  See all your books in a clear, numbered list.

- 🔍 **Search**  
  Search titles, authors, or genres with any keyword.

- ✏️ **Edit Book**  
  Select a book by number and change any field.

- ❌ **Delete Book**  
  Choose a book to delete (with confirmation).

- 📤 **Export to CSV**  
  Write all books to books_export.csv – spreadsheet-ready.

- 📊 **Statistics**  
  Get a breakdown by genre and status, with totals.

- 💾 **Persistent Storage**  
  Your collection is saved between sessions using JSON.

---

## 📚 Demo Library Included

To help testers: the app includes a preloaded demo library with 10 books.
You can immediately press [2] to explore.

## 🖼️ Screenshots

A few glimpses of the interface in use:
- ** Full App Flow (Heroku):**
  ![Workflow GIF](media/workflow.gif)

- **Banner / Welcome**:  
  ![Menu](media/banner.png)

  - **App Startup (Console View)**:  
  ![Console](media/console_start.png)

- **Main Menu**:  
  ![Menu](media/menu.png)

- **Add Book Dialog**:  
  ![Add Book](media/add_book.png)

- **Book List View**:  
  ![View Books](media/view_books.png)

- **Library Statistics**:  
  ![Statistics](media/statistics.png)

---

## 🧪 Manual Testing

All functions were tested in:

- ✅ Windows Terminal (PowerShell & CMD)
- ✅ VS Code terminal
- ✅ Browser via Heroku deployment link
- ✅ Replit deployment
- ✅ flask deployment

### Covered Scenarios:
- Adding new books (valid and invalid inputs)
- Editing book details (boundary testing)
- Deleting entries (confirmation flow)
- Searching (case-insensitive, empty queries)
- JSON storage & reload after restart
- CSV export and file verification
- Error handling for invalid menu choices
- Input validation for book numbers

### Code Quality & Validation:
- **PEP8 Validation**: Code tested with Python linter
  - All major PEP8 issues resolved
  - Consistent indentation (4 spaces)
  - Line length under 79 characters
  - Duplicate string literals replaced with constants
- **Manual Testing Results**: 
  - ✅ All core features functional
  - ✅ Error handling works as expected
  - ✅ Data persistence confirmed
  - ✅ User input validation active

### Testing Process:
1. **Input Validation Tests**:
   - Invalid menu choices → Clear error message
   - Empty book fields → Prompts for valid input
   - Invalid book numbers → "Invalid book number" error
2. **Data Persistence Tests**:
   - App restart → Data retained
   - JSON file validation → Correct structure
3. **Feature Tests**:
   - All CRUD operations tested
   - Export functionality verified
   - Search with various inputs tested

---

## � Deployment

### Live Application
- **Heroku URL**: https://mylibrapy-pp3-3db58ea9dc6b.herokuapp.com
- **GitHub Repository**: https://github.com/freewimoe/PP3-MyLibraPy-resub

### Deployment Steps (Heroku)

1. **Prepare Files**:
   - `requirements.txt` - Lists Python dependencies
   - `Procfile` - Defines how Heroku runs the app
   - `runtime.txt` - Specifies Python version (3.12.2)

2. **Heroku Setup**:
   ```bash
   heroku create mylibrapy-pp3
   git push heroku main
   ```

3. **Configure Buildpacks**:
   - Python buildpack for backend
   - Node.js buildpack for terminal interface

4. **Environment Variables**: None required for this project

### Local Development Setup

1. **Clone Repository**:
   ```bash
   git clone https://github.com/freewimoe/PP3-MyLibraPy-resub.git
   cd PP3-MyLibraPy-resub
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Application**:
   ```bash
   python run.py
   ```

---

## �🐛 Known Issues

- No dropdowns or fixed status choices (user can mistype)
- Genre & status inputs are free text
- No duplication checks yet

---

## 🚀 Run it Yourself

1. Clone this repository:

```bash
   git clone https://github.com/freewimoe/MyLibraPy-PP3.git
   cd MyLibraPy-PP3
   pip install -r requirements.txt
   python run.py


2. (Optional) Create a virtual environment:
   
```bash
   python -m venv venv
   venv\Scripts\activate  # Windows
   source venv/bin/activate  # macOS/Linux


3. Install the required package:

```bash
   pip install -r requirements.txt

4. Launch the app:
   
```bash
   python main.py

---

## 📦 Dependencies

colorama==0.4.6

---

## 🔮 What’s Next?

- Full GUI (Tkinter or PyQt)
- Multi-user mode with login
- Ratings & personal reviews
- Cloud sync (e.g. Firebase or Supabase)

---

## 🙏 Thanks & Credits

- My **students** at the European School Karlsruhe
- The **Code Institute** for the structured challenge
- [Colorama](https://github.com/tartley/colorama) for terminal color magic
- My mentor **Mo Shami** for valuable guidance
- **Kay Welfare**, my cohort facilitator, for ongoing support

---

## 🔗 Repository

👉 [github.com/freewimoe/MyLibraPy-PP3](https://github.com/freewimoe/MyLibraPy-PP3)

If you're a teacher, student, or just a curious coder – I hope MyLibraPy inspires you like it inspired us in class. 📚✨