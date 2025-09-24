# Next Permutation Visualizer

An interactive, educational web application that visualizes the "Next Permutation" algorithm step-by-step. Perfect for learning algorithms, understanding permutations, and seeing how the algorithm transforms arrays.

## 🎯 Live Demo

**Try it now**: [https://next-permutation.netlify.app/](https://next-permutation.netlify.app/)

## ✨ Features

### 🎮 Interactive Controls
- **Array Input**: Type or paste comma-separated numbers
- **Preset Examples**: Quick access to common test cases like [1,2,3], [3,2,1], [1,1,5]
- **Language Selector**: Switch between Python, JavaScript, and Java implementations
- **Step Controls**: Play/Pause/Next Step/Reset for full control

### 📊 Visual Learning
- **Step-by-Step Visualization**: See each element highlighted as the algorithm processes it
- **Color-Coded Elements**: Different colors for scanning, pivoting, swapping, and reversing
- **Real-time Array Updates**: Watch the array transform during swaps and reversals
- **Index Labels**: Clear indication of array positions

### 💻 Multi-Language Support
- **Python**: Clean, readable implementation
- **JavaScript**: Modern ES6+ syntax
- **Java**: Traditional OOP approach with helper methods
- **Syntax Highlighting**: Current step highlighted in code

### 📚 Educational Features
- **Dynamic Explanations**: Step-by-step commentary that adapts to the current state
- **Plain English Descriptions**: No jargon, just clear explanations
- **Algorithm Overview**: Understand the three key steps of the algorithm

## 🎯 How to Use

1. **Choose an Array**: Enter numbers like `1,2,3` or use presets
2. **Select Language**: Pick Python, JavaScript, or Java
3. **Watch the Magic**: Hit "Next Step" or "Play" to see the algorithm in action!

### Example Walkthroughs

#### Example 1: `[1,2,3]` → `[1,3,2]`
- **Step 1**: Find pivot at index 1 (value 2)
- **Step 2**: Find swap target at index 2 (value 3)
- **Step 3**: Swap and reverse suffix
- **Result**: `[1,3,2]`

#### Example 2: `[3,2,1]` → `[1,2,3]`
- **Special Case**: Array is in descending order
- **Action**: Reverse the entire array
- **Result**: `[1,2,3]`

#### Example 3: `[1,1,5]` → `[1,5,1]`
- **Step 1**: Find pivot at index 1 (value 1)
- **Step 2**: Find swap target at index 2 (value 5)
- **Step 3**: Swap and reverse suffix
- **Result**: `[1,5,1]`

## 🔍 Algorithm Details

The Next Permutation algorithm follows three key steps:

1. **Find Pivot**: Scan from right to left to find the first decreasing element
2. **Find Swap Target**: Find the smallest element to the right that's greater than the pivot
3. **Swap & Reverse**: Swap the pivot with the target, then reverse the suffix

### Time Complexity: O(n)
### Space Complexity: O(1)

## 🛠️ Technical Details

### Built With
- **HTML5**: Semantic structure and accessibility
- **CSS3**: Modern styling with gradients and animations
- **Vanilla JavaScript**: No external dependencies
- **Responsive Design**: Works on desktop, tablet, and mobile

### Browser Support
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 📚 Educational Value

### For Beginners
- **Visual Learning**: See algorithms in action
- **Plain English**: No jargon, just clear explanations
- **Step-by-Step**: Understand each operation
- **Multiple Languages**: Learn syntax differences

### For Students
- **Algorithm Understanding**: See how permutations work
- **Code Examples**: Copy-paste ready implementations
- **Interactive Practice**: Try different inputs and see results

### For Developers
- **Interview Prep**: Common algorithm interview question
- **Code Review**: Compare different implementation styles
- **Best Practices**: See clean, commented code

## 🤝 Contributing

Contributions are welcome! Here are some ways you can help:

### Bug Reports
- Found a bug? Open an issue with details
- Include browser version and steps to reproduce

### Feature Requests
- Have an idea? Open an issue with your suggestion
- Explain the use case and expected behavior

### Code Contributions
- Fork the repository
- Create a feature branch
- Make your changes
- Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **LeetCode**: For the original problem inspiration
- **Algorithm Community**: For sharing knowledge and techniques
- **Open Source**: For the tools and libraries that made this possible

---

**Made with ❤️ for the coding community**

*Happy coding and happy learning!* 🚀