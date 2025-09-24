# 🔄 Array Rotation Visualizer

An interactive, educational web application that visualizes the "rotate array to the right by k steps" problem using three different algorithms. Perfect for learning algorithms, understanding array manipulation, and comparing different approaches to the same problem.

![Array Rotation Visualizer](https://img.shields.io/badge/Status-Live-brightgreen) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🎯 What It Does

This visualizer helps you understand how to rotate an array to the right by k steps using three different approaches:

- **Extra Array Method** - The "Copy and Paste" approach (easy to understand)
- **Reverse Method** - The "Flip and Flip Again" trick (in-place, O(1) space)
- **Cyclic Replacements** - The "Musical Chairs" approach (mathematically elegant)

## ✨ Features

### 🎮 Interactive Controls
- **Array Input**: Type or paste comma-separated numbers
- **K Slider**: Adjust rotation steps with visual feedback
- **Preset Examples**: Quick access to common test cases
- **Random Generator**: Generate random arrays for practice

### 🔧 Three Algorithms
- **Extra Array**: Shows mapping arrows and temporary array
- **Reverse Method**: Visualizes the three-step reversal process
- **Cyclic Replacements**: Shows cycle detection and element movement

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
Visit the live demo at: **[https://cerulean-mooncake-78f68b.netlify.app/](https://rotating-array.netlify.app/)**

## 🎯 How to Use

### Basic Usage
1. **Choose an Array**: Enter numbers like `1,2,3,4,5,6,7` or use presets
2. **Set K**: Use the slider or input field to set rotation steps
3. **Pick Algorithm**: Select from Extra Array, Reverse, or Cyclic
4. **Watch the Magic**: Hit Play to see the algorithm in action!

### Example Walkthroughs

#### Example 1: `[1,2,3,4,5,6,7]` with `k=3`
- **Result**: `[5,6,7,1,2,3,4]`
- **What happens**: Each element moves 3 positions to the right, wrapping around

#### Example 2: `[-1,-100,3,99]` with `k=2`
- **Result**: `[3,99,-1,-100]`
- **What happens**: Elements shift right by 2 positions

### Keyboard Shortcuts
- **Space**: Play/Pause
- **← →**: Step forward/backward
- **R**: Reset visualization

## 🔍 Algorithm Details

### 1. Extra Array Method
```python
def rotate(nums, k):
    n = len(nums)
    k = k % n
    temp = [0] * n
    
    for i in range(n):
        temp[(i + k) % n] = nums[i]
    
    nums[:] = temp
```

**Pros**: Easy to understand, straightforward
**Cons**: Uses O(n) extra space
**Time Complexity**: O(n)
**Space Complexity**: O(n)

### 2. Reverse Method
```python
def rotate(nums, k):
    n = len(nums)
    k = k % n
    
    nums.reverse()           # Step 1: Reverse entire array
    nums[:k] = nums[:k][::-1]  # Step 2: Reverse first k elements
    nums[k:] = nums[k:][::-1]  # Step 3: Reverse remaining elements
```

**Pros**: In-place, constant extra space
**Cons**: Less intuitive, requires understanding of reversals
**Time Complexity**: O(n)
**Space Complexity**: O(1)

### 3. Cyclic Replacements
```python
def rotate(nums, k):
    n = len(nums)
    k = k % n
    count = 0
    start = 0
    
    while count < n:
        current = start
        prev = nums[start]
        
        while True:
            next_idx = (current + k) % n
            nums[next_idx], prev = prev, nums[next_idx]
            current = next_idx
            count += 1
            
            if current == start:
                break
        
        start += 1
```

**Pros**: In-place, mathematically elegant
**Cons**: Complex to understand, requires cycle detection
**Time Complexity**: O(n)
**Space Complexity**: O(1)

## 🎨 Visual Features

### Color-Coded Elements
- **Blue**: Currently active element
- **Green**: Destination position
- **Orange**: Visited elements (cyclic method)
- **Purple**: Highlighted range (reverse method)

### Animations
- **Smooth Transitions**: Elements slide to new positions
- **Mapping Arrows**: Show element movement paths
- **Step Counter**: Track progress through algorithm
- **Real-time Updates**: Array changes as you watch

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
- Add more algorithms (left rotation, matrix rotation)
- Include more programming languages (C++, Go, Rust)
- Add unit tests and validation
- Improve mobile responsiveness
- Add dark mode theme

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

