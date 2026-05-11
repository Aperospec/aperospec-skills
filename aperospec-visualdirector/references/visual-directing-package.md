# Visual Directing Package Template

Use this template only when the input is a complete Concept Deck Package (CDP) from `aperospec-conceptdeck`.

## Input Gate

Confirm the CDP contains:
- Concept Sequence
- Emotional Curve
- Cognitive Triggers
- Atmosphere Directions
- Narrative Rhythm
- Typography Density
- Silence / Breathing Structure

If fields are missing, ask for a valid CDP from `aperospec-conceptdeck`.

## Required Output

```markdown
# Visual Directing Package (VDP)

## INPUT SOURCE

Concept Deck Package:
[briefly name the concept deck]

## 1. COMPOSITION DIRECTION

For each page:

### Slide [number]

Image-first Composition:
[Confirm the complete Narrative Hero Image is generated before typography placement.]

Standalone Hero Image Value:
[Explain how the Hero Image works independently without text.]

Composition Type:
[Fullscreen / Floating Composition / Cinematic Crop / Split Atmosphere / Black Frame / Minimal Composition]

Negative Space Ratio:
[high / medium-high / medium / low. Default to high unless the concept deck requires pressure.]

Focus Point:
[the first visual focus the audience notices]

Visual Weight:
[emotional weight this page carries in the deck]

## 2. TYPOGRAPHY DIRECTION

Overall typography principle:
[treat type as editorial typography implanted into the image structure, not PPT text]

Image Composition Analysis:
- Light-dark relationship:
- Visual center of gravity:
- Highlight areas:
- Shadow areas:
- Negative space:
- Depth-of-field / blur areas:
- Visual flow:

For each page:
- Amount of text:
- Sentence style:
- Breathing:
- Emotional function:
- Dynamic placement:
- Image-text relationship:

Typography must avoid:
- dense text
- document paragraphs
- bullet points
- enterprise layout
- information-first hierarchy
- fixed left-text/right-image templates
- forcing image cuts or blank text panels

## 3. ATMOSPHERE DIRECTION

For each page:

Lens:
[35mm / 50mm / Wide Lens / Extreme Close-up / Long Shot / other]

Lighting:
[Cold Blue / Warm Natural / Screen Glow / High Contrast / Dark Ambient / other]

Atmosphere:
[Psychological Pressure / Isolation / Silent Anxiety / Emotional Escape / Documentary Reality / other]

Texture:
[Film Grain / Blur Reflection / Digital Noise / Matte Texture / Fog Atmosphere / other]

Camera Feeling:
[Intimate / Distant / Surveillance / Human POV / other]

## 4. VISUAL RHYTHM

Black frame pages:
[which pages are black frames and why]

Still pages:
[which pages should feel still]

Emotional impact pages:
[which pages create visual impact]

Atmosphere pages:
[which pages establish pure atmosphere]

Minimal pages:
[which pages use extreme restraint]

One-sentence pages:
[which pages use only one line]

Rhythm principle:
[how the sequence feels like cinema, not presentation]

## 5. GPT IMAGE 2 PROMPT

For each page:

```text
Lens: [lens]
Lighting: [lighting]
Atmosphere: [atmosphere]
Emotional Tone: [emotion]
Environment: [specific environment]
Time: [time of day / lighting condition]
Texture: [grain / blur / noise / matte / fog]
Cinematic Composition: [composition and framing]
Prompt: [single integrated cinematic Hero Image prompt]
```

After each prompt is generated, GPT Image 2 must be actually called to generate the Hero Image.
Do not stop at prompt writing.
The generated Hero Image must become the dominant visual subject of the corresponding slide.

## 6. HERO IMAGE RENDERING

Image-led rule:
[how the Hero Image dominates the page]

Standalone image rule:
[the Hero Image must still work as a poster, photographic artwork, magazine spread, architectural photograph, or Narrative Scene without typography]

Hero Image insertion rule:
[insert the generated Hero Image into the final PPTX as the page's primary visual body]

Fullscreen default:
[all images are fullscreen unless otherwise specified]

Forbidden styles:
- Canva style
- corporate imagery
- stock photo feel
- generic illustration
- PPT image style

Required aesthetic:
- cinematic
- emotional
- atmospheric
- narrative space
- visual tension
- concept-driven
- architecture photography
- editorial photography
- restrained premium feeling

## 7. IMAGE-FIRST TYPOGRAPHY INTEGRATION

For each page:

Typography placement zone:
[shadow / dark area / sky / wall / depth-of-field / blur / blank area / composition edge / visual pause area]

Placement reason:
[why this typography placement fits the generated Hero Image structure]

Layout intelligence:
[how this page's layout differs from adjacent pages]

Editorial rhythm:
[how image scale, typography, density, and negative space vary from previous and next pages]

## 8. FINAL SLIDE RENDERING NOTES

Final pages should:
[look like a narrative-driven editorial presentation magazine, not a unified-template PPT]

Final deliverable rule:
[render all pages into a deliverable .pptx file. Do not deliver only VDP, prompt text, or a written plan.]
```

## Validation Checklist

Before finalizing, confirm:
- VDP is produced as an intermediate visual directing artifact, not as the final deliverable.
- No world analysis appears.
- No Narrative or Concept Deck is rewritten.
- Every page has Composition Type, Negative Space Ratio, Focus Point, and Visual Weight.
- Every page generates the complete Narrative Hero Image before typography placement.
- Every Hero Image can stand independently without text.
- Typography placement is based on image composition analysis.
- Consecutive pages do not repeat the same Layout Structure.
- Every page has Lens, Lighting, Atmosphere, Texture, and Camera Feeling.
- Every page has a GPT Image 2 Prompt.
- Every page actually calls GPT Image 2 and receives a generated Hero Image.
- Every generated Hero Image is inserted into the final PPTX as the page's primary visual body.
- Final output includes a deliverable .pptx file, not only VDP, prompts, or text planning.
- Slides are Image-led, not Text-led.
- Typography behaves like editorial typography integrated into the image, not Word layout.
