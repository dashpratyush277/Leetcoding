# 🎯 Two Sum Visualizer

An interactive, educational web application that visualizes the "Two Sum" problem using two different algorithms. Perfect for learning algorithms, understanding hash maps, and comparing different approaches to the same problem.

![Two Sum Visualizer](https://img.shields.io/badge/Status-Live-brightgreen) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🎯 What It Does

This visualizer helps you understand how to find two numbers that add up to a target using two different approaches:

- **Brute Force Method** - The "Check Everything" approach (simple to understand)
- **Hash Map Method** - The "Smart Lookup" approach (fast, single pass)

## ✨ Features

### 🎮 Interactive Controls
- **Array Input**: Type or paste comma-separated numbers
- **Target Input**: Set the target sum with visual feedback
- **Preset Examples**: Quick access to common test cases
- **Random Generator**: Generate random arrays for practice

### 🔧 Two Algorithms
- **Brute Force**: Shows nested loop traversal and pair checking
- **Hash Map**: Visualizes complement lookup and hash map updates

### 🎬 Playback Controls
- **Play/Pause**: Animated step-by-step execution
- **Step Forward/Back**: Manual navigation through steps
- **Speed Control**: 5 levels from very slow to very fast
- **Reset**: Start over with current settings

### 💻 Multi-Language Support
- **Python**: Clean, readable syntax
- **JavaScript**: Modern ES6+ features
- **Java**: Object-oriented approach with helper methods

### 📚 Educational Features
- **Real-time Explanations**: Plain English step-by-step commentary
- **Code Breakdowns**: Line-by-line explanations for each language
- **Complexity Analysis**: Time and space complexity for each algorithm
- **Before/After Comparison**: Visual comparison of original vs rotated array

## 🚀 Getting Started

### Option 1: Direct Use
1. Download `index.html`
2. Open it in any modern web browser
3. Start exploring immediately!

### Option 2: Live Demo
Visit the live demo at: **[https://two-sum-leetcode.netlify.app/](https://two-sum-leetcode.netlify.app/)**

## 🎯 How to Use

### Basic Usage
1. **Choose an Array**: Enter numbers like `2,7,11,15` or use presets
2. **Set Target**: Use the input field to set the target sum
3. **Pick Algorithm**: Select from Brute Force or Hash Map
4. **Watch the Magic**: Hit Play to see the algorithm in action!

### Example Walkthroughs

#### Example 1: `[2,7,11,15]` with `target=9`
- **Result**: `[0,1]` (indices of 2 and 7)
- **What happens**: 2 + 7 = 9, so we return their positions

#### Example 2: `[3,2,4]` with `target=6`
- **Result**: `[1,2]` (indices of 2 and 4)
- **What happens**: 2 + 4 = 6, so we return their positions

#### Example 3: `[3,3]` with `target=6`
- **Result**: `[0,1]` (indices of both 3s)
- **What happens**: 3 + 3 = 6, so we return their positions

### Keyboard Shortcuts
- **Space**: Play/Pause
- **← →**: Step forward/backward
- **R**: Reset visualization

## 🔍 Algorithm Details

### 1. Brute Force Method
```python
def twoSum(nums, target):
    n = len(nums)
    
    # Check every pair of numbers
    for i in range(n):
        for j in range(i + 1, n):
            if nums[i] + nums[j] == target:
                return [i, j]  # Found the pair!
    
    return []  # No solution found
```

**Pros**: Simple to understand, no extra space
**Cons**: Slow for large arrays
**Time Complexity**: O(n²)
**Space Complexity**: O(1)

### 2. Hash Map Method
```python
def twoSum(nums, target):
    hashmap = {}           # Store numbers we've seen
    
    for i, num in enumerate(nums):
        complement = target - num  # What number do we need?
        
        if complement in hashmap:
            return [hashmap[complement], i]  # Found the pair!
        
        hashmap[num] = i    # Remember this number and its position
    
    return []  # No solution found
```

**Pros**: Fast, single pass through array
**Cons**: Uses extra space for hash map
**Time Complexity**: O(n)
**Space Complexity**: O(n)

## 🎨 Visual Features

### Color-Coded Elements
- **Blue**: Currently active element being checked
- **Green**: Second element being checked (brute force)
- **Red**: Found solution elements
- **Orange**: Visited elements (hash map method)

### Animations
- **Smooth Transitions**: Elements highlight as they're checked
- **Hash Map Updates**: Real-time hash map visualization
- **Step Counter**: Track progress through algorithm
- **Target Display**: Prominent target sum display

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

### Performance
- **Lightweight**: Single HTML file (~50KB)
- **Fast Loading**: No external resources
- **Smooth Animations**: 60fps transitions
- **Memory Efficient**: Minimal memory footprint

## 📚 Educational Value

### For Beginners
- **Visual Learning**: See algorithms in action
- **Plain English**: No jargon, just clear explanations
- **Step-by-Step**: Understand each operation
- **Multiple Languages**: Learn syntax differences

### For Students
- **Algorithm Comparison**: See trade-offs between approaches
- **Complexity Analysis**: Understand time and space requirements
- **Code Examples**: Copy-paste ready implementations
- **Interactive Practice**: Try different inputs and parameters

### For Developers
- **Interview Prep**: Common algorithm interview question
- **Code Review**: Compare different implementation styles
- **Performance Analysis**: Understand algorithm efficiency
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

### Ideas for Enhancement
- Add more algorithms (Three Sum, Four Sum)
- Include more programming languages (C++, Go, Rust)
- Add unit tests and validation
- Improve mobile responsiveness
- Add dark mode theme
- Add more LeetCode problems (Valid Parentheses, Merge Intervals)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **LeetCode**: For the original problem inspiration
- **Algorithm Community**: For sharing knowledge and techniques
- **Open Source**: For the tools and libraries that made this possible

## 📞 Support

Having trouble? Here's how to get help:

1. **Check the Issues**: Look for similar problems
2. **Create an Issue**: Describe your problem clearly
3. **Include Details**: Browser, steps to reproduce, expected vs actual behavior

## 🌟 Star History

If you found this project helpful, please give it a star! ⭐

---

**Made with ❤️ for the coding community**

*Happy coding and happy learning!* 🚀
