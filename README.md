# :books: LOOK FOR A BOOK

## :open_book: OVERVIEW
Date: November 2021\
Developer(s): Ashneet Rathore, Michelle Prasouvo, Henry Reyes\
Mentored by Aaron Chen

Look For A Book is a full-stack web application for searching books by title and viewing key details such as cover image, synopsis, and author. The app was developed in a 12-hour time span as a submission for the ZotHacks beginner-friendly hackathon hosted at UCI.

**Tech Stack** | Python, Flask, JavaScript, Google Books API, HTML, CSS, Heroku

## :film_strip: DEMO
![Demo](demo.gif)

## :classical_building: ARCHITECTURE
The backend is implemented in **Python** using **Flask**, which defines two routes - `/` for the home page and `/search` for queries. The frontend uses **JavaScript**, **HTML**, **CSS**, and **Jinja2** templating for server-side rendering.

Flow of a search query:

- JavaScript captures user input and redirects it to the `/search` route
- Flask receives the request and fetches data from the **Google Books API**
- Flask processes data into a structured format and passes it to Jinja2
- Jinja2 injects the data into a HTML template and delivers the fully rendered page to the browser

The app was originally deployed on **Heroku** during the hackathon, but is now only available to run locally.

## :open_file_folder: PROJECT FILE STRUCTURE
```bash
look-for-a-book/
│── app/
│   ├── main.py            # Flask backend and Google Books API integration
│   ├── static/
│   │   │── searchbar.js   # Search input and query handling
│   │   └── mainpage.css   # Webpage styles
│   └── templates/         
│       └── index.html     # Flask frontend interface
│── requirements.txt       # External dependencies
│── README.md              # Project documentation
│── .gitignore             # Ignored files
└── demo.gif               # Demo GIF
```

## :hammer: CONFIGURATION
**1. Clone the repository**
```bash
git clone https://github.com/ashneetrathore/look-for-a-book.git
```

**2. Install dependencies**
```bash
cd look-for-a-book
pip install -r requirements.txt
```

## :rocket: EXECUTION
```bash
cd app
python3 main.py
```

Open [http://127.0.0.1:5000](http://127.0.0.1:5000) to use the book searcher.

## :wrench: TRY IT OUT
1. Enter the title of a book into the search bar and click the search icon.
2. Books matching the inputted title will be displayed. Multiple entries may appear for the same title due to different editions or volumes.