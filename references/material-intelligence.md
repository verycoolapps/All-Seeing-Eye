# Material Intelligence

## Purpose
Identify, evaluate, and specify materials in visual contexts — their physical properties, visual appearance, appropriate use, and the tells that expose fake or mismatched materials.

## Core knowledge
- **Material categories:** woods (hardwood/softwood, grain patterns, finishes), metals (steel, aluminum, brass, copper, chrome), stone (marble, granite, limestone, travertine), glass (clear, frosted, tinted, textured), ceramics (porcelain, stoneware, terracotta), fabrics (cotton, linen, wool, velvet, leather, synthetic), plastics (ABS, acrylic, polycarbonate), composites.
- **Visual properties:** albedo/color, roughness (matte↔gloss), metallic (0-1), transparency/opacity, texture (grain, weave, pores), reflectivity, subsurface scattering (skin, wax, marble), anisotropy (brushed metal directional highlights).
- **PBR material setup:** base color map, roughness map, metallic map, normal map, height/displacement; correct gamma/linear workflow; texel density consistency.
- **Material realism tells:** wood grain too uniform, marble veins too perfect/random, metal too mirror-like (no micro-scratches), fabric too smooth (no weave), plastic looking like wood (wrong SSS/roughness), glass without thickness or refraction.
- **Age and wear:** patina (bronze verdigris, copper oxidation), scratches (direction follows use), stains (water rings, oil marks), fading (UV exposure), dirt accumulation in crevices.
- **Material pairing:** wood+metal (warm/cool contrast), stone+wood (natural pair), glass+metal (modern), fabric+leather (texture variation); avoid pairing materials with identical visual properties (two shiny plastics).
- **Scale and context:** material choice must suit application — exterior materials weather, interior materials can be delicate; weight implications (stone floors need structure); maintenance (porous stone stains, sealed surfaces wipe clean).

## Evaluation criteria / rules
- Identify material from visual cues: grain pattern → wood type; veining → stone type; weave → fabric; brushed lines → metal finish; transparency → glass/plastic.
- Check physical plausibility: wood grain follows form, stone has consistent veining, metal has directional brushing, fabric drapes with gravity.
- Flag fake materials: plastic-looking wood (no grain depth, wrong roughness), fake marble (veins too uniform or too random), synthetic leather (too perfect, no pores), chrome without environment reflections.
- Evaluate material harmony: do materials complement or compete? Count distinct materials; >5 usually needs justification.
- For specification: name material, finish, color, and intended application; avoid generic "wood" or "metal."
- Consider maintenance: high-traffic areas need durable materials; specify accordingly.

## Confidence & limits
- High confidence: obvious material identification (wood grain, marble veining, metal finish), impossible material properties (transparent wood, matte chrome).
- Medium: wood species from grain alone, stone type from veining, fabric composition.
- Cannot assert: exact material composition without testing, durability ratings, cost, authenticity (real vs. veneer vs. laminate).
- Always note: visual appearance ≠ physical material; renders may simulate materials that don't exist physically.
