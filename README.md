# Hogwarts House Sorting Hat Quiz 🧙‍♂️

A magical web application that sorts users into one of four Hogwarts-inspired houses based on their personality traits and preferences. This is an interactive quiz built with Flask that mimics the famous Sorting Hat from the Harry Potter universe.

## 🎯 Features

- **Interactive Quiz**: Users answer 3 questions to determine their house
- **Dynamic House Assignment**: Scoring system based on answer selection
- **Visual Results**: Displays the assigned house with corresponding imagery
- **Responsive Design**: Beautiful gradient UI with Hogwarts-themed background
- **Fast & Lightweight**: Minimal dependencies with quick load times

## 🏠 Houses

The quiz sorts users into one of these four houses:

- **Garudwar**: For the brave and courageous
- **Nagsakti**: For the ambitious and cunning
- **Cheelghat**: For the intelligent and wise
- **Mehnatkash**: For the loyal and hardworking

## 📋 Quiz Questions

1. **What quality do you value most?**
   - Bravery → Garudwar
   - Ambition → Nagsakti
   - Intelligence → Cheelghat
   - Loyalty → Mehnatkash

2. **Which animal do you relate to?**
   - Dragon → Garudwar
   - Snake → Nagsakti
   - Owl → Cheelghat
   - Badger → Mehnatkash

3. **What's your favorite subject?**
   - Defense → Garudwar
   - Potions → Nagsakti
   - Charms → Cheelghat
   - Herbology → Mehnatkash

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Installation

1. **Clone or download the project**
   ```bash
   cd d:\projects
   ```

2. **Install Flask**
   ```bash
   pip install flask
   ```

3. **Verify project structure**
   ```
   d:\projects\
   ├── app.py
   ├── templates/
   │   ├── Harry_quiz.html
   │   └── result.html
   ├── static/
   │   ├── hogwart.jpg
   │   ├── garudwar.jpg
   │   ├── nagsakti.jpg
   │   ├── cheelghat.jpg
   │   ├── mehnatkash.jpg
   │   └── style.css
   └── README.md
   ```

### Running the Application

1. **Start the Flask server**
   ```bash
   python app.py
   ```

2. **Open your browser and navigate to**
   ```
   http://localhost:5000
   ```

3. **Take the quiz and discover your house!**

## 📁 Project Structure

### `app.py`
The main Flask application file containing:
- **Route `/`**: Serves the quiz page (Harry_quiz.html)
- **Route `/result` (POST)**: Processes quiz answers and calculates house assignment
- Scoring logic that tallies points for each house based on user responses
- Dynamic result page rendering with house name and image

### `templates/Harry_quiz.html`
The quiz interface featuring:
- 3 personality/preference questions
- Radio button options for each question
- Styled form with Hogwarts background
- Gradient background card with shadow effects
- Responsive design for various screen sizes

### `templates/result.html`
The results page displaying:
- "The sorting hat has spoken!" message
- Assigned house name
- House-themed image (garudwar.jpg, nagsakti.jpg, etc.)
- Styled container with shadow and rounded corners

### `static/`
Contains static assets:
- **hogwart.jpg**: Background image for quiz page
- **House images**: garudwar.jpg, nagsakti.jpg, cheelghat.jpg, mehnatkash.jpg
- **style.css**: Optional external styling (referenced in templates)

## 🎨 Styling

The application uses inline CSS with:
- Linear gradients for modern look
- Flexbox for centering and alignment
- Box shadows for depth
- Responsive font sizing
- Custom color scheme (blues, greens, and reds)

## 🔧 How the Sorting Works

1. User answers 3 questions on the quiz page
2. Form submits to `/result` endpoint with POST method
3. Backend calculates scores:
   - Each answer corresponds to one house
   - Points increment for each matching answer
   - Tallied across all 3 questions
4. House with highest score is selected (using `max()` function)
5. Result page displays the winning house with image

## 🖼️ Image Assets Required

Create/add the following images to the `static/` folder:
- `hogwart.jpg` - Background for quiz page
- `garudwar.jpg` - House image for Garudwar
- `nagsakti.jpg` - House image for Nagsakti
- `cheelghat.jpg` - House image for Cheelghat
- `mehnatkash.jpg` - House image for Mehnatkash

## 💡 Usage Example

1. Open application at `http://localhost:5000`
2. Read the three questions carefully
3. Select your answer for each question
4. Click the Submit button
5. View your assigned house and its corresponding image
6. Return to quiz to try again with different answers

## 🔄 Refreshing the Quiz

After seeing results, users can:
- Navigate back to the main page
- Retake the quiz with different answers
- Each attempt is independent

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Port 5000 already in use | Change `app.run(port=5001)` in app.py |
| Images not loading | Ensure all images are in `static/` folder |
| 404 error on quiz page | Check that templates are in `templates/` folder |
| Module not found error | Run `pip install flask` |
| Template not rendering | Verify HTML files are in `templates/` folder with correct names |

## ⚙️ Development Mode

The application runs in debug mode by default (`debug=True`), which provides:
- Automatic page reload on code changes
- Detailed error messages
- Interactive debugger in browser
- Hot reloading during development

**Note**: Disable debug mode in production by changing `app.run(debug=False)`

## 📝 Customization

### Add More Questions
1. Add new form fields in Harry_quiz.html
2. Add corresponding logic in app.py result route
3. Update house scoring for new answers

### Modify House Names
1. Edit the `houses` dictionary in app.py
2. Update quiz options in Harry_quiz.html
3. Add/update corresponding images in static/

### Change Styling
1. Modify inline CSS in HTML templates
2. Or update external `style.css` file
3. Adjust colors, fonts, and layouts as needed

## 📄 License

This project is open source and available for personal and educational use.

## 🤝 Contributing

Feel free to fork, modify, and improve this project. Some ideas:
- Add more questions
- Implement different house systems
- Add user accounts and history
- Create a database for storing results
- Add social sharing features

## 📞 Support

For issues or questions:
1. Check the Troubleshooting section above
2. Verify all files are in correct locations
3. Ensure Flask is properly installed
4. Check browser console for JavaScript errors

---

**Enjoy discovering your Hogwarts house!** 🏰✨
