![Title Image lol](https://media.fab.com/image_previews/gallery_images/a9acc7c8-9040-40c1-b5a0-93755beca0a9/730f4cbf-fbc8-49f3-9f7e-8c667b0e3f21.jpg)

> [!WARNING]
> **Real-time lighting does not work in this template.** All lighting must be baked. Movable lights will have no effect without additional configuration.
>
> If you are converting an existing project to use this template, **back up your project first**. Disabling Lumen and Virtual Shadow Maps can break existing lighting setups and is not easily reversible.

# Perfectly Optimized — UE5 Mobile Performance Template

A minimal Unreal Engine 5 starter template built for **Android and mobile hardware**. Replaces UE5's default ray-traced, virtualized rendering pipeline with a lightweight configuration suited to mobile GPUs and low-power devices.

> If Lumen, Nanite, or DX12 overhead is holding your mobile project back — this is your starting point.

---

## Why This Exists

UE5's defaults are designed for high-end desktop GPUs. On mobile hardware, features like Lumen GI and Virtual Shadow Maps are either unsupported or cause severe performance drops. This template disables those systems upfront so you're building on a **stable, predictable baseline** suited to Android targets.

---

## What's Changed

### Renderer
| Setting | Default UE5 | This Template |
|---|---|---|
| RHI | DirectX 12 | **Vulkan** |
| Anti-Aliasing | TAA | **Disabled** |
| Global Illumination | Lumen | **Disabled (baked)** |
| Reflections | Lumen | **Disabled** |
| Shadows | Virtual Shadow Maps | **Disabled** |
| Geometry | Nanite | **Disabled** |

### Post Processing
Unnecessary post-process passes removed to reduce per-frame GPU cost.

### Package / Build
- Prerequisites installer removed
- Editor content excluded from cook
- Movies excluded from staging

---

## Intended For

- Android mobile targets
- VR projects on mobile hardware
- Stylized, low-poly, or small-scale 3D projects
- Performance-sensitive prototypes
- Developers transitioning from Unity to UE5

## Not Intended For

- iOS (not supported)
- Cinematic or high-fidelity rendering
- Projects requiring dynamic global illumination or real-time shadows

---

## Contents

| | |
|---|---|
| Blueprints | None |
| Maps | 1 (lightweight sample scene) |
| Input Bindings | None |
| Network Replication | No |
| Platform Support | Android only |

---

## Getting Started

```
1. Clone or download this repository (or grab it from Fab)
2. Open the .uproject in Unreal Engine 5
3. Build lighting (required — Lumen is disabled)
4. Start building
```

---

## License

See [LICENSE](LICENSE) for details.
