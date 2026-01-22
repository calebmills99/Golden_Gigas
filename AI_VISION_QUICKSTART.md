# AI-Vision Prompt Refinement Feature - Quick Start Guide

## Overview
The Golden Gigas notebook now includes an intelligent AI-vision step that automatically refines your Stability AI prompts for better image quality!

## What Does It Do?
Takes your simple prompt like:
```
"Dorothy at a kitchen table"
```

And transforms it into a detailed, optimized prompt like:
```
"Comic-book style illustration featuring Dorothy Zbornak seated at a sunlit kitchen table 
in Miami, morning golden hour lighting streaming through windows, her expressive face 
showing determined concentration, warm wood tones, vintage 1980s kitchen aesthetic, 
detailed character rendering, vibrant colors, professional comic panel composition, 4k quality"
```

## Setup Instructions

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

This installs:
- `jupyter` - For running the notebook
- `requests` - For Stability AI API calls
- `openai` - For AI-vision prompt refinement

### 2. Set API Keys
```bash
# Required for image generation
export STABILITY_API_KEY='your-stability-ai-key'

# Optional but recommended for prompt refinement
export OPENAI_API_KEY='your-openai-key'
```

### 3. Launch Jupyter
```bash
jupyter notebook
```

### 4. Open the Notebook
Open `npm_tutorial_golden_girls.ipynb` in your browser

### 5. Uncomment the Functions
Find and uncomment these cells:
- Cell 2: `refine_prompt_with_ai_vision` function
- Cell 3: `generate_stability_image` function

### 6. Generate Images!

**Without AI-vision refinement:**
```python
generate_stability_image(
    "Dorothy confused at laptop",
    "images/dorothy.png"
)
```

**With AI-vision refinement (RECOMMENDED!):**
```python
generate_stability_image(
    "Dorothy confused at laptop",
    "images/dorothy.png",
    refine_prompt=True,
    context="Educational comic about npm. Dorothy is the teacher."
)
```

## How It Works

1. **You provide a basic prompt** - Keep it simple!
2. **AI-vision analyzes it** - GPT-4 understands the context
3. **Prompt gets enhanced** - Adds lighting, composition, art style details
4. **Stability AI generates** - Creates a better image from the refined prompt
5. **You get amazing results!** - Higher quality with less effort

## Benefits

✅ **Better Quality** - More detailed, professional-looking images  
✅ **Consistency** - Characters look like themselves across all images  
✅ **Time Saving** - No need to manually craft complex prompts  
✅ **Easy to Use** - Just add `refine_prompt=True`  
✅ **Context Aware** - Understands Golden Girls characters and scenes  

## Cost Estimate

- **Without refinement**: ~$0.04-0.10 per image (Stability AI only)
- **With refinement**: ~$0.05-0.13 per image (adds ~$0.01-0.03 for GPT-4)

The small cost increase is worth it for the quality improvement!

## Troubleshooting

### "NameError: name 'refine_prompt_with_ai_vision' is not defined"
→ Make sure you uncommented the function in Cell 2

### "OpenAI API error"
→ Check that your OPENAI_API_KEY environment variable is set correctly

### "Refinement failed, using original prompt"
→ The system will gracefully fall back to your original prompt if refinement fails

## Examples

All example cells in the notebook now show two options:

**Option 1: Original (without refinement)**
```python
# generate_stability_image(
#     "Dorothy at kitchen table",
#     "images/dorothy.png"
# )
```

**Option 2: With AI-vision refinement**
```python
# generate_stability_image(
#     "Dorothy at kitchen table",
#     "images/dorothy_refined.png",
#     refine_prompt=True,
#     context="Educational comic. Dorothy teaching npm."
# )
```

## Tips for Best Results

1. **Always use context** - Helps the AI understand your scene better
2. **Keep base prompts simple** - Let the AI add the details
3. **Be specific in context** - "Dorothy frustrated" vs "Dorothy happy"
4. **Compare results** - Generate with and without refinement to see the difference
5. **Iterate if needed** - Adjust your context for even better results

## Character Context Examples

**Dorothy:**
```
context="Educational comic about npm. Dorothy is the teacher - frustrated but determined."
```

**Sophia:**
```
context="Golden Girls comic. Sophia sharing Sicily wisdom about code reuse."
```

**Blanche:**
```
context="Golden Girls tutorial. Blanche making tech look glamorous and sophisticated."
```

**Rose:**
```
context="Educational comic. Rose using St. Olaf analogies to explain concepts."
```

**Group scenes:**
```
context="All four Golden Girls celebrating with cheesecake after success."
```

## Testing

Run the test suite to validate the feature:
```bash
python3 test_ai_vision_refinement.py
```

This runs mock tests that don't require API keys.

## Support

- 📖 See README.md for full documentation
- 🐛 Open an issue on GitHub for bugs
- 💡 Share your refined prompts with the community!

---

**Remember:** The AI-vision refinement is optional but highly recommended for the best results! 

Stay Golden! 🌟
