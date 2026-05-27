# Aether Shaders Pro

### Product Overview
A high-performance dynamic weather and volumetric lighting shader suite built explicitly for Unity's Universal Render Pipeline (URP) and High Definition Render Pipeline (HDRP). This package handles complete atmospheric lighting parameter injection seamlessly, providing AAA-quality visual effects without manual render pipeline modification.

Engineered with extreme optimization at its core, Aether Shaders Pro ensures zero performance overhead on modern mobile pipelines while delivering stunning visual fidelity on desktop and console hardware.

---

### Key Features

* **Adaptive Dynamic Accumulation Maps:** Automatic real-time snow and rain accumulation parameters that seamlessly overlay onto arbitrary meshes based on global normal space up-vectors.
* **Bi-Directional Wind Vectors:** Fully customizable interactive wind channels that drive procedural vertex displacement on grass, foliage, and cloth shaders.
* **Volumetric Fog & Lighting:** Light-weight, screen-space volumetric fog that respects directional, point, and spot light cookie projections.
* **PBR Wetness & Puddles:** Procedural water pooling with dynamic ripple configurations that respond automatically to global weather intensity values.

---

### Quick Start & Setup

1. **Import the Package:** Import `AetherShadersPro.unitypackage` via the Unity Asset Store or package manager.
2. **Assign the Feature:** Add the `AetherWeatherRenderFeature` to your Universal Render Pipeline Asset's renderer list.
3. **Initialize via Script:** Drop the following initialization routine into your primary environment manager or game startup loop:

```csharp
using WisteriaLabs.AetherShaders;
using UnityEngine;

public class WeatherInitializer : MonoBehaviour
{
    void Start()
    {
        // Initialize core pipeline components with maximum fidelity
        AetherShaderEngine.InitializeCorePipeline(PipelineMode.HighFidelity);
        
        // Set global weather presets (Options: Clear, Rainy, Blizzarding)
        AetherShaderEngine.SetWeatherPreset(WeatherPreset.Rainy);
    }
}