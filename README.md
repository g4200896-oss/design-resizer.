# Design BG Remover + 4500x5400 Resizer

Design upload karein → background remove → 4500×5400 transparent PNG (TeePublic / POD ready).
Sab processing browser mein hoti hai — koi server ya paid API nahi.

## Methods
- **AI** — photos / complex backgrounds ke liye (pehli dafa ~40MB model download hota hai)
- **Color remove** — solid white/black background wale designs ke liye (fast, sharp edges)
- **None** — design pehle se transparent ho to sirf resize

## Deploy (GitHub + Cloudflare Pages)
1. GitHub par new repo banayen, `index.html` aur `README.md` upload karein
2. Cloudflare → Workers & Pages → Create → Pages → Connect to Git → repo select karein
3. Build command khali chhor dein, output directory `/` → Deploy
