# Contributing to Diabetes Prediction ML Project

First off, thank you for considering contributing to this project! 🎉

## How Can I Contribute?

### 🐛 Reporting Bugs

If you find a bug, please create an issue with:
- Clear title and description
- Steps to reproduce the issue
- Expected vs actual behavior
- Screenshots (if applicable)
- Your environment details (OS, Python version, etc.)

### 💡 Suggesting Enhancements

Have an idea to improve the project? Great! Please:
- Check if the suggestion already exists in issues
- Create a new issue with tag "enhancement"
- Clearly describe your idea and its benefits
- Provide examples if possible

### 🔧 Pull Requests

1. **Fork the Repository**
   ```bash
   git clone https://github.com/shreyashpatil530/diabetes-prediction-ml.git
   ```

2. **Create a Branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. **Make Your Changes**
   - Write clean, readable code
   - Follow existing code style
   - Add comments where necessary
   - Update documentation if needed

4. **Test Your Changes**
   - Ensure all existing tests pass
   - Add new tests if applicable
   - Run the notebook/script to verify

5. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "Add: Brief description of your changes"
   ```

6. **Push to GitHub**
   ```bash
   git push origin feature/AmazingFeature
   ```

7. **Open a Pull Request**
   - Go to the original repository
   - Click "New Pull Request"
   - Describe your changes clearly
   - Link any related issues

## 📝 Code Style Guidelines

- Use **4 spaces** for indentation (not tabs)
- Follow **PEP 8** style guide for Python
- Use **meaningful variable names**
- Add **docstrings** to functions
- Keep functions **small and focused**
- Add **comments** for complex logic

### Example:
```python
def calculate_bmi(weight: float, height: float) -> float:
    """
    Calculate Body Mass Index (BMI).
    
    Args:
        weight (float): Weight in kilograms
        height (float): Height in meters
    
    Returns:
        float: Calculated BMI value
    """
    return weight / (height ** 2)
```

## 🧪 Testing

- Test your code before submitting
- Ensure notebook runs without errors
- Check all visualizations display correctly
- Verify model predictions are accurate

## 📚 Documentation

If you add new features:
- Update README.md
- Add usage examples
- Include necessary comments
- Update requirements.txt if needed

## ✅ Checklist Before Submitting PR

- [ ] Code follows project style guidelines
- [ ] All tests pass successfully
- [ ] Documentation is updated
- [ ] Commit messages are clear and descriptive
- [ ] No merge conflicts with main branch
- [ ] Screenshots added for UI changes (if any)

## 🤔 Questions?

Feel free to:
- Open an issue with tag "question"
- Contact the maintainer
- Check existing discussions

## 🙏 Thank You!

Your contributions make this project better for everyone!

---

**Happy Coding! 🚀**
