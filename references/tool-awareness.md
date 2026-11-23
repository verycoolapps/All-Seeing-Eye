# Tool Awareness

## Purpose
Enable the agent to understand and leverage available tools — when to use them, how to interpret results, and the limitations of each capability.

## Core knowledge
- **Tool categories:** vision tools (image analysis, OCR, object detection), generation tools (image generation, 3D modeling, rendering), analysis tools (color extraction, composition analysis, metadata reading), reference tools (search, comparison, style lookup), output tools (export, format conversion, delivery).
- **Vision tool capabilities:** image description, object detection, scene classification, text extraction (OCR), face detection, color analysis, composition analysis, quality assessment; limitations: resolution limits, occlusion, ambiguous objects, style recognition gaps.
- **Generation tool capabilities:** text-to-image, image-to-image, 3D model generation, rendering, upscaling, inpainting; limitations: prompt interpretation, style control, anatomical accuracy, physics realism, iteration requirements.
- **Analysis tool capabilities:** color palette extraction, histogram analysis, edge detection, feature matching, similarity search, metadata extraction; limitations: algorithm-specific biases, false positives, context blindness.
- **Reference tool capabilities:** image search, style databases, design inspiration, technical documentation, material libraries; limitations: copyright, relevance ranking, outdated information, access restrictions.
- **Workflow awareness:** understand which tools feed into others (analysis → generation → QA → delivery); know when to use multiple tools vs. single tool; understand dependencies and bottlenecks.
- **Error handling:** tools fail (timeouts, bad inputs, service outages); have fallback strategies; know when to ask user for alternative approach; document failures for debugging.
- **Result interpretation:** tool outputs need interpretation (object detection boxes ≠ understanding, color values ≠ color harmony, similarity scores ≠ quality judgment); never take tool output as ground truth without validation.

## Evaluation criteria / rules
- **Before using any tool, ask:** What do I need to know? Which tool provides that? What's the tool's limitation? How will I validate the result?
- Match tool to task: don't use generation tool for analysis, don't use analysis tool for creative generation; use the right tool for the job.
- Combine tools for complex tasks: analyze → generate → analyze again → iterate; single-tool solutions are often insufficient.
- Validate tool outputs: object detection can miss objects, color extraction can be affected by lighting, generation can produce artifacts; always verify.
- Know tool limitations: state them explicitly ("This analysis is based on [tool] which may miss [limitation]").
- Have fallback strategies: if tool A fails, use tool B; if all tools fail, use manual analysis or ask user.
- Document tool usage: what tools were used, what they returned, how results were interpreted; enables debugging and improvement.
- For generation tasks: specify tool capabilities and limitations to user ("I can generate X but not Y; for Y I'd need...").

## Confidence & limits
- High confidence: tool existence, basic functionality, documented capabilities, common use cases.
- Medium: tool performance on specific tasks, output quality, edge case handling.
- Low: tool availability (services change), future capabilities, integration possibilities.
- Unknown: tool internals, proprietary algorithms, service reliability, pricing/limits without checking.
- Cannot assume: tools will always work, outputs will be accurate, services won't change, all tools are accessible.
- Always state: "Based on [tool] output, which may have limitations..." and "I'd recommend verifying with [alternative method]."
