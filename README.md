# 음파 도플러 주파수 계산기

매질 기준 1차원 음원·관측자 운동의 도플러 주파수 계산

- Plan ID: E092
- App: https://nanalab.kr/eng-sound-doppler/
- Repository: https://github.com/NaNaCompany/eng-sound-doppler
- Formula: `f_obs = f₀(c_s+v_o)/(c_s−v_s)`
- Output: 관측 주파수 f_obs

## Model

f₀,c_s>0, |v_o|,|v_s|<c_s. 관측자는 음원 쪽, 음원은 관측자 쪽 속도를 양수로 입력한다. 속도는 매질 기준이다. 충격파·반사·전자기 상대론 도플러는 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `1111.11111111111`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
