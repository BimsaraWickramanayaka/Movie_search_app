# 🎬 React Movie Search App

A modern movie search application built with React, Vite, and Tailwind CSS that allows users to search for movies and view trending films using The Movie Database (TMDB) API.

![React](https://img.shields.io/badge/React-19.1.1-blue.svg)
![Vite](https://img.shields.io/badge/Vite-7.1.7-purple.svg)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.1.13-teal.svg)

## ✨ Features

- 🔍 **Real-time Movie Search** - Search for movies with debounced input
- 🎭 **Movie Details** - View movie ratings, release dates, and languages
- 🌟 **Trending Movies** - Display popular movies on initial load
- ⚡ **Fast Performance** - Built with Vite for lightning-fast development
- 📱 **Responsive Design** - Works seamlessly on all devices
- 🎨 **Modern UI** - Beautiful interface with Tailwind CSS v4
- 🔄 **Loading States** - Smooth loading indicators and error handling

## 🛠️ Tech Stack

- **Frontend Framework**: React 19.1.1
- **Build Tool**: Vite 7.1.7
- **Styling**: Tailwind CSS 4.1.13
- **API**: The Movie Database (TMDB)
- **Backend**: Appwrite (for search analytics)
- **Utilities**: react-use (for debouncing)

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- TMDB API key
- Appwrite account (optional, for analytics)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/BimsaraWickramanayaka/Movie_search_app.git
   cd Movie_search_app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```env
   VITE_TMDB_API_KEY=your_tmdb_api_key_here
   VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
   VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
   VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
   ```

4. **Get your TMDB API key**
   - Visit [The Movie Database](https://www.themoviedb.org/)
   - Create an account and go to Settings → API
   - Generate your API key

5. **Run the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to `http://localhost:5173`

## 🏗️ Project Structure

```
src/
├── Components/
│   ├── MovieCard.jsx      # Individual movie display component
│   ├── Search.jsx         # Search input component
│   └── Spinner.jsx        # Loading spinner component
├── App.jsx                # Main application component
├── main.jsx              # Application entry point
├── index.css             # Global styles and Tailwind configuration
└── appwrite.js           # Appwrite database integration
```

## ⚙️ Key Features Explained

### Debounced Search
The app uses the `react-use` library to implement debounced search, reducing API calls:
```javascript
useDebounce(
  () => setDebouncedSearchTerm(searchTerm),
  500,
  [searchTerm]
);
```

### Movie Data Integration
Fetches movie data from TMDB API with proper error handling:
```javascript
const endpoint = query ? 
  `${API_BASE_URL}/search/movie?query=${encodeURIComponent(query)}` : 
  `${API_BASE_URL}/discover/movie?sort_by=popularity.desc`;
```

### Custom Tailwind Utilities
Uses Tailwind CSS v4's new `@utility` directive for custom styling:
```css
@utility text-gradient {
    @apply bg-linear-to-r from-[#D6C7FF] to-[#AB8BFF] bg-clip-text text-transparent;
}
```

## 🎨 Styling

This project uses Tailwind CSS v4 with:
- Custom color palette defined in `@theme`
- Responsive design patterns
- Custom gradient utilities
- Modern glassmorphism effects

## 📝 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🌐 API Integration

### TMDB API Endpoints Used:
- **Search Movies**: `/search/movie?query={query}`
- **Discover Popular**: `/discover/movie?sort_by=popularity.desc`

### Appwrite Integration:
- Tracks search analytics
- Stores popular search terms
- Provides trending movie data

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [The Movie Database (TMDB)](https://www.themoviedb.org/) for providing the movie API
- [Vite](https://vitejs.dev/) for the amazing build tool
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [React](https://reactjs.org/) for the component-based UI library

## 📞 Contact

Bimsara Wickramanayaka - [@BimsaraWickramanayaka](https://github.com/BimsaraWickramanayaka)

Project Link: [https://github.com/BimsaraWickramanayaka/Movie_search_app](https://github.com/BimsaraWickramanayaka/Movie_search_app)

---

⭐ Don't forget to star this repo if you found it helpful!
