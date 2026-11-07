# 3D Skills UZ — AI uçun 3D-studiya, özbekça qöllanma

> **168 ta bepul, oçiq kodli skill** — Claude Code, Cursor, Codex va 70 dan ortiq AI agentni rasm çizadigan, 3D model yasaydigan, yoruğlik qöyadigan, animatsiya qiladigan va öyin tayyorlaydigan studiyaga aylantiradi.

Bu repozitoriy — [**Scenario Agent Skills**](https://github.com/scenario-labs/skills) loyihasi uçun **özbekça qöllanma**. Skillarning özi Scenario Inc. tomonidan yaratilgan va MIT litsenziyasi bilan tarqatiladi. Bu yerda ularni qanday örnatiş va işlatişni özbek tilida tuşuntiramiz. Bu Scenario'ning rasmiy sahifasi emas.

---

## Mundarija

- [Bu nima?](#bu-nima)
- [Nima bepul, nima pullik?](#nima-bepul-nima-pullik)
- [Tez boşlaş — 3 qadam](#tez-boşlaş--3-qadam)
- [Kasbingizga qarab örnatiş](#kasbingizga-qarab-örnatiş)
- [Ekspert vositalar: Blender, Unreal, Unity…](#ekspert-vositalar-blender-unreal-unity)
- [Nimalar deb söraş mumkin](#nimalar-deb-söraş-mumkin)
- [Yangilaş](#yangilaş)
- [Köp beriladigan savollar](#köp-beriladigan-savollar)
- [**Töliq katalog — 168 ta skill özbekça tavsif bilan →**](KATALOG.md)

## Bu nima?

**Skill** — AI agentga ma'lum bir işni qanday qiliş kerakligini örgatadigan qöllanma (`SKILL.md` fayli). Agent kerak bölganda uni özi öqib oladi. Natijada siz oddiy gap yozasiz, agent esa mutaxassis kabi işlaydi.

Scenario töplamida ikki xil skill bor:

| Turi | Soni | Nima qiladi | Nima kerak |
|---|---|---|---|
| **Scenario skillari** | 81 | Rasm, video, ovoz, tekstura, skybox, 3D model yaratadi | Scenario hisobi + Scenario MCP |
| **Ekspert vositalar** | 87 | Kompyuteringizdagi Blender, Maya, ZBrush, Unreal, Unity, Godot, Roblox Studio'ni boşqaradi | Şu dasturning özi |

**Jami: 168 ta skill.**

## Nima bepul, nima pullik?

- ✅ **Skillarning özi bepul** va oçiq kod (MIT litsenziyasi).
- ✅ **Ekspert vositalar** (Blender, Godot va boşqalar) Scenario hisobisiz işlaydi — faqat dasturning özi kerak. Blender va Godot ham bepul.
- ⚠️ **Rasm, video, 3D generatsiya** Scenario serverida bajariladi. Buning uçun [Scenario](https://scenario.com) hisobi kerak, generatsiya esa ularning tariflariga köra pullik bölişi mumkin. Narxlarni [scenario.com](https://scenario.com) saytidan tekşiring.
- ⚠️ AI agentning özi (Claude, Codex, Cursor) ham öz tarifiga ega.

## Tez boşlaş — 3 qadam

**Kerak böladi:** [Node.js](https://nodejs.org) (18 yoki yangiroq) va AI agent — masalan, [Claude Code](https://claude.com/claude-code).

### 1-qadam. Skillarni örnating

Terminalni oçing va yozing:

```bash
npx skills add scenario-labs/skills
```

Menyu oçiladi: kerakli guruhlarni **probel** bilan belgilang, keyin **Enter** bosing. Menyu böş holda oçiladi — heç narsa tanlamasangiz, heç narsa örnatilmaydi.

Hamma Scenario skillarini (ekspert vositalarsiz) bitta buyruq bilan örnatiş:

<details><summary>Buyruqni körsatiş</summary>

```bash
npx skills add scenario-labs/skills --skill scenario scenario-inspiration scenario-image scenario-multi-reference scenario-product-shots scenario-brand-kit scenario-image-editing scenario-text-overlay scenario-storyboards scenario-game-assets scenario-sprite-animation scenario-side-view-game-kit scenario-blender-2d-animation scenario-textures scenario-skyboxes scenario-3d scenario-video-to-motion scenario-blender scenario-patina-retexture scenario-orbit-views scenario-walkable-room scenario-playable-ads scenario-video scenario-video-editing scenario-video-color-grade scenario-seedance-music-video scenario-kinetic-music-video scenario-chatgpt-pet-create scenario-chatgpt-pet-update scenario-seedance-storyboard scenario-seedance-drafts scenario-video-ads scenario-ugc scenario-fan-cam scenario-reel-recast scenario-audio scenario-video-assembly scenario-motion-loops scenario-caption-studio scenario-consistency scenario-identity-library scenario-model-training scenario-asset-analysis scenario-quality-gate scenario-refine-loop scenario-model-comparison scenario-formats scenario-workflows scenario-workflow-authoring scenario-moderation scenario-report scenario-team-admin scenario-admin-analytics scenario-gpt-image scenario-mai-image scenario-seedream scenario-gemini-image scenario-reve scenario-ideogram scenario-grok-imagine-image scenario-luma-image scenario-minimax-video scenario-gemini-omni scenario-grok-imagine-video scenario-veo scenario-seedance scenario-kling scenario-vidu scenario-wan scenario-runway scenario-luma-video scenario-minimax-music scenario-elevenlabs scenario-ace-step scenario-sonilo scenario-meshy scenario-rodin scenario-sparc3d scenario-3d-worlds scenario-ad-variants scenario-thumbnails
```
</details>

### 2-qadam. Scenario MCP'ni ulang

Rasm, video, 3D yaratadigan skillar uçun kerak. Claude Code'da:

```bash
claude mcp add --transport http scenario https://mcp.scenario.com/mcp
```

Boşqa agentlarda MCP sozlamalariga `https://mcp.scenario.com/mcp` manzilini qöşing va Scenario hisobingiz bilan kiring. Faqat ekspert vositalardan (masalan, Blender) foydalansangiz, bu qadamni ötkazib yuborsangiz böladi.

### 3-qadam. Agentga yozing

Agentni oçing va oddiy tilda vazifa bering. Masalan:

```text
Menga 3D-studiya qurib ber: avval miltiq eskizini çiz, keyin undan 3D model yasa va GLB qilib eksport qil.
```

## Kasbingizga qarab örnatiş

Hammasini emas, faqat kerakli töplamni örnatiş mumkin. Buyruqni nusxalab terminalga qöying.

### 3D rassom
3D modellar, teksturalar, skybox, Blender.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-3d scenario-orbit-views scenario-meshy scenario-blender scenario-skyboxes scenario-patina-retexture scenario-video scenario-rodin scenario-sparc3d scenario-3d-worlds scenario-video-to-motion scenario-video-editing
```

### Muhit rassomi
Teksturalar, 3D dunyolar, xonalar.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-textures scenario-skyboxes scenario-3d-worlds scenario-walkable-room scenario-3d scenario-meshy scenario-image scenario-gemini-image scenario-audio scenario-sonilo
```

### 2D rassom
Rasmlar, spraytlar, 2D animatsiya.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-inspiration scenario-image scenario-sprite-animation scenario-side-view-game-kit scenario-blender-2d-animation scenario-game-assets scenario-image-editing scenario-text-overlay scenario-3d scenario-video scenario-consistency scenario-model-training scenario-refine-loop scenario-gpt-image scenario-mai-image scenario-seedream scenario-gemini-image scenario-reve scenario-ideogram scenario-grok-imagine-image scenario-luma-image scenario-multi-reference scenario-chatgpt-pet-create scenario-chatgpt-pet-update
```

### Video prodyuser
Video, storyboard, montaj, subtitr.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-video scenario-storyboards scenario-video-assembly scenario-caption-studio scenario-formats scenario-image scenario-image-editing scenario-text-overlay scenario-video-editing scenario-video-color-grade scenario-audio scenario-seedance-music-video scenario-seedance-storyboard scenario-seedance-drafts scenario-reel-recast scenario-video-ads scenario-consistency scenario-asset-analysis scenario-minimax-video scenario-gemini-omni scenario-grok-imagine-video scenario-veo scenario-seedance scenario-kling scenario-vidu scenario-wan scenario-runway scenario-luma-video scenario-ad-variants scenario-thumbnails scenario-kinetic-music-video scenario-ace-step scenario-motion-loops
```

### Marketing dizayner
Mahsulot suratlari, brend, video reklama, UGC.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-formats scenario-brand-kit scenario-text-overlay scenario-product-shots scenario-video-ads scenario-ugc scenario-inspiration scenario-image scenario-image-editing scenario-video scenario-video-editing scenario-audio scenario-video-assembly scenario-consistency scenario-asset-analysis scenario-veo scenario-seedance scenario-kling scenario-elevenlabs scenario-ad-variants scenario-thumbnails scenario-fan-cam scenario-playable-ads scenario-game-assets scenario-3d
```

### Ovoz dizayneri
Musiqa, effektlar, ovoz.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-audio scenario-sonilo scenario-video-assembly scenario-minimax-music scenario-elevenlabs scenario-ace-step
```

### Art-direktor
Bir xillik, sifat nazorati, öz modellar.

```bash
npx skills add scenario-labs/skills --skill scenario scenario-moderation scenario-report scenario-consistency scenario-identity-library scenario-quality-gate scenario-asset-analysis scenario-model-training scenario-image scenario-image-editing scenario-sprite-animation scenario-video scenario-refine-loop scenario-seedream scenario-gemini-image
```

## Ekspert vositalar: Blender, Unreal, Unity…

Bu skillar kompyuteringizga örnatilgan dasturni boşqaradi va Scenario hisobini talab qilmaydi. Har bir oila **bitta töplam** bölib örnatiladi, çunki ular boş skillning skriptlaridan foydalanadi.

### Blender — 15 ta skill
Kerak: **Blender 5.2**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/dcc/blender/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-blender-expert scenario-blender-animation scenario-blender-blockout scenario-blender-export scenario-blender-geometry-nodes scenario-blender-grease-pencil scenario-blender-hair scenario-blender-hard-surface scenario-blender-lighting-rendering scenario-blender-previs-storyboard scenario-blender-retopology scenario-blender-rigging scenario-blender-sculpting scenario-blender-texturing-shading scenario-blender-uv-baking
```

### Maya — 11 ta skill
Kerak: **Autodesk Maya**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/dcc/maya/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-maya-expert scenario-maya-animation scenario-maya-deformation scenario-maya-fx scenario-maya-groom scenario-maya-lighting-rendering scenario-maya-lookdev scenario-maya-modeling scenario-maya-pipeline-scripting scenario-maya-retopology-uv scenario-maya-rigging
```

### ZBrush — 9 ta skill
Kerak: **ZBrush**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/dcc/zbrush/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-zbrush-expert scenario-zbrush-automation scenario-zbrush-character-creature scenario-zbrush-hard-surface scenario-zbrush-paint-render scenario-zbrush-pose-print scenario-zbrush-retopology-export scenario-zbrush-sculpting scenario-zbrush-stylized
```

### Unreal Engine — 10 ta skill
Kerak: **Unreal Engine**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/game-engines/unreal/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-unreal-expert scenario-unreal-animation scenario-unreal-cinematics scenario-unreal-gameplay scenario-unreal-lighting-rendering scenario-unreal-materials scenario-unreal-performance scenario-unreal-pipeline-automation scenario-unreal-vfx scenario-unreal-world-building
```

### Unity — 14 ta skill
Kerak: **Unity 6.3 LTS**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/game-engines/unity/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-unity-expert scenario-unity-2d scenario-unity-animation scenario-unity-architecture scenario-unity-gameplay scenario-unity-mobile scenario-unity-performance scenario-unity-pipeline-automation scenario-unity-rendering-lighting scenario-unity-shaders scenario-unity-ui scenario-unity-vfx scenario-unity-web scenario-unity-world-building
```

### Godot — 14 ta skill
Kerak: **Godot 4.7**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/game-engines/godot/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-godot-expert scenario-godot-2d scenario-godot-3d-world scenario-godot-animation scenario-godot-architecture scenario-godot-audio scenario-godot-gameplay scenario-godot-multiplayer scenario-godot-performance-export scenario-godot-pipeline-automation scenario-godot-rendering-lighting scenario-godot-shaders scenario-godot-ui scenario-godot-vfx
```

### Roblox Studio — 14 ta skill
Kerak: **Roblox Studio**. Batafsil: [asl qöllanma (inglizça)](https://github.com/scenario-labs/skills/blob/main/skills/game-engines/roblox/README.md).

```bash
npx skills add scenario-labs/skills --skill scenario-roblox-expert scenario-roblox-animation scenario-roblox-architecture scenario-roblox-assets scenario-roblox-data scenario-roblox-environment scenario-roblox-gameplay scenario-roblox-luau scenario-roblox-monetization scenario-roblox-networking scenario-roblox-performance scenario-roblox-tooling scenario-roblox-ui scenario-roblox-vfx-audio
```

> ℹ️ Unreal Engine skillari mualliflar tomonidan dvijok içida töliq sinab körilmagan — bu haqda asl README'da yozilgan.

## Nimalar deb söraş mumkin

- «RPG öyinim inventari uçun bir xil stildagi 4 ta iksir ikonkasini şaffof fonda yasab ber.»
- «Çoksiz ğişt teksturasini yasa va uni 2048 gaça kattalaştir, lekin çoklari buzilmasin.»
- «Şu eskizdan 3D props yasa, GLB qilib eksport qilişdan oldin körsat.»
- «Blender'da şu personajga Rigify bilan rig qöy va yuriş siklini animatsiya qil.»
- «Unity'da oddiy platformer level yasa: terrain, yoruğlik, öyinçi kontrolleri.»

## Yangilaş

Skillar deyarli har kuni yangilanadi. Yangi versiyani oliş uçun:

```bash
npx skills update
```

## Köp beriladigan savollar

**Bu haqiqatan ham bepulmi?**  
Skillar — ha, MIT litsenziyasi bilan oçiq. Lekin Scenario orqali generatsiya va AI agentning özi pullik bölişi mumkin. Ekspert vositalar faqat dasturni talab qiladi.

**Qaysi agentlarda işlaydi?**  
Claude Code, Cursor, Codex, GitHub Copilot va 70 dan ortiq agentda — `npx skills` örnatuvçisi qöllaydigan hammasida.

**Kompyuterim kuçsiz bölsa-çi?**  
Scenario skillari generatsiyani bulutda bajaradi, kompyuter kuçi muhim emas. Ekspert vositalar uçun esa tegişli dastur (masalan, Blender) yurişi kerak.

**Dasturlaşni biliş kerakmi?**  
Yöq. Terminalga bir neçta buyruq nusxalab qöyasiz, qolganini agent bilan oddiy tilda gaplaşib qilasiz.

**Xato çiqsa nima qilaman?**  
Avval `npx skills update` qiling. Muammo qolsa, [asl repozitoriyda issue oçing](https://github.com/scenario-labs/skills/issues).

## Manba va litsenziya

- Skillar: [scenario-labs/skills](https://github.com/scenario-labs/skills) — © 2026 Scenario Inc., [MIT litsenziyasi](https://github.com/scenario-labs/skills/blob/main/LICENSE).
- Bu qöllanmadagi özbekça matnlar: [LICENSE](LICENSE) faylida.
- "Scenario" nomi va logotipi Scenario Inc.'ga tegişli. Bu repozitoriy Scenario bilan rasmiy aloqador emas.
