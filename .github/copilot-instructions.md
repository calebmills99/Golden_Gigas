# Golden Gigas - Copilot Instructions

## Repository Overview

This repository contains **Golden Gigas** - an educational project that teaches npm and package management through Golden Girls-themed tutorials. The project uses humor, storytelling, and beloved characters to make technical education memorable and engaging.

**Core Philosophy**: "Boring is the only unforgivable sin in education." This codebase prioritizes memorable, entertaining education over conventional technical writing.

## Project Type & Languages

- **Project Type**: Educational Jupyter notebook with optional AI image generation
- **Primary Language**: Python 3.x
- **Main Components**:
  - Jupyter notebook (`npm_tutorial_golden_girls.ipynb`)
  - Python test suite (`test_ai_vision_refinement.py`)
  - Documentation (README.md, AI_VISION_QUICKSTART.md)

## Dependencies & Requirements

Dependencies are managed via `requirements.txt`:
- `jupyter>=1.0.0` - Core notebook functionality
- `requests>=2.31.0` - Stability AI image generation
- `openai>=1.0.0` - AI-vision prompt refinement (optional)

### Installing Dependencies
```bash
pip install -r requirements.txt
```

## Build & Test Instructions

### Running the Jupyter Notebook
```bash
# Install dependencies first
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook

# Open npm_tutorial_golden_girls.ipynb in the browser interface
```

### Running Tests
```bash
# Run the AI-vision refinement test suite
python3 test_ai_vision_refinement.py
```

Expected output: All tests should pass with "🎉 ALL TESTS PASSED!" message.

**Note**: Tests are mock tests that don't require API keys. They validate the prompt refinement logic without making actual API calls.

### Setting Up API Keys (Optional)
For image generation features (optional functionality):
```bash
export STABILITY_API_KEY='your-stability-ai-key'  # For image generation
export OPENAI_API_KEY='your-openai-key'  # For AI-vision prompt refinement
```

## Project Layout

### Root Directory Files
- `README.md` - Main documentation with the project philosophy and setup instructions
- `npm_tutorial_golden_girls.ipynb` - Main Jupyter notebook tutorial
- `requirements.txt` - Python dependencies
- `test_ai_vision_refinement.py` - Test suite for AI-vision feature
- `AI_VISION_QUICKSTART.md` - Quick start guide for the AI-vision prompt refinement feature
- `.gitignore` - Git ignore patterns

### Directory Structure
```
Golden_Gigas/
├── .github/
│   └── copilot-instructions.md (this file)
├── npm_tutorial_golden_girls.ipynb
├── test_ai_vision_refinement.py
├── requirements.txt
├── README.md
├── AI_VISION_QUICKSTART.md
└── .gitignore
```

## Key Features

### 1. Educational Jupyter Notebook
The main tutorial teaches npm through a six-act Golden Girls storyline:
- Act 1: Introduction to npm
- Act 2: Package installation
- Act 3: Understanding node_modules
- Act 4: Version conflicts and troubleshooting
- Act 5: npm scripts and semantic versioning
- Act 6: Final resolution and best practices

### 2. AI-Vision Prompt Refinement
Optional feature that enhances Stability AI image generation prompts:
- Takes simple prompts and adds lighting, composition, and technical details
- Context-aware based on Golden Girls characters and scenes
- Gracefully falls back to original prompt if refinement fails

## Validation & Testing

### Pre-commit Validation
No automated CI/CD pipelines are currently configured. Manual validation steps:

1. **Test the Python code**:
   ```bash
   python3 test_ai_vision_refinement.py
   ```
   All tests must pass.

2. **Validate Jupyter notebook** (if modified):
   ```bash
   jupyter notebook --execute npm_tutorial_golden_girls.ipynb
   ```
   Ensure cells execute without errors (API calls may be commented out).

3. **Check Python syntax**:
   ```bash
   python3 -m py_compile test_ai_vision_refinement.py
   ```

### Code Style
- Python code follows standard PEP 8 conventions
- Documentation uses an intentionally casual, humorous tone - this is by design
- Comments should match the existing Golden Girls-themed voice

## Important Notes

### Content Style Guidelines
- **DO maintain the humorous, Golden Girls-themed voice** in all documentation
- **DO keep educational content accurate** despite the entertaining presentation
- **DO NOT make documentation "more professional"** - the casual, fun tone is intentional
- **DO respect the philosophy**: memorable > conventional

### Modification Guidelines
When making changes:
- Test changes using the test suite
- Maintain the Golden Girls character voices and humor
- Keep technical accuracy high even when presentation is casual
- Don't remove or "professionalize" the unique storytelling approach
- Remember: "Boring is the only unforgivable sin"

### Dependencies
- No dependency on Node.js/npm to RUN the tutorial (it teaches npm conceptually)
- Users may install Node.js/npm separately to follow along with examples
- All Python dependencies are in requirements.txt

### Common Pitfalls
- Don't assume the notebook will have API keys set up - image generation is optional
- Test suite uses mocks and doesn't require API keys
- The notebook file is JSON - edit carefully to avoid corruption
- The project has no build artifacts or compiled code

## Quick Reference

### File Purposes
- `npm_tutorial_golden_girls.ipynb` - Main educational content
- `test_ai_vision_refinement.py` - Validates AI-vision refinement logic
- `requirements.txt` - Python dependencies
- `README.md` - Project documentation and philosophy
- `AI_VISION_QUICKSTART.md` - Setup guide for optional AI features

### Commands Summary
```bash
# Setup
pip install -r requirements.txt

# Run notebook
jupyter notebook

# Run tests
python3 test_ai_vision_refinement.py

# Validate Python syntax
python3 -m py_compile test_ai_vision_refinement.py
```

## Trust These Instructions

These instructions are comprehensive and tested. Only search for additional information if something in these instructions is incomplete or incorrect. The unique educational approach and tone are intentional design choices, not mistakes to be corrected.
