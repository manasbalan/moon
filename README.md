# Moon

# Product Concept Design & 3D Interactive Landing Page

**Overview**

Moon.html is a high-end, futuristic, single-file concept design and marketing landing page for a fictional flagship smartphone named "Moon One." It features a deep-space aesthetic, cinematic 3D scroll-driven camera movements via Three.js, and an immersive user journey that mimics diving into the device's physical layers, camera optics, and internal architecture.

**Key Features & Visual Design**

Unified Deep-Space Theme: Built with a dark palette featuring deep cosmic gradients (#05070d to #020407), soft lunar-champagne accents (#d8c6a4), and subtle starfield backgrounds powered by layered CSS radial gradients and point shaders.  
Scroll-Driven Camera Runway: A massive 1700vh scroll container pins a 3D WebGL stage. Scrolling drives a cinematic camera dive that transitions from the Moon down to the phone's back glass, tilts through parallax orbit layers, zooms into the physical lens, and explores exploded internal components.  
Interactive Tilt Parallax: Real-time pointer tracking tilts the 3D phone model and shifts the nested orbit planes against each other.  
Dynamic Morphing & Exploded Views: The 3D scene features a morphing sequence where a procedural moon splits apart down its center seam to reveal a physical multi-element camera lens underneath.  
**Modular Specifications & Lineup**: Cleanly structured sections detail hardware features (Snapdragon 8 Elite Gen 6, 200MP Night Sensor, Vapour Chamber cooling, 120W charging) alongside a 3-tier product lineup (Moon Lite, Moon One, and Moon Pro).  
Responsive Layout: Gracefully scales from ultra-wide desktop monitors down to mobile viewports with adjusted padding, safe-area insets, and touch-optimized navigation.  

**Technical Architecture**

1. File Structure (Single-File Component)
HTML5 Markup (<main>, <section>, <div class="stage">): Houses the text overlays, dynamic chapter cards, specs grid, lineup pricing cards, and pre-order form.
CSS3 Styling (<style>): Utilizes custom CSS properties (:root), Flexbox/Grid layouts, fluid typography (clamp()), and smooth transitions. Incorporates Google Fonts (Sora for display text and Inter for body/labels).  
JavaScript & WebGL Engine (<script>):
Powered by Three.js (r128) loaded via CDN.  
Generates procedural canvas textures on-the-fly for moon maps, bump maps, PCB layouts, battery cells, copper vapour chambers, and chip inscriptions.
Manages camera keyframing, scroll interpolation, and smooth easing loops (requestAnimationFrame).
Implements graceful degradation: if WebGL initialization fails, it falls back to static layout elements (#fb) without breaking the page.
 
**Scroll Narrative Journey (The Chapter Sequence)**

The user's scroll position (p) maps to distinct stage transformations:
00 Deep Space (#c0): Intro view of the Moon floating against a starfield.  
01 Orbit Glass (#c1): The phone’s back glass appears, featuring layered planetary rings orbiting the camera module.  
02 Depth Parallax (#c2): Highlights the multi-depth card structure as the phone tilts.  
03 Side Rail (#cs): Focuses on the milled aluminium ruler edge and the 28-segment Side Light strip.  
04 Lens Revealed (#c3): The moon parts like an aperture to expose the real 200MP f/1.6 lens.  
05 Exploded View (#c4): The phone’s 8 internal layers pull apart (Orbit layers \rightarrow Camera \rightarrow Glass \rightarrow Cooling \rightarrow Processor \rightarrow Battery \rightarrow Logic Board \rightarrow Display).  
06–10 Hardware Deep Dives (#k1 to #k5): Sequential camera, processor, vapour chamber, battery, and curved display breakdowns.  
11 Moon One Finale (#c5): Returns to the full device view ahead of specs, pricing, and pre-order registration.  
Interactive Elements & Components
Pre-order Form (#form): Features client-side email regex validation with clean state messaging (.msg) for the concept interface.  
Dynamic Header (.top / .where): Automatically tracks the active section index and updates the chapter subtitle indicator in real time.
