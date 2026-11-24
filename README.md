# AI Studio na Colabie

Notebook startowy do uruchamiania **ComfyUI** na GPU z abonamentu **Google AI Pro**
(200 jednostek obliczeniowych miesięcznie, bez dodatkowych opłat).

## Start

1. Otwórz notebook w Colabie:
   https://colab.research.google.com/github/kubis1993/ai-studio-colab/blob/main/AI-Studio-Colab.ipynb
2. `Środowisko wykonawcze → Zmień typ środowiska wykonawczego → GPU` (T4 / L4 / A100).
3. W komórce 2 wybierz preset (`flux-schnell-q4`, `sdxl-turbo`, `illustrious-xl`, `wlasny`).
4. `Uruchom wszystko`. Po 4–6 min ostatnia komórka wypisze link `trycloudflare.com`.

## Co gdzie ląduje

- Modele: `MyDrive/AI-Colab/models/{checkpoints,loras,vae,clip,unet,controlnet}` — zostają między sesjami.
- Wyniki: `MyDrive/AI-Colab/output`.
- ComfyUI instaluje się od zera w każdej sesji (2–4 min), modele nie są pobierane ponownie.

## Koszty

Notebook nie kupuje żadnych zasobów. Zużywa wyłącznie jednostki z AI Pro.
Przy zerowym saldzie Colab wraca do trybu darmowego — nie pobiera pieniędzy z karty.

| GPU | VRAM | ~jednostek/h | 200 j. ≈ |
|---|---|---|---|
| T4 | 16 GB | ~1,8 | ~110 h |
| L4 | 24 GB | ~4,8 | ~40 h |
| A100 40 GB | 40 GB | ~11,8 | ~17 h |
