# Local Explorer 🗺️

A modern, responsive web application for discovering local places and generating personalized first date ideas. Built with HTML, Tailwind CSS, and JavaScript with a mobile-first design approach.

## Features

### 🏠 Landing Page
- Beautiful hero section with gradient backgrounds
- Feature showcase highlighting key capabilities  
- Statistics display and call-to-action sections
- Smooth animations and transitions

### 🔍 Explore Section
- Advanced filtering system with multiple criteria
- Search functionality across place names, descriptions, and tags
- Location-based filtering (Downtown, Uptown, Waterfront, etc.)
- Price range filtering (Free, Budget, Moderate, Premium)
- Rating filtering (3.0+ to 4.5+ stars)
- Category buttons for restaurants, entertainment, parks, shopping, culture, and cafes
- Real-time filtering with instant results
- Results counter and filter management

### 🌙 Nightlife Section
- Specialized nighttime entertainment focus
- Time-based filtering (Evening, Night, Late Night)
- Vibe options (Energetic, Relaxed, Romantic, Social, Upscale)
- Group size preferences (Couple, Small Group, Large Group, Solo)
- Categories: Bars, Nightclubs, Live Music, Lounges, Late-Night Food, Activities
- Operating hours display and detailed venue descriptions
- Purple-themed UI for visual distinction

### 💕 Date Ideas Generator
- Personalized date suggestion form
- Location and vibe preference inputs
- Budget range and time preference selection
- Ready for API integration with customizable suggestions

## Technical Stack

- **Frontend**: Pure HTML5, CSS3, JavaScript (vanilla)
- **Styling**: Tailwind CSS (CDN)
- **Icons**: Feather Icons (CDN)
- **Architecture**: Single-page application with component-based structure
- **Design**: Mobile-first responsive design

## Getting Started

### Prerequisites
- A modern web browser
- Internet connection (for CDN dependencies)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/local-explorer.git
cd local-explorer
```

2. Open `index.html` in your web browser or serve it using a simple HTTP server:
```bash
# Using Python
python -m http.server 5000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:5000
```

3. Navigate to `http://localhost:5000` in your browser

## API Integration

The application is prepared for API integration with placeholder functions ready for replacement:

### Places API
```javascript
// In the loadPlacesData() function
fetch('/api/places')
  .then(response => response.json())
  .then(data => {
    placesData = data;
    renderPlaces();
  });
```

### Nightlife API
```javascript
// In the loadNightlifeData() function
fetch('/api/nightlife')
  .then(response => response.json())
  .then(data => {
    nightlifeData = data;
    renderNightlife();
  });
```

### Date Ideas API
```javascript
// In the generateDateIdea() function
fetch('/api/generate-date-idea', {
  method: 'POST',
  body: formData
})
.then(response => response.json())
.then(dateIdea => displayDateIdea(dateIdea));
```

## Data Structure

### Places Data Format
```javascript
{
  name: "Place Name",
  category: "restaurants|cafes|parks|shopping|culture|entertainment",
  type: "Restaurant",
  rating: 4.8,
  location: "downtown|uptown|midtown|suburbs|waterfront",
  price: "free|budget|moderate|expensive",
  description: "Description of the place",
  image: "https://example.com/image.jpg",
  tags: ["Tag1", "Tag2", "Tag3"]
}
```

### Nightlife Data Format
```javascript
{
  name: "Venue Name",
  category: "bars|clubs|live-music|lounges|late-night-eats|activities",
  rating: 4.5,
  location: "downtown|uptown|midtown|suburbs|waterfront", 
  price: "budget|moderate|expensive",
  time: "evening|night|late-night",
  vibe: "energetic|relaxed|romantic|social|upscale",
  groupSize: "couple|small|large|solo",
  description: "Description of the venue",
  image: "https://example.com/image.jpg",
  tags: ["Tag1", "Tag2", "Tag3"],
  hours: "Operating hours"
}
```

## Deployment

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to repository Settings > Pages
3. Select source branch (usually `main`)
4. Your site will be available at `https://yourusername.github.io/local-explorer`

### Netlify
1. Connect your GitHub repository to Netlify
2. Build settings: No build command needed (static site)
3. Publish directory: `/` (root)
4. Deploy automatically on push

### Vercel
1. Import your GitHub repository to Vercel
2. Framework preset: Other
3. Build settings: No build command needed
4. Deploy automatically on push

## Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Tailwind CSS](https://tailwindcss.com/) for the utility-first styling framework
- [Feather Icons](https://feathericons.com/) for the beautiful icon set
- [Unsplash](https://unsplash.com/) for placeholder images in examples