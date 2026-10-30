# Character Setup Prompts

> **How to use:** These templates help create consistent character reference sheets and alternate views. Replace bracketed placeholders and check anatomy, clothing, and identity consistency before using outputs in a video.
>
> **Source:** [Original Google Doc tab](https://docs.google.com/document/d/1RgXPPnZDVRpd6gduzfA2LjNzKQQubsoMhPTooiIvAOo/edit?tab=t.jd05nlrm8iy0)
>
> **Editorial note:** The source prompts are preserved in their original order with only light Markdown structure and em dash cleanup. Instructions above are added for clarity. Validate tool-specific features before relying on them.

## Source material

Character Setup Prompt :

### PROMPT : 1

Full-body triptych, three distinct views: front facing, 3/4 side view, and back view. High resolution, flat studio lighting, consistent anatomical proportions across all views, solid white background. [DESCRIBE BODY AND OUTFIT]

### PROMPT : 2

{

"character_sheet_generator": {

"render_style_override": {

"style": "Photorealistic",

"description": "This must NOT look like 3D cartoon, Pixar animation, Disney animation, CGI-stylized character, or toy-like render. The result must look like a real photograph of a real human being ,  natural skin texture with pores, natural imperfections, realistic muscle and bone structure, real fabric texture, real hair strands (not smooth cartoon hair), natural lighting like a professional photoshoot.",

"avoid": [

"3D cartoon look",

"Pixar-style rendering",

"Disney animation style",

"plastic/toy-like skin",

"over-smoothed CGI skin",

"exaggerated cartoon proportions",

"glossy animated eyes",

"stylized illustration look"

],

"target_look": "Ultra-realistic photography, DSLR quality, studio photoshoot of a real person in costume, hyper-realistic skin texture, real fabric folds and weight, real hair physics, cinematic realism"

},

"reference_instructions": {

"face_lock": true,

"description": "Use the EXACT facial features from the uploaded reference photo. Same face shape, same eye shape and color, same nose structure, same lip shape, same skin tone, same distinguishing facial features (moles, dimples, jawline, scars, etc.). Render with REAL human skin texture, not smooth animated skin.",

"rules": [

"Do NOT alter, beautify, or generate a different face",

"Do NOT apply cartoon or CGI stylization to the face",

"Do NOT smooth out natural skin texture ,  keep realistic pores, subtle texture, natural skin tone variation",

"Generated character face must be 100% recognizable as the same person from uploaded photo",

"Treat uploaded photo as single source of truth for facial identity AND for skin realism reference"

]

},

"character_base": {

"age": "match_uploaded_photo",

"body_type": "",

"face_shape": "extracted_from_uploaded_photo",

"skin_tone": "extracted_from_uploaded_photo_photorealistic",

"skin_texture": "real_human_skin_with_natural_pores_and_texture",

"eye_shape": "extracted_from_uploaded_photo",

"eye_color": "extracted_from_uploaded_photo",

"eyebrows": "match_uploaded_photo",

"hair_color": "match_uploaded_photo",

"hair_texture": "real_strand_by_strand_hair_not_cartoon_smooth",

"hairstyle": "",

"distinguishing_features": "preserve_all_moles_scars_dimples_from_photo"

},

"costume": {

"outfit": "",

"footwear": "",

"jewelry": "",

"accessories": "",

"weapons_or_props": "",

"color_palette": "",

"material_texture": "real_fabric_texture_with_natural_folds_weight_and_sheen_not_plastic_or_cartoon_cloth"

},

"facial_expression": {

"primary_expression": "",

"expression_consistency_rule": "Face must remain anatomically identical to reference photo across all expression variants, with realistic micro-expressions like a real photograph",

"eye_focus": "camera_direct_or_specified"

},

"pose_and_views": {

"required_views": [

{

"view_name": "close_up_front_facing",

"description": "Head and shoulders only, direct eye contact with camera, professional studio portrait lighting, maximum realistic facial detail visible, like a real DSLR headshot"

},

{

"view_name": "front_view_full_body",

"description": "Standing pose, full body visible, front-facing, photorealistic studio photography"

},

{

"view_name": "back_view_full_body",

"description": "Full body, back turned to camera, photorealistic"

},

{

"view_name": "left_profile",

"description": "90 degree left side view, full body, photorealistic"

},

{

"view_name": "right_profile",

"description": "90 degree right side view, full body, photorealistic"

},

{

"view_name": "three_quarter_angle_45",

"description": "45 degree angled view, full body, photorealistic"

},

{

"view_name": "hero_pose",

"description": "Dynamic, confident stance, full body, photorealistic"

},

{

"view_name": "neutral_pose",

"description": "Relaxed standing pose, full body, photorealistic"

},

{

"view_name": "t_pose",

"description": "Arms extended horizontally, animation-reference pose, full body, photorealistic"

},

{

"view_name": "full_turnaround_sheet",

"description": "All angles combined into single character sheet layout, consistent photorealistic rendering across every panel"

}

]

},

"style_and_technical": {

"render_quality": "Photorealistic, hyper-realistic photography",

"rendering_reference": "Professional studio photoshoot quality, like a real actor in costume photographed by a DSLR camera",

"detail_level": "Ultra detailed, real skin pores, real fabric weave, real hair strands",

"camera_reference": "Shot on DSLR/mirrorless camera, 85mm portrait lens feel, natural depth of field",

"mesh_or_render_type": "Photographic realism, NOT 3D animated render",

"texture_resolution": "8K photographic detail",

"lighting": "Professional studio lighting setup, soft key light with natural shadow falloff, no flat cartoon lighting",

"background": "Pure white background, seamless studio backdrop",

"layout_type": "Character reference sheet, turnaround style, multiple angles in grid format",

"output_resolution": "4K",

"restrictions": [

"No text overlays",

"No watermark",

"No logos",

"No cartoon rendering",

"No 3D animated look",

"No plastic/glossy skin",

"No extra fingers or limb distortion",

"No facial feature drift between views"

]

},

"consistency_lock": {

"face_identity_lock": true,

"rule": "Every single angle and pose must show the SAME real face ,  same bone structure, same eye spacing, same facial proportions, same realistic skin as uploaded reference photo. No angle should look cartoon-ish or CGI-animated.",

"costume_lock": "Costume, jewelry, and accessories remain identical and photorealistic across all views",

"color_lock": "Color palette must remain consistent across all views, no drift or shift",

"style_lock": "Photorealistic style must remain identical across ALL views ,  no single panel should shift toward cartoon or 3D-animated rendering"

},

"usage_notes": {

"step_1": "Upload reference photo of the face/character to be used",

"step_2": "Fill in bracketed/empty fields above (costume, age, pose theme) as per project needs",

"step_3": "Keep face and skin-related fields as photorealistic reference so the AI treats the photo as a real-photography reference, not a stylization reference",

"step_4": "Submit this JSON prompt along with the uploaded photo to an image generation tool that supports face-reference or character-reference input",

"recommended_tools_note": "If your tool has a style/render-mode selector, explicitly select 'Photorealistic' or 'Realistic Photography' mode instead of '3D/Cartoon/Illustration' mode before generating"

}

}

}
